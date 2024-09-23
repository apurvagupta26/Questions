function palindrome(text){
    let reverseString = '';
    let textarray = [...text];
    let reverseArray = textarray.reverse();
    reverseArray.forEach(x=>{
        reverseString = reverseString+=x;
    })
   if(text === reverseString){
       return true
   }
   else {
       return false;
   }
}

console.log(palindrome('refer'));