``` javascript
const letterPositions = function(sentence) {
  const results = {};

  [...sentence].forEach((letter, index)=>{
    if (results[letter]) {
      results[letter].push(index);
    } else {
      results[letter] = [index];
    }
  });

  delete results[" "];
  return results;
}

```
[...sentence] is turning the string into an array of each character


