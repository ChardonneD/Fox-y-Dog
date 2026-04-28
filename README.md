# Fox-y-Dog
Book Four - Chap 1


*Async b4 a promise
const myFunction = async () => {
    // Function body
}

The function automatically returns a Promise
You can use the await keyword inside the function

*await b4 a promise
const myFunction = async () => {
    const result = await somePromise();
    // Code here waits until somePromise() resolves
    console.log(result);
}

It pauses the execution of the function until the Promise resolves
It then returns the resolved value of the Promise



const displayDogImage = async () => {
    const response = await fetch("https://random.dog/woof.json")
    const dogData = await response.json()
    const dogImage = document.querySelector("#dog")
    dogImage.src = dogData.url
}
dogButton.addEventListener("click", displayDogImage)