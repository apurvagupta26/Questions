 <!-- indexOf(): Get the index of the first occurrence of an element in an array. -->

Array.prototype.custom_lastIndexOf = function(element, fromIndex = this.length-1) {
for(let i = fromIndex; i>0; i--) {
    if(this[i]===element) {
        return i
        }
    }
    return -1;
}

console.log([1,3,5,7,3,0].custom_lastIndexOf(3));
