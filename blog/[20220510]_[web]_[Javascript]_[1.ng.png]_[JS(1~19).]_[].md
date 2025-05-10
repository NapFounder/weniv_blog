- This Js write is based on this course : 🌐 [Website]((https://www.google.com/search?q=google+color+picker&oq=google+color+p&gs_lcrp=EgZjaHJvbWUqBwgAEAAYgAQyBwgAEAAYgAQyBwgBEAAYgAQyBggCEEUYOTIGCAMQABgeMgYIBBAAGB4yBggFEAAYHjIGCAYQABgeMgYIBxAAGB4yBggIEAAYHjIICAkQABgKGB7SAQgzODMxajBqN6gCALACAA&sourceid=chrome&ie=UTF-8)), 
📚 [Reference]((https://github.com/jonasschmedtmann/complete-javascript-course))

## 1. How to link Javascript
JS = Dynamic effects and web applications in the browser

1. Web applications (React)
2. Web server (Node.js)
3. mobile applications (React Native)
4. Desktop applications (Electron)

- How to link Javascript file
```
    <script src="script.js"></script>
```

## 2. Values and Variables
- How to declaring Variables
```
let firstName = 'James' // Variable = values
console.log(firstName);
```
When we assign variables we have to use camlecase.

write firstcase lowercase, Othercasese Uppercase.
ex) firstNamePersone

- How to write Variables in Javascript.
📚 [Reference]((https://github.com/jonasschmedtmann/complete-javascript-course))

Variable is bascially box into we can store values.
## 3. Practice Assignment
1. Declare variables called country, continent and population and assign their values according to your own country (population in millions).

2. Log their values to the console.
```
let country = "korea";
let continent = "Asia";
let population = 50000000;

console.log(country);  //korea
console.log(continent);  // Asia
console.log(population); // 50000000
```
## 4. Data Types 
1. Number : Used for decimals and integers ```let age = 23;```

2. String : Used for text ```let firstName = 'Jonas';```

    [string needs quotes('', "")]

3. Boolean : Logic type can be true or false : ```let fullAge = true;```

4. Undefined : Value taken by a variable that is not yet defined ('empty value') : ```let children;```

5. Null : Also means empty value but it is just empty

6. Symbol : That is unique and cannot be changed [Not useful for now

7. BigInt : Large than the number type can hold.

(6,7 is not used that much)

+) Javascript comment is written by ```//, (/**/)```

- Special Operator 'type of'
```
console.log(typeof true)   // boolean
console.log(typeof 23)     // number 
console.log(typeof 'Git')  // string
```

- How to change Values in Variable
```
let JavascriptIsFun = true;
console.log(typeof JavascriptIsFun); // boolean

JavascriptIsFun = "YES!";
console.log(typeof JavascriptIsFun); // string
```

- Undefined
```
let year;
console.log(year); // undefined
console.log(typeof year); // undefined

year = 1991;
console.log(year); // 1991
console.log(typeof year); // number
```

- Error exsits in typeof Operator
```
console.log(typeof null);  // object
```
[As for now just know that this is Legacy (bug)code.]
## 5. let, const and var
- When we mutate Variable let keyword is used, also declare empty Variables.
```
let age = 31;
let age = 30;
let name =;
```

* const keyword make a variable that we can't assign.
```
const PI = 3.14;
```
- use constant normally and use let when that variable needs change.

> var(actually aviod these keyword!!), Just know as a 'Legacy' reason.

```
var job = 'teacher';
job = 'programmer';
```
It seems like let and var are simillar but It's actually very different.(pass now and we can learn later.)

Don't declare the variables not to use these 3 variables.
## 6. Basic Operators
Operators basically allow us to transform values or combine values.

1. Mathematical operators(+, -, *, /, %..)
```
const NOW = 2025;
const AGEJAMES = NOW - 1991;
const AGEKEVIN = NOW - 1994;
console.log(AGEJAMES, AGEKEVIN);  // 34, 31
console.log(AGEKEVIN * 2, AGEJAMES / 2);  // 62, 17
console.log(2 ** 3); // 8
```

- (+)operator can connect stirngs.
```
const FIRSTNAME = 'KIM';
const SECONDNAME = 'MINSOO'
console.log(FIRSTNAME + " " + SECONDNAME);  // KIM MINSOO
```

- Assignment operator(=)
```
let x = 10 + 5;  // 15
x += 15  // x = x + 15 (This syntax can be used *=, -=, /=)
console.log(x);  // 25
x ++
console.log(x);  // 26
x --
console.log(x);  // 25
```

- Comparison Operators (<, >, <=, >=)
```
console.log(AGEJAMES > AGEKEVIN);  // true
console.log(AGEJAMES < AGEKEVIN);  // false
```
## 7. Operators Precedence
```
console.log(2 + 5 * 3);  // 17
console.log((2 + 5)* 3); // 21
```
Most important thing is that () is first Precedence.
📚 [Reference]((http://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_precedence))

## 8. #1 Coding Challenge.
CHALLENGE #1
Mark and John are trying to compare their BMI (Body Mass Index), which is calculated using the formula: BMI = mass / (height * height) (mass in kg and height in meters).

Your task is to write some code to help them:

Store Mark's and John's mass and height in variables called massMark, heightMark, massJohn and heightJohn.

Calculate both their BMIs using the formula, and store the results in two variables called BMIMark and BMIJohn.

Log the value of BMIMark and BMIJohn to the console.

BONUS: Create a boolean variable markHigherBMI containing information about whether Mark has a higher BMI than John. Log it to the console too

TEST DATA 1: Marks weighs 78 kg and is 1.69 m tall. John weighs 92 kg and is 1.95 m tall.

TEST DATA 2: Marks weights 95 kg and is 1.88 m tall. John weights 85 kg and is 1.76 m tall.



👋 OPTIONAL: You can watch my solution in video format in the next lecture



IMPORTANT: The ** operator is not supported in this editor. Please make sure to use exactly this formula mass / (height * height), and not this one mass / (height ** 2).

```
let massMark = 78;
let heightMark = 1.69;
let massJohn = 92;
let heightJohn = 1.95;

let BMIMark = massMark / (heightMark * heightMark);
let BMIJohn = massJohn / (heightJohn * heightJohn);
let markHigherBMI = BMIMark > BMIJohn;

console.log("First Data:");
console.log("Mark BMI:", BMIMark.toFixed(2)); // how to make numbers round?
console.log("John BMI:", BMIJohn.toFixed(2));
console.log("Mark's BMI higher than John's?", markHigherBMI);
console.log('---');
massMark = 95; 
heightMark = 1.88;
massJohn = 85;
heightJohn = 1.76;

BMIMark = massMark / (heightMark * heightMark); // 
BMIJohn = massJohn / (heightJohn * heightJohn);
markHigherBMI = BMIMark > BMIJohn; 

console.log("Second Data:");
console.log("Mark BMI:", BMIMark.toFixed(2));
console.log("John BMI:", BMIJohn.toFixed(2));
console.log("Mark's BMI higher than John's?", markHigherBMI);
```
- In this course he use let instead const but i use let.(no problem) also i upgrade code!

> acutally it can be solved by function but we didn't learn yet so..
## 9. Strings & Templete Literals
```
let firstName = 'Jonas';
let job = 'teacher';
let age = 33;

let intro = "I'm " + firstName + ", a " + job + " " + age
console.log(intro)  // I'm Jonas, a teacher 33
```
- This is complex as you see, How make it more simple.
> Now let we use templet Literal by (backtick and ${}).
```
let intro = `I'm ${firstName}, ${job} and my age is ${age}`;
console.log(intro)  // I'm Jonas, teacher and my age is 33
```
When we use string cover by ``(backtick) is very useful don't miss it.

> Templete Literals are also useful in multi line
```
console.log('string with\n\
multiple\n\
lines')
```
-> let's change it. (by use backtick)
```
console.log(`string with 
multiple 
lines.`)
```
## 10. if/else statements
* ex1)
```
let age = 19;
const OLDENOUGH >= age;

if (OLDENOUGH) {  // (condition)
    console.log(`OOO is okay to drive👌`);  // inside of {} this code block is executed if it's true.
} else {  // else part is for condition is false.
    console.log(`ooo is not allowed to drive🤬.)
}
```
- ex2)
```
let birthYear = 1991;
let century;

if (birthYear < 2000) {
    century = 20;
} else {
    century = 21;
}

console.log(century);  // 20
```
## 11. # Challenge 2 
Suggested code may be subject to a license. Learn more: ~LicenseLog:3299365783.

Suggested code may be subject to a license. Learn more: ~LicenseLog:3571101487.

CHALLENGE #2
Use the BMI example from Challenge #1, and the code you already wrote, and improve it:

1. Print a nice output to the console, telling the user who has the higher BMI. The message can be either:

"Mark's BMI is higher than John's!" or "John's BMI is higher than Mark's!".

2. Modify the outputs above to use template literals to include the BMI values in the outputs.

Example: "Mark's BMI (28.3) is higher than John's (23.9)!" or "John's BMI (29.1) is higher than Mark's (27)!".

Note: Don't round the BMI values. Leave them as they are.



👋 OPTIONAL: You can watch my solution in video format in the next lecture



IMPORTANT: The ** operator is not supported in this editor. 

Please make sure to use exactly this formula mass / (height * height), and not this one mass / (height ** 2).

```
let massMark = 78;
let heightMark = 1.69;
let massJohn = 92;
let heightJohn = 1.95;

let BMIMark = massMark / (heightMark * heightMark);
let BMIJohn = massJohn / (heightJohn * heightJohn);
console.log(BMIMark, BMIJohn);

if (BMIMark > BMIJohn) {
 console.log(`Mark's BMI (${BMIMark.toFixed(2)}) is higher than John's (${BMIJohn.toFixed(2)})!`)
} else {
 console.log(`John's BMI (${BMIJohn.toFixed(2)}) is higher than Mark's (${BMIMark.toFixed(2)})!`)
}
```
----