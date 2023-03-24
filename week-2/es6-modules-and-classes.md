## Importing and Exporting Modules

Importing and exporting modules is a feature in JavaScript that allows you to organize your code into reusable modules that can be shared between files and projects. It was introduced in ES6 (ECMAScript 2015) and provides a more modular and scalable approach to programming.

### **Exporting Modules**

To export a module in JavaScript, you use the **`export`** keyword followed by the name of the variable, function, or class that you want to export. Here's an example:

```

// myModule.js
export const myVariable = 42;

export function myFunction() {
  console.log('Hello, world!');
}

export class MyClass {
  constructor(name) {
    this.name = name;
  }

  sayHello() {
    console.log(`Hello, ${this.name}!`);
  }
}

```

In this example, we define a module **`myModule`** that exports a constant **`myVariable`**, a function **`myFunction`**, and a class **`MyClass`**. To use these exports in another module, we need to import them.

### **Importing Modules**

To import a module in JavaScript, you use the **`import`** keyword followed by the path to the module file and the names of the exports that you want to use. Here's an example:

```

// index.js
import { myVariable, myFunction, MyClass } from './myModule.js';

console.log(myVariable); // Output: 42

myFunction(); // Output: Hello, world!

const myObject = new MyClass('John');
myObject.sayHello(); // Output: Hello, John!

```

In this example, we import the exports from the **`myModule`** module using their names. We then use these exports in our **`index`** module to log the value of **`myVariable`**, call the **`myFunction`** function, and create an instance of the **`MyClass`** class.

**Quizzes**

1. Define a module named **`math`** that exports a function called **`add`** that takes two parameters and returns their sum.

2. Define a module named **`utils`** that exports a constant called **`PI`** with the value **`3.14159`** and a function called **`square`** that takes a parameter and returns its square.

3. Import the **`add`** function from the **`math`** module and use it to calculate the sum of **`5`** and **`10`**.

4. Import the **`PI`** constant and the **`square`** function from the **`utils`** module and use them to calculate the area of a circle with a radius of **`5`**.

# Classes and Inheritance

### **Classes**

A class in JavaScript is a blueprint for creating objects with similar properties and behaviors. It provides a way to define the structure of an object, including its instance variables and methods.

To define a class in JavaScript, you use the **`class`** keyword followed by the name of the class and a set of curly braces that contain the class definition. Here's an example:

```
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  sayHello() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}

```

In this example, we define a **`Person`** class that has a constructor that takes a **`name`** and an **`age`** parameter and sets them as instance variables. We also define a **`sayHello`** method that logs a greeting to the console.

### **Inheritance**

Inheritance is a way to create new classes that are based on existing classes. It allows you to reuse code and create a hierarchy of classes that share common properties and behaviors.

To create a subclass in JavaScript, you use the **`extends`** keyword followed by the name of the class that you want to inherit from. Here's an example:

```
class Student extends Person {
  constructor(name, age, grade) {
    super(name, age);
    this.grade = grade;
  }

  sayHello() {
    console.log(`Hello, my name is ${this.name}, I am ${this.age} years old, and I am in grade ${this.grade}.`);
  }
}

```

In this example, we define a **`Student`** class that extends the **`Person`** class. We add a **`grade`** instance variable and a new **`sayHello`** method that includes the student's grade.

When you create an instance of the **`Student`** class, it will have access to all the instance variables and methods of the **`Person`** class, as well as its own instance variables and methods.

```
const person = new Person('John', 30);
person.sayHello(); // Output: Hello, my name is John and I am 30 years old.

const student = new Student('Jane', 15, 10);
student.sayHello(); // Output: Hello, my name is Jane, I am 15 years old, and I am in grade 10.

```

Overall, classes and inheritance provide a way to create complex and reusable code structures in JavaScript that are easy to understand and maintain.

# Quizzes

1. Define a class called **`Animal`** that has a constructor that takes a **`name`** parameter and sets it as an instance variable. Add a method called **`speak`** that logs the string **`'I am an animal'`** to the console.

2. Define a class called **`Dog`** that extends the **`Animal`** class. Add a method called **`speak`** that logs the string **`'Woof!'`** to the console.

3. Create an instance of the **`Animal`** class and call its **`speak`** method.

4. Create an instance of the **`Dog`** class and call its **`speak`** method.

5. Define a class called **`Cat`** that extends the **`Animal`** class. Add a method called **`speak`** that logs the string **`'Meow!'`** to the console.

6. Create an array of **`Animal`** instances that includes a **`Dog`** and a **`Cat`** instance. Loop over the array and call the **`speak`** method on each instance.
