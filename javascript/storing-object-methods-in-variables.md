# Storing object methods in variables

The `this` keyword refers to the object that is the context in which the function is called. In JavaScript, storing object methods in variables can have unintended consequences for the meaning of `this`.  
Consider the following code:  
```javascript
var person = {
  firstName : 'Khwilo',
  lastName  : 'Kabaka',
  greet     : function(){
    console.log('Hi, ' + this.firstName );
  }
};

var sayIt = person.greet;

sayIt(); // logs 'Hi, undefined'
```  

When you store the `.greet()` method in a variable `sayIt` and then call `sayIt()`, the context object changes to the global `window` object, not the `person` object. Since the `window` object does not have a property `firstName`, you get `undefined` when you try to access it.  

As a programmer remember that you can force the meaning of `this` to be what you want it to be, using the `.call()` or `.apply()` method on the function itself.  
Example:  
```javascript
var person = {
  firstName : 'Khwilo',
  lastName  : 'Kabaka',
  greet     : function(){
    console.log('Hi, ' + this.firstName);
  }
};

var sayIt = person.greet;

sayIt.call(person); // logs 'Hi, Khwilo'
```  

Both `.call()` and the very similar `.apply()` method allows you to pass arguments to the functions you are invoking.  

Another example with `.call()`:  
```javascript
var person = {
  firstName : 'Khwilo',
  lastName  : 'Kabaka',
  greet     : function(greeting, punctuation){
    console.log(greeting + ', ' + this.firstName + punctuation);
  }
};

var sayIt = person.greet;

sayIt.call(person, 'Hello,', '!!!'); // logs 'Hello,Khwilo!!!'
```  

The same thing can also be done using `.apply()`, but we would pass the arguments within a single array instead of as separate arguments:  

`sayIt.apply(person, ['Hello', '!!!']);`
