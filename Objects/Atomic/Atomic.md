# Atomic object in JS
## Prequisite
1. basic syntax of JS.
2. basic concept of OOP.
3. basic concept of static class.
4. All prequisites in my notes (such as atomic operation).



## Recall
1. Atomic operation

Atomic operation can NOT be interrupted so that it is ensured to execute the whole operation.

It can prevent the data race condition.

## Feature
1. Static class
 
        Since it is a static class, we can NOT instantiate it.
        
        We to have to invoke such as 
        
        Atomic.Add(); 
        
        rather than x=new Atomic(); x.Add(); 

## Static methods

1. Atomics.add()

2. Atomics.and()

### Atomics.add()

#### intro
Add a new key (, or said, index) k and its corresponding value v into the array arr, then returning the old array.

#### Parameters
Atomics.add(k,v,arr)

where

k: key that will be insert into the array arr.

v: value of the corresponding key.

arr: The specified array.

#### Return value
The old array arr.










