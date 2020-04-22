# String Methods

## Practice String Methods-writeTextAnswer

Go to this [link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charAt) and look for the name of method to learn about it.

**Write in your own way of understanding (dont copy paste)**

Only if you are done with step 1 you should go ahead.

1. Practice it by yourself in console (4-5 times to understand)
2. Data types of parameters
3. Return value type
4. Example (3)
5. In your words what this method does.

Example:

1. `charAt`

   - This method accepts one parameter (index) of number data type.
   - It returns the charater on specific index (provided through parameter)
   - Example:
     ```js
     let name = "Arya Stark";
     name.charAt(2); //"y"
     let sentance = "A quick brown fox jumped over a lazy dog";
     sentance(4); // "i"
     let houseName = "Starks";
     houseName.charAt(0); // "S"
     ```
   - `charAt` accepts a index (number data type) and return the character on that index.

2. `toUpperCase`

   - This method accepts no parameter.
   - It returns the calling string value converted to uppercase.
   ```js
    let name = "Arya Stark";
    name.toUpperCase(); //"ARYA STARK"
    let sentance = "A quick brown fox jumped over a lazy dog";
    sentance().toUpperCase(); //"A QUICK BROWN FOX JUMPED OVER A LAZY DOG"
    let surname = "starks";
    surname.toUpperCase(); //"STARKS"
   ```
   - `toUpperCase` returns a calling string value converted to uppercase.

3. `toLowerCase`

   - This method accepts no parameter.
   - It returns the calling string value converted to lowercase.
   ```js
    let name = "Arya Stark";
    name.toLowerCase(); //"arya stark"
    let sentance = "A quick brown fox jumped over a lazy dog";
    sentance().toLowerCase(); //"a quick brown fox jumped over a lazy dog"
    let surname = "starks";
    surname.toLowerCase(); //"STARKS"
   ```
   - `toLowerCase` returns a calling string value converted to lowercase.

4. `trim`

  - This method accepts no parameter.
  - It returns a string stripped of whitespace from both ends.
  ```js
    let name = "  Arya Stark ";
    name.trim(); //"Arya Stark"
    let sentance = "  A quick brown fox      jumped over a lazy dog  ";
    sentance.trim(); //"A quick brown fox       jumped over a lazy dog";
    let surname = " starks  "
    surname.trim(); //"starks"
  ```
  - trim() method returns the string stripped of whitespace from both ends. trim() does not affect the value of the str itself.

5. `trimEnd`

- This method accepts no parameter.
- It returns a string stripped of whitespace from the end.
```js
  let name = "  Arya Stark  ";
  name.trimEnd(); //" Arya Stark";
  let sentance = "  A quick brown fox      jumped over a lazy dog  ";
  sentance.trimEnd(); // "  A quick brown fox      jumped over a lazy dog";
  let surname = " starks ";
  surname.trimEnd(); //" starks"
```
- trimEnd() method returns a string string stripped of whitespace from right end. It does not affect the value of the string itself.


6. `trimStart`

- This method accepts no parameter.
- It returns a string stripped of whitespace from the start.
```js
  let name = "  Arya Stark ";
  name.trimStart(); // "Arya Stark "
  let sentance = "  A quick brown fox      jumped over a lazy dog  ";
  sentance.trimStart(); // "A quick brown fox      jumped over a lazy dog  "
  let surname = " starks ";
  surname.trimStart(); // "starks "

```
- trimStart() method returns a stirng stripped of whitespace from the left end. It does not affect the value of the string itself.

7. `concat`

- This method accepts 1 or more parameters that are to be concatenated.
- It returns a new string containing the combined text of the strings provided.
```js
  let str1 = "Hello";
  let str2 = "World";
  str1.concat(str2); // "HelloWorld"
  let str3 = " ";
  str1.concat(str3, str2); // "Hello World"
  let str4 = ", ";
  str1.concat(str4, str2); // "Hello, World"
```
- concat() method returns a new string containing the combined text of the strings provided. It does not affect the original string to which it is applied.

8. `endsWith`

