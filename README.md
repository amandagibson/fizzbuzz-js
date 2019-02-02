# JavaScript FizzBuzz

<b>Question 1:</b> To the best of your knowledge please explain what the following lines of code do:
```
let  fizzBuzz = fs.readFileSync('./src/js/fizz-buzz.js');
eval( fizzBuzz + `\nexports.FizzBuzz = FizzBuzz;`)
```

A: The fs.readFileSync will return the contents of './src/js/fizz-buzz.js' <br>
The eval() function evaluates or executes an argument; *eval(string)* <br>
We have added these lines in our spec.helper for the sake of testing.
<br><br>


<b>Question 2:</b> To the best of your knowledge please explain why we are placing the `let fizzBuzz = new FizzBuzz` outside the `it` block? <br>

A: We are creating new objects from the function FizzBuzz.
<br><br>


<b>Question 3:</b> To the best of your knowledge please explain the difference between using === and == in JS? <br>

A: In JavaScript, the triple equals === compares both the type and the value. Double equals == doesn't compare the type so much as it compares more of the vaule of two things. i.e. <br>
123 === '123' // false<br>
123 == '123' //true 
<br><br>

<b>Question 4:</b> To the best of your knowledge please explain why we are moving (number % 5 === 0) to the top? <br>

A: We move this to the top because the function runs from top to bottom. For example, 15 is divisible by both 3 and 5 but we want it to return 'Buzz' before it returns 'Fizz'.


******
created by: Amanda Gibson, https://github.com/amandagibson