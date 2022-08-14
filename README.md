# JAVASCRIPT CHEATSHEET

**STRING METHODS:**
[String.charAt](#charAt) | [String.charCodeAt](#charCodeAt) | [String.endsWith](#endsWith) | [String.includes](#includes) | [String.indexOf](#indexOf) | [String.lastIndexOf](#lastIndexOf) | [String.match](#match) | [String.matchAll](#matchAll) | [String.padEnd](#padEnd) | [String.padStart](#padStart) | [String.repeat](#repeat) | [String.replace](#replace) | [String.replaceAll](#replaceAll) | [String.search](#search) | [String.slice](#slice) | [String.split](#split) | [String.startsWith](#startsWith) | [String.substring](#substring) | [String.substr](#substr) | [String.toLowerCase](#toLowerCase) | [String.toUpperCase](#toUpperCase) | [String.toString](#toString) | [String.trim](#trim) | [String.charAt](#charAt) | [String.trimEnd](#trimEnd) | [String.trimStart](#trimStart)

**ARRAYS METHODS:**

**ADDING**: [.push()](#push) | [.unshift()](#unshift) | [.splice()](#splice) | **REORGANIZING**: [.copyWithin()](#copyWithin) | [.slice()](#slice) | [.splice()](#splice) | **COMBINING**: [.concat()](#concatArrayMethod) | [...](#dots) | **REMOVING**: [.pop()](#pop) | [.shift()](#shift) | [.splice()](#spliceRemove) | **FILTERING/SEARCHING**: [.filter()](#push) | [.find()](#find) | [.findIndex()](#findIndex) | [.indexOf()](#indexOfFind) | [.lastIndexOf()](#lastIndexOfFind) | **SORTING**:  [.sort()](#sort) | **LOOP STRUCTURES**: [.map()](#sort) | [.flatMap()](#flatMap) | [.forEach()](#forEach) | [.reduce()](#reduce) | **BOOLEANS**: [.every()](#every) | [.some()](#some) | [.includes()](#includesBooleans) | **CREATING**: [Array.of()](#arrayof) | [Array.from()](#arrayfrom) | [.fill()](#fill) | **MORPHING**: [.entries()](#entries) | [.values()](#values) | [.keys()](#keys) | [.join()](#join) | [.toString()](#toString2) | [.toLocalString()](#toLocalString2) | **INFORMATION**: [.at() - ⚠ Experimental technology!](#at) | [.length()](#length) | [Array.isArray()](#arrayarray) | **MISC**: [.flat()](#flat) | [.reverse()](#reverse2) |

**OPERATORS:**
[Basic operators](#basicoperators) | [Comparison operators](#comparisonoperators) | [Logical operators](#logicaloperators) | [Bitwise operators](#bitwise) | [Arithmetic](#arithmetic) |

**REGULAR EXPRESSIONS:**
[Patern modifiers](#paternmodifiers) | [Brackets](#brackets) | [Metacharacters](#metacharacters) | [Quantifiers](#quantifiers) |

**NUMBERS AND MATH:**
[Numbers](#numbers) | [Math](#math) |

## JAVASCRIPT STRING METHODS

#### <a name="charAt"></a>String.charAt()

```javascript
// Returns a string representing the character at the given index.
let str = "Hello World";
str.charAt(0); // "H"
```

#### <a name="charCodeAt"></a>String.charCodeAt()

```javascript
// Returns a number representing the UTF-16 code unit value of the character at the given index.
let str = "Hello World";
str.charCodeAt(0); // 72
```

#### <a name="concat"></a>String.concat()

```javascript
// Returns a new string containing the concatenation of the given strings.
let str = "Hello";
let str2 = " World";
str.concat(str2); // "Hello World"

console.log(`${str}${str2}`); // "Hello World"
console.log(str + str2); // "Hello World"
```

#### <a name="endsWith"></a>String.endsWith()

```javascript
// Returns true if the string ends with the given string, otherwise false.
let str = "Hello World";
str.endsWith("World"); // true
```

#### <a name="includes"></a>String.includes()

```javascript
// Returns true if the string contains the given string, otherwise false.
let str = "Hello World";
str.includes("World"); // true
```

#### <a name="indexOf"></a>String.indexOf()

```javascript
// Returns the index within the string of the first occurrence of the specified value, or -1 if not found.
let str = "Hello World";
str.indexOf("World"); // 6
```

#### <a name="lastIndexOf"></a>String.lastIndexOf()

```javascript
// Returns the index within the string of the last occurrence of the specified value, or -1 if not found.
let str = "Hello World";
str.lastIndexOf("World"); // 6
```

#### <a name="match"></a>String.match()

```javascript
// Returns a list of matches of a regular expression against a string.
let str = "Hello World";
str.match(/[A-Z]/); // ["H"]
```

#### <a name="matchAll"></a>String.matchAll()

```javascript
// Returns a list of matches of a regular expression against a string.
let str = "Hello World";
str.matchAll(/[A-Z]/g); // ["H", "W"]
// OR
str.match(/[A-Z]/gi); // ["H", "W"]

// /g is global
// /gi is global and case-insensitive
```

#### <a name="padEnd"></a>String.padEnd()

```javascript
// Returns a new string with some content padded to the end of the string.
let str = "Hello";
str.padEnd(14, "World"); // "HelloWorldWorl"
```

#### <a name="padStart"></a>String.padStart()

```javascript
// Returns a new string with some content padded to the start of the string.
let str = "Hello";
str.padStart(12, "World"); // "WorldWoHello"
```

#### <a name="repeat"></a>String.repeat()

```javascript
// Returns a new string that contains the specified number of copies of the string.
let str = "Hello";
str.repeat(3); // "HelloHelloHello"
```

#### <a name="replace"></a>String.replace()

```javascript
// Returns a new string with some or all matches of a regular expression replaced by a replacement string.
let str = "Hello World";
str.replace("l", "*"); // "He*lo World"
```

#### <a name="replaceAll"></a>String.replaceAll()

```javascript
// Returns a new string with some or all matches of a regular expression replaced by a replacement string.
let str = "Hello World";
str.replaceAll("l", "*"); // "He**o Wor*d"
OR;
str.replace(/l/g, "*"); // "He**o Wor*d"
```

#### <a name="search"></a>String.search()

```javascript
// Returns the index within the string of the first occurrence of the specified value, or -1 if not found.
let str = "Hello World 1";
let regex = /[^\D\s]/g; // Find digit
str.search(regex); // 12
```

[Check Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)
[Check Regular Expressions HERE](#regularexp)

#### <a name="slice"></a>String.slice()

```javascript
// Returns a new string containing the characters of the string from the given index to the end of the string.
let str = "Hello World";
str.slice(6); // "World"
```

#### <a name="split"></a>String.split()

```javascript
// Returns an array of strings split at the given index.
let str = "Hello World";
str.split(" "); // ["Hello", "World"]
```

#### <a name="startsWith"></a>String.startsWith()

```javascript
// Returns true if the string starts with the given string, otherwise false.
let str = "Hello World";
str.startsWith("Hello"); // true
```

#### <a name="substring"></a>String.substring()

```javascript
// Returns a new string containing the characters of the string from the given index to the end of the string.
let str = "Hello World";
str.substring(1, 2); // "e"
```

#### <a name="substr"></a>String.substr()

```javascript
// Returns a new string containing the characters of the string from the given index to the end of the string.
let str = "Hello World";
str.substr(1, 2); // "el"
```

*NOTE: **substr** takes parameters as (from, length).*

#### <a name="toLowerCase"></a>String.toLowerCase()

```javascript
// Returns a new string with all the uppercase characters converted to lowercase.
let str = "Hello World";
str.toLowerCase(); // "hello world"
```

#### <a name="toUpperCase"></a>String.toUpperCase()

```javascript
// Returns a new string with all the lowercase characters converted to uppercase.
let str = "Hello World";
str.toUpperCase(); // "HELLO WORLD"
```

#### <a name="toString"></a>String.toString()

```javascript
// Returns the string representation of the specified object.
let str = new String("Hello World");
console.log(str); // Object of String
str.toString(); // "Hello World"
```

#### <a name="trim"></a>String.trim()

```javascript
// Returns a new string with the leading and trailing whitespace removed.
let str = "  Hello World  ";
str.trim(); // "Hello World"
```

#### <a name="trimEnd"></a>String.trimEnd()

```javascript
// Returns a new string with the trailing whitespace removed.
let str = "  Hello World  ";
str.trimEnd(); // "  Hello World"
```

#### <a name="trimStart"></a>String.trimStart()

```javascript
// Returns a new string with the leading whitespace removed.
let str = "  Hello World  ";
str.trimStart(); // "Hello World  "
```

## JAVASCRIPT ARRAYS METHODS

### ADDING

#### <a name="push"></a>.push()

```javascript
// Add anything to the end of an array.
let a = []
let b = {}
a.push(b)
console.log(a[0] === b) // true

// Add more than one item at a time.
let x = ['a']
x.push('b', 'c')
console.log(x) // ['a', 'b', 'c']
```

#### <a name="unshift"></a>.unshift()

```javascript
// Add to the beginning of array and returns the new length of the array.
let x = ['c', 'd']
x.unshift('a', 'b') // 4
console.log(x) // ['a', 'b', 'c', 'd']
```

#### <a name="splice"></a>.splice()

```javascript
// Add element to an arbitrary location (second param 0).
let a = [1, 2, 3, 4]
a.splice(2, 0, 'foo')
console.log(a) // [1, 2, "foo", 3, 4]
```

### REORGANIZING

#### <a name="copyWithin"></a>.copyWithin()

```javascript
// Copy part of an array to another location within the same array.
let a = ['a', 'b', 'c', 'd', 'e']
// target, start, end
array1.copyWithin(0, 3, 4)
console.log(a) // ["d", "b", "c", "d", "e"]
```

#### <a name="slice"></a>.slice()

```javascript
// Returns a portion of an array selected with the start and end parameters.
let a = ['ant', 'bison', 'camel', 'duck', 'elephant']
console.log(animals.slice(2)) // ["camel", "duck", "elephant"]
console.log(animals.slice(2, 4)) // ["camel", "duck"]
```

#### <a name="splice"></a>.splice()

```javascript
// Replace an arbitrary element in array (second param 1).
let a = [1, 2, 3, 4]
a.splice(2, 1, 'foo')
console.log(a) // [1, 2, "foo", 4]
```

### COMBINING

#### <a name="concatArrayMethod"></a>.concat()

```javascript
// Create a new array from two arrays.
let x = ['a', 'b', 'c']
let y = ['d', 'e', 'f']
let z = x.concat(y)
console.log(z) // ['a', 'b', 'c', 'd', 'e', 'f']
```

#### <a name="dots"></a>...

```javascript
// Not a method, but create a new array from two arrays by spreading them.
let x = ['a', 'b']
let y = ['c', 'd']
let z = [...x, ...y]
console.log(z) // ['a', 'b', 'c', 'd']
```

### REMOVING

#### <a name="pop"></a>.pop()

```javascript
// Removes the last element from array and returns it. Changes the length of the array.
let a = ['a', 'b', 'c']
console.log(a.pop()) // c
console.log(a) // ["a", "b"]
```

#### <a name="shift"></a>.shift()

```javascript
// Like pop but removes the first element from array and returns it. Also changes the length of the array.
let a = ['a', 'b', 'c']
console.log(a.shift()) // a
console.log(a) // ["b", "c"]
```

#### <a name="spliceRemove"></a>.splice()

```javascript
// Remove elements from the middle of an array. Param 1: index to start removing. Param 2: index to stop removing.
let a = ['a', 'b', 'c', 'd', 'e']
a.splice(1, 3)
console.log(a) // ["a", "e"]
```

### FILTERING/SEARCHING

#### <a name="filter"></a>.filter()

```javascript
// Keeps the items in the array that pass the test provided by the callback function.
let a = ['foo', 'bar', 'fooz']
let b = a.filter(v => v.startsWith('foo'))
console.log(b) // ['foo', 'fooz']
```

#### <a name="find"></a>.find()

```javascript
// Finds the first item in an array that matches.
let a = [5, 12, 8, 130, 44]
let b = a.find(v => v > 10)
console.log(b) // 12
```

#### <a name="findIndex"></a>.findIndex()

```javascript
// Like find but instead of returning the item, it returns the index.
let a = [5, 12, 8, 130, 44]
let b = a.findIndex(v => v > 13)
console.log(b) // 3
```

#### <a name="indexOfFind"></a>.indexOf()

```javascript
// Finds the first index of an element. Returns -1 if not found.
let a = ['foo', 'bar', 'baz']
console.log(a.indexOf('baz')) // 2
console.log(a.indexOf('quix')) // -1
```

#### <a name="lastIndexOfFind"></a>.lastIndexOf()

```javascript
// Like indexOf, but finds the last index of an element. Returns -1 if not found.
let a = ['foo', 'bar', 'baz', 'foo']
console.log(a.lastIndexOf('foo')) // 3
console.log(a.lastIndexOf('quix')) // -1
```

### SORTING

#### <a name="sort"></a>.sort()

```javascript
// Sort alphabetically.
let a = ['d', 'j', 'a', 'b', 'c', 'g']
a.sort()
console.log(a) // ["a", "b", "c", "d", "g", "j"]

// Sort in reversed alphabetical order.
let a = ['d', 'j', 'a', 'b', 'c', 'g']
a.sort().reverse()
console.log(a) // [ "j", "g", "d", "c", "b", "a"]

// 	Sort numerically.
let a = [5, 10, 7, 1, 3, 2]
a.sort((a, b) => a - b)
console.log(a) // [ 1, 2, 3, 5, 7, 10]

// Descending numerical sort (flip the `a` anb `b` around).
let a = [5, 10, 7, 1, 3, 2]
a.sort((a, b) => b - a)
console.log(a) // [10, 7, 5 ,3, 2, 1]
```

### LOOP STRUCTURES

#### <a name="map"></a>.map()

```javascript
// Maps an array to another array by executing a callback function on each element.
let a = [1, 2, 3, 4]
let b = a.flatMap(v => [v * 2])
console.log() // 2, 4, 6, 8
```

#### <a name="flatMap"></a>.flatMap()

```javascript
// Same as map but it flattens the array, same as: [[]].map(v => v).flat().
let a = [1, 2, 3, 4]
let b = a.map(v => v * 2)
console.log(b) // 2, 4, 6, 8
```

#### <a name="forEach"></a>.forEach()

```javascript
// Executes a function for every element in array, does not return anything.
let a = [1, 2]
a.forEach(x => console.log(x))
// 1
// 2
```

#### <a name="reduce"></a>.reduce()

```javascript
// Executes a user-supplied “reducer” callback function on each element of the array, in order, passing in the return value from the calculation on the preceding element.
let a = [1, 2, 3, 4]
let b = a.reduce((acc, v) => acc + v)
// Basically: 1 + 2 + 3 + 4
console.log(b) // 10

// Return object from an array method.
let a = [1, 2, 3, 4]
let b = a.reduce((acc, v) => ({ [v]: v, ...acc }), {})
console.log(b) // {"1": 1,"2": 2,"3": 3,"4": 4}
```

### BOOLEANS

#### <a name="every"></a>.every()

```javascript
// Tests if every item in the array passes the test.
let isBelow = v => v < 40
let a = [1, 30, 39, 29, 10, 13]
console.log(a.every(isBelow)) // true
```

#### <a name="some"></a>.some()

```javascript
// Tests if some items in the array passes the test.
let isOver = v => v > 40
let a = [1, 30, 41, 29, 10, 13]
console.log(a.some(isOver)) // true
```

#### <a name="includesBooleans"></a>.includes()

```javascript
// Tests if some items in the array passes the test.
let a = [1, 2, 3]
let b = a.includes(2)
console.log(b) // true
```

### CREATING

#### <a name="arrayof"></a>Array.of()

```javascript
// Creates a new array from the given arguments.
Array.of('foo', 'bar')
// ['foo', 'bar']
```

#### <a name="arrayfrom"></a>.Array.from()

```javascript
// Creates a new array from an array-like or iterable object.
console.log(Array.from('foo')) // ['f', 'o', 'o']
console.log(Array.from([1, 2, 3], x => x + x)) // [2, 4, 6]
```

#### <a name="fill"></a>.fill()

```javascript
// Change all elements in an array to a static value.
let a = [1, 2, 3, 4]
let b = a.fill(0, 2, 4)
console.log(b) // [1, 2, 0, 0]
```

### MORPHING

#### <a name="entries"></a>.entries()

```javascript
// Returns an iterator object with key/value pairs for each index in the array.
let a = ['a', 'b', 'c']
let iterator = a.entries()
console.log(iterator.next().value) // [0, "a"]
console.log([...iterator]) // [[0, "a"], [1, "b"], [2, "c"]]`]
```

#### <a name="values"></a>.values()

```javascript
// 	Returns an iterator object with values for each index in the array. Changes the data type from array to iterator.
let a = ['a', 'b', 'c']
let iterator = a.values()
for (const v of iterator) { console.log(v) } // a, b, c
```

#### <a name="keys"></a>.keys()

```javascript
// 	Returns an iterator object with keys for each index in the array. Changes the data type from array to iterator.
let a = ['a', 'b', 'c']
let iterator = a.keys()
for (const v of iterator) { console.log(v) } // 1, 2, 3
```

#### <a name="join"></a>.join()

```javascript
// Turn array into a string by joining the element togethe
let a = ['foo', 'bar', 'baz']
a.join() // foo,bar,baz
a.join('-') // foo-bar-baz
```

#### <a name="toString2"></a>.toString()

```javascript
// Turn array or any other object into a string.
let a = ['foo', 'bar', 'baz']
a.toString() // foo,bar,baz
```

#### <a name="toLocalString2"></a>.toLocalString()

```javascript
// Stringifies an array in a locale sensitive way.
let a = [1, 'a', new Date('21 Dec 1997 14:12:00 UTC')]
a.toLocaleString('en', { timeZone: 'UTC' }) // 1,a,12/21/1997, 2:12:00 PM
a.toLocaleString('de') // '1,a,21.12.1997, 15:12:00'
// toLocaleString(locales, options)
```

[.toLocalString() - Parameter Values](https://www.w3schools.com/jsref/jsref_tolocalestring.asp)

### INFORMATION

#### <a name="at"></a>.at() - ⚠ Experimental technology!

```javascript
// Takes in integer value and returns the array element at that index. -1 returns the last element. ⚠️ Experimental technology.
let x = ['a', 'b', 'c']
console.log(a.at(1)) // b
console.log(a.at(-1)) // c
```

#### <a name="length"></a>.length()

```javascript
// Gets the element count of an array.
let x = ['a', 'b', 'c']
console.log(a.length) // 3
```

#### <a name="arrayarray"></a>Array.isArray()

```javascript
// Tests if a given variable is an array.
let a = ['a', 'b']
console.log(Array.isArray(a)) // true
```

### MISC

#### <a name="flat"></a>.flat()

```javascript
// Flatten a nested array.
let a = [0, 1, 2, [3, 4]]
let b = a.flat()
console.log(b) // [0, 1, 2, 3, 4]
```

#### <a name="reverse2"></a>.reverse()

```javascript
// Reverses the order of an array.
let a = [1, 2, 3, 4]
a.reverse()
console.log(a) // [4, 3, 2, 1]
```

## JAVASCRIPT OPERATORS
### <a name="basicoperators"></a>BASIC OPERATORS
```
+     // Addition
-     // Subtraction
*     // Multiplication
/     // Division
(..)  // Grouping operator
%     // Modulus (remainder)
++    // Increment numbers
--    // Decrement numbers
```

### <a name="comparisonoperators"></a>COMPARISON OPERATORS
```
==    // Equal to
===   // Equal value and equal type
!=    // Not equal
!==   // Not equal value or not equal type
>     // Greater than
<     // Less than
>=    // Greater than or equal to
<=    // Less than or equal to
?     // Ternary operator
```

### <a name="logicaloperators"></a>LOGICAL OPERATORS
```
&&   // Logical and
||   // Logical or
!    // Logical not
```

### <a name="bitwise"></a>BITWISE OPERATORS
```
&    // AND statement
|    // OR statement
~    // NOT
^    // XOR
<<   // Left shift
>>   // Right shift
>>>  // Zero fill right shift
```

### <a name="arithmetic"></a>ARITHMETIC
```
a * (b + c)         // grouping
person.age          // member
person[age]         // member
!(a == b)           // logical not
a != b              // not equal
typeof a            // type (number, object, function...)
x << 2  x >> 3      // minary shifting
a = b               // assignment
a == b              // equals
a != b              // unequal
a === b             // strict equal
a !== b             // strict unequal
a < b   a > b       // less and greater than
a <= b  a >= b      // less or equal, greater or eq
a += b              // a = a + b (works with - * %...)
a && b              // logical and
a || b              // logical or
```

## JAVASCRIPT REGULAR EXPRESSIONS
### <a name="paternmodifiers"></a>PATERN MODIFIERS
```
e    // Evaluate replacement
i    // Perform case-insensitive matching
g    // Perform global matching
m    // Perform multiple line matching
s    // Treat strings as single line
x    // Allow comments and whitespace in pattern
U    // Non Greedy pattern
```

### <a name="brackets"></a>BRACKETS
```
[abc]    // Find any of the characters between the brackets
[^abc]   // Find any character not in the brackets
[0-9]    // Used to find any digit from 0 to 9
[A-z]    // Find any character from uppercase A to lowercase z
(a|b|c)  // Find any of the alternatives separated with |
```

### <a name="metacharacters"></a>METACHARACTERS
```
.       // Find a single character, except newline or line terminator
\w      // Word character
\W      // Non-word character
\d      // A digit
\D      // A non-digit character
\s      // Whitespace character
\S      // Non-whitespace character
\b      // Find a match at the beginning/end of a word
\B      // A match not at the beginning/end of a word
\0      // NUL character
\n      // A new line character
\f      // Form feed character
\r      // Carriage return character
\t      // Tab character
\v      // Vertical tab character
\xxx    // The character specified by an octal number xxx
\xdd    // Character specified by a hexadecimal number dd
\uxxxx  // The Unicode character specified by a hexadecimal number xxxx
```

### <a name="quantifiers"></a>QUANTIFIERS
```
n+      //Matches any string that contains at least one n
n*      //Any string that contains zero or more occurrences of n
n?      //A string that contains zero or one occurrences of n
n{X}    //String that contains a sequence of X n’s
n{X,Y}  //Strings that contains a sequence of X to Y n’s
n{X,}   //Matches any string that contains a sequence of at least X n’s
n$      //Any string with n at the end of it
^n      //String with n at the beginning of it
?=n     //Any string that is followed by a specific string n
?!n     //String that is not followed by a specific string n

```


## JAVASCRIPT NUMBERS AND MATH
### <a name="numbers"></a>NUMBERS
```
let pi = 3.141;
pi.toFixed(0);            // returns 3
pi.toFixed(2);            // returns 3.14 - for working with money
pi.toPrecision(2)         // returns 3.1
pi.valueOf();             // returns number
Number(true);             // converts to number
Number(new Date())        // number of milliseconds since 1970
parseInt("3 months");     // returns the first number: 3
parseFloat("3.5 days");   // returns 3.5
Number.MAX_VALUE          // largest possible JS number
Number.MIN_VALUE          // smallest possible JS number
Number.NEGATIVE_INFINITY  // -Infinity
Number.POSITIVE_INFINITY  // Infinity
```

### <a name="math"></a>MATH
```
let pi = Math.PI;                     // 3.141592653589793
Math.round(4.4);                      //  4 - rounded
Math.round(4.5);                      //  5
Math.pow(2,8);                        //  256 - 2 to the power of 8
Math.sqrt(49);                        //  7 - square root 
Math.abs(-3.14);                      //  3.14 - absolute, positive value
Math.ceil(3.14);                      //  4 - rounded up
Math.floor(3.99);                     //  3 - rounded down
Math.sin(0);                          //  0 - sine
Math.cos(Math.PI);                    // OTHERS: tan,atan,asin,acos,
Math.min(0, 3, -2, 2);                //  -2 - the lowest value
Math.max(0, 3, -2, 2);                //  3 - the highest value
Math.log(1);                          //  0 natural logarithm 
Math.exp(1);                          //  2.7182pow(E,x)
Math.random();                        // random number between 0 and 1
Math.floor(Math.random() * 5) + 1;    // random integer, from 1 to 5
```
