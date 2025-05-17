# 1. Type conversion and Coercion
- type conversion 

```js
let inputYear = '1990';  // string
console.log(inputYear + 10);  // 199010
```

- Use Number function and change data type.
```js
let inputYear = '1990';
console.log(Number(inputYear));
console.log(inputYear + 10);  // 2000
```

```js
console.log(Number('Andy'));  // NaN (Not a Number);
console.log(typeof NaN);      // number (It means invalid number);
```

```js
console.log(String(23));  // 23
```

- type Coercion
```js
console.log("I'm + 23 + 'years old');
```

- This example(+) is important
```js
console.log('23' - '10' - 3);  // 10
console.log('23' + '10' + 3);  // 23103 (+ shows concatenate)
console.log('23' * '2');       // 46
console.log('24' / '2');       // 12
```

- Let me give you an example
```js
let n = '1' + 1;
n = n - 1;
console.log(n);  // n = 10
```

## 2. TRUTHY AND FALSY VALUES
<u> falsy values :  (0, '', undefined, null, NaN) </u>


```js
console.log(Boolean(0));           // false
console.log(Boolean(undefined));   // false
console.log(Boolean('Alex'));      // true
console.log(Boolean({}));          // true
```

1. fasly value example
```js
let money = 0;
if (money) {
  console.log(`Don't spend it all`);
} else {
  console.log("You should get a job");  // 0 is falsy value so this code is executed.
}
```

2. fasly value example
```JS
let height;  // undefined
if (height) {
    console.log('Height is defined');
} else {
    console.log('Height is "UNDEFINED"');
}
```

## 3. Equality Operators (==, ===)
```js
let age = 18;
if (age === 18) console.log('You just became an adult.');
```

```js
'18' == 18   // true (use '===' for clean code!!)
'18' === 18  // false
'11' != 11   // false
'11' !== 11  // true
```

```js
let favourite = Number(prompt("what's your favorite number?"));
console.log(favourite);
console.log(typeof favourite);  // string

if (favourite === 23) { // 23 === 23
  console.log('Cool! 23 is amazing number')
} else if (favourite === 7) {
  console.log('7 is also a cool number');
} else {
  console.log('Number is not 23 or 7');
}
```

## 4. Boolean logic 
> (for all programming language)
Boolean variables that can be either TRUE or FALSE
Operators (and(&&), or(||), not(!))

> Logical Operators
- example for true results
```js
true && true    // true (only if all of them are true)
false || false  // false (only if all of them are false)
!true           // false (not operator)
```

## 5. CHALLENGE #3
There are two gymnastics teams: Dolphins and Koalas. They compete against each other 3 times. The winner with the highest average score wins a trophy!

Your tasks:

1. Calculate the average score for each team, using the test data included below. 

The average score for Dolphins should be assigned to the scoreDolphins variable, and the average score of Koalas should be assigned to the scoreKoalas variable.

2. Compare the team's average scores to determine the winner of the competition, and print to the console:

"Dolphins win the trophy" if Dolphins win, or

"Koalas win the trophy" if Koalas win, or

"Both win the trophy" if their average scores are equal.

TEST DATA: Dolphins scored 96, 108, and 89. Koalas scored 88, 91, and 110.

```js
let scoreDolphins = ((96 + 108+ 89)/ 3);
let scoreKoalas = ((88 + 91 + 110)/ 3);

if (scoreDolphins > scoreKoalas) {
    console.log("Dolphins win the trophy🏆");
} else if (scoreDolphins < scoreKoalas) {
    console.log("koalas win the trophy🏆");
} else {
    console.log("Both win the trophy🏆");
}
```

## 6. The Switch Statement
```js
let day ='monday';

switch(day) {
  case 'monday' :  // day === 'monday'
    console.log('Plan course structure');
    console.log('Go to coding meetup');
    break;
  case 'tuesday' :
    console.log('Prepare theory videos');
    break;
  case 'wednesday' :
  case 'thursday' :
    console.log('Write code examples');
    break;
  case 'friday' :
    console.log('Record videos');
    break;
  case 'saturday' :
  case 'sunday' : 
    console.log('Enjoy the weekend😊');
    break;
  default:
    console.log('Not a valid day!');
}
```

- Let's use if statement instead of the switch statement 
```js
let day = 'monday';

if (day === 'monday') {
    console.log('Plan course structure');
    console.log('Go to coding meetup');
} else if (day === 'tuesday') {
    console.log('Prepare theory videos');
} else if (day === 'wednesday' || day === 'thursday') {
    console.log('Write code examples');
} else if (day === 'friday') {
    console.log('Record videos');
} else if (day === 'saturday' || day === 'sunday') {
    console.log('Enjoy the weekend😊');
} else {
    console.log('Not a valid day!');
}
```

> Actually nowadays the switch statement isn't used as often, but you should know it.

## 7. Statement And Expression

- Statement : It tells the computer what to do

```js
let message = '안녕하세요';
```

- Expression : It represents something and evaluates to a value

```js
let num = 5;
num
```

> As an example we can't put Statement inside ${}
```js
console.log(`I'm ${no statement})
``` 

## 8. The Conditonal (Ternary) Operator
if -> ? , else -> :

```js
let age = 23;
age >= 18 ? console.log('I like to drink wine🍷') :
console.log('I like to drink water💧');
```

- Let's make it simpler

```js
let age = 23;
let drink = age >= 18 ? 'wine🍷' : 'water💧';
console.log(drink);
```

> But we can use Ternary Operator inside ${}
```js
let age = 21;
let drink = age >= 18 ? 'wine🍷' : 'water💧';
console.log(`I like to drink ${ age >= 18 ? 'wine🍷' : 'water💧'}`);
```

## 9. CHALLENGE #4
Steven needs a very simple tip calculator for whenever he goes to eat in a restaurant. In his country, it's usual to tip 15% if the bill value is between 50 and 300. If the value is different, the tip is 20%.

Your tasks:

Calculate the tip, depending on the bill value. Create a variable called tip for this. It's not allowed to use an if...else statement (if it's easier for you, you can start with an if...else statement, and then try to convert it to a ternary operator).

Print a string to the console containing the bill value, the tip, and the final value (bill + tip).

Example: The bill was 275, the tip was 41.25, and the total value 316.25.

Note: Use the values of the bill and tip variables to construct this string. Don't hard-code them 🙂

TEST DATA: Test with different bill values: 275, 40, and 430

HINT: To calculate 20% of a value, simply multiply it by 20/100 = 0.2

HINT 2: Value X is between 50 and 300, if it's >= 50 && <= 300 😉



```js
let bill = 275;
let tip = bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;
console.log(`The bill was ${bill}, the tip was ${tip}, and the total value ${bill + tip}`)
```

## 10. Javascript Relase: ES5, ES6+ and ESNEXT
1. Netscape vs Microsoft 
2. Became EcmaScript
3. 2015 : Js received its most significant language update ever! (ES6+)
4. And it continues to update every single year (ESNEXT)

> Old features are never removed because they Don't Break the web.
---