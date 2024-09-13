 <!-- indexOf(): Get the index of the first occurrence of an element in an array. -->

Array.prototype.custom_indexOf = function(element, fromIndex = 0) {
for(let i = fromIndex; i<this.length; i++) {
    if(this[i]===element) {
        return i
        }
    }
    return -1;
}

console.log([1,3,5,7,0].custom_indexOf(3));
