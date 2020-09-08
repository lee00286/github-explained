# Readme

## Table of Contents
1. [Mardown Character Syntax](#markdown-character-syntax)
1. [Text](#text)
1. [List](#list)
1. [Hyperlink](#hyperlink)
1. [Table](#table)
1. [Emoji](#emoji)
1. [Badges](#badges)

---

## Mardown Character Syntax

| Character | Syntax |
| --- | --- |
| \ | Backslash |
| ` | Backtick |
| * | Asterisk |
| _ | Underscore |
| {} | Curly Braces |
| [] | Square Brackets |
| () | Parentheses |
| # | Hash Mark |
| + | Plus Sign |
| - | Minus Sign (Hyphen) |
| . | Dot |
| ! | Exclamation Mark |

## Text

1. [Insert Heading](#insert-heading)
1. [Insert Text Decoration](#insert-text-decoration)
1. [Insert Code](#insert-code)
1. [Insert Quotation](#insert-quotation)

### Insert Heading

You can use `# (Hash)` before the text to insert heading. The smaller number of hash, the larger heading is.

**Example**

```
# h1 tag with one hash
## h2 tag two hashes
### h3 tag three hashes
#### h4 tag four hashes
##### h5 tag five hashes
###### h6 tag six hashes
```

### Insert Text Decoration

#### Emphasize Text

You can cover the text with `* (Asterisk)` or `_ (Underscore)` to italicize the text.

You can cover the text with `** (Asterisks)` or `__ (Underscores)` to bold the text.

**Example**

```
*Italicize text with asterisk*
_Italicize text with underscore_
**Bold text with asterisks**
__Bold text with asterisks__
```

**Result**

*Italicize text with asterisk*

_Italicize text with underscore_

**Bold text with asterisks**

__Bold text with asterisks__

### Insert Code

You can cover the text with `` ` (Backtick)`` to insert the code or command.

You can cover the text with ` ``` (Backticks)` to insert the code blocks.

**Example**
````
`Code or Command`

```
Line 1
Line 2
Line 3
``` 
````

**Result**

`Code or Command`

```
Line 1
Line 2
Line 3
``` 

### Insert Quotation

You can use `> (Right Angle Bracket)` before the text to insert quotation.

**Example**

`> Quoting Text`

**Result**

> Quoting Text

---

## List

You can use `* (Asterisk)` before the text to insert unordered list.

You can use `1. 2. 3.` before the text to insert ordered list. Instead, `1. 1. 1.` works as well.

If you insert tab before the asterisk or the number, then you can indent the list.

**Example**

````
```
* Unordered
* List
  1. Indented
  2. List
1. Ordered
2. List
  * Indented
  * List
```
````

**Result**

* Unordered
* List
  1. Indented
  1. List
1. Ordered
2. List
  * Indented
  * List

---

## Hyperlink

1. [Insert Link](#insert-link)
1. [Insert Image](#insert-image)

### Insert Link

You can use `[TEXT](URL)` to insert link to the text. Replace TEXT with any text and URL with link you want. You have three types of hyperlink:

* Heading inside markdown file
  * Replace URL with hash and a title like `#link`
  * If a title has space in between, then replace it with a dash like `#insert-link`
  * The title shouldn't have any special text
* File inside repository
  * Replace URL with a directory like `/md-files/Readme.md`
* Any website
  * Replace URL with a link

**Example**

```
[Hyperlink One](#insert-link)
[Hyperlink Two](/README.md)
[Hyperlink Three](https://lee00286.github.io/portfolio)
```

**Result**

[Hyperlink One](#insert-link)

[Hyperlink Two](/README.md)

[Hyperlink Three](https://lee00286.github.io/portfolio)

### Insert Image

You can use `![TEXT](URL)` to insert image. Replace TEXT with any text and URL with link of the image.

---

## Table

[Tables Generator](https://www.tablesgenerator.com/markdown_tables) will generate the table code for you. 

## Emoji

## Badges

Collection of badges are collected [here](https://gist.github.com/tterb/982ae14a9307b80117dbf49f624ce0e8)
