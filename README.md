# maps-and-sets-exercise

Quick Question #1
What does the following code return?

new Set([1,1,2,2,3,4])

Answer: A set with a size of four containing '1', '2', '3', and '4'.

______

Quick Question #2
What does the following code return?

[...new Set("referee")].join("")

Answer: the string "ref"

______

Quick Questions #3
What does the Map m look like after running the following code?

let m = new Map();
m.set([1,2,3], true);
m.set([1,2,3], false);

Answer: It has two entries with a key of an array containing 1, 2, and 3, where the value to the first key is true, and the value for the second key is false.

______

hasDuplicate
Write a function called hasDuplicate which accepts an array and returns true or false if that array contains a duplicate

function hasDuplicate(arr) {
  let arrSet = [...new Set(arr)];
  console.log(arrSet);
  console.log(arr);
  return !arr.every((val, index) => val === arrSet[index]);
}

_______

vowelCount
Write a function called vowelCount which accepts a string and returns a map where the keys are numbers and the values are the count of the vowels in the string.

function vowelCount(str) {
  let mapVowel = new Map([
  ['a', 0],
  ['e', 0],
  ['i', 0],
  ['o', 0],
  ['u', 0]]);
  
  Array.from(str).forEach((val, index) => {
    mapVowel.set(val, mapVowel.get(val)+1);
  });
  return mapVowel;
}

_______
