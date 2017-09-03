# JavaScript String

JavaScript strings are used for storing and manipulating text. 

## JavaScript Strings

A JavaScriipt string simply stores a series of characters like "John Doe".

A string can be any text inside quotes. You can use single or double quotes:

> var carname = "Volvo XC60";<br>
> var carname = 'Volvo XC60';

You can use quotes inside a string, as long as they don't match the quotes surrounding the string:

## String Length

The length of a string is found in the built in property **length**:

## Special Characters

Because strings must be written within quotes, JavaScript will misunderstand this string:

The string will be chopped to "We are the so-called".

The solution to avoid this problem, is to use the **\ escape character**.

The backslash escape character turns special characters into string characters:

The escape character (\) can also be used to insert other special characters in a string. 

These are commonly used special characters that can be inserted in a text with the backslash sign:

Code|Outputs
---|---
\'|single quote
\"|double quote
\\|backslash

Five other escape characters are valid in JavaScript

Code|Outputs
---|---
\b|Backspace
\r|Carriage Return
\f|Form Feed
\t|Horizontal Tabulator
\v|Vertical Tabulator

> The 5 escape characters above were originally designed to control typewriters, teletypes, and fax machines. They do not make any sense in HTML. 

## Breaking Long Code Lines

For best readability, programmers often like to avoid code lines longer than 80 characters.

If a JavaScript statement does not fit on one line, the best place to break it is after an operator:

