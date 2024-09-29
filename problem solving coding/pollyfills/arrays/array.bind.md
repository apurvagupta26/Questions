<!-- bind method is similar to the call method but the only difference is that call method invokes the function but incase of bind it returns a new function which can be invoked later. -->

let person = {
  firstname: "Apurva",
  lastname: "Gupta"
}

let printName = function (country) {
  console.log(this.firstname + " " + this.lastname + " from " 
  + country);
}

Function.prototype.custom_bind = function(object,...args) {
  let func = this;
  return function (...args1) {
    return func.apply(object, [...args, ...args1]);
  }
}

let newPrintName = printName.custom_bind(person, "India");
newPrintName();

Output: 
"Apurva Gupta from India"