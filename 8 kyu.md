# 8 kyu - JavaScript

## [A Needle in the Haystack](https://www.codewars.com/kata/56676e8fabd2d1ff3000000c)

Can you find the needle in the haystack?

Write a function findNeedle() that takes an array full of junk but containing one "needle".

After your function finds the needle it should return a message (as a string) that says:

"found the needle at position " plus the index it found the needle, so:

Example(Input --> Output): ["hay", "junk", "hay", "hay", "moreJunk", "needle", "randomJunk"] --> "found the needle at position 5" 

```
function findNeedle(haystack) {
  return `found the needle at position ${haystack.indexOf('needle')}`;
}
```

## [Add Length](https://www.codewars.com/kata/559d2284b5bb6799e9000047)

What if we need the length of the words separated by a space to be added at the end of that same word and have it returned as an array?

Example(Input --> Output)
- "apple ban" --> ["apple 5", "ban 3"]
- "you will win" -->["you 3", "will 4", "win 3"]

Your task is to write a function that takes a String and returns an Array/list with the length of each word added to each element .

Note: String will have at least one element; words will always be separated by a space.

```
function addLength(str){
  return str.split(" ").map(x => `${x} ${x.length}`);
}
```

## [Array plus array](https://www.codewars.com/kata/5a2be17aee1aaefe2a000151)

I'm new to coding and now I want to get the sum of two arrays... Actually the sum of all their elements. I'll appreciate for your help.

P.S. Each array includes only integer numbers. Output is a number too.

```
function arrayPlusArray(arr1, arr2) {
  return arr1.concat(arr2).reduce((a, c) => a + c);
}
```

## [Beginner - Lost Without a Map](https://www.codewars.com/kata/57f781872e3d8ca2a000007e)

Given an array of integers, return a new array with each value doubled.

For example: [1, 2, 3] --> [2, 4, 6]

```
function maps(x){
  return x.map(n => n * 2);
}
```

## [Beginner - Reduce but Grow](https://www.codewars.com/kata/57f780909f7e8e3183000078)

Given a non-empty array of integers, return the result of multiplying the values together in order. 

Example:
[1, 2, 3, 4] => 1 * 2 * 3 * 4 = 24

```
function grow(x){
  return x.reduce((a, b)=> a * b, 1);
}
```

## [Calculate average](https://www.codewars.com/kata/57a2013acf1fa5bfc4000921)

Write a function which calculates the average of the numbers in a given list.

Note: Empty arrays should return 0.

```
function find_average(array) {
  return array.length ? array.reduce((a, c)=> a + c, 0) / array.length : 0
}
```

## [Convert a Boolean to a String](https://www.codewars.com/kata/551b4501ac0447318f0009cd)

Implement a function which convert the given boolean value into its string representation.

Note: Only valid inputs will be given.

```
function booleanToString(b){
  return b.toString();
}
```

## [Convert a Number to a String!](https://www.codewars.com/kata/5265326f5fda8eb1160004c8)

We need a function that can transform a number (integer) into a string.

What ways of achieving this do you know?

Examples (input --> output):
- 123  --> "123"
- 999  --> "999"
- -100 --> "-100"

```
function numberToString(num) {
  return num.toString();
}
```

## [Convert a string to an array](https://www.codewars.com/kata/57e76bc428d6fbc2d500036d)

Write a function to split a string and convert it into an array of words.

Examples (Input ==> Output):
- "Robin Singh" ==> ["Robin", "Singh"]
- "I love arrays they are my favorite" ==> ["I", "love", "arrays", "they", "are", "my", "favorite"]

```
function stringToArray(string){
  return string.split(' ');
}
```

## [Convert boolean values to strings 'Yes' or 'No'.](https://www.codewars.com/kata/53369039d7ab3ac506000467)

Complete the method that takes a boolean value and return a "Yes" string for true, or a "No" string for false.

```
function boolToWord(bool){
  return bool ? 'Yes':'No';
}
```

