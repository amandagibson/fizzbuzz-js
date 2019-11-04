# JavaScript FizzBuzz
Deployed with netlify at https://fizzbuzzbomb.netlify.com/ <br>

- <b>Instructions:</b>
To play, open the browswer and enter a number into the field, click on 'click' button. Answer is displayed below your input.<br>
- <b>Rules:</b>
The rules of FizzBuzz are as follows: So that the game can be played by the rules; I want a number divisible by 3 to return 'fizz', a number divisible by 5 to return 'buzz', and a number divisible by 15 to return 'fizzbuzz'.<br>
- <b>Testing:</b>
Testing for this program can be run through terminal using npm run test.


***********
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

<b>Question 7:</b> To the best of your knowledge please explain what expectations in the context of testing are. <br>

A: In testing, expectations tell our tests what we expect the outcome to be. Expectations are the answers to your questions. (A possible oversimplification?)
<br><br>

<b>Question 8:</b> To the best of your knowledge please write a line to line explanation of what is happening in this code:
```
<script src="./js/fizz-buzz.js"></script>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            let button = document.getElementById('button')
            let displayDiv = document.getElementById('display_answer')
            button.addEventListener('click', () =>{
                let value = document.getElementById('value').value
                let fizzBuzz = new FizzBuzz
                let result = fizzBuzz.check(value)
                displayDiv.innerHTML = result;
            })
        })
    </script>
```

A: <br>
1: script src pulls javascript code from the specified file. <br>
2-6: the page is loaded, button and displayDiv are defined. <br>
7-11: listening for someone to click the button, then evaluates the value entered and returns the result according to the game FizzBuzz.
<br><br>

<b>Question 9:</b> To the best of your knowledge please explain what a CDN (Content Delivery Network) is? <br>

A: CDN, A Content Delivery Network, can be thought of as a content repeater. It takes content and repeats it to other conneted servers all around the world. Loading times are better, other servers can be used as backup in the event that something fails in one place. This works so long as the origin server remains.
<br><br>

******
Created by: Amanda Gibson, https://github.com/amandagibson <br>
Built using JavaScript.