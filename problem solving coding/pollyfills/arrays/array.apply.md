<!-- //apply accepts arguments as an array -->
<!-- apply method is very similar to the call method but the only difference is that call method takes the argumetns as comma seperated values where as apply method takes an array of arguments. -->

let person = {
  firstname: "Apurva",
  lastname: "Gupta"
}

let printName = function (country) {
  console.log(this.firstname + " " + this.lastname + " from " 
  + country);
}

Function.prototype.custom_apply = function(obj,...args){
  let sym = Symbol();                                     
  obj[sym] = this;
  let res = obj[sym](...args[0]); 
  delete obj[sym];
  return res;
}

printName.custom_apply(person, ["India"]);

Output: 
"Apurva Gupta from India"