## [Convert number to reversed array of digits](https://www.codewars.com/kata/5583090cbe83f4fd8c000051)

Convert number to reversed array of digits.

Given a random non-negative number, you have to return the digits of this number within an array in reverse order.

Example(Input => Output):
- 35231 => [1,3,2,5,3]
- 0 => [0]

```
function digitize(n){
  return String(n).split('').map(Number).reverse()
}
```

## [Count by X](https://www.codewars.com/kata/5513795bd3fafb56c200049e)

Create a function with two arguments that will return an array of the first n multiples of x.

Assume both the given number and the number of times to count will be positive numbers greater than 0.

Return the results as an array or list ( depending on language ).

Examples:
- countBy(1,10) === [1,2,3,4,5,6,7,8,9,10]
- countBy(2,5) === [2,4,6,8,10]

```
function countBy(x, n) {
  var z = [];
  for (i = 1; i <= n; i++) {
    z.push(x * i);
  }
  return z;
}
```

## [Count of positives/sum of negatives](https://www.codewars.com/kata/576bb71bbbcf0951d5000044)

Given an array of integers.

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers. 0 is neither positive nor negative.

If the input is an empty array or is null, return an empty array.

Example: For input [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15], you should return [10, -65].

```
function countPositivesSumNegatives(input) {
  if (input == null || input.length == 0) {
    return [];
  }else {
    let positive = input.filter(x => x > 0);
    let negative = input.filter(x => x < 0);
    return [positive.length, negative.reduce((a, c) => a + c, 0)];
  }
}
```

## [Count the Monkeys!](https://www.codewars.com/kata/56f69d9f9400f508fb000ba7)

You take your son to the forest to see the monkeys. You know that there are a certain number there (n), but your son is too young to just appreciate the full number, he has to start counting them from 1.

As a good parent, you will sit and count with him. Given the number (n), populate an array with all numbers up to and including that number, but excluding zero.

For example(Input --> Output):
- 10 --> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
- 1 --> [1]
 
 ```
 function monkeyCount(n) {
   let monkeys = [];
   for (let i = 1; i < n+1; i++) {
     monkeys.push(i);
   }
   return monkeys;
}
 ```

## [Counting Sheep...](https://www.codewars.com/kata/54edbc7200b811e956000556)

Consider an array/list of sheep where some sheep may be missing from their place. We need a function that counts the number of sheep present in the array (true means present).

For example:

[true,  true,  true,  false,
  true,  true,  true,  true ,
  true,  false, true,  false,
  true,  false, false, true ,
  true,  true,  true,  true ,
  false, false, true,  true]

The correct answer would be 17.

Hint: Don't forget to check for bad values like null/undefined

```
function countSheeps(arrayOfSheeps) {
  return arrayOfSheeps.filter(Boolean).length;
}
```

## [CSV representation of array](https://www.codewars.com/kata/5a34af40e1ce0eb1f5000036)

Create a function that returns the CSV representation of a two-dimensional numeric array.

Example:

input:
   [[ 0, 1, 2, 3, 4 ],
    [ 10,11,12,13,14 ],
    [ 20,21,22,23,24 ],
    [ 30,31,32,33,34 ]] 
    
output:
     '0,1,2,3,4\n'
    +'10,11,12,13,14\n'
    +'20,21,22,23,24\n'
    +'30,31,32,33,34'

Array's length > 2.

```
function toCsvText(array) {
   return array.join('\n');
}
```

## [Even or Odd](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe)

Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.

```
function even_or_odd(number) {
  return number % 2 ? "Odd" : "Even";
}
```

## [Fake Binary](https://www.codewars.com/kata/57eae65a4321032ce000002d)

Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

Note: input will never be an empty string

```
function fakeBin(x) {
  return x.split('').map(n => n < 5 ? 0 : 1).join('');
}
```

## [Filter out the geese](https://www.codewars.com/kata/57ee4a67108d3fd9eb0000e7)

Write a function that takes a list of strings as an argument and returns a filtered list containing the same elements but with the 'geese' removed.

