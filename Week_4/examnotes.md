
 * Question 3
 
 *  Implement the 'mode' function defined below
 
 * MODE - the most frequently occurring number
 for this test, the provided lists will only have a single value for the mode
 
 * For example:
  mode([6,2,3,4,9,6,1,0,5]);
  Returns: 6

``` javascript
//PESUEDO CODE

// you have to loop through all the array
// you have to count each item 
// make an object to track the counts
// then compare the object[key] value 
// return the highestValue's object[key]

const mode = function(arr) {
  const occurrences = {};

  for (let i = 0; i < arr.length; i++) {
    const num = arr[i];
    //if there was no previous occurences[num], it will be undefined, therefore needs to add 0
    occurrences[num] = (occurrences[num] || 0) + 1;
  }

  let highestValue = 0;
  let highestKey = '';
  for (const key in occurrences) {
    const val = occurrences[key];
    if (val > highestValue) {
      highestValue = val;
      highestKey = key;
    }
  }

  console.log(highestKey);
  return highestKey;

};



mode([6, 2, 3, 4, 9, 6, 1, 0, 5]);

```