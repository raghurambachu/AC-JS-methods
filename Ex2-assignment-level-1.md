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
- padEnd() thus adds padding at the end until padding causes the string to reach the target length.

13. `padStart`

- This method accepts two parameters. 1st parameter is the target length and the other is padString. targetLength is of number type and padString is of string type. padString parameter is though optional.
- This method returns the string padded with either spaces or the padString provided.
```js
let accountNo = '1234';
accountNo.padStart(10,"*"); // "******1234"

accountNo.padStart(10); // "      1234"

accountNo.padStart(5,"-"); // "-1234"
```
- padStart() adds padding at the start of the given String, it can be either in the form of spaces or in the form of padString.

14. `repeat`

- This method takes one parameter ie count. And it is of number type.Repeat count must be non negative and less than infinity(that is it should not overflow maximum stirng size.)
- It returns a new string conaining the specified number of copies of the given string.
```js
  let str = "raghuram";
  str.repeat(2); // "raghuramraghuram"

  "raghuram".repeat(0) // ""

  "somestring".repeat(-1) // rangeError
```
- repeat() method constructs and returns a new string which contains the specified number of copies of the string on which it was called. Though it returns a new string.

15. `replace`

- This method accepts two parameters. One is regexp|substr, other is newSubStr| function. regexp is a pattern and newSubStr is the replacement String. If pattern is string only the first occurence will be replaced.
- It returns a new string with some or all matches of a pattern replaced by a replacement which can be either a string or function.
```js
const p = 'The quick brown fox jumps over the lazy dog. If the dog reacted, was it really lazy?';

const regex = /dog/gi;

const str = "India is my country";
str.replace("my","our"); // "India is our country"
```
- replace() method does not change the string, rather returns a new string. To do global search and replace we need to use regular expressions with flag g.

16. `slice`

- This method takes two parameter. One is the beginIndex and other is the endIndex. The parameter endIndex is optional. Both of these parameters are of number type. The index value can even be a negative number. For instance -1 is equivalent to saying array.length - 1 which is basically last element. If no parameter is passed it leads to creation of copy of the string as by default beginIndex is set to 0.
- It returns a new string containing an extracted section of the original string.
```js
let name = "raghuram";
name.slice(); // "raghuram"

name.slice(5); // "ram"

name.slice(0,5); // "raghu"

name.slice(-3) // "ram"
```
- slice() method thus extracts a portion of string. Original string remains unaffected.

17. `split`
- This method takes two parameters. One is separator and other is the limit. Both of them are optional. separator is the basis on which string is split into. seperator is of string type and limit is of number type. If the limit is less than string length, array would be of length of the limit based on the separator used. If no separator is mentioned the string is placed in array and array is returned.
- It returns an array of elements based on the separator. If limit parameter is set to 0 no splitting is performed.
```js
let name = "raghuram";
name.split("") // ['r','a','g','h','u','r','a','m'];

name = "raghuram,raju,bachu";
name.split(",") // ["raghuram","raju","bachu"];

name = "raghuram";
name.split() // ["raghuram"];
```
- split() returns an array of strings, which is split at each point where the separator occurs in the given string.

18. `substring`

- This method takes two parameters. One is indexStart and other is indexEnd. Both are of number type. indexEnd though is optional. 
- This method returns a portion of string within an original string. It will return the string from indexStart till the indexEnd excluding the indexEnd.
```js
let str = "raghuram"
str.substring(0,5); // "raghu"

str.substring(5); // "ram"

str.substring(5,5) // ""
```
- substring() is used to extract characters or portion of the string.

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
let indexOfIs = quote.indexOf("is") // 6

/*
2. Find the character at, the index indexOfIs (Problem 1) in quote.
*/
// Your code goes here
quote[indexOfIs]; // "i"

/*
3. Log the message saying `The index of first is in quote is 7`
*/
// Your code goes here
console.log(`The index of first is in quote is ${indexOfIs + 1}`);

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
let strArr = quote.split("",6);
function log(el,index) {
  console.log(`The character at index ${index} is '${el}'`)
}
strArr.forEach(log)

/*
5. Using the variable from , to and quote variable dispaly this message
"Syrio Forel said There is only one thing we say to death: Not today to Arya Stark." (use concat method)

*/
from.concat(" said ", quote," to ",to);

/*
6. Does from, to and quote ends with "rk". Check all three.
*/
from.endsWith("rk"); //false
to.endsWith("rk");  //false
quote.endsWith("rk"); //true

