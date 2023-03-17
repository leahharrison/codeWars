# 8 kyu

## [Add Length](https://www.codewars.com/kata/559d2284b5bb6799e9000047)

What if we need the length of the words separated by a space to be added at the end of that same word and have it returned as an array?

Example(Input --> Output)
- "apple ban" --> ["apple 5", "ban 3"]
- "you will win" -->["you 3", "will 4", "win 3"]

Your task is to write a function that takes a String and returns an Array/list with the length of each word added to each element .

Note: String will have at least one element; words will always be separated by a space.

```
function addLength(str){
  return str.split(" ").map(x => `${x} ${x.length}`)
}
```

## [N-th Power](https://www.codewars.com/kata/57d814e4950d8489720008db)

You are given an array with positive numbers and a non-negative number N. You should find the N-th power of the element in the array with the index N. If N is outside of the array, then return -1. Don't forget that the first element has the index 0.

Let's look at a few examples:
- array = [1, 2, 3, 4] and N = 2, then the result is 3^2 == 9
- array = [1, 2, 3] and N = 3, but N is outside of the array, so the result is -1

```
function index(array, n){
    return array.length > n ? Math.pow(array[n], n) : -1
}
```
