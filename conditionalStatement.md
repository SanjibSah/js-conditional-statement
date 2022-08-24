# Introduction to the JavaScript if statement

The if statement executes block if a condition is true. The following shows the syntax of the if statement:

```JavaScript
if(condition)
    statement;
```
The condition can be a value or an expression. Typically, the condition evaluates to a Boolean value, which is true or false.

If the condition evaluates to true, the if statement executes the statement. Otherwise, the if statement passes the control to the next statement after it.

If the condition evaluates to a non-Boolean value, JavaScript implicitly converts its result to a Boolean value by calling the Boolean() function.

If you have more than one statement to execute, you need to use wrap them in a block using a pair of curly braces as follows:

```JavaScript
if(condition){
    // statements to execute
}
```
However, it’s a good practice to always use curly braces with the if statement. By doing this, you make your code easier to maintain and avoid possible mistakes.

## JavaScript if statement examples

The following example uses the if statement to check if the age is equal to or greater than 18:

```JavaScript
const age = 18;
if (age >= 18) {
  console.log('You can sign up');
}
// Yoy can sign up
```
__How it works.__
First, declare and initialize the variable age to 18: 

```JavaScript
const age =18;
```
Second, check if the age is greater or equal to 18 using the if statement. Because the expression age >= 18 is true, the code inside the if statement executes that outputs a message to the console:

```JavaScript
if (age >= 18) {
  console.log('You can sign up');
}
```
The following example also uses the if statement. However, the age is 16 which causes the condition to evaluate to false. Therefore, you won’t see any message in the output:

```JavaScript
let age = 16;
if (age >= 18) {
  console.log('You can sign up');
}
```
## Nested if statement

It’s possible to use an if statement inside another if statement. For example:

```JavaScript
let age = 16;
let state = 'CA';

if (state == 'CA') {
  if (age >= 16) {
    console.log('You can drive.');
  }
}
// You can drive.
```
__How it works.__

First, declare and initialize the age and state variables:

```JavaScript
let age = 16;
let state = 'CA';
```
Second, check if the state is 'CA' using an if statement. If yes, check if the age is greater than 16 using a nested if statement and output a message to the console:

```JavaScript
if (state == 'CA') {
  if (age == 16) {
    console.log('You can drive.');
  }
}
```
In practice, you should avoid using nested if statements as much as possible. For example, you can use the && operator to combine the conditions and use an if statements as follows:

```JavaScript
let age = 16;
let state = 'CA';

if (state == 'CA' && age == 16) {
  console.log('You can drive.');
}
```
# Introduction to the JavaScript if…else statement

The if statement executes a block if a condition is true. When the condition is false, it does nothing. But if you want to execute a statement if the condition is false, you can use an if...else statement.

The following shows the syntax of the if...else statement:

```JavaScript
if( condition ) {
  // ...
} else { 
  // ...
}
```
In this syntax, the condition is a value or an expression that evaluates to true or false. If the condition is true, the if...else statement executes the block that follows the if branch.

If the condition is false, the if...else statement executes the block that follows the else branch.

Typically, the condition evaluates to a boolean value, which is true or false. However, if it evaluates to a non-boolean value, the if...else statement will convert it to the boolean value.

## JavaScript if…else statement examples

The following example uses the if...else statement to check if the age is greater than or equal to 18:
```JavaScript
let age = 18;

if (age >= 18) {
  console.log('You can sign up.');
} else {
  console.log('You must be at least 18 to sign up.');
}
```
In this example, the age is 18. Therefore, the expression age >= 18 is true. Hence, you’ll see the following message in the console:

```JavaScript
You can sign up.
```
The following example is the same as above except that the age is 16 instead of 18:

```JavaScript
let age = 16;

if (age >= 18) {
  console.log('You can sign up.');
} else {
  console.log('You must be at least 18 to sign up.');
}
// You must be at least 18 to sign up.
```
In this example, the age is 16. Therefore, the expression age >= 18 evaluates to false. Hence, the statement in the else branch executes that output the message to the console.

The following example uses a logical operator AND (&&) as the condition in the if block:

```JavaScript
let age = 16;
let country = 'Nepal';

if (age >= 16 && country === 'Nepal') {
  console.log('You can get a driving license.');
} else {
  console.log('You are not eligible to get a driving license.');
}

```
Because the age is 16 and the country is the Nepal, the following expression returns true.

# Introduction to the JavaScript if else if statement

The if an if…else statements accept a single condition and execute the if or else block accordingly based on the condition.

