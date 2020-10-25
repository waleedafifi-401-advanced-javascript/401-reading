### Name 3 advantages to Test Driven Development
1. Writing the tests first requires you to really consider what do you want from the code.
1. TDD creates a detailed specification.
1. TDD reduces the time spent on rework.

### In what case would you need to use beforeEach() or afterEach() in a test suite? 
 The behavior I am noticing is that beforeEach and afterEach are run before/after every, it blocks in the current context and all nested contexts.

### What is one downside of Test Driven Development? 
Big-time investment. For the simple case, you lose about 20% of the actual implementation, but for complicated cases, you lose much more.

### What’s the primary difference between ES6 Classes and Constructor/Prototype Classes? 
The most important difference between class- and prototype-based inheritance is that a class defines a type that can be instantiated at runtime, whereas a prototype is itself an object instance.

### Name a use case for a static method
Static methods, like many other features introduced in ES6, are meant to provide class-specific methods for object-oriented programming in Javascript. Static methods in Javascript are similar to class methods in Ruby. To declare a static method, simply prefix a method declaration with the word static inside the class declaration.

```
class Foo(){
   static methodName(){
      console.log("bar")
   }
}
```

### Write an example of a Higher Order function and describe the use case it solves
Higher-order functions allow us to abstract over actions, not just values. They come in several forms. For example, we can have functions that create new functions.

```
function greaterThan(n) {
  return m => m > n;
}
let greaterThan10 = greaterThan(10);
console.log(greaterThan10(11));
// → true
```

**functions that change other functions**

```
function noisy(f) {
  return (...args) => {
    console.log("calling with", args);
    let result = f(...args);
    console.log("called with", args, ", returned", result);
    return result;
  };
}
noisy(Math.min)(3, 2, 1);
// → calling with [3, 2, 1]
// → called with [3, 2, 1] , returned 1
```

### Test Driven Development (TDD): 
Is a software development process that relies on the repetition of a very short development cycle: requirements are turned into very specific test cases, so its an evolutionary approach to development which combines test-first development where you write a test before you write just enough production code to fulfill that test and refactoring.

### this:
The value of this is determined by how a function is called. It can't be set by assignment during execution, and it may be different each time the function is called.

### classes: 
Classes are "special functions", the class syntax has two components: class expressions and class declarations.
- Class declarations
- Class expressions

### OOP:
Object-oriented programming (OOP) refers to a type of computer programming (software design) in which programmers define the data type of a data structure, and also the types of operations (functions) that can be applied to the data structure.

### Objects: 
Are complex and each object may contain any combination of the primitive data-types as well as reference data-types.
And objects in JavaScript may be defined as an unordered collection of related data, of primitive or reference types, in the form of “key: value” pairs.

### Immutable state: 
Immutable data cannot change its structure or the data in it.

### Prototype: 
Is a property can be used to add methods to existing constructors.

