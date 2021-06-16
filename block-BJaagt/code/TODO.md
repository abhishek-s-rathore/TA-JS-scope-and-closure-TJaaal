Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = "Arya";
}
console.log(username); // output
```

In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.

The above code will throw an error `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = "Arya";
}
console.log(username); // output
```

`const` create a block scope.
In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside the `block` and we can't access the `const` defined inside a block from outside.

The above code will throw an error `Reference Error username is not defined`.

3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = "Arya";
}
console.log(username); // output
```

`let` create a block scope.
In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside the `block` and we can't access the `let` defined inside a block from outside.

The above code will throw an error `Reference Error username is not defined`.

4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = "Arya";
}
console.log(username); // Arya
```

Var never form a lock scope thus we will get output.
Output is `Arya.

5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
if (true) {
  var username = "Arya";
  I;
}
console.log(useranme); // output
```

The above code will throw an error `Syntax Error Identifier username is already defined`.

6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
if (true) {
  let username = "Arya";
}
console.log(useranme); // John
```

Output will be according to Global scope.
Output is `John`.

7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
function sayHello() {
  let username = "Arya";
}
sayHello();
console.log(username); // John
```

Output will be according to Global scope.
Output is `John`

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
  console.log(i, "First");
  // Output
  // 0 "First"
  //  1 "First"
  //  2 "First"
  //  3 "First"
  //  4 "First"
  //  5 "First"
  //  6 "First"
  //  7 "First"
  //  8 "First"
  //  9 "First"
}
console.log(i, "Second");
// Output
//  10 "Second"
```

`var` will not create block scope.
Thus `i= 10` will be displayed as output along with `Second`.
Output is
`1 "First" 2 "First" 3 "First" 4 "First" 5 "First" 6 "First" 7 "First" 8 "First" 9 "First" 10 "Second`

9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, "First");
  // output
  // 0 "First"
  // 1 "First"
  // 2 "First"
  // 3 "First"
  // 4 "First"
  // 5 "First"
  // 6 "First"
  // 7 "First"
  // 8 "First"
  // 9 "First"
}
console.log(i, "Second");
// output
// Undefined
```

`let` will create block scope.

Output is
0 "First"
1 "First"
2 "First"
3 "First"
4 "First"
5 "First"
6 "First"
7 "First"
8 "First"
9 "First"
`