/*
7. Does quote includes the word "Only"
*/
quote.includes("Only") // false

/*
8. Does quote includes the word " we"
*/
quote.includes(" we"); // true

/*
9. Find the index of the the word `we` in quote
*/
let indexOfWe = quote.indexOf("we");

/*
10. Split the quote into individual word and store it in a variable name quoteSplitted
*/
let quoteSplitted = quote.split(" ");
//["There", "is", "only", "one", "thing", "we", "say", "to", "death:", "Not", "today"]

/*
11. Change the word "today" in quoteSplitted to "tomorrow" and join all the words to form a sentance.
*/
quoteSplitted[quoteSplitted.length - 1] = "tomorrow";
quoteSplitted.join(" ");
//Output "There is only one thing we say to death: Not tomorrow"

/*
12. Find the index of second "o" in quote. Use indexOf
*/
let indexOfFirstO = quote.indexOf("o");
let indexOfSecondO = quote.indexOf("o",indexOfFirstO + 1) // 14

/*
13. Find the last index of letter "a" in quote.
*/
quote.lastIndexOf("a"); // 48


/*
14. Find the second last index of letter "a" in quote.
*/ //DOUBT
let lastIndexOfA = quote.lastIndexOf("a");
let secondLastIndexOfA = quote.lastIndexOf("a",lastIndexOfA)

/*
15. Make the quote 70 character long. If it has less characters add rest as .......
Example: "Hello" (convert to 10 characters) => "Hello....."
*/
quote.padEnd(70,".");
//"There is only one thing we say to death: Not today...................."

/*
16. Do same as (15) but the ... should come in start.
*/
quote.padStart(70,".");
// "....................There is only one thing we say to death: Not today"

/*
17. Log the repeat of "Hello World!" 10 times.
*/
"Hello World!".repeat(10);
//output: "Hello World!Hello World!Hello World!Hello World!Hello World!Hello World!Hello World!Hello World!Hello World!Hello World!"

/*
18. Replace today to tomorrow in quote.
*/
let replacedStr = quote.replace("today", "tomorrow");
//"There is only one thing we say to death: Not tomorrow"


/*
19. Replace Stark to Lannister in quoteTo
*/
let surname = to.replace("Stark","Lannister");

/*
20. Make the quote of length 30 and put ... at the end. (use slice)
*/
quote.slice(0,27).padEnd(30,".");
//"There is only one thing we ..."

/*
21. Find out does quote, quoteFrom, quoteTo starts with "A"
*/
quote.startsWith("A"); //false
quote.startsWith("A"); //false
quote.startsWith("A"); //true
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

- This method accepts 1 parameter ie separator. It is of string type and moreover it is optional parameter. If there is no separator, default separator is "," comma.
- It returns a string with all array elements joined. And if empty array invokes join then it returns an empty string.
- Example:
```js
  let naturalForces = ["water","fire","air"];
  naturalForces.join(); // "water,fire,air"

  naturalForces.join(" "); // "water fire air"

  naturalForces = ["fire"];
  naturalForces.join("*"); // "water"  separator has no role when only one element is there.
```
- join() thus allows array to string conversion wherein one string of all array elements is obtained. And if the array has only one element it will be returned without using the separator.

3. `flat`

- This method takes only one parameter ie Depth. It is of number type. Although this parameter is optional. By default depth is 1, that is recursively it will flatten the subarray until the depth, in this case only upto one level.
- It returns a new array with the sub array elements concatenated into it.
- Example:
```js
let numbers = [1,2,3,[4,5]];
numbers.flat(2); //[1, 2, 3, 4, 5]

numbers = [1,2,[3,4,[5,6]]];
numbers.flat(); // [1,2,3,4,[5,6]]

numbers.flat(infinity) // [1,2,3,4,5,6]

numbers = [1,2,3, ,4,5];
numbers.flat(); // [1,2,3,4,5]
```
- flat() creates a new array with all sub-elements concatenated into it recursively upto the specified depth.
- In case if an array contains a hole or empty slots, even they are removed.

4. `push`

- This method accepts one or more paramaters. Atleast one element is to be added and remaining being optional parameters. Parameters can be of any value type. If no parameter is passed it returns the current lenght of array or array-like object.
- It returns the new length property of the object upon which the method was called.
- Example : 
```js
const colors = ["yellow","red","green"];
colors.push("blue"); // returns 4

colors.push("white","black","tomatored"); // 7

colors.push();// 7 If no element
```
- push() appends values to an array. 

