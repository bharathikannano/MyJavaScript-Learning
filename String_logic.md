### Capitalize a String

```javascript
const capitalize = str => str.charAt(0).toUpperCase() + str.slice(1)

capitalize("javascript one-liners are fun")  //Javascript one-liners are fun
```

### Check if a string consists of a repeated character sequence

```javascript
const consistsRepeatedSubstring = (str) => `${str}${str}`.indexOf(str, 1) !== str.length;

consistsRepeatedSubstring('aa'); // true
consistsRepeatedSubstring('aaa'); // true
consistsRepeatedSubstring('ababab'); // true
consistsRepeatedSubstring('abc'); // false
```

### Check if a string is a palindrome

```javascript
const isPalindrome = (str) => str === (typeof str === 'string') ? str.split('').reverse().join('') : "Give perm is not string";

isPalindrome('abc'); // false
isPalindrom('abcba'); // true
```

### Check if two strings are anagram
```javascript
const anagram = (str1, str2) => str1.split('').sort().join('') === str2.split('').sort().join('');

areAnagram('listen', 'silent'); // true
areAnagram('they see', 'the eyes'); // true
areAnagram('node', 'deno'); // true
```

### Get the file extension from a file name

```javascript
const ext = (fileName) => fileName.split('.').pop();

ext("hello.js") //'js'
ext("index.html") //'html'

```

### Repeat a string
```javascript
const repeat = (str, numberOfTimes) => str.repeat(numberOfTimes);

// or

const repeat = (str, numberOfTimes) => Array(numberOfTimes + 1).join(str);

repeat("a",10) //'aaaaaaaaaa'

```

### Replace the first given number of characters of a string with another character
```javascript
const mask = (str, num, mask) => `${str}`.slice(num).padStart(`${str}`.length, mask);
mask(1234567890, 3, '*'); // ***4567890
```

### Sort the characters of a string in the alphabetical order
```javascript
const sort = (str) =>
    str
        .split('')
        .sort((a, b) => a.localeCompare(b))
        .join('');
        
 sort('hello world'); // dehllloorw       
```
