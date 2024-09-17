<!-- Join the elements of an array into a string. -->
<!-- default separator is comma -->

Array.prototype.custom_join = function (separator = ",") {
   let result = "";

   for (let i = 0; i < this.length; i++) {
     if (i === this.length - 1) {
        <!-- only one element in array -->
       result += this[i];
     } else {
        <!-- join by separator -->
       result += this[i] + separator;
     }
   }

   return result;
 };
 
 console.log(['a','b','c','d','e'].custom_join(' '))