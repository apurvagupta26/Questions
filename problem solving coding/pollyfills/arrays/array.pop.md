//pollyfill for pop function

Array.prototype.pop = function(){
    let lastEl = this[this.length-1]
    this.length = this.length-1
    return lastEl
}
 console.log([1,2,3,4,5].pop());  // 5