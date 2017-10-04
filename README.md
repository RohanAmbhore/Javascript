# Javascript
Interview preparation for Javascript
Object Oreinted Programming in Javascript
------
### 1.) Polymorphism

```// Animal methods
Animal.prototype.talk = function talk() {
  console.log('?')
}

// ------------------------------
// Bird "class"
function Bird() {
  // if you want to call the parent constructor, you can do that here
  // Animal.call(this, arg1, arg2, ... argN)
}

// Bird inherits from Animal
Bird.prototype = Object.create(Animal.prototype)
Bird.prototype.constructor = Bird

// Bird methods
Bird.prototype.talk = function() {
  console.log('tweet tweet')
}
Bird.prototype.fly = function() {
  console.log('flap flap')
}

// ------------------------------
// Parrot "class"
function Parrot() {
  // if you want to call the parent constructor, you can do that here
  // Bird.call(this, arg1, arg2, ... argN)
}

// Parrot inherits from Bird
Parrot.prototype = Object.create(Bird.prototype)
Parrot.prototype.constructor = Parrot

// Parrot methods
Parrot.prototype.talk = function() {
  console.log('polly want a cracker')
}

var a = new Animal()
var b = new Bird()
var p = new Parrot()

a.talk()
b.talk()
b.fly()
p.talk()
p.fly()
```


### a.) Method Overloading in Javascript
There are multiple aspects to argument overloading in Javascript:

#### Variable arguments - 
You can pass different sets of arguments (in both type and quantity) and the function will behave in a way that matches the arguments passed to it.
#### Default arguments - 
You can define a default value for an argument if it is not passed.
#### Named arguments - 
Argument order becomes irrelevant and you just name which arguments you want to pass to the function.

Logic for method overloading
```
// method declaration for .data()
 data: function(key, value) {
     if (arguments.length === 0) {
         // .data()
         // no args passed, return all keys/values in an object
     } else if (typeof key === "string") {
         // first arg is a string, look at type of second arg
         if (typeof value !== "undefined") {
             // .data("key", value)
             // set the value for a particular key
         } else {
             // .data("key")
             // retrieve a value for a key
         }
     } else if (typeof key === "object") {
         // .data(object)
         // set all key/value pairs from this object
     } else {
         // unsupported arguments passed
     }
 },
 ```
 <a href="https://stackoverflow.com/questions/10855908/how-to-overload-functions-in-javascript">Clicke here</a>
 
 ### 2.) Abstraction in Javascript
 
 <a href="http://www.yusufaytas.com/achieving-abstraction-in-javascript/">click here</a>
