<!-- slice(): Create a new array that is a slice of the original array. -->

Array.prototype.custom_slice = function(start ,end) {
    let slicedArray = [];
    start = start ?? 0; // Default to 0 if start is undefined
    end = end ?? this.length; // Default to array length if end is undefined
    // Handle negative indices
    if (start < 0) start = this.length + start;
    if (end < 0) end = this.length + end;
         for (let i = start; i < end && i < this.length; i++) {
           slicedArray.push(this[i]);
          }
        return slicedArray
}


console.log([ 1, 2, 3, 4, 5 ].custom_slice(2))
