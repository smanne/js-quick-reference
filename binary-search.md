**Binary Search**
Binary search is an efficient algorithm for finding an item from an ordered list of items. It works by repeatedly dividing in half the portion of the list that could contain the item, until you've narrowed down the possible locations to just one.  (If you are new to binary search [start here](https://www.khanacademy.org/computing/computer-science/algorithms/intro-to-algorithms/a/a-guessing-game))

Binary Search implemented in js.

```javascript
var binarySearch = function(array, targetValue) {
	var min = 0;
	var max = array.length - 1;
    var guess;
    while (min <= max) {
        guess = Math.floor((max + min) / 2); 
        if (array[guess] === targetValue) {
            return guess;
        } else if (array[guess] < targetValue) {
            min = guess+1;
        } else {
            max = guess-1;
        }
    }
	return -1;
};
```