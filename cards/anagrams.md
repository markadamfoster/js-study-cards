## Check if anagrams

One string is an anagram of another if it uses the same characters in the same quantity. Only consider characters, not spaces or punctuation.  Consider capital letters to be the same as lower case.

Hint: Here's the RegExp for cleaning the string: `str.replace(/[^\w]/g, "")`

### Setup:
```js
const anagrams = (str1, str2) => {
  return;
};

console.log(anagrams("rail safety", "fairy tales")); // true
console.log(anagrams("RAIL! SAFETY!", "fairy tales")); // true
console.log(anagrams("Hi there", "Bye there")); // false
```

---

### Solution 1:
```js
function anagrams(stringA, stringB) {
  const mapA = cleanAndMap(stringA)
  const mapB = cleanAndMap(stringB)
  
  if (Object.keys(mapA).length !== Object.keys(mapB).length) return false
  
  for (let char in mapA) {
    if (mapA[char] !== mapB[char]) return false
  }

  return true
}

function cleanAndMap(str) {
  const cleaned = str.replace(/[^\w]/g, "").toLowerCase()
  
  return cleaned.split("").reduce((map, char) => {
    map[char] = ++map[char] || 1
    return map
  }, {})
}
```

### Solution 2:
```js
function anagrams(stringA, stringB) {
  return cleanAndSort(stringA) === cleanAndSort(stringB)
}

function cleanAndSort(str) {
  return str.replace(/[^\w]/g, "").toLowerCase().split("").sort().join("")
}
```