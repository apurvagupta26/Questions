<!-- concat(): Concatenate two or more arrays into one. -->
<!-- The concat() method of Array instances is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array. -->

<!-- there are two references inside the prototype- this = [1,2,3,4], arguments = [5,6] -->
<!-- concat method does not flatten- conact two arrays as is -->

Array.prototype.custom_concat = function(){
  let result=[];
  result=[...this];
  for(i=0;i<arguments.length;i++) {
      if(Array.isArray(arguments[i])) {
      const dummyArr = arguments[i];
      for (let i = 0; i < dummyArr.length; i++) {
         result.push(dummyArr[i]);
        }
      } else {
          result.push(arguments[i])
      }
  }
  return result
}
console.log([1,2,3,4].custom_concat([5,6,[7,8]]))


<!-- Array.prototype.custom_concat = function(...args) {
  let result = [...this];
  
  for (const arg of args) {
    if (Array.isArray(arg)) {
      result.push(...arg); // Use spread operator to push all elements of the array
    } else {
      result.push(arg); // Directly push non-array values
    }
  }
  
  return result; // Return the new concatenated array
}; -->


<!-- concat with flatenning -->
<!-- Array.prototype.custom_concat = function(){
  let result=[];
  result=[...this];
  for(i=0;i<arguments[0].length;i++) {
      if(Array.isArray(arguments[0][i])) {
      const dummyArr = arguments[0][i];
      for (let i = 0; i < dummyArr.length; i++) {
         result.push(dummyArr[i]);
        }
      } else {
          result.push(arguments[0][i])
      }
  }
  console.log(result)
} -->


