# Flatten Array

### different code

``` javascript
const flatten = function(array) {
  let finalArr = [];
 
  for (let i = 0; i < array.length; i++) {
    if (!Array.isArray(array[i])) {
      finalArr.push(array[i]);
    } else if (Array.isArray(array[i])) {
      for (let j = 0; j < array[i].length; j++) {
        finalArr.push(array[i][j]);
      }
    }
  }
  return finalArr;
};


// or 

const flatten = function(array) {
  let flatArray = [];
  for (let element of array) {
    if (Array.isArray(element)) {
      flatArray = flatArray.concat(element);
    } else {
      flatArray.push(element);
    }
  }
  return flatArray;
};
```

