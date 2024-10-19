
JavaScript provides a rich set of string methods to manipulate and work with string values. Here's a detailed explanation of each string method you listed:

### 1. **anchor()**
   - **Description**: Creates an HTML `<a>` anchor element with a `name` attribute.
   - **Syntax**: `str.anchor(name)`
   - **Example**: `'Google'.anchor('google')` → `<a name="google">Google</a>`

### 2. **at()**
   - **Description**: Returns the character at the given index. Accepts both positive and negative indices.
   - **Syntax**: `str.at(index)`
   - **Example**: `'hello'.at(1)` → `'e'`

### 3. **big()**
   - **Description**: Wraps the string in an HTML `<big>` tag to make the text larger.
   - **Syntax**: `str.big()`
   - **Example**: `'Hello'.big()` → `<big>Hello</big>`

### 4. **blink()**
   - **Description**: Wraps the string in a `<blink>` tag, which used to create a blinking effect in older browsers.
   - **Syntax**: `str.blink()`
   - **Example**: `'Warning'.blink()` → `<blink>Warning</blink>`
   - **Note**: This tag is deprecated and not supported in modern browsers.

### 5. **bold()**
   - **Description**: Wraps the string in a `<b>` tag to make the text bold.
   - **Syntax**: `str.bold()`
   - **Example**: `'Bold Text'.bold()` → `<b>Bold Text</b>`

### 6. **charAt()**
   - **Description**: Returns the character at the specified index.
   - **Syntax**: `str.charAt(index)`
   - **Example**: `'hello'.charAt(0)` → `'h'`

### 7. **charCodeAt()**
   - **Description**: Returns the Unicode value of the character at the given index.
   - **Syntax**: `str.charCodeAt(index)`
   - **Example**: `'A'.charCodeAt(0)` → `65`

### 8. **codePointAt()**
   - **Description**: Returns the code point of the character at the specified index (supports characters outside the basic multilingual plane).
   - **Syntax**: `str.codePointAt(index)`
   - **Example**: `'😄'.codePointAt(0)` → `128516`

### 9. **concat()**
   - **Description**: Combines the text of two or more strings and returns a new string.
   - **Syntax**: `str.concat(str2, str3, ...)`
   - **Example**: `'Hello'.concat(' World')` → `'Hello World'`

### 10. **constructor**
   - **Description**: Returns the constructor function for the string object.
   - **Syntax**: `str.constructor`
   - **Example**: `'hello'.constructor === String` → `true`

### 11. **endsWith()**
   - **Description**: Checks if a string ends with a given substring.
   - **Syntax**: `str.endsWith(substring)`
   - **Example**: `'Hello world'.endsWith('world')` → `true`

### 12. **fixed()**
   - **Description**: Wraps the string in a `<tt>` tag to display text in fixed-pitch (monospace) font.
   - **Syntax**: `str.fixed()`
   - **Example**: `'Monospace'.fixed()` → `<tt>Monospace</tt>`

### 13. **fontcolor()**
   - **Description**: Wraps the string in a `<font>` tag with a specified color.
   - **Syntax**: `str.fontcolor(color)`
   - **Example**: `'Text'.fontcolor('red')` → `<font color="red">Text</font>`

### 14. **fontsize()**
   - **Description**: Wraps the string in a `<font>` tag with a specified size.
   - **Syntax**: `str.fontsize(size)`
   - **Example**: `'Text'.fontsize(5)` → `<font size="5">Text</font>`

### 15. **includes()**
   - **Description**: Checks if the string contains a specified substring.
   - **Syntax**: `str.includes(substring)`
   - **Example**: `'JavaScript'.includes('Script')` → `true`

### 16. **indexOf()**
   - **Description**: Returns the index of the first occurrence of a specified value. Returns `-1` if not found.
   - **Syntax**: `str.indexOf(substring)`
   - **Example**: `'JavaScript'.indexOf('S')` → `4`

### 17. **isWellFormed()**
   - **Description**: Returns whether the string is well-formed UTF-16.
   - **Syntax**: `str.isWellFormed()`
   - **Example**: `'hello'.isWellFormed()` → `true`

### 18. **italics()**
   - **Description**: Wraps the string in an HTML `<i>` tag to make the text italic.
   - **Syntax**: `str.italics()`
   - **Example**: `'Text'.italics()` → `<i>Text</i>`

### 19. **lastIndexOf()**
   - **Description**: Returns the index of the last occurrence of a specified value. Returns `-1` if not found.
   - **Syntax**: `str.lastIndexOf(substring)`
   - **Example**: `'hello world'.lastIndexOf('o')` → `7`

### 20. **length**
   - **Description**: Returns the length of the string.
   - **Syntax**: `str.length`
   - **Example**: `'hello'.length` → `5`

### 21. **link()**
   - **Description**: Wraps the string in an HTML `<a>` tag with an `href` attribute.
   - **Syntax**: `str.link(url)`
   - **Example**: `'Google'.link('http://google.com')` → `<a href="http://google.com">Google</a>`

### 22. **localeCompare()**
   - **Description**: Compares two strings in the current locale.
   - **Syntax**: `str.localeCompare(compareString)`
   - **Example**: `'a'.localeCompare('b')` → `-1` (because `'a'` comes before `'b'`)

### 23. **match()**
   - **Description**: Searches the string for a match against a regular expression and returns the matches.
   - **Syntax**: `str.match(regex)`
   - **Example**: `'hello'.match(/l/g)` → `['l', 'l']`

### 24. **matchAll()**
   - **Description**: Returns an iterator of all results matching a regular expression.
   - **Syntax**: `str.matchAll(regex)`
   - **Example**: `Array.from('test1test2'.matchAll(/t(e)(s)/g))` → `[['te', 'e', 's'], ['te', 'e', 's']]`

### 25. **normalize()**
   - **Description**: Returns the Unicode Normalization Form of the string.
   - **Syntax**: `str.normalize([form])`
   - **Example**: `'é'.normalize('NFD')` → `'é'` (decomposed form)

### 26. **padEnd()**
   - **Description**: Pads the current string with another string (repeated if needed) until it reaches the given length.
   - **Syntax**: `str.padEnd(targetLength, padString)`
   - **Example**: `'abc'.padEnd(5, 'x')` → `'abcxx'`

### 27. **padStart()**
   - **Description**: Pads the current string from the start.
   - **Syntax**: `str.padStart(targetLength, padString)`
   - **Example**: `'abc'.padStart(5, 'x')` → `'xxabc'`

### 28. **repeat()**
   - **Description**: Repeats the string a specified number of times.
   - **Syntax**: `str.repeat(count)`
   - **Example**: `'ha'.repeat(3)` → `'hahaha'`

### 29. **replace()**
   - **Description**: Replaces matches of a string or a regular expression with a new substring.
   - **Syntax**: `str.replace(searchValue, replaceValue)`
   - **Example**: `'hello world'.replace('world', 'everyone')` → `'hello everyone'`

### 30. **replaceAll()**
   - **Description**: Replaces all matches of a string or a regular expression with a new substring.
   - **Syntax**: `str.replaceAll(searchValue, replaceValue)`
   - **Example**: `'aabbcc'.replaceAll('b', 'x')` → `'aaxxcc'`

### 31. **search()**
   - **Description**: Searches the string for a match against a regular expression and returns the index of the match.
   - **Syntax**: `str.search(regex)`
   - **Example**: `'hello'.search(/l/)` → `2`

###
