## writeCode

```js
let words = [
  "mystery",
  "brother",
  "aviator",
  "crocodile",
  "pearl",
  "orchard",
  "crackpot",
  "rhythm"
];
// - Write a function findLongestWord that takes an array of words and returns the longest word from the array. (Use above array "words" to test it). If there are 2 with the same length, it should return the first occurrence.
function findLongestWord(words) {
  let longestWord = words.map(word => ({"word":word,"len":word.length})).reduce((max,curr)=> {
    if(curr.len > max.len  ) max = curr;
    return max;
  },{len:0})
  return longestWord.word;
}

console.log(findLongestWord(words))
//crocodile

// - Convert the above array "words" into an array of length of word instead of word.
let arrayLenOfWords = words.map(word => word.length);
console.log(arrayLenOfWords);
//[7, 7, 7, 9, 5, 7, 8, 6, 9]

// - Create a new array that only contains word with atleast one vowel.
let doesContainVowel = function(word){
  let vowels = ["a","e","i","o","u"];
  return word.split("").some(letter => vowels.includes(letter))
}

let arrOfWordsWithVowel = words.filter(doesContainVowel);
console.log(arrOfWordsWithVowel);
//["mystery", "brother", "aviator", "crocodile", "pearl", "orchard", "crackpot"]

// - Find the index of the word "rhythm"
let indexOfRhythm = words.indexOf("rhythm");
console.log(indexOfRhythm); //7

// - Create a new array that contians words not starting with vowel.
let checkVowelStart = function(word) {
  let vowels = ["a","e","i","o","u"];
  return vowels.includes(word[0]);
}

let vowelStart = words.filter(checkVowelStart);
console.log(vowelStart);
//["aviator", "orchard"]

// - Create a new array that contianse words not ending with vowel
let checkVowelNotStart = function(word) {
  let vowels = ["a","e","i","o","u"];
  return !vowels.includes(word[0]);
}
let vowelNotStart = words.filter(checkVowelNotStart);
console.log(vowelNotStart);
//["mystery", "brother", "crocodile", "pearl", "crackpot", "rhythm"]

let numbers = [6, 12, 1, 18, 13, 16, 2, 1, 8, 10];

// - Create a sumArray function that takes an array of number as a parameter, and calculate the sum of all its numbers
let sumArray = function(numbers) {
  let sum = numbers.reduce((sum,number) => sum + number,0);
  return sum;
}

console.log(sumArray(numbers)); //87


// - Make a new array that contains number multiplied by 3 like [6, 18, 27 ...]
let tripledArray = numbers.map(number => number * 3);
console.log(tripledArray);
//[18, 36, 3, 54, 39, 48, 6, 3, 24, 30]

// - Create a new array that contains only even numbers
let checkIsEven = function(number) {
  return number % 2 === 0;
}
let arrayOfEvens = numbers.filter(checkIsEven);
console.log(arrayOfEvens);
//[6, 12, 18, 16, 2, 8, 10]

// - Create  a new array that contains only odd numbers.
let checkIsOdd  = function(number) {
  return number % 2 !== 0;
}
let arrayOfOdd = numbers.filter(checkIsOdd);
console.log(arrayOfOdd);
//[1, 13, 1]

// - Create a new array that should have true for even number and false for odd numbers.
let arrOfBoolean = function(number){
  return number % 2 ? false : true
}
let arrOfTrueFalse = numbers.map(arrOfBoolean);
console.log(arrOfTrueFalse);
//[true, true, false, true, false, true, true, false, true, true]

// - Sort the above number in assending order.
let ascendingOrder = numbers.sort((a,b) => a - b);
console.log(ascendingOrder);
//[1, 1, 2, 6, 8, 10, 12, 13, 16, 18]

// - Does sort mutate the original array?
//Sort mutates the original array

// - Find the sum of the numbers in the array.
let sum = numbers.reduce((sum,number)=> sum + number, 0);
console.log(sum); //87

//- Write a function averageNumbers that receives an array of numbers and calculate the average of the numbers
let averageNumbers = function(numbers) {
  let sum = numbers.reduce((sum,number) => sum + number,0);
  return sum / numbers.length;
}
console.log(averageNumbers(numbers));
//8.7

let strings = [
  "seat",
  "correspond",
  "linen",
  "motif",
  "hole",
  "smell",
  "smart",
  "chaos",
  "fuel",
  "palace"
];
// - Write a function averageWordLength that receives an array of words2 and calculate the average length of the words.
let averageWordLength = function(words){
  let wordsLen = words.map(word => word.length);
  let sumOfWordsLen = wordsLen.reduce((sum,len)=> sum + len,0);
  let average = sumOfWordsLen / wordsLen.length;
  return average;
}

console.log(averageWordLength(strings)); // 5.3
```

## String Methods-writeCode

- Write a JavaScript function to check whether input value is a string or not.

```js
/* Requirements
  @name isString
  @parameter (any value) val
  @return Boolean
*/

// your code goes here
let isString = function(val) {
  return typeof val === "string";
}

// Test
console.log(isString("tony stark")); // true;
console.log(isString([1, 2, 4, 0])); // false;
```

