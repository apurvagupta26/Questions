//resolve promise after 3 seconds

const delayedPromise = () => {
   return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("Promise resolved after 3 seconds!");
    }, 3000);  // 3000 milliseconds = 3 seconds
  });
}
  
  delayedPromise().then((message)=>{
      console.log(message)
  })