To check multiple conditions and execute the corresponding block if a condition is true, you use the if...else...if statement like this:

```JavaScript
if (condition1) {
  // ...
} else if (condition2) {
  // ...
} else if (condition3) {
  //...
} else {
  //...
}
```
In this syntax, the if...else...if statement has three conditions. In theory, you can have as many conditions as you want to, where each else...if branch has a condition.

The if...else...if statement checks the conditions from top to bottom and executes the corresponding block if the condition is true.

The if...else...if statement stops evaluating the remaining conditions as soon as a condition is true. For example, if the condition2 is true, the if...else...if statement won’t evaluate the condition3.

If all the conditions are false, the if...else...if statement executes the block in the else branch.

## JavaScript if else if examples

The following example uses the if...else...if statement to get the month name from a month number:

```JavaScript
let month = 6;
let monthName;

if (month == 1) {
  monthName = 'Jan';
} else if (month == 2) {
  monthName = 'Feb';
} else if (month == 3) {
  monthName = 'Mar';
} else if (month == 4) {
  monthName = 'Apr';
} else if (month == 5) {
  monthName = 'May';
} else if (month == 6) {
  monthName = 'Jun';
} else if (month == 7) {
  monthName = 'Jul';
} else if (month == 8) {
  monthName = 'Aug';
} else if (month == 9) {
  monthName = 'Sep';
} else if (month == 10) {
  monthName = 'Oct';
} else if (month == 11) {
  monthName = 'Nov';
} else if (month == 12) {
  monthName = 'Dec';
} else {
  monthName = 'Invalid month';
}
console.log(monthName);
// Jun
```
In this example, we compare the month with 12 numbers from 1 to 12 and assign the corresponding month name to the monthName variable.

Since the month is 6, the expression month==6 evaluates to true. Therefore, the if...else...if statement assigns the literal string 'Jun' to the monthName variable. Therefore, you see Jun in the console.

If you change the month to a number that is not between 1 and 12, you’ll see the Invalid Month in the console because the else clause will execute.

__Using JavaScript if…else…if statement to calculate the body mass index__

The following example calculates a body mass index (BMI) of a person. It uses the if...else...if statement to determine the weight status based on the BMI:

```JavaScript
let weight = 70; // kg
let height = 1.72; // meter

// calculate the body mass index (BMI)
let bmi = weight / (height * height);

let weightStatus;

if (bmi < 18.5) {
  weightStatus = 'Underweight';
} else if (bmi >= 18.5 && bmi <= 24.9) {
  weightStatus = 'Healthy Weight';
} else if (bmi >= 25 && bmi <= 29.9) {
  weightStatus = 'Overweight';
} else {
  weightStatus = 'Obesity';
}

console.log(weightStatus);
// Healthy Weight
```
__How it works.__

- First, declare two variables that hold the weight in kilogram and height in meter. In a realworld application, you’ll get these values from a web form.

- Second, calculate the body mass index by dividing the weight by the square of the height.

- Third, determine the weight status based on the BMI using the if...else..if statement.

- Finally, output the weight status to the console.

# Introduction to JavaScript ternary operator

When you want to execute a block if a condition evaluates to true, you often use an if…else statement. In this example, we show a message that a person can drive if the age is greater than or equal to 16. Alternatively, you can use a ternary operator instead of the if-else statement like this:

```JavaScript
let age = 18;
let message;

age>=16 ? (message:'You can drive') : (message:'You cannot drive.');
console.log(message);
```
Or you can use the ternary operator in an expression as follows:

```JavaScript
let age =18;
let message;
message=age>=16?'You can drive.':'You cannot drive.';
console.log(message);
```
Here’s the syntax of the ternary operator:

```JavaScript
condition ? expressionIfTrue : expressionIfFalse;
```
In this syntax, the condition is an expression that evaluates to a Boolean value, either true or false.

If the condition is true, the first expression (expresionIfTrue) executes. If it is false, the second expression (expressionIfFalse) executes.

The following shows the syntax of the ternary operator used in an expression:

```JavaScript
let variableName = condition ? expressionIfTrue : expressionIfFalse;
```
In this syntax, if the condition is true, the variableName will take the result of the first expression (expressionIfTrue) or expressionIfFalse otherwise.

## JavaScript ternary operator examples

__Using the JavaScript ternary operator to perform multiple statements__

