# Classes

Classes are a staple of object-oriented programming, and allow coders to create objects with set values and methods. The `class` itself creates the basic values and methods, and you can then make specific `instances` that use unique data.

An important part of classes that carries over to JS classes is `inheritance`. The below example shows that `Coder` is an extension of `Person`, so it inherits everything from it and can add/overwrite other methods too. A common practice is defining a base class that sets up frequent methods, especially ones that talk with an API, and extend different portions of the application off of this. This way developers can quickly scale up new functionality that can interface with the core app.

```javascript
class Person {
  constructor(firstname, lastname) {
    this.firstname = firstname;
    this.lastname = lastname;
  }

  getName() {
    return this.firstname + ' ' + this.lastname;
  }
}

class Coder extends Person {
  getJob() {
    return 'Coder';
  }
}

var me = new ReactDeveloper('Max', 'Antonucci');

console.log(me.getName());
console.log(me.getJob());
```

You'll see classes used this way a lot in JavaScript frameworks like Ember and React.

## Resources

* [JavaScript fundamentals before learning React](https://www.robinwieruch.de/javascript-fundamentals-react-requirements/#react-javascript)