5. `indexOf`

- This method accepts two parameters. One is searchElement and other being fromIndex. searchElement is of string type and fromIndex is of number type.
- It returns the first index at which the given element is found, else -1 if it is not present.
- Example
```js
const colors = ["green","yellow","blue","red","yellow"];
colors.indexOf("yellow"); // 1

colors.indexOf("yellow",2); // 4

colors.indexOf("maroon"); //-1
```
- indexOf() method uses strict equality comparision to compare searchElement to the elements of the array.
- If negative value is taken as fromIndex it is taken as offset from the end of an array.

6. `lastIndexOf`

- This method accepts two parameters ie searchValue and fromIndex. fromIndex being optional. searchValue is of string type and fromIndex is of number type.
- It returns the index of last occurence of the searchValue else -1 if not found.
- Example :
```js
const animals = ["Lion", "Tiger", "rhino","rabbit","Tiger"];
animals.lastIndexOf("Tiger") // 4

animals.lastIndexOf("Dodo") // -1
```
- lastIndexOf() compares searchElement to elements of the array using strict equality. Based on that it returns the array index.

7. `includes`

- This method takes two parameters. One is valueToFind and other is fromIndex. valueToFind is of string type and fromIndex of the number type. fromIndex though is optional. 
- It returns true if valueToFind is within the array else returns false.
- Example :
```js
let colors = ["white","yellow", "blue"];
colors.includes("yellow"); // true

colors.includes("maroon"); // false

colors.includes("low") // false
```
- includes() determines whether an array includes a certain element or not.

8. `reverse`

- This method accepts no parameters.
- It returns a reversed array.
- Example :
```js
const arr = [1,2,3,4,5];
arr.reverse() // [5,4,3,2,1]

const colors = ["blue","yellow"];
colors.reverse() //["yellow","blue"]
```
- reverse() transposes the elements of the calling array object in place. It also mutates the array and returns the reference.

9. `every`

- This method accepts two parameters, one is the callback and other being the thisArg. callback is a function that is object type. Callback further receives 3 parameters that is the element, index and the whole array itself.
- It returns true of callback returns a truthy value for every array element, otherwise false.
- Example :
```js
let students = [
  {
    name: "raghuram",
    age: 26,
    location:"mumbai"
  },
  {
    name:"jayaram",
    age:24,
    location:"allapuzha"
  }
  ]
  let checkAgeAbove18 = function({age}){
    return age > 18 ? true : false;
  }

  let endsWithM = function({name}) {
    return name.endsWith("m"); 
  }

  let startsWithR = function({name}) {
    return name.startsWith("r"); 
  }
  students.every(checkAgeAbove18); // true

  students.every(endsWithM); // true

  students.every(startsWithR); // false
```
- every() for every element in the array executes the callback and based on whether a truthy or falsy value returned the boolean value is returned.

10. `shift`

- This method accepts no paramter.
- It removes the first element from an array and returns the removed element.
- Example :
```js
let colors = ["red", "yellow", "blue"];
colors.shift() // "red"
colors // ["yellow","blue"]

let numbers = [1,2,3,4,5];
numbers.shift() // 1

let someArr = [];
someArr.shift() // undefined for empty array
```
- shift() removes the element from the beginning of the array. It mutates the array.

11. `splice`

- It accepts 3 main parameters ie. start, deleteCount and item .... start and deleteCount are of number type and item can be of any value type. We can insert multiple items in the array.start parameter describes from where we need to start removing the element, deleteCount describes how many elements to be removed from the start. Both deleteCount and item are optional. If only start is mentioned in invocation then all the elements from the position start will be removed.
- It can return a array containing the deleted elements. OR if only one element is removed, an array of one element is removed. OR if no elements are removed an empty array is returned.
- Example :
```js
let months = ['Jan','Feb','Mar','Apr'];
//remove 'Feb'
months.splice(1,1)

//From position 1 remove 0 elements and insert "Feb"
months.splice(1,0,'Feb'); // returns [], but modifies the array by adding Feb in months // ["Jan", "Feb", "Mar", "Apr"]

months.splice(4,0,"May","Jun","Jul","Aug"); // returns []
// months is modified to ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug"]

months.splice(2); // returns ["Mar", "Apr", "May", "Jun", "Jul", "Aug"]
// months is modified to ["Jan","Feb"]
```
- splice() method mutates the array and changes the content of an array by either removing, replacing or/and adding new elements in the place.

