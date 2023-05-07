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

## Ref
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Atomics