The geese are any strings in the following array, which is pre-populated in your solution: ["African", "Roman Tufted", "Toulouse", "Pilgrim", "Steinbacher"]

For example, if this array were passed as an argument: ["Mallard", "Hook Bill", "African", "Crested", "Pilgrim", "Toulouse", "Blue Swedish"]

Your function would return the following array: ["Mallard", "Hook Bill", "Crested", "Blue Swedish"]

The elements in the returned array should be in the same order as in the initial array passed to your function, albeit with the 'geese' removed. Note that all of the strings will be in the same case as those provided, and some elements may be repeated.

```
function gooseFilter (birds) {
  var geese = ["African", "Roman Tufted", "Toulouse", "Pilgrim", "Steinbacher"];
  return birds.filter(goose => !geese.includes(goose));
}
```

## [Find Multiples of a Number](https://www.codewars.com/kata/58ca658cc0d6401f2700045f)

In this simple exercise, you will build a program that takes a value, integer , and returns a list of its multiples up to another value, limit . If limit is a multiple of integer, it should be included as well. There will only ever be positive integers passed into the function, not consisting of 0. The limit will always be higher than the base.

For example, if the parameters passed are (2, 6), the function should return [2, 4, 6] as 2, 4, and 6 are the multiples of 2 up to 6.

```
function findMultiples(integer, limit) {
  let multiples = [];
  for (let i = integer; i <= limit; i = i+integer){
    multiples.push(i);
  }
  return multiples;
}
```

## [Find the first non-consecutive number](https://www.codewars.com/kata/58f8a3a27a5c28d92e000144)

Your task is to find the first element of an array that is not consecutive.

By not consecutive we mean not exactly 1 larger than the previous element of the array.

E.g. If we have an array [1,2,3,4,6,7,8] then 1 then 2 then 3 then 4 are all consecutive but 6 is not, so that's the first non-consecutive number.

If the whole array is consecutive then return null.

The array will always have at least 2 elements and all elements will be numbers. The numbers will also all be unique and in ascending order. The numbers could be positive or negative and the first non-consecutive could be either too!

```
function firstNonConsecutive(arr) {
  for (let i = 0; i < arr.length - 1; ++i) {
    if (arr[i] + 1 !== arr[i + 1]) {
      return arr[i + 1]
    }
  }
  return null
}
```

## [Find the smallest integer in the array](https://www.codewars.com/kata/55a2d7ebe362935a210000b2)

Given an array of integers your solution should find the smallest integer.

For example:
- Given [34, 15, 88, 2] your solution will return 2
- Given [34, -345, -1, 100] your solution will return -345

You can assume, for the purpose of this kata, that the supplied array will not be empty.

```
class SmallestIntegerFinder {
  findSmallestInt(args) {
    return args.sort((a, b) => a - b)[0];
  }
}
```

## [Get the mean of an array](https://www.codewars.com/kata/563e320cee5dddcf77000158)

It's the academic year's end, fateful moment of your school report. The averages must be calculated. All the students come to you and entreat you to calculate their average for them. Easy ! You just need to write a script.

Return the average of the given array rounded down to its nearest integer.

The array will never be empty.

```
function getAverage(marks){
  return Math.floor(marks.reduce((a, c) => a + c) / marks.length);
}
```

## [Gravity Flip](codewars.com/kata/5f70c883e10f9e0001c89673)

Bob is bored during his physics lessons so he's built himself a toy box to help pass the time. The box is special because it has the ability to change gravity.

There are some columns of toy cubes in the box arranged in a line. The i-th column contains a_i cubes. At first, the gravity in the box is pulling the cubes downwards. When Bob switches the gravity, it begins to pull all the cubes to a certain side of the box, d, which can be either 'L' or 'R' (left or right).

Given the initial configuration of the cubes in the box, find out how many cubes are in each of the n columns after Bob switches the gravity.