12. `find`

- This method accepts two parameters ie callback and thisArg. callback is function and is a object type. thisArg is optional in nature.
- It returns the first element in the array that satisfies the provided testing function or otherwise undefined is returned.
- Example :
```js
let students = [
  {
    name: "raghuram",
    age: 26,
    location:"mumbai"
  },
  {
    name:"jayaram",
    age:24,
    location:"allapuzha"
  }
  ]

  let findStudWithAge24 = function({age}) {
    return age === 24;
  }

  let findStudWithLocation = function({location}) {
    return location === 'mumbai';
  }

  let findNothing = function({name}) {
    return name === "swaroop";
  }

  students.find(findStudWithAge24); // {name:"jayaram",age:24 location:"allapuzha"}

  students.find(findStudWithLocation); // {name:"raghuram",age:26,location: "mumbai"}

  students.find(findNothing); // undefined

```
- find() executes the callback for each index of the array until the callback returns a truthy value. If it finds truthy value it returns value of the element else undefined is returned.
- It does not mutate the array.

13. `unshift`

- This method can accept multiple parameters. Each of them can be of any value type.
- It returns the new length property of array like object on calling the method or when the element is inserted at the beginning of the array.
- Example :
```js
let colors = ["red","blue"];
colors.unshift("green","yellow"); // returns 2
// colors is modified to ["green", "yellow", "red", "blue"]

colors.unshift("pink",["maroon","gray"]) //returns 6
//colors is modified.
```
- unshift() inserts the given values at the beginning of the element.

14. `findIndex`
- This method accepts two parameters ie callback and thisArg. callback is an optional parameter. callback itself takes 3 parameters that is element, index and array.
- It returns the index of the the first element in the array that passes the test. otherwise -1
- Example :
```js
let arr1 = [5,6,7,8,9];
let findGreaterThan7 = function(num) {
  return num > 7;
}

let findLessThan5 = function(num) {
  return num < 5;
}

arr1.findIndex(findGreaterThan7) // 3 (returns index of 3)
arr1.findIndex(findLessThan5) // returns -1 as no element is less than 5
```
- findIndex() executes callback function for each of the index in the array and if truthy value is returned, it stops and returns the index of the corresponding element for which truthy value was executed.

15. `filter`
- This method accepts two parameters ie callback and thisArg, thisArg is optional type.
- It returns a new array with the elements that pass the tests. If no elements pass the test an empty array is returned.
- Example :
```js
let names = ["raghuram","kunal","akshat","sudhanshu","devika","manish","ashik","abhishek"];

let findNamesLengthGreaterThan7 = function(name) {
  return name.length > 7;
}

let namesAboveA = function(name) {
  return name[0] > "a"
}

names.filter(findNamesLengthGreaterThan7);
//["raghuram", "sudhanshu", "abhishek"]

names.filter(namesAboveA);
//["raghuram", "kunal", "sudhanshu", "devika", "manish"]

```
- filter() runs callback for each of index and for each of the index/element passing the test function(ie returns true), the element is placed in the new Array and returned as filtered array that satisfy the test function.


16. `flat`

- This method takes only one parameter ie Depth. It is of number type. Although this parameter is optional. By default depth is 1, that is recursively it will flatten the subarray until the depth, in this case only upto one level.
- It returns a new array with the sub array elements concatenated into it.
- Example:
```js
let numbers = [1,2,3,[4,5]];
numbers.flat(2); //[1, 2, 3, 4, 5]

numbers = [1,2,[3,4,[5,6]]];
numbers.flat(); // [1,2,3,4,[5,6]]

numbers.flat(infinity) // [1,2,3,4,5,6]

numbers = [1,2,3, ,4,5];
numbers.flat(); // [1,2,3,4,5]
```
- flat() creates a new array with all sub-elements concatenated into it recursively upto the specified depth.
- In case if an array contains a hole or empty slots, even they are removed.


17. `forEach`

- This method accepts two parameters ie callback and thisArg. thisArg being optional.
- It returns undefined.
- Example : 
```js
let colors = ["blue","yellow"];
let logColors = function(color) {
  console.log(color);
}
colors.forEach(logColors); // "blue"/n "yellow"
```
- forEach() executes a provided function once for each array element.

18. `map`

