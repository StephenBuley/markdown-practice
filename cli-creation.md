# Creating a CLI with npm

Recently I have been really impressed with command line applications. While many people (_including myself_) get into coding and web development because you can immediately see your changes, there is something really cool to me about understanding a command line tool and using it quickly and efficiently. As I was thinking about CLIs, I started thinking **"how does that even work?"**

Well tonight I finally understood the process of setting up a command line interface with npm and configuring it to make sure your shell understands what to do.

## Step 1: Init

First create a directory where your code will live and move into the file:

```bash
mkdir cool-cli
cd cool-cli
```

Next create a package.json file with npm init:

```bash
# in cool-cli
npm init
# or "npm init -y" if you just want the default settings
```

## Step 2: Configuration

Now you should have a folder named "cool-cli" with one file in it, `package.json`. Change `"main"` to `./bin/index.js`, or whatever the folder and file name is where you will be running the main code (bin/index.js is just the best-practice name).

Somewhere else in the file, you will need to add a `"bin"` property, with an object that contains the name of the command you want to use when running your application, as well as the same file path you used in main. In my case, I am using the folder name as the cli command, but it could be anything. Your package.json should look something like this.

```json
"main": "./bin/index.js",
// other properties...
"bin": {
  "cool-cli": "./bin/index.js"
}
```

Finally, run `npm install -g .` in the root directory of your project to install the CLI into OS, that way you can use the newly configured command anywhere on your machine. You may run into an error that looks like you should just run `sudo`, but **this is not recommended**. Instead, add this to your ~/.bashrc or equivalent shell config file:

```bash
npm set prefix ~/.npm
PATH="$HOME/.npm/bin:$PATH"
PATH="./node_modules/.bin:$PATH"
```

Run `source ~/.bashrc` to make sure your shell is synced up, and then run `npm install -g .` again.

## Step 3: Add code!

The final step is to add code in the place where you told the computer to look for code!

Create a `bin` folder and an `index.js` folder inside of it:

```bash
mkdir bin
cd bin
touch index.js
```

If you decided to use another file location in the `package.json` configuration in Step 2, you'll need to create the folders and files as you specified there.

Add `#!/usr/bin/env node` to the top of your `index.js` file. This makes sure the shell reads the code using the node environment the user has specified for their machine.

Finally, add some code to `index.js`:

```javascript
const myString = 'World'
console.log('Hello' + myString)
```

Go back to the terminal and run the command you specified in the `package.json` file in Step 2, and you should see the output from your index.js file! **CONGRATULATIONS!!!** You just made a command line application in js and node.

Special thanks to [Manav Shrivastava](https://github.com/manavshrivastavagit/mycli) for his [great blog post](https://medium.com/@manavshrivastava/lets-build-a-cli-command-line-interface-with-node-js-d3b5faacc5ea) on Medium that finally helped me understand exactly what was going on.
