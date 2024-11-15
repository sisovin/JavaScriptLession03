# Lesson 03: Strings represents Text

# Table of Contents

1. [Lesson 03: Strings represents Text](#lesson-03-strings-represents-text)
   - [Explanation](#explanation)
     - [Creating Strings](#creating-strings)
     - [Concatenation](#concatenation)
     - [Accessing Characters](#accessing-characters)
     - [String Properties and Methods](#string-properties-and-methods)
     - [Strings are Immutable](#strings-are-immutable)
     - [Common string methods in JavaScript include](#common-string-methods-in-javascript-include)
   - [Practices](#practices)
   - [Review](#review)
     - [String Represents Text](#string-represents-text)
     - [Using Strings and Numbers Together](#using-strings-and-numbers-together)
     - [Three Ways to Create Strings](#three-ways-to-create-strings)
     - [Escape Characters](#escape-characters)
     - [Interpolation, Multi-line Strings](#interpolation-multi-line-strings)

This Table of Contents provides a structured overview of the sections and subsections in the **# Lesson 03: Strings represents Text**

## Explanation

Explain me the Strings in javascript and how they work with examples? Does Strings represent Text?
Yes, in JavaScript, strings represent text. A string is a sequence of characters used to represent text. It can be any length and can include letters, numbers, symbols, and whitespace characters.

Here's a basic overview of strings in JavaScript with examples:

### Creating Strings

Strings can be created using single quotes (`'`), double quotes (`"`), or backticks (`` ` ``), also known as template literals.

```javascript
let singleQuoteString = 'Hello, world!';
let doubleQuoteString = 'Hello, world!';
let backtickString = `Hello, world!`;
```

### Concatenation

You can combine strings using the `+` operator or template literals.

```javascript
let firstName = 'John';
let lastName = 'Doe';
let fullName = firstName + ' ' + lastName; // "John Doe"
let fullNameWithTemplate = `${firstName} ${lastName}`; // "John Doe"
```

### Accessing Characters

You can access individual characters in a string by their index using bracket notation.

```javascript
let greeting = 'Hello, world!';
let firstCharacter = greeting[0]; // "H"
```

### String Properties and Methods

Strings come with a set of properties and methods that allow you to manipulate and inspect them.

```javascript
let text = 'Hello, world!';

// Length of the string
console.log(text.length); // 13

// Converting to upper case
console.log(text.toUpperCase()); // "HELLO, WORLD!"

// Includes - checks if the string contains a substring
console.log(text.includes('world')); // true

// Slice - extracts a section of the string
console.log(text.slice(0, 5)); // "Hello"
```

### Strings are Immutable

In JavaScript, strings are immutable, which means once a string is created, it cannot be changed. However, you can create a new string based on operations performed on the original string.

```javascript
let originalString = 'Hello';
let modifiedString = originalString + ', world!';
console.log(modifiedString); // "Hello, world!"
```

In summary, strings in JavaScript are used to work with text. They provide a rich set of methods and properties for text manipulation and inspection.

### Common string methods in JavaScript include:

1. **`charAt(index)`**: Returns the character at the specified index.

   ```javascript
   'Hello'.charAt(1); // "e"
   ```

2. **`concat(...strings)`**: Concatenates the string arguments to the calling string and returns a new string.

   ```javascript
   'Hello'.concat(' ', 'world!'); // "Hello world!"
   ```

3. **`includes(searchString, position)`**: Determines whether one string may be found within another string, returning true or false as appropriate.

   ```javascript
   'Hello world!'.includes('world'); // true
   ```

4. **`indexOf(searchValue, fromIndex)`**: Returns the index of the first occurrence of the specified value, starting the search at `fromIndex`. Returns -1 if the value is not found.

   ```javascript
   'Hello world!'.indexOf('world'); // 6
   ```

5. **`toLowerCase()`**: Returns the calling string value converted to lowercase.

   ```javascript
   'HELLO WORLD!'.toLowerCase(); // "hello world!"
   ```

6. **`toUpperCase()`**: Returns the calling string value converted to uppercase.

   ```javascript
   'hello world!'.toUpperCase(); // "HELLO WORLD!"
   ```

7. **`replace(searchFor, replaceWith)`**: Returns a new string with some or all matches of a pattern replaced by a replacement.

   ```javascript
   'Hello world!'.replace('world', 'everyone'); // "Hello everyone!"
   ```

8. **`slice(startIndex, endIndex)`**: Extracts a section of a string and returns it as a new string, without modifying the original string.

   ```javascript
   'Hello world!'.slice(0, 5); // "Hello"
   ```

9. **`split(separator, limit)`**: Splits a String object into an array of strings by separating the string into substrings.

   ```javascript
   'Hello world!'.split(' '); // ["Hello", "world!"]
   ```

10. **`trim()`**: Trims whitespace from both ends of a string.

    ```javascript
    '   Hello world!   '.trim(); // "Hello world!"
    ```

11. **`substring(startIndex, endIndex)`**: Returns the part of the string between the start and end indexes, or to the end of the string.
    ```javascript
    'Hello world!'.substring(0, 5); // "Hello"
    ```

These methods provide various ways to manipulate and inspect strings in JavaScript.

## Practices:

1. 'Hello' press Enter, this is a string represents the text // output: 'Hello'
2. alert('Hello!'); this code create the popup page when you press Enter // Output: supersimple.dv says Hello!
3. 'some' + 'text' // output: 'sometext' this result of concatenation
4. 'some' + 'more' + 'string' // Output: 'somemorestring'
5. typeof 2 // Output: 'number'
6. typeof 'hello' // Output: 'string'
7. 'hello' + 3 // Output: 'hello3'
8. typeof 'hello' + 3 // Output: 'string3'
9. typeof 3 + 'hello' // Output: 'numberhello'
10. '$' + 20.95 + 7.99 // Output: '$20.957.99'
11. '$' + (20.95 + 7.99) // Output: '$28.939999999999998'
12. '$' + Math.round(20.95 + 7.99) // Output: '$29'
13. '$' + (2095 + 799) / 100 // Output: '$28.94'
14. '$' + 2095 / 100 // Output: '$20.95'
15. '$' + 799 / 100 // Output: '$7.99'
16. 'Items (' + (1 + 1 ) + '): $' + (2095 + 799) / 100 // Output: 'Items (2): $28.94'
17. alert('Items (' + (1 + 1 ) + '): $' + (2095 + 799) / 100); // Output: popup 'supersimple.dv says Items (2): $28.94
18. "I'm learning JavaScript" // Output: "I'm learning JavaScript" the single quotes does not work
19. 'I\'m learning JavaScript' // Output: "I'm learning JavaScript", this way you can use single quote that works in JavaScript [\']: escape character
20. alert('some\ntext'); // Output: popup some text this [\n] escape character for the new line string / character
21. `Items(${1 + 1}): $${(2095 + 799) /100 }` this using back tick // Output: 'Items(2): $28.94'
22. `some text` Between `some` and `text` press Enter, while we are using back tick in the console to enter multiple line // Output: 'some\ntext'

## REVIEW

Please explain me with examples the following points of reviews in JavaScript as below:

1. String represents text
2. Using strings and numbers together
3. Three ways to create strings: '...', "...", `...` (template strings)
4. Escape characters: [...\'...], [...\n...]
5. Interpolation, multi-line strings

6. **String Represents Text**

   - Strings in JavaScript are used to represent text. They can be any sequence of characters, including letters, numbers, symbols, and spaces.
     ```javascript
     let greeting = 'Hello, world!';
     ```

7. **Using Strings and Numbers Together**

   - You can combine strings and numbers using the `+` operator. When a number is used with a string, the number is converted to a string.
     ```javascript
     let age = 25;
     let ageText = 'I am ' + age + ' years old.';
     console.log(ageText); // "I am 25 years old."
     ```

8. **Three Ways to Create Strings**

   - Single quotes (`'...'`), double quotes (`"..."`), and backticks (`` `...` ``) for template strings.
     ```javascript
     let singleQuotes = 'Hello, world!';
     let doubleQuotes = 'Hello, world!';
     let templateString = `Hello, world!`;
     ```

9. **Escape Characters**

   - Use backslash ([`\`] to escape special characters within strings, such as single quotes, double quotes, and newlines (`\n`).
     ```javascript
     let quote = "He said, 'Hello, world!'";
     let multiLine = 'This is the first line.\nAnd this is the second.';
     ```

10. **Interpolation, Multi-line Strings**
    - Template strings (using backticks) allow for interpolation (inserting expressions into strings) and creating multi-line strings easily.
      ```javascript
      let name = 'John';
      let greeting = `Hello, ${name}!`; // Interpolation
      let multiLine = `This is the first line.
      And this is the second.`; // Multi-line string
      ```

These features make working with text in JavaScript flexible and powerful, allowing for easy manipulation and presentation of data as strings.

## Common string manipulation methods in JavaScript include:

1. **`slice(start, end)`**: Extracts a part of a string and returns it as a new string, without modifying the original string.

   ```javascript
   'Mozilla'.slice(0, 3); // "Moz"
   ```

2. **`substring(start, end)`**: Similar to `slice()`, but cannot handle negative indices.

   ```javascript
   'Mozilla'.substring(0, 3); // "Moz"
   ```

3. **`substr(start, length)`**: Similar to `slice()` but the second parameter specifies the number of characters to extract.

   ```javascript
   'Mozilla'.substr(0, 3); // "Moz"
   ```

4. **`replace(searchFor, replaceWith)`**: Replaces occurrences of a specified value with another value in a string.

   ```javascript
   'Mozilla'.replace('Moz', 'Van'); // "Vanilla"
   ```

5. **`toUpperCase()`**: Converts the entire string to uppercase letters.

   ```javascript
   'Mozilla'.toUpperCase(); // "MOZILLA"
   ```

6. **`toLowerCase()`**: Converts the entire string to lowercase letters.

   ```javascript
   'Mozilla'.toLowerCase(); // "mozilla"
   ```

7. **`concat(string2, string3, ..., stringN)`**: Concatenates two or more strings.

   ```javascript
   'Hello'.concat(' ', 'world!'); // "Hello world!"
   ```

8. **`trim()`**: Removes whitespace from both ends of a string.

   ```javascript
   '   Mozilla   '.trim(); // "Mozilla"
   ```

9. **`split(separator, limit)`**: Splits a string into an array of substrings.

   ```javascript
   'Mozilla Firefox'.split(' '); // ["Mozilla", "Firefox"]
   ```

10. **`charAt(position)`**: Returns the character at the specified position.

    ```javascript
    'Mozilla'.charAt(0); // "M"
    ```

11. **`charCodeAt(position)`**: Returns the Unicode of the character at the specified position.

    ```javascript
    'Mozilla'.charCodeAt(0); // 77
    ```

12. **`includes(searchString, position)`**: Determines whether one string may be found within another string, returning true or false as appropriate.

    ```javascript
    'Mozilla'.includes('zilla'); // true
    ```

13. **`startsWith(searchString, position)`**: Determines whether a string begins with the characters of a specified string.

    ```javascript
    'Mozilla'.startsWith('Moz'); // true
    ```

14. **`endsWith(searchString, length)`**: Determines whether a string ends with the characters of a specified string.
    ```javascript
    'Mozilla'.endsWith('lla'); // true
    ```

These methods provide a robust toolkit for manipulating and inspecting strings in JavaScript.