- This method accepts two parameters ie callback and thisArg. thisArg being optional.
- It returns a new array with each element being the result of the callback function. The length of the new array will be equal to that of original array.
- Example :
```js
let names = ["raghuram","kunal","akshat","sudhanshu","devika","manish","ashik","abhishek"];
let getLength = function(name) {
  return name.length;
}

let capitalise = function(name) {
  return name[0].toUpperCase() + name.slice(1)
}
let namesLength = names.map(getLength);
//nameslength will hold [8, 5, 6, 9, 6, 6, 5, 8]

let capitalised = names.map(capitalise);
// capitalised will hold ["Raghuram", "Kunal", "Akshat", "Sudhanshu", "Devika", "Manish", "Ashik", "Abhishek"]

```
- map() creates a new array populated with the results of calling a provided function on every element in the calling array.
- Should not be used when array is not required to be returned.

19. `pop`
- This method accepts no parameter.
- It returns the removed element from the array or undefined if the array is empty.
- Example : 
```js
let colors = ["yellow","green","blue"];
colors.pop() // returns "blue" and modifies the colors to ["yellow","green"];

let names = ["raghuram","jayaram"];
colors.pop(); // returns "jayaram"
```
- pop() removes the last element from an array and returns that value.
- It mutates the array.
- If pop is called on [](empty array) undefined is returned.

20. `reduce`

- This method accepts two parameters ie callback and initialValue. initialValue is an optional parameter and it can accept any value type. callback in reduce accepts 4 parameters of which accumulator and currentValue are must and index and array being the optional parameters.
- It returns a single value that results from the reduction.
- Example : 
```js
const numArray = [1,2,3,4,5];
let reducer = function(accumulator,currentValue) {
  return accumulator + currentValue;
}

let sum  = numArray.reduce(reducer,0);
// 0 is the initial value;
// sum is 15

// let colors = ["yellow", "red", "pink","yellow", "green","red"];
// let count = colors.reduce((accumulator,color) => {
//   if(color in accumulator){
//     accumulator[color] = ++accumulator[color];
//     return accumulator;
//   } else {
//     accumulator[color] = 0;
//     return accumulator;
//   }
  
// },{})
```
- reduce() method executes a reducer function (that you provide) on each element of the array, resulting in a single output value.

21. `slice`

- This method requires 0,1 or 2 parameters. The parameters are optional in nature. Two parameters are begin and end.
- It returns a shallow copy of a portion of an array into a new array object selected from begin to end.
- Example :
```js
const colors = ["yellow","green","white"];

colors.slice() // returns a shallow copy of array. ie ["yellow","green","white"]

colors.slice(1) // ["green","white"]

colors.slice(0,2) // ["yellow","green"]
```
- slice() returns a shallow copy of portion of an array into a new array selected from begin to end in which end is not included. 
- Original array is not modified.

22. `some`

- This method accepts two parameters ie. callback and thisArg. thisArg being optional.
- It returns true if the callback function returns a truthy value for atleast one element in the array otherwise false.
- Example
```js
let students = [
  {
    name: "raghuram",
    age: 26,
    location:"mumbai"
  },
  {
    name:"jayaram",
    age:24,
    location:"allapuzha"
  }
  ]
  let someAbove25 = function({age}) {
    return age > 25;
  }
  students.some(someAbove25); // true

  let someLiveinMumbai = function({location}) {
    return location === "mumbai"
  }

  student.some(someLiveinMumbai) // true
```
- some() tests whether atleast one element in the array passes the test implemented by a test function and it returns a boolean value.


## writeCode

Using above methods you practiced above, do the following.

