# Bubble Sorting

```js
function bubbleSort(array, ascending = false, steps = false) {
  if (ascending === true && steps === true) {
    for (let i = 0; i < array.length; i++) {
      console.log(`step ${i + 1}:`);
      for (let j = 0; j < array.length - i - 1; j++) {
        console.log(`j = ${j} : ${array}`);
        // sorting in ascending order
        if (array[j] > array[j + 1]) {
          // swapping
          [array[j], array[j + 1]] = [array[j + 1], array[j]];
          console.log(`Swapping: ${array[j]} with ${array[j + 1]}`);
        }
      }
      console.log("\n");
    }
    return array;
  } else if (ascending === false && steps === true) {
    for (let i = 0; i < array.length; i++) {
      console.log(`step ${i + 1}:`);
      for (let j = 0; j < array.length - i - 1; j++) {
        console.log(`j = ${j} : ${array}`);
        // sorting in descending order
        if (array[j] < array[j + 1]) {
          // swapping
          [array[j], array[j + 1]] = [array[j + 1], array[j]];
          console.log(`Swapping: ${array[j]} with ${array[j + 1]}`);
        }
      }
      console.log("\n");
    }
    return array;
  } else if (ascending === true && steps === false) {
    for (let i = 0; i < array.length; i++) {
      for (let j = 0; j < array.length - i - 1; j++) {
        // sorting in ascending order
        if (array[j] > array[j + 1]) {
          // swapping
          [array[j], array[j + 1]] = [array[j + 1], array[j]];
        }
      }
    }
    return array;
  } else {
    for (let i = 0; i < array.length; i++) {
      for (let j = 0; j < array.length - i - 1; j++) {
        // sorting in descending order
        if (array[j] < array[j + 1]) {
          // swapping
          [array[j], array[j + 1]] = [array[j + 1], array[j]];
        }
      }
    }
    return array;
  }
}

```
