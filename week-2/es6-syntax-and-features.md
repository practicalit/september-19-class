## ES6 Syntax and Features

### **`let and const`**

In ECMAScript 6 (ES6), **`let`** and **`const`** are two new ways to declare variables, introduced as an improvement over the traditional **`var`** keyword.

**`let`**: The **`let`** keyword allows you to declare variables with block scope, which means that the variables declared with **`let`** are limited in scope to the block, statement, or expression in which they are used. This helps prevent unintended side effects caused by variable hoisting and reduces the chance of accidentally overwriting variables in the global scope.

Example:

```
if (true) {
  let x = 10;
}
console.log(x); // ReferenceError: x is not defined, because x is limited to the scope of the if block

```

**`const`**: The **`const`** keyword is used to declare variables that should not be reassigned after their initial declaration. Like **`let`**, **`const`** also has block scope. The main difference is that **`const`** variables must be initialized with a value when they are declared, and their value cannot be changed afterwards.

Example:

```
const PI = 3.14159;
PI = 3.14; // TypeError: Assignment to constant variable, because PI is a constant and cannot be reassigned

```

In summary, **`let`** and **`const`** are more modern and safer ways to declare variables in JavaScript compared to **`var`**. It is recommended to use **`let`** when you need to declare variables with block scope that will change over time, and **`const`** when you need to declare variables that should not be changed after their initial declaration.

**Example 1:**

```
function exampleLet() {
  for (let i = 0; i < 5; i++) {
    setTimeout(() => console.log(i), i * 1000);
  }
}

exampleLet();

```

In this example, **`let`** is used to declare a loop counter **`i`**. Since **`let`** has block scope, each iteration of the loop has its own separate **`i`** variable. This means that when the **`setTimeout`** function executes, it logs the correct value of **`i`** for each iteration.

**Quiz 1:**

Rewrite the function above, replacing **`let`** with **`var`**. What will be the output, and why?

**Example 2:**

```
const user = {
  firstName: "John",
  lastName: "Doe",
};

user.firstName = "Jane";
console.log(user.firstName); // Output: "Jane"

```

In this example, the **`const`** keyword is used to declare a constant **`user`** object. Although the **`user`** variable itself cannot be reassigned, its properties can be modified.

**Quiz 2:**

Can you make the **`user`** object immutable so that its properties cannot be changed after the initial declaration? (Hint: You can use **`Object.freeze`** method)

**Example 3:**

```
function calculateArea(width, height) {
  const area = width * height;
  return area;
}

console.log(calculateArea(5, 10)); // Output: 50

```

In this example, the **`const`** keyword is used to declare the **`area`** variable. Since the **`area`** value does not change after its initial calculation, it's appropriate to use **`const`**.

**Quiz 3:**

What happens if you try to reassign the **`area`** variable to a new value inside the function? What error message will be displayed?
