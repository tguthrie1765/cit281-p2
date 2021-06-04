In this project I got more eperence using the command line interface. I was also able to practice refactoring. 

<br>

Here is the code for project 2
```js
/*
    CIT 281 Project 2
    Name: Thomas Guthrie
*/

// Returns a random number between min (inclusive) and max (exclusive)
const getRandomInteger = function(minLength, maxLength) {
    return Math.floor(Math.random() * (maxLength - minLength) + minLength);
}

const alphabet = "abcdefghijklmnopqrstuvwxyz".split("");
let result = "";
let string = "";




//returns a single random letter from alphabet from 0 to the length of alphabet
const getRandomLetter = function(){

    let randomNumber = getRandomInteger(0,alphabet.length-1)
   
    let letter = alphabet[randomNumber];
    
    return letter;
}

//sets the min & max length of string, gets random length, then calls random letter until the length is filled
const getRandomString = function(minLength, maxLength){
    srtingLength = getRandomInteger(minLength, maxLength);
    let i = 0
    while (i< srtingLength){
        string += getRandomLetter();
        i++;
    }
    return string;
}

//takes string converts to array, sorts, converts to string, removes commas
const getSortedString = function(string){
    return string.split("").sort().toString().replace(/,/g, "");
 }
 
 console.log(getRandomString(10,20));
 
 for (let i = 0; i < getRandomInteger(5, 26); i++) {
    result += alphabet[getRandomLetter(1,alphabet.length-1)];
}
```

```js
/*
    CIT 281 Project 2
    Name: Thomas Guthrie
*/

// Returns a random number between min (inclusive) and max (exclusive)
function getRandomInteger(minLength, maxLength) {
    return Math.floor(Math.random() * (maxLength - minLength) + minLength);
}

const alphabet = "abcdefghijklmnopqrstuvwxyz".split("");
let result = "";
let string = "";

for (let i = 0; i < getRandomInteger(5, 26); i++) {
    result += alphabet[getRandomLetter(1,alphabet.length-1)];
}


//returns a single random letter from alphabet from 0 to the length of alphabet
function getRandomLetter(){

    let randomNumber = getRandomInteger(0,alphabet.length-1)
   
    let letter = alphabet[randomNumber];
    
    return letter;
}

//sets the min & max length of string, gets random length, then calls random letter until the length is filled
function getRandomString(minLength, maxLength){
    srtingLength = getRandomInteger(minLength, maxLength);
    let i = 0
    while (i< srtingLength){
        string += getRandomLetter();
        i++;
    }
    return string;
}

//takes string converts to array, sorts, converts to string, removes commas
function getSortedString(string){
    return string.split("").sort().toString().replace(/,/g, "");
 }
 
 console.log(getRandomString(10,20));
 ```
