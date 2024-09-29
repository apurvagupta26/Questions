let person = {
  firstname: "Apurva",
  lastname: "Gupta"
}

let printName = function (country) {
  console.log(this.firstname + " " + this.lastname + " from " 
  + country);
}

<!-- Now, we want to perform a printName method for each person object. -->
<!-- let person = {
  firstname: "Apurva",
  lastname: "Gupta",
  printName : function (country) {
             console.log(this.firstname + " " + this.lastname 
             + " from " + country);
             }    
}

person.printName("India"); -->
<!-- the above code will have repeated code of function in each object -->

Function.prototype.custom_call = function(obj,...args) { 
    let symbol = Symbol();         
    obj[symbol] = this;
    let res = obj[symbol](...args);
    delete obj[symbol];
    return res;
}

/*
Note: Applying mycall method to printName function so this
will be equal to printName inside mycall function as 
printName is on the left side of the '.' 
*/

printName.mycall(person, "India");

Output: 
"Apurva Gupta from India"