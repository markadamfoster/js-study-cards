Given an array and chunk size, divide the array into many subarrays where each subarray is of length size

### Examples:
```js
chunk([1, 2, 3, 4], 2) // [[ 1, 2], [3, 4]]
chunk([1, 2, 3, 4, 5], 2) // [[ 1, 2], [3, 4], [5]]
chunk([1, 2, 3, 4, 5, 6, 7, 8], 3) // [[ 1, 2, 3], [4, 5, 6], [7, 8]]
chunk([1, 2, 3, 4, 5], 4) // [[ 1, 2, 3, 4], [5]]
chunk([1, 2, 3, 4, 5], 10) // [[ 1, 2, 3, 4, 5]]
```

---

## Solution 1
```js
function chunk(array, size) {
  let allChunks = []
  
  array.forEach(item => {
    const lastChunk = allChunks[allChunks.length - 1]
    
    if (!lastChunk || lastChunk.length === size) {
      allChunks.push([item])
    } else {
      lastChunk.push(item)
    }
  })

  return allChunks;
}
```

## Solution 2
```js
function chunk(array, size) {
  let allChunks = []
  let i = 0

  while(i < array.length) {
    allChunks.push(array.slice(i, i + size))
    i += size
  }
  return allChunks
}
```
