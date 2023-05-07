# binded objects
## intro
Binded objects are objects that are binded (as the term says).

In JS, by defaults the objects are NOT binded. Thus, the <b>this</b> does NOT refer to the object.

Therefore, in the following example, this will return undefined. And of course, also this.x .

However, if we bind the objects, then this will refer to the objects so that this will NOT be undefined.

## How to in JS
We can bind an object with bind method. Look at the following example.

### Example

      const module = 
      {
        x: 42,
        getX: function() {
          return this.x;
        }
      };

      const unboundGetX = module.getX;
      console.log(unboundGetX()); // The function gets invoked at the global scope
      // Expected output: undefined

      const boundGetX = unboundGetX.bind(module);
      console.log(boundGetX());
      // Expected output: 42

## Ref

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/bind