Examples (input -> output:
- 'R', [3, 2, 1, 2]      ->  [1, 2, 2, 3]
- 'L', [1, 4, 5, 3, 5 ]  ->  [5, 5, 4, 3, 1]

```
const flip = (d, a) => d === "R" ? a.sort((a, b) => a - b) : a.sort((a, b) => b - a)
```

## [I love you, a little, a lot, passionately...not at all](https://www.codewars.com/kata/57f24e6a18e9fad8eb000296)

Who remembers back to their time in the schoolyard, when girls would take a flower and tear its petals, saying each of the following phrases each time a petal was torn:

1. "I love you"
2. "a little"
3. "a lot"
4. "passionately"
5. "madly"
6. "not at all"

If there are more than 6 petals, you start over with "I love you" for 7 petals, "a little" for 8 petals and so on.

When the last petal was torn there were cries of excitement, dreams, surging thoughts and emotions.

Your goal in this kata is to determine which phrase the girls would say at the last petal for a flower of a given number of petals. The number of petals is always greater than 0.

```
let phrases = [
  'I love you',
  'a little',
  'a lot',
  'passionately',
  'madly',
  'not at all',
]

function howMuchILoveYou(nbPetals) {
  return phrases[(nbPetals - 1) % phrases.length];
}
```

## [Invert Values](https://www.codewars.com/kata/5899dc03bc95b1bf1b0000ad)

Given a set of numbers, return the additive inverse of each. Each positive becomes negatives, and the negatives become positives.

Examples:
- invert([1,2,3,4,5]) == [-1,-2,-3,-4,-5]
- invert([1,-2,3,-4,5]) == [-1,2,-3,4,-5]
- invert([]) == []

You can assume that all values are integers. Do not mutate the input array/list.

```
function invert(array) {
  return array.map(x => -x);
}
```

## [Is there a vowel in there?](https://www.codewars.com/kata/57cff961eca260b71900008f)

Given an array of numbers, check if any of the numbers are the character codes for lower case vowels (a, e, i, o, u).

If they are, change the array value to a string of that vowel.

Return the resulting array.

```
function isVow(a){
  return a.map(x => /[aeiou]/.test(String.fromCharCode(x)) ? String.fromCharCode(x) : x);
}
```

## [MakeUpperCase](https://www.codewars.com/kata/57a0556c7cb1f31ab3000ad7)

Write a function which converts the input string to uppercase.

```
function makeUpperCase(str) {
  return str.toUpperCase();
}
```

## [Multiply](https://www.codewars.com/kata/50654ddff44f800200000004)

This code does not execute properly. Try to figure out why.

```
multiply = function (a, b) {
  return a * b;
}
```

## [My head is at the wrong end!](https://www.codewars.com/kata/56f699cd9400f5b7d8000b55)

You're at the zoo... all the meerkats look weird. Something has gone terribly wrong - someone has gone and switched their heads and tails around!

Save the animals by switching them back. You will be given an array which will have three values (tail, body, head). It is your job to re-arrange the array so that the animal is the right way round (head, body, tail).

Same goes for all the other arrays/lists that you will get in the tests: you have to change the element positions with the same exact logics

Simples!

```
function fixTheMeerkat(arr) {
  return arr.reverse();
}
```

## [N-th Power](https://www.codewars.com/kata/57d814e4950d8489720008db)

You are given an array with positive numbers and a non-negative number N. You should find the N-th power of the element in the array with the index N. If N is outside of the array, then return -1. Don't forget that the first element has the index 0.

Let's look at a few examples:
- array = [1, 2, 3, 4] and N = 2, then the result is 3^2 == 9
- array = [1, 2, 3] and N = 3, but N is outside of the array, so the result is -1

```
function index(array, n){
  return array.length > n ? Math.pow(array[n], n) : -1;
}
```

## [Opposite number](https://www.codewars.com/kata/56dec885c54a926dcd001095)

Very simple, given an integer or a floating-point number, find its opposite.

Examples:
- 1: -1
- 14: -14
- -34: 34

```
function opposite(number) {
  return(-number);
}
```

## [Price of Mangoes](https://www.codewars.com/kata/57a77726bb9944d000000b06)

There's a "3 for 2" (or "2+1" if you like) offer on mangoes. For a given quantity and price (per mango), calculate the total cost of the mangoes.

Examples
- mango(2, 3) ==> 6    (# 2 mangoes for $3 per unit = $6; no mango for free)
- mango(3, 3) ==> 6    (# 2 mangoes for $3 per unit = $6; +1 mango for free)
- mango(5, 3) ==> 12   (# 4 mangoes for $3 per unit = $12; +1 mango for free)
- mango(9, 5) ==> 30   (# 6 mangoes for $5 per unit = $30; +3 mangoes for free)

```
function mango(quantity, price){
  return price * (quantity - Math.floor(quantity / 3));
}
```

## [Remove First and Last Character](https://www.codewars.com/kata/56bc28ad5bdaeb48760009b0)

It's pretty straightforward. Your goal is to create a function that removes the first and last characters of a string. You're given one parameter, the original string. You don't have to worry with strings with less than two characters.

```
function removeChar(str) {
  return str.slice(1, -1);
}
```

## [Removing Elements](https://www.codewars.com/kata/5769b3802ae6f8e4890009d2)

Take an array and remove every second element from the array. Always keep the first element and start removing with the next element.

Example: ["Keep", "Remove", "Keep", "Remove", "Keep", ...] --> ["Keep", "Keep", "Keep", ...]

None of the arrays will be empty, so you don't have to worry about that!

```
function removeEveryOther(arr){
  return arr.filter((elem, index) => index % 2 === 0);
}
```

## [Return Negative](https://www.codewars.com/kata/55685cd7ad70877c23000102)

In this simple assignment you are given a number and have to make it negative. But maybe the number is already negative?

Examples
- makeNegative(1);    // return -1
- makeNegative(-5);   // return -5
- makeNegative(0);    // return 0
- makeNegative(0.12); // return -0.12

Notes
- The number can be negative already, in which case no change is required.
- Zero (0) is not checked for any specific sign. Negative zeros make no mathematical sense.

```
function makeNegative(num) {
  return -Math.abs(num);
}
```

## [Reversed Strings](https://www.codewars.com/kata/5168bb5dfe9a00b126000018)

Complete the solution so that it reverses the string passed into it.

- 'world'  =>  'dlrow'
- 'word'   =>  'drow'

```
function solution(str){
  return str.split('').reverse().join('');  
}
```

## [Sentance Smash](https://www.codewars.com/kata/53dc23c68a0c93699800041d)

Write a function that takes an array of words and smashes them together into a sentence and returns the sentence. You can ignore any need to sanitize words or add punctuation, but you should add spaces between each word. Be careful, there shouldn't be a space at the beginning or the end of the sentence!

Example: ['hello', 'world', 'this', 'is', 'great']  =>  'hello world this is great'

```
function smash(words){
  return words.join(" ");
}
```

## [Square(n) Sum](https://www.codewars.com/kata/515e271a311df0350d00000f)

Complete the square sum function so that it squares each number passed into it and then sums the results together.

For example, for [1, 2, 2] it should return 9 because 1<sup>2</sup> + 2<sup>2</sup> + 2<sup>2</sup> = 9.

```
function squareSum(numbers){
  return numbers.reduce((a, c) => a + (c ** 2), 0);
}
```

## [String Repeat](https://www.codewars.com/kata/57a0e5c372292dd76d000d7e)

Write a function that accepts an integer n and a string s as parameters, and returns a string of s repeated exactly n times.

Examples (input -> output)
-6, "I"     -> "IIIIII"
-5, "Hello" -> "HelloHelloHelloHelloHello"

```
function repeatStr(n, s) {
  return s.repeat(n);
}
```

## [Sum Arrays](https://www.codewars.com/kata/53dc54212259ed3d4f00071c)

Write a function that takes an array of numbers and returns the sum of the numbers. The numbers can be negative or non-integer. If the array does not contain any numbers then you should return 0.

Examples
- Input: [1, 5.2, 4, 0, -1] // Output: 9.2
- Input: [] // Output: 0
- Input: [-2.398] // Output: -2.398

Assumptions
- You can assume that you are only given numbers.
- You cannot assume the size of the array.
- You can assume that you do get an array and if the array is empty, return 0.

```
function sum(numbers) {
  return numbers.reduce((a, c) => a + c, 0);
}
```

## [Sum Mixed Array](https://www.codewars.com/kata/57eaeb9578748ff92a000009)

Given an array of integers as strings and numbers, return the sum of the array values as if all were numbers.

Return your answer as a number.

```
function sumMix(x){
  return x.reduce((a, c) => Number(a) + Number(c), 0);
}
```

## [Sum of positive](https://www.codewars.com/kata/5715eaedb436cf5606000381)

You get an array of numbers, return the sum of all of the positives ones.

Example [1,-4,7,12] => 1 + 7 + 12 = 20

Note: if there is nothing to sum, the sum is default to 0.

```
function positiveSum(arr) {
   return arr.reduce((a, c) => a + (c > 0 ? c : 0), 0);
}
```

## [Total amount of points](https://www.codewars.com/kata/5bb904724c47249b10000131)

Our football team has finished the championship.

Our team's match results are recorded in a collection of strings. Each match is represented by a string in the format "x:y", where x is our team's score and y is our opponents score.

For example: ["3:1", "2:2", "0:1", ...]

Points are awarded for each match as follows:
- if x > y: 3 points (win)
- if x < y: 0 points (loss)
- if x = y: 1 point (tie)

We need to write a function that takes this collection and returns the number of points our team (x) got in the championship by the rules given above.

Notes:
- our team always plays 10 matches in the championship
- 0 <= x <= 4
- 0 <= y <= 4

```
function points(games) {
  return games.reduce((a,c) => a + (c[0] > c[2] ? 3 : c[0] === c[2] ? 1 : 0), 0 )
}
```

## [Training JS #1: create your first JS function and print "Hello World!"](https://www.codewars.com/kata/571ec274b1c8d4a61c0000c8)

...write your first JS function.

- mission 1: use keyword function to define your function, function name should be helloWorld(don't forget the () and {})
- mission 2: use keyword var (or let or const) to define a variable str, value of str should be a string: "Hello World!"(don't forget the =).
- mission 3: type the console.log() in the next line (don't forget to put the str in the parentheses).

```
function helloWorld() {
  let str = 'Hello World!';
  console.log(str);
}
```

## [Training JS #2: Basic data types--Number](https://www.codewars.com/kata/571edd157e8954bab500032d)

I've written five function equal1,equal2,equal3,equal4,equal5, defines six global variables v1 v2 v3 v4 v5 v6, every function has two local variables a,b, please set the appropriate value for the two variables(select from v1--v6), making these function return value equal to 100. the function equal1 is completed, please refer to this example to complete the following functions.

```
let v1 = 50,
    v2 = 100,
    v3 = 150,
    v4 = 200,
    v5 = 2,
    v6 = 250;

function equal1(){
  let a = v1,   
      b = v1;   
  return a + b;
}

//Please refer to the example above to complete the following functions
function equal2(){
  let a = v3, //set number value to a
      b = v1; //set number value to b
  return a - b;
}

function equal3(){
  let a = v1, //set number value to a
      b = v5; //set number value to b
  return a * b;
}

function equal4(){
  let a = v4, //set number value to a
      b = v5; //set number value to b
  return a / b;
}

function equal5(){
  let a =  v6, //set number value to a
      b =  v3; //set number value to b
  return a % b;
}
```

## [Training JS #3: Basic data types--String](https://www.codewars.com/kata/571edea4b625edcb51000d8e)

misson 1: I've create three function, and defined some global variables, please select some variables that can make up the name of the function, and return them(Please note the uppercase and lowercase letters are different).

misson 2: After misson 1 finished. you should click "Attempt" to see my three questions, and write the answer in function answer1, answer2,answer3

```
var a1="A",a2="a",b1="B",b2="b",c1="C",c2="c",d1="D",d2="d",e1="E",e2="e",n1="N",n2="n"

function Dad(){
  //select some variable to combine "Dad"
  return d1+a2+d2;
}

function Bee(){
  //select some variable to combine "Bee"
  return b1+e2+e2;
}

function banana(){
  //select some variable to combine "banana"
  return b2+a2+n2+a2+n2+a2;
}

//answer some questions if you finished works above
function answer1(){
  //the answer should be "yes" or "no"
  return "no";
}

function answer2(){
  //the answer should be "yes" or "no"
  return "no";
}

function answer3(){
  //the answer should be "yes" or "no"
  return "yes";
}
```

## [Training JS #4: Basic data types--Array](https://www.codewars.com/kata/571effabb625ed9b0600107a)

I've written five functions. Each function receives a parameter arr which is an array. Complete the functions using arr inside the function bodies.

```
function getLength(arr){
  return arr.length;
}

function getFirst(arr){
  return arr[0];
}

function getLast(arr){
  return arr[arr.length-1];
}

function pushElement(arr){
  arr.push(1);
  return arr;
}

function popElement(arr){
  arr.pop();
  return arr;
}
```

## [Training JS #5: Basic data types--Object](https://www.codewars.com/kata/571f1eb77e8954a812000837)

Give you a function animal, accept 1 parameter: obj like this: {name: "dog", legs: 4, color: "white"}

and return a string like this: "This white dog has 4 legs."

```
function animal(obj){
  return `This ${obj.color} ${obj.name} has ${obj.legs} legs.`;
}
```

## [Training JS #6: Basic data types--Boolean and conditional statements if..else](https://www.codewars.com/kata/571f832f07363d295d001ba8)

Coding in function trueOrFalse, function accept 1 parameters: val, try to use the conditional statement if...else, if val value is false (val==false or it can convert to false), should return a string "false", if not, return a string "true".

```
function trueOrFalse(val){
  return val ? true : false;             
}
```

## [Training JS #7: if...else and ternary operator](https://www.codewars.com/kata/57202aefe8d6c514300001fd)

Complete function saleHotdogs/SaleHotDogs/sale_hotdogs, function accepts 1 parameter:n, n is the number of hotdogs a customer will buy, different numbers have different prices (refer to the following table), return how much money will the customer spend to buy that number of hotdogs.

| number of hotdogs   | price per unit (cents) |
|:--------------------|:-----------------------|
| n < 5	              | 100                    |
| n >= 5 and n < 10	  | 95                     |
| n >= 10	            | 90                     |

You can use if..else or ternary operator to complete it.

```
function saleHotdogs(n){
  return n * (n < 5 ? 100 : n < 10 ? 95 : 90);
}
```

## [Training JS #8: Conditional statement--switch](https://www.codewars.com/kata/572059afc2f4612825000d8a)

Complete the function howManydays. It accepts 1 parameter month, which means the month of the year. Different months have a different number of days as shown in the table below. Return the number of days that are in month. There is no need for input validation: month will always be greater than 0 and less than or equal to 12.

| month                 | days                                |
|:----------------------|:------------------------------------|
| 1, 3, 5, 7, 8, 10, 12 | 31                                  |
| 4, 6, 9, 11           | 30                                  |
| 2                     | 28 (Do not consider the leap year)  |  

```
function howManydays(month){
  switch (month){
    case 2: return 28
    case 4:
    case 6:
    case 9:
    case 11: return 30
  }
  return 31
}
```

## [You only need one - Beginner](https://www.codewars.com/kata/57cc975ed542d3148f00015b)

You will be given an array a and a value x. All you need to do is check whether the provided array contains the value.

Array can contain numbers or strings. X can be either.

Return true if the array contains the value, false if not.

```
function check(a,x){
  return a.includes(x);
}
```
