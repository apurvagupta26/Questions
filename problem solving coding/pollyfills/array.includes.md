<!-- includes(): Check if an element exists in an array or not. -->

 Array.prototype.custom_includes = function (element, fromIndex = 0) {
   for (let i = fromIndex; i < this.length; i++) {
     if (this[i] === element) {
       return true;
     }
   }
   return false;
 };
 
 console.log([1,3,5,7,0].custom_includes(5))