- Write a JavaScript function to check whether a string is blank or not.

```js
/* Requirements
  @name isBlank
  @parameter (any value) val
  @return Boolean
*/

// your code goes here
let isBlank = function(val) {
  return !val.length;
}

// Test
console.log(isBlank("")); // true;
console.log(isBlank("abc")); // false;
```

- Write a JavaScript function to split a string and convert it into an array of words.

```js
/* Requirements
  @name stringToArray
  @parameter (string) text
  @return Array
*/
// your code goes here
let stringToArray = function(text) {
  let array = text.split(" ");
  return array;
}

// Test
console.log(stringToArray("Hello World")); // ["Robin", "Singh"];
console.log(stringToArray("Lady Bird")); // ["Lady", "Bird"];
```

- Write a JavaScript function to return specified number of characters from a string.

```js
/* Requirements
  @name truncate
  @parameter (string, number) text, len
  @return String
*/
// your code goes here
let truncate = function (text, len) {
  return text.substring(0,len)
};

// Test
console.log(truncate("Robin Singh", 4)); //"Robi";
```

- Write a JavaScript function to convert a `string` in abbreviated form.

```js
/* Requirements
  @name abbrevName
  @parameter (string) fullName
  @return String
*/
// your code goes here
let abbrevName = function(fullName) {
  let splitFullname = fullName.split(" ");
  return splitFullname[0] + " " + splitFullname[1][0] + ".";
}

// Test
console.log(abbrevName("Robin Singh")); //"Robin S."
```

- Write a JavaScript function to hide email addresses to protect from unauthorized user.

```js
/* Requirements
  @name protect
  @parameter (string) email
  @return String
*/
// your code goes here
let protect = function(email) {
  let indexOfUnderscore = email.indexOf("_");
  let indexOfAtrate = email.indexOf("@");
  return email.slice(0,indexOfUnderscore) + "..." + email.slice(indexOfAtrate);
}

// Test
console.log(protect("robin_singh@example.com")); // "robin...@example.com"
```

- Write a JavaScript function to parameterize a string.

```js
/* Requirements
  @name parameterize
  @parameter (string) str
  @return String
*/
// your code goes here
let parameterize = function(str) {
  let arrOfStr = str.split(" ").map(word => word.toLowerCase());
  return arrOfStr.join("-");
}

// Test
console.log(parameterize("Robin Singh from USA.")); // "robin-singh-from-usa"
```

- Write a JavaScript function to capitalize the first letter of a `string`.

```js
/* Requirements
@name capitalizeFirst
@parameter (string, number) text, len
@return String
*/
// your code goes here
let capitalizeFirst = function(text,len) {
  return text[0].toUpperCase() + text.slice(1);
}
// Test
console.log(capitalizeFirst("js string exercises")); // "Js string exercises"
```

- Write a JavaScript function to capitalize the first letter of each word in a string.

```js
/* Requirements
  @name capitalizeWords
  @parameter (string) text
  @return String
*/
// your code goes here
let capitalizeWords = function(text) {
  let splitText = text.split(" ")
  let arrOfCapitalWords = splitText.map(text => text[0].toUpperCase() + text.slice(1));
  return arrOfCapitalWords.join(" ");
}
console.log(capitalizeWords("js string exercises")); // "Js String Exercises"
```

- Write a function that takes a string which has lower and upper case letters as a parameter and converts upper case letters to lower case, and lower case letters to upper case.

```js
/* Requirements
  @name swapcase
  @parameter (string) text
  @return String
*/
// your code goes here
function checkUnicode(letter) {
  let letterCode = letter.charCodeAt();
  if (letterCode < 97) {
    letterCode += 32;
  } else {
    letterCode -= 32;
  }
  let modifiedLetter = String.fromCharCode(letterCode);
  return modifiedLetter;
}

let swapcase = function (text) {
  let splitText = text.split("");
  let swapText = splitText.map(checkUnicode);
  return swapText.join("");
};

// Tets
console.log(swapcase("AaBbc")); // "aAbBC"
```

- Write a function to convert a string into camel case.

Example:

```js
/* Requirements
  @name camelize
  @parameter (string) text
  @return String
*/
// your code goes here
let checkChar = function(word,index) {
  let charCode =  word[0].charCodeAt()
  let firstChar;
  if(!index) {
    firstChar = charCode < 97 ? charCode + 32 : charCode;
  } else {
    firstChar = charCode > 97 ? charCode - 32 : charCode;
  }
   return String.fromCharCode(firstChar) + word.slice(1);
}
function camelize(text) {
  let splitText = text.split(" ");
  let formattedWords = splitText.map(checkChar);
  let camelizedText = formattedWords.join("");
  return camelizedText;
}

// Test
console.log(camelize("JavaScript Exercises")); // "JavaScriptExercises"
console.log(camelize("JavaScript exercises")); // "JavaScriptExercises"
console.log(camelize("JavaScriptExercises")); // "JavaScriptExercises"
```

- Write a function to uncamelize a string. Example:

