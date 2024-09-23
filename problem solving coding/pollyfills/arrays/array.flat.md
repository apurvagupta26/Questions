 <!-- The flat() method creates a new array with all sub-array elements concatenated into it recursively up to the specified depth. -->

 <!-- inbuilt flat()
 array=[1,2,3,[4,6,[7,8,9]]];
console.log(array.flat(1)) -->

<!-- Pollyfill -->
array=[1,2,3,[4,6,[7,8,9]]];
Array.prototype.custom_flat = function(depth=1) {
    let flattenedArray = [];
   // Helper function to flatten recursively
    const flatten = (arr, currentDepth) => {
        for (let i = 0; i < arr.length; i++) {
            if (Array.isArray(arr[i]) && currentDepth < depth) {
                flatten(arr[i], currentDepth + 1); // Recursively flatten if depth allows
            } else {
                flattenedArray.push(arr[i]); // Push element if not an array or max depth reached
            }
        }
    };

    flatten(this, 0); // Start flattening the array
    return flattenedArray;
}

console.log(array.custom_flat())
