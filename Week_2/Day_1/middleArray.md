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