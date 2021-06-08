1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// Your code goes here
let calcPercentage = function (marks, total) {
  return (marks * 100) / total;
};

let calcPercentage = (marks, total) => {
  return (marks * 100) / total;
};

let calcPercentage = (marks, total) => (marks * 100) / total;
```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// Function Declaration 
```

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
};

// Function Expression
```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};

// Function Expression
```

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};

// Function Expression
```

```js
let percentage = (marks, total) => (marks * 100) / total;

// Function Expression
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.
ANS:  Function is an object and object is an expression, expressions are those which results in a value, function also do the same, so it is an expression.

```js
let average = (num1, num2, num3)=> (num1+num2+num3)/3;

```

4. Why is a function call an expression in JavaScript?
ANS: When we call any function, it will return any value or undefined which is also a value, so it is called an expression.



5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); // VALID; it will return result 5.

five = add; // VALID; it will return function reference.

five = five(10, 11); // VALID; it will return result 21, since function will assign to variable five .

five = function () {
  return "Hello";
};               //VALID; new function will be assign to the variable five. 
```


6. What is the difference between function definition and function call? Explain with an example.
ANS:In "function definition" we define that how function will perform an in "function call" we call it to perform certain action.

```js
//Function  Definition
function add(a, b) {
  return a + b;  
}
 
// Function Call
add(2, 3);
```

7. What is the similarities between function definition and function call?
ANS: Both are expressions and can be stored in a variable.

8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log("Hello World!");
}

hello.user = "Sam"; // Valid; Because function is an object, it can have any key. 
```

9. What is higher order function explain with an example.
ANS: Higher-order functions are functions that take other functions as arguments or return functions as their results.
```js
function add(sum){
  sum();
}

function add(){
  function sum(num1, num2){ return num1+num2};
}return sum;

```


10. Explain what is callback function. Why you can pass a function inside a function?
ANS: Function which is accepted by a Higher Order Funtion is called Callback Function.
We can pass a function because an argument can be an expression,and function is an expression. 