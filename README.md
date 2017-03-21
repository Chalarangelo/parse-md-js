# Parse-MD.js

A regular expression Markdown parser, written in functional Javascript.

## Usage

Include the javascript file in your page, then simply call `parseMarkdown`:

	var parsedMD = parseMarkdown(yourMarkdownVar);

The parser will parse the contents of `yourMarkdownVar` into `parsedMD` as HTML.

## Recognized Syntax

- **Headers** are only available using the `#` syntax:
```
# Heading 1
## Heading 2
### Heading 3
```

- **Italics** and **bold** are available using asterisks:
```
*Italics* and **bold**
```

- **Unordered lists** are available using either `-` or `+` and **ordered lists** are available using `1.`, `2.` etc:
```
 - Unordered list item 1
 + Unordered list item 2

 1. Ordered list item 1
 2. Ordered list item 2
```
**Note** that list nesting is not supported and might cause unexpected behavior.

- **Links** are only available using the `[title](link_url)` syntax and **images** are only available using the `![title](image_url)` syntax:
```
[link_title](https://github.com/Chalarangelo/parse-md-js)
![image_tite](https://github.com/Chalarangelo/parse-md-js/image.png)
```

- **Inline code** can be written using the `` ` `` symbol and **code blocks** are only available using single tab indentation:
```
`code goes here`

	code block
```

- **Single line blockquotes** are available using the `>` symbol:
```
> blockquote
```

- **Horizontal rules** are available using either `---` or `===`:
```
 ---
 ===
```

- **Line breaks** are only supported using two or more newline characters.

- **Tables**, **inline HTML** and **Youtube vide embedding** are not supported.

## License

The source code is licensed under the MIT license.
