# Reverse String 

### my code...
``` javascript
const reverse = function(numOfArg) {
  numOfArg = process.argv.slice(2);

  for (let i = 0; i < numOfArg.length; i++) {
    let reversedStr = "";
    for (let j = numOfArg[i].length - 1; j >= 0; j--) {
      reversedStr += numOfArg[i][j];
    }
    console.log(reversedStr);
  }
};

reverse();

```

### Farz's code...
``` javascript
const reverseString = function(str) {
  let reversed = "";
  for (let i = str.length - 1; i >= 0; i --) {
    reversed += str[i];
  }
  return reversed;
};

const inputStrings = process.argv.slice(2);

if (inputStrings.length === 0) {
  console.log(`There is nothing to reverse. \n Feel free to insert some strings,`);
} else {
  for (let string of inputStrings) {
    console.log(reverseString(string));
  }
}

```