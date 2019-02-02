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
<br><br>

<b>Question 5:</b> To the best of your knowledge please explain the difference between feature and unit test. <br>

A: Unit testing tests individual functions to make sure the expected outcome is what it should be. We unit test by writing small scripts in our spec files that we can plug our expected outcomes into and tie these to the files that contain the actual functions we are testing. Feature testing tests what the user sees so you test this way by running and interacting with your program.
<br><br>

<b>Question 6:</b> To the best of your knowledge please explain what this following code does:
```
describe('User can input a value and get FizzBuzz results', () => {
    before(async () => {
        await  browser.init()
        await  browser.visitPage('http://localhost:8080/')
    });

    beforeEach(async () => {
        await  browser.page.reload();
    })

    after(async ()=> {
        await  browser.close();
    })
})
```

A: This describe block is describing asynchronous flow. <br>
We are initializing the browser & visiting the address for the server that we will be testing on, reloading after each test, and making sure the browswer closes after testing. With async these things can initialize while the processes that started before them are still running, there's no need for each process to wait for completion of the other before starting.
<br><br>


******
created by: Amanda Gibson, https://github.com/amandagibson