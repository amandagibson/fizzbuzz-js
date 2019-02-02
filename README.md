# JavaScript FizzBuzz

<b>Question 1:</b> In your README to the best of your knowledge please explain what the following lines of code do:
```
let  fizzBuzz = fs.readFileSync('./src/js/fizz-buzz.js');
eval( fizzBuzz + `\nexports.FizzBuzz = FizzBuzz;`)
```

A: The fs.readFileSync will return the contents of './src/js/fizz-buzz.js' <br>
The eval() function evaluates or executes an argument; *eval(string)* <br>
We have added these lines in our spec.helper for the sake of testing.<br>
<br>

<b>Question 2:</b> In your README to the best of your knowledge please explain why we are placing the `let fizzBuzz = new FizzBuzz` outside the `it` block? <br>


A: We are creating new objects from the function FizzBuzz.


******
created by: Amanda Gibson, https://github.com/amandagibson