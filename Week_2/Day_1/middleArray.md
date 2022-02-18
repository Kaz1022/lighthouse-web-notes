``` javascript
const middle = (array) => {
  const midIndex = Math.floor(array.length / 2);
  return (array.length <= 2) ? []
    : (array.length % 2 !== 0) ? [array[midIndex]]
      : [array[midIndex - 1], array[midIndex]];
};
```
``` javascript
const middle = function(array) {
  let middleArr = [];
  const middleIndex = Math.floor(array.length / 2);

  if (array.length >= 4 && array.length % 2 === 0) {
    middleArr.push(array[middleIndex - 1], array[middleIndex - middleIndex / 2]);
  }

  if (array.length >= 3 && array.length % 2 !== 0) {
    middleArr.push(array[middleIndex]);
  }
  return middleArr;
};
```

``` javascript
const middle = function(array) {
  const mid = array.length / 2;
  let middleArray = [];
  if (mid > 1) {
    // 1. check if the array has only one or two elements, return [];
    middleArray.push(array[Math.floor(mid)]);
    // [1,2,3] --> [2]  - [1,2,3,4] --> [3]
    if (Number.isInteger(mid)) {
      // for [1,2,3,4] we need 2 as well
      // add it to the left side of array --> [2,3]
      middleArray.unshift(array[mid - 1]);
    }
  }
  return middleArray;
};


const middle = (array) => {
  let middleArray = [];
  if (array.length <= 2 && array.length >= 0) {
    return middleArray;
  } else if (array.length % 2 !== 0) {
    middleArray.push(array[Math.floor(array.length / 2)]);
  } else if (array.length % 2 === 0) {
    middleArray.push(array[(array.length / 2) - 1], array[array.length / 2]);
  }
  return middleArray;
};
```