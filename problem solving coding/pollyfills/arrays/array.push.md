//pollyfill for push()

Array.prototype.myPush= function(number){
    this[this.length]=number;
    return this;
}

console.log([1,2,3,4,5].myPush(80));
//output: [1,2,3,4,5,80]