# Atomic object in JS -- Atomics
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

     k: key indicated the index for insertion of the array arr.

     v: value of the corresponding key. The value v will be inserted into the array arr.

     arr: The specified array.

#### Return value
     The old array arr.

#### Ref
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Atomics/add

### Atomic.and()
#### intro

Evaluate them with bitwise and operation for the value which corresponds to the key k and the given value

, then writes the result back to the value which corresponds to the key k in the specified array arr.

#### Parameters
    Atomics.and(arr,k,v)

where

     k: key that indiciate the index for the first operand.

     v: value of second operand. 

     arr: The specified array.

Here, I use regular expression to express the evaluation of this method.

     <old_value> := v
     
     <first_operand> := arr[k]
     
     <second_oeprand> := v
     
     <new_value> := <first_operand> & <second_oeprand>
     
     <return_value> := <old_value>
     
     arr[k] := <first_operand>
     
     
     & represents bitwise AND
     
#### Return value
     The old array arr.

#### Ref
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Atomics/and

### Atomics.load()
#### intro
    It returns the corresponding value of the specified index idx.
#### Parameters
    Atomics.load(arr, idx)
    
where 
   
     arr : the specified array arr.
     
     index : the index idx indiciates to return the corresponding value.
     
#### Return value
     The corresponding value of the index idx in the array arr.
     
     <return_value> := arr[idx]
       
#### Ref

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Atomics/load

### Atomics.or()
#### intro

Evaluate them with bitwise and operation for the value which corresponds to the key k and the given value

, then writes the result back to the value which corresponds to the key k in the specified array arr.

#### Parameters
    Atomics.and(arr,k,v)

where

     k: key that indiciate the index for the first operand.

     v: value of second operand. 

     arr: The specified array.

Here, I use regular expression to express the evaluation of this method.

     <old_value> := v
     
     <first_operand> := arr[k]
     
     <second_oeprand> := v
     
     <new_value> := <first_operand> /| <second_oeprand>
     
     <return_value> := <old_value>
     
     arr[k] := <first_operand>
     
     / is the espace letter.
     
     | represents bitwise OR.
     
#### Return value
     The old array arr.
     
#### Ref
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Atomics/or

### Atomics.store()
#### intro
It stores a given value at the given position in the array and returns that value.

#### Parameter
    Atomics.store(arr,k,v)
 
where 
    
    arr : the specified arr.
    
    k : the key k indiciate the position to store.
    
    v : the value v will be stored.
   
#### Return value
  
     Return value v.
  
#### Ref
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Atomics/store

### Atomics.wait()
#### intro
It sleeps, awaiting a wake-up notification or times out iff it is true that given position in an Int32Array still contains a given value.

#### Note
This operation only works with a shared Int32Array or BigInt64Array and may not be allowed on the main thread. 

For a non-blocking, asynchronous version of this method, see Atomics.waitAsync().

### Syntax

    Atomics.wait(typedArray, index, value)
    Atomics.wait(typedArray, index, value, timeout)

#### Parameter
    typedArray : A specified array it should be either shared Int32Array or BigInt64Array.
    
    index : The position in the typedArray to wait on.
    
    value : The expected value to test. 
    
    timeout : time to wait in milliseconds. It is assume to positive infinity, if it is specified. 
    
    That means, it will wait forever unless the wake-up notification is recieved.
    
#### Ref
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Atomics/wait
    
    
## Ref
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Atomics