```js
/* Requirements
  @name uncamelize
  @parameter (string, string) text, joinStr
  @return String
*/
// your code goes here
let getPositions = function(splittedArr,getPositionOfCapitals) {
  splittedArr.filter(function(letter,index){
    if(letter.charCodeAt() < 97) {
      getPositionOfCapitals.push(index);
    }
  })
  return getPositionOfCapitals;
}

let uncamelize = function(text,joinStr) {
  let textSplit = text.split("");
  let getPositionOfCapitals = getPositions(textSplit,[]);
  getPositionOfCapitals.unshift(0);
  let words = []
  for(let i = 0; i < getPositionOfCapitals.length; i++) {
    if(i !== getPositionOfCapitals.length) {
       words.push(text.slice(getPositionOfCapitals[i],getPositionOfCapitals[i+1]));
    }
  }

  let wordsLowercased = words.map(word => word.toLowerCase());

  return wordsLowercased.join(joinStr);
}

// Tets
console.log(uncamelize("helloWorld", "_")); // "hello_world"
```

- Write a function to concatenates a given string n times (default is 1).

```js
/* Requirements
  @name repeat
  @parameter (string, number) text, times
  @return String
*/
// your code goes here
let repeat = function(text,times) {
  return text.repeat(times);
}

// Test
console.log(repeat("Ha!", 3)); // "Ha!Ha!Ha!"
```

- Write a function to insert a string within a string at a particular position (default is 1).

```js
/* Requirements
  @name insert
  @parameter (string, number) text, position
  @return String
*/
// your code goes here
let insert = function(text,insertStr,position) {
  return text.slice(0,position) + insertStr + text.slice(position);
}

// Test
console.log(insert("We are doing some exercises.", "JavaScript ", 18)); // "We are doing some JavaScript exercises."
```

- Write a JavaScript function to humanized number (Formats a number to a human-readable string.) with the correct suffix such as 1st, 2nd, 3rd or 4th.

```js
/* Requirements
  @name humanize
  @parameter ( number) num
  @return String
*/
// your code goes here
let humanize = function(num) {
  let humanWords = ["th","st","nd","rd","th","th","th","th","th","th"];
  let getLastPosDigit = +`${num}`[`${num}`.length - 1];
  return `${num}${humanWords[getLastPosDigit]}`;
}


// Test
console.log(humanize(301)); // "301st"
console.log(humanize(402)); // "402nd"
```

###

Write a function to truncates a string if it is longer than the specified number of characters. Truncated strings will end with a translatable ellipsis sequence ("…") (by default) or specified characters.

```js
/* Requirements
  @name testTruncate
  @parameter (string, number, string) text, len, postfix
  @return String
*/
// your code goes here
let textTruncate = function(text,len,postfix="...") {
  let textLen = len - postfix.length;
  let textContent = text.slice(0,textLen);
  let truncatedText = textContent.padEnd(len,postfix);
  return truncatedText;
}

// Test
console.log(textTruncate("We are doing JS string exercises.", 15, "!!")); //"We are doing !!"
```

- Write a JavaScript function to chop a string into chunks of a given length.

```js
/* Requirements
  @name chop
  @parameter (string, number) text, size
  @return String
*/
// your code goes here
let stringChop = function(text,size) {
  let chops = [];
  for(let i = 0; i < text.length / size; i++) {
    chops.push(text.slice(size * i, size * i + size))
  }
  return chops;
}

// Test
console.log(stringChop("hello world", 2)); // ["he", "ll", "o ", "wo", "rl", "d"]
```

- Write a function to count the occurrence of a substring in a string.

```js
/* Requirements
  @name count
  @parameter (string, string) text, char
  @return Number
*/
// your code goes here
let count = function(text,char) {
  let splittedText = text.split(" ");
  let count = 0;
  for(let i = 0; i < splittedText.length ;i++){
    if(splittedText[i].toLowerCase() === char.toLowerCase()){
      count++;
    }
  }
  return count;
}

// Test
console.log(count("The quick brown fox jumps over the lazy dog", "the")); // 2
```

- Write a function to strip leading and trailing spaces from a string.

```js
/* Requirements
  @name strip
  @parameter (string) text
  @return String
*/

//Your code here
let strip = function(text) {
  return text.trim();
}

// Test
console.log(strip("   Hello World ")); // "Hello World"
```

- Write a JavaScript function to truncate a string to a certain number of words.

```js
/* Requirements
  @name chopWords
  @parameter (string, number) text, words
  @return String
*/

//Your code here
let chopWords = function(text,words) {
  let splittedTextArr = text.split(" ");
  splittedTextArr.splice(words);
  return splittedTextArr.join(" ");
}

// Test
console.log(chopWords("The quick brown fox jumps over the lazy dog", 4)); // "The quick brown fox"
```

- Write a function to alphabetize a given string.(A - z)

```js
/* Requirements
  @name alphabetize
  @parameter (string, number) text, times
  @return String
*/

//Your Code Here
let alphabetize = function(text,times) {
  return text.split("").sort().join("").trim();
}

// Test
console.log(alphabetize("United States")); // 'SUadeeinsttt'
```
