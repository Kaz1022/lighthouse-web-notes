``` javascript
const findKey = function(obj, fn) {
  for (const [key, val] of Object.entries(obj)) {
    if (fn(val)) {
      return key;
    }
  }
  return undefined;
};
```


``` javascript
const findKey = function(inputObject, callbackFn) {
  for (const key in inputObject) {
    if (callbackFn(inputObject[key])) {
      return key;
    }
  }
}
```