- This method accepts two parameters. One is searchString and other is length. The second parameter is optional. Though it sets the length of the string.
- Based on whether a string ends with the characters of a specified string, it returns true or false.
```js
  let str = "Raghuram";
  let searchString = "ram";
  str.endsWith(searchString); // true
  str.endsWith("ur",6); // true
  let str2 = "Is it ends with question? Yes";
  str2.endsWith("?"); //  false

```
- endsWith() method lets us determine whether or not a string ends with another string. This method is case sensitive.

9. `includes`

- This method accepts two parameters. One is searchString of "string" data type and other being position that is of "number" data type. Though position parameter is optional. It tells where to searchString from.
- It returns true if search string is found anywhere within the string, otherwise false if not.

```js
  let str = "Power rangers SPD";
  let searchString = "rangers";
  str.includes(searchString) // true
  str.includes(searchString,8) // false

  str.includes("raghuram"); //false
```
- includes() lets us search for a string within a string and is case insensitive.

10. `indexOf`

- This method accepts two parameters. First parameter is searchElement which is of string type and the second is fromIndex which is of number type. fromIndex parameter is of number type and if specified searchElement is searched from that index onwards.
- This method returns the first index of the element in the array, or -1 if not found.
```js
  const colors = ["red","yellow","white","blue","green"];
  let searchElement = "yellow";
  colors.indexOf(searchElement) // 1
  colors.indexOf(searchElement,3) // -1

  searchElement = "white";
  colors.indexOf(searchElement) // 2
```
- indexOf() method returns the first index at which a given element can be found in the array or -1

11. `lastIndexOf`

- This method includes two parameters one is searchValue and other is fromIndex. searchValue is of string type and fromIndex is of number type. fromIndex is from where search is started. Though fromIndex is optional parameter
- This method returns the position of last occurrence of the searchElement or returns -1 if the element is not found.
```js
  const colors = ["red","yellow","white","blue","green","yellow"];
  let searchColor = "yellow";
  colors.lastIndexOf(searchColor); // 5 and not 1
  colors.lastIndexOf("white"); // 2
  colors.lastIndexOf("maroon"); // -1
```
- lastIndexOf() returns the occurence of searchElement from the end and it is case sensitive.

12. `padEnd`

- This method accepts two parameters. One is the targetLength and another is padString. TargetLength is what that would be the final string length once padding is achieved and it is of number type. The second parameter ie padString is optional and it is the string that gets added to string until the target length is reached. By default the padding string is " " and if paddingString exceeds targetLength the part of padString is truncated from end.
- This method returns the string with some padding either with spaces or paddingString added to the string.

```js
let str = `5`;
str.padEnd(5,"0"); // "50000"

str = "raghuram";
str.padEnd(10,"."); // "raghuram.."

str.padEnd(10); // "raghuram  "

```

13. `padStart`
14. `repeat`
15. `replace`
16. `slice`
17. `split`
18. `substring`

## writeCode

Using above methods you practiced above, do the following.

```js
let from = "Syrio Forel";
let quote = "There is only one thing we say to death: Not today";
let to = "Arya Stark";

/*
1. Find the index of the first 'is' in the variable quote. And store it in a new variable named indexOfIs
*/
// Your code goes here

/*
2. Find the character at, the index indexOfIs (Problem 1) in quote.
*/
// Your code goes here

/*
3. Log the message saying `The index of first is in quote is 7`
*/
// Your code goes here

/*
4. Log the message for first 6 characters of quote like this.
The character at index 0 is 'T'
The character at index 1 is 'h'
The character at index 2 is 'e'
The character at index 3 is 'r'
The character at index 4 is 'e'
The character at index 5 is ' '
*/
// Your code goes here

/*
5. Using the variable from , to and quote variable dispaly this message
"Syrio Forel said There is only one thing we say to death: Not today to Arya Stark." (use concat method)
*/

/*
6. Does from, to and quote ends with "rk". Check all three.
*/

/*
7. Does quote includes the word "Only"
*/

/*
8. Does quote includes the word " we"
*/

/*
9. Find the index of the the word `we` in quote
*/

/*
10. Split the quote into individual word and store it in a variable name quoteSplitted
*/

/*
11. Change the word "today" in quoteSplitted to "tomorrow" and join all the words to form a sentance.
*/

/*
12. Find the index of second "o" in quote. Use indexOf
*/

/*
13. Find the last index of letter "a" in quote.
*/

/*
14. Find the second last index of letter "a" in quote.
*/

/*
15. Make the quote 70 character long. If it has less characters add rest as .......
Example: "Hello" (convert to 10 characters) => "Hello....."
*/

/*
16. Do same as (15) but the ... should come in start.
*/

/*
17. Log the repeat of "Hello World!" 10 times.
*/

/*
18. Replace today to tomorrow in quote.
*/

/*
19. Replace Stark to Lannister in quoteTo
*/

/*
20. Make the quote of length 30 and put ... at the end. (use slice)
*/

/*
21. Find out does quote, quoteFrom, quoteTo starts with "A"
*/
```