The following example uses the ternary operator to perform multiple operations, where each operation is separated by a comma. For example:
```JavaScript
let authenticated = true;
let nextURL = authenticated
  ? (alert('You will redirect to admin area'), '/admin')
  : (alert('Access denied'), '/403');

// redirect to nextURL here
console.log(nextURL); // '/admin'
```
In this example, the returned value of the ternary operator is the last value in the comma-separated list.

__Simplifying ternary operator example__
See the following example:

```JavaScript
let locked = 1;
let canChange = locked != 1 ? true : false;
```
If the locked is 1, then the canChange variable is set to false, otherwise, it is set to true. In this case, you can simplify it by using a Boolean expression as follows:

```JavaScript
let locked = 1;
let canChange = locked != 1;
```
__Using multiple JavaScript ternary operators example__

The following example shows how to use two ternary operators in the same expression:
```JavaScript
let speed = 90;
let message = speed >= 120 ? 'Too Fast' : speed >= 80 ? 'Fast' : 'OK';

console.log(message);
// Fast
```
It’s a good practice to use the ternary operator when it makes the code easier to read. If the logic contains many if...else statements, you should avoid using the ternary operators.

# Introduction to the JavaScript switch case statement

The switch statement evaluates an expression, compares its result with case values, and executes the statement associated with the matching case value.

The following illustrates the syntax of the switch statement:

```JavaScript
switch (expression) {
    case value1:
        statement1;
        break;
    case value2:
        statement2;
        break;
    case value3:
        statement3;
        break;
    default:
        statement;
}
```
__How it works.__

- First, evaluate the expression inside the parentheses after the switch keyword.

- Second, compare the result of the expression with the value1, value2, … in the case branches from top to bottom. The switch statement uses the strict comparison (===).

- Third, execute the statement in the case branch where the result of the expression equals the value that follows the case keyword. The break statement exits the switch statement. If you skip the break statement, the code execution falls through the original case branch into the next one. If the result of the expression does not strictly equal to any value, the switch statement will execute the statement in the default branch.

That the switch statement will stop comparing the expression‘s result with the remaining case values as long as it finds a match.

The switch statement is like the if…else…if statement. But it has more readable syntax.

In practice, you often use a switch statement to replace a complex if...else...if statement to make the code more readable.

Technically, the switch statement is equivalent to the following  if...else...if statement:

__Using JavaScript switch statement to get the day of the week__

The following example uses the switch statement to get the day of the week based on a day number:
```JavaScript
let day = 3;
let dayName;

switch (day) {
  case 1:
    dayName = 'Sunday';
    break;
  case 2:
    dayName = 'Monday';
    break;
  case 3:
    dayName = 'Tuesday';
    break;
  case 4:
    dayName = 'Wednesday';
    break;
  case 5:
    dayName = 'Thursday';
    break;
  case 6:
    dayName = 'Friday';
    break;
  case 7:
    dayName = 'Saturday';
    break;
  default:
    dayName = 'Invalid day';
}

console.log(dayName); // Tuesday

```
__How it works.__

First, declare the day variable that holds the day number and the day name variable (dayName).

Second, get the day of the week based on the day number using the switch statement. If the day is 1, the day of the week is Sunday. If the day is 2, the day of the week is Monday, and so on.

Third, output the day of the week to the console.

# Introduction to the JavaScript for loop statement

The for loop statement creates a loop with three optional expressions. The following illustrates the syntax of the for loop statement:

```JavaScript
for (initializer; condition; iterator) {
    // statements
}
```
# Introduction to the JavaScript for loop statement

The for loop statement creates a loop with three optional expressions. The following illustrates the syntax of the for loop statement:

```JavaScript
for (initializer; condition; iterator) {
    // statements
}
```
1. initializer

    The for statement executes the initializer only once the loop starts. Typically, you declare and initialize a local loop variable in the initializer.

2. condition

    The condition is a boolean expression that determines whether the for should execute the next iteration.

    The for statement evaluates the condition before each iteration. If the condition is true (or is not present), it executes the next iteration. Otherwise, it’ll end the loop.

3. iterator

    The for statement executes the iterator after each iteration.

In the for loop, the three expressions are optional. The following shows the for loop without any expressions:


```JavaScript
for ( ; ; ) {
   // statements
}
```
__JavaScript for loop examples__


```JavaScript
for (let i = 1; i < 5; i++) {
  console.log(i);
}

```
Output

```JavaScript
1
2
3
4
```

__How it works__

- First, declare a variable  counter and initialize it to 1.

- Second, display the value of counter in the console if counter is less than 5.

- Third, increase the value of counter by one in each iteration of the loop.