```js
// Use the below two arrays and practice array methods
var numbers = [1, 12, 4, 18, 9, 7, 11, 3, 101, 5, 6, 9];
var strings = ["This", "is", "a", "collection", "of", "words"];

// - Find the index of `101` in numbers
let indexOf101 = numbers.indexOf(101);
console.log(indexOf101) ;// 8

// - Find the last index of `9` in numbers
let lastIndexOf9 = numbers.lastIndexOf(9);
console.log(lastIndexOf9) // 11


// - Convert value of strings array into a sentance like "This is a collection of words"
let sentance = strings.join(" ");
console.log(sentance) // "This is a collection of words"

// - Add two new words in the strings array "called" and "sentance"
strings.push("called","sentance");

// - Again convert the updated array (strings) into sentance like "This is a collection of words called sentance"
let updateSentance = strings.join(" ");
console.log(updateSentance);
//"This is a collection of words called sentance"

// - Remove the first word in the array (strings)
strings.shift(); // "This"
//strings would be ["is", "a", "collection", "of", "words", "called", "sentance"]

// - Find all the words that contain 'is' use string method 'includes'
let wordWithIs = function(word) {
  return word.includes("is")
}
let filterWordsWithIs = strings.filter(wordWithIs);
//["This", "is"]

// - Find all the words that contain 'is' use string method 'indexOf'
let index = 0;
let searchString = "is";
let words = [];
while(strings.indexOf(searchString,index) != -1) {
  if(strings[index].includes(searchString)){
    words.push(strings[index]);
  }
  index++;
}
console.log(words); //["This", "is"]

// - Check if all the numbers in numbers array are divisible by three use array method (every)
let checkDivisibility = function(number) {
  return number % 3 === 0;
}
numbers.every(checkDivisibility); //false

// -  Sort Array from smallest to largest
let sortedArray = numbers.sort((a,b) => a - b)
//[1, 3, 4, 5, 6, 7, 9, 9, 11, 12, 18, 101]

// - Remove the last word in strings
strings.pop() //returns last removed word "words"

// - Find largest number in numbers
let sortedArray = numbers.sort((a,b) => a - b)
console.log(sortedArray[sortedArray.length - 1])

// - Find longest string in strings
let largestString = strings.reduce((max,currString) => {
  if(currString.length > max.length){
    max = currString;
  }
  return max;
},"")

// largestSting is "collection"

// - Find all the even numbers
let isEven = function(number) {
  return number % 2 === 0;
}
let evenNumbers = numbers.filter(isEven);
console.log(evenNumbers); //[12, 4, 18, 6]s

// - Find all the odd numbers
let isOdd = function(number) {
  return number % 2;
}
let oddNumbers = numbers.filter(isOdd) ;
console.log(oddNumbers)
// [1, 9, 7, 11, 3, 101, 5, 9]


// - Place a new word at the start of the array use (upshift)
strings.unshift("new-word");

// - Make a subset of numbers array [18,9,7,11]
let numberSubset = numbers.slice(3,7);
console.log(numberSubset);

// - Make a subset of strings array ['a','collection']
let stringSubset = strings.slice(2,4);
console.log(stringSubset);

// - Replace 12 & 18 with 1221 and 1881
let replacer = function(number) {
  if(number === 12) return 1221;
  if(number === 18) return 1881;
  return number;
}
let replaceNumbers = numbers.map(replacer);
console.log(replaceNumbers);
//[1, 1221, 4, 1881, 9, 7, 11, 3, 101, 5, 6, 9]

// - Replace words in strings array with the length of the word
let strLengths = function(word) {
  return word.length;
}
let strLengthArr = strings.map(strLengths);
console.log(strLengthArr);//[4, 2, 1, 10, 2, 5]

// - Find the sum of the length of words using above question
let sumOfWordLength = strLengthArr.reduce((sum,curr)=>sum + curr,0);
console.log(sumOfWordLength); // 24

// - Customers Array
var customers = [
  { firstname: "Joe", lastname: "Blogs" },
  { firstname: "John", lastname: "Smith" },
  { firstname: "Dave", lastname: "Jones" },
  { firstname: "Jack", lastname: "White" }
];
// - Find all customers whose firstname starts with 'J'
let doesNameWithJ = function(customer) {
  return customer.firstname.startsWith("J")
}
let customerWithJ = customers.filter(doesNameWithJ);
console.log(customerWithJ);

// - Create new array with only first name
let getFirstName = function(customer) {
  return customer.firstname;
}
let firstNames = customers.map(getFirstName);
console.log(firstNames); //["Joe", "John", "Dave", "Jack"]

// - Create new array with all the full names (ex: "Joe Blogs")
let getFullName = function(customer) {
  return `${customer.firstname} ${customer.lastname}`;
}
let fullNames = customers.map(getFullName);
console.log(fullNames);
//["Joe Blogs", "John Smith", "Dave Jones", "Jack White"]

// - Sort the array created above alphabetically
let sortFullNames = fullNames.sort();
console.log(sortFullNames);
//["Dave Jones", "Jack White", "Joe Blogs", "John Smith"]

// - Create a new array that contains only user who has at least one vowel in the firstname.
let getUserWithVowel = function(customer) {
  let vowels = ["a","e","i","o","u"];
  return customer.firstname.split("").find(letter => vowels.includes(letter));
}
let customersWithVowels = customers.filter(getUserWithVowel);
console.log(customersWithVowels);
```
