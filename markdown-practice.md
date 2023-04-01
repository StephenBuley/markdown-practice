# Markdown

An exploratory report by **Stephen Buley**

## Headings

Headings can be denoted using the `#` symbol, which makes it easy to see what level heading you are using

```markdown
# heading 1

## heading 2

### heading 3
```

You can also use heading levels 1 and 2 like this

```md
# Heading 1

## Heading 2
```

At least 3 of each symbol are needed to denote the heading, and it needs to be directly under the words

## Paragraphs

```markdown
each paragraph needs to be on its own line seperated by one line, otherwise it jumps up and appends itself to the next line
like this

or like this
```

each paragraph needs to be on its own line seperated by one line, otherwise it jumps up and appends itself to the next line
like this

or like this

## Ordered and Unordered Lists

You can create unordered lists just by putting an asterisk before each line

```markdown
- Milk
- Eggs
- Cookies
- More cookies
```

- Milk
- Eggs
- Cookies
- More cookies

Ordered lists are similar. You can use the actual numbers you want, or you can just let the markdown parser do things for you.

```markdown
1. Go to store
1. Cry a lot
1. Have a hard time

or this

1. Go to Store
2. Get a monkey
3. Wait a monkey?
4. Does this work? We will see!
```

1. Go to store
1. Cry a lot
1. Have a hard time

or this

1. Go to Store
2. Get a monkey
3. Wait a monkey?
4. Does this work? We will see! doesn't look like it, the parser always does it for you

## Italics, bold, strikethrough

You can use either `*` or `_` for bold and italics, just the number makes the difference

```markdown
_italics_

**bold**

_italics_

**bold**
```

_italics_

**bold**

_italics_

**bold**

```markdown
strikethrough ~~can't~~ can be done
```

strikethrough ~~can't~~ can be done

underlining text isn't recommended because it gets confused with links <u>apparently</u>

## Links!

links work in several different ways

1. the `<>` way
2. the `[]()` way
3. the `[][]` way

### the `<>` way

```markdown
add a link like this: <https://www.google.com>
```

add a link like this: <https://www.google.com>

The problem with this way is that it doesn't just link text, you have to put in the whole url

### the `[]()` way

```markdown
add a link like this: go to [Google](https://www.google.com)

you can also do this to create a little title/tooltip: [Google](https://www.google.com "This is the tool tip")
```

add a link like this: go to [Google](https://www.google.com)

you can also do this to create a little title/tooltip: [Google](https://www.google.com "This is the tool tip")

This is better for creating a link within a word, and the only way to get the tool tip action going, but it looks a little clunky in my opinion.

### the `[][]` way

Finally the `[][]` way!

```markdown
add a link like this: Go to [Google][1]

somewhere else in your markdown file you can write this but it won't show up

[1]: https://www.google.com
```

add a link like this: Go to [Google][1]

somewhere else in your markdown file you can write this but it won't show up

[1]: https://www.google.com

Isn't that so cool? Then you can just nicely keep your links in order at the bottom or top or something and link things [everywhere][1] if you want like [this][1]

## Code

Finally, writing code into markdown is easy

There are a few ways to do this as well

1. indentation
2. backticks

```markdown
with indentation at least 4 spaces and a line free above and below

    const x = 100;
```

    const x = 100

Or you can use back ticks with the specified language you are using, which I believe is the only way to get the syntax highlighting

````markdown
```javascript
const x = 100
```
````

```javascript
const x = 100
```

## Images

I almost forgot Images! They work almost exactly like links, except you need a bang at the front of the square brackets like so:

```markdown
![This is the alt text](https://unsplash.it/300/300?random)
```

![This is the alt text](https://unsplash.it/300/300?random)

## Conclusion

One more thing I didn't mention was that you can use some html components if you need to do something specific:

```markdown
<img src="https://unsplash.it/300/300?random" alt="a different cool pic" id="pic-i-need-an-id-on">
```

<img src="https://unsplash.it/300/300?random" alt="a different cool pic" id="pic-i-need-an-id-on">

<br><br>
Well, I am sure I forgot something, but I am really glad I got all of this time practicing my _new and improved_ fancy **MARKDOWN** ~~shenanigans~~ skills!

Thanks for reading!

Stephen