## Practice Array Methods-writeTextAnswer

Go to this [link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#) and look for the name of method to learn about it.

**Write in your own way of understanding (dont copy paste)**

Only if you are done with step 1 you should go ahead.

1. Practice it by yourself in console (2-3 times to understand)
2. Data types of parameters
3. Return value type
4. Example (3)
5. In your words what this method does.
6. Does it mutate the original value (check https://doesitmutate.xyz)

Example:

1. `concat`

   - n(any) number of values (number, string, boolean, array, null, undefined, object and function.)
   - It returns a single Array consisting of by all the values passed as parameters in the same order.
   - Example:
     ```js
     let numbers = [1, 2, 3];
     numbers.concat(4); //[1,2,3,4]
     let sentanceArray = "A quick brown fox jumped over a lazy".split(" ");
     sentanceArray.concat("dog").join(" "); //"A quick brown fox jumped over a lazy dog"
     let colors = ["red", "green", "blue"];
     colors.concat("black", "red", 21, true); // ['red','green','blue','black', 'red', 21, true]
     ```
   - `concat` accepts n number of values and returns one array with all the values in same order. It doesnot change the original array.
   - No it doesnot mutate the original array

2. `join`
3. `flat`
4. `push`
5. `indexOf`
6. `lastIndexOf`
7. `includes`
8. `reverse`
9. `every`
10. `shift`
11. `splice`
12. `find`
13. `unshift`
14. `findIndex`
15. `filter`
16. `flat`
17. `forEach`
18. `map`
19. `pop`
20. `reduce`
21. `slice`
22. `some`

## writeCode

Using above methods you practiced above, do the following.

```js
// Use the below two arrays and practice array methods
var numbers = [1, 12, 4, 18, 9, 7, 11, 3, 101, 5, 6, 9];
var strings = ["This", "is", "a", "collection", "of", "words"];

// - Find the index of `101` in numbers

// - Find the last index of `9` in numbers

// - Convert value of strings array into a sentance like "This is a collection of words"

// - Add two new words in the strings array "called" and "sentance"

// - Again convert the updated array (strings) into sentance like "This is a collection of words called sentance"

// - Remove the first word in the array (strings)

// - Find all the words that contain 'is' use string method 'includes'

// - Find all the words that contain 'is' use string method 'indexOf'

// - Check if all the numbers in numbers array are divisible by three use array method (every)

// -  Sort Array from smallest to largest

// - Remove the last word in strings

// - Find largest number in numbers

// - Find longest string in strings

// - Find all the even numbers

// - Find all the odd numbers

// - Place a new word at the start of the array use (upshift)

// - Make a subset of numbers array [18,9,7,11]

// - Make a subset of strings array ['a','collection']

// - Replace 12 & 18 with 1221 and 1881

// - Replace words in strings array with the length of the word

// - Find the sum of the length of words using above question

// - Customers Array
var customers = [
  { firstname: "Joe", lastname: "Blogs" },
  { firstname: "John", lastname: "Smith" },
  { firstname: "Dave", lastname: "Jones" },
  { firstname: "Jack", lastname: "White" }
];
// - Find all customers whose firstname starts with 'J'

// - Create new array with only first name

// - Create new array with all the full names (ex: "Joe Blogs")

// - Sort the array created above alphabetically

// - Create a new array that contains only user who has at least one vowel in the firstname.
```
