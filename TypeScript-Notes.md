# Chp 2
## Core types

### Type assignment

* We can use colons after any variable to say the file that we wamt that particular datatype only.
* This will help us to avoid unexpected output, like in adding 2 numbers both must be *numbers* and not *strings*.

### Type Inference
* This assures that any variable does have same datatype.
* If we try to assign different datatype value to that variable , then it'll throw error.

### Types of JS and TS
* TS is static type (fixes during development) and JS is dynamic type (resolved at runtime).


### Object Types
* It shows the key with its datatype in an object if we hover, this will let us know what type of value is present in the key.
* We can also specify the type before value respresentation but its not much used.

### Array Types
* Same as object types, its just for array and when we hover we see the type of value.

### Tuple
* When we have fixed-length of array, then we must use tuple and can specify the datatype before assigning the value. 

### Union Types
* When we want more than one datatype for certain key or parameter, then we can use **|** and mention as many datatypes as we want. 

### Literal Type
* We can specifically mention certain values in combination with **union type** , so if the value matches only then the code will run. 
* For eg, mentioning the string which we'll useuse so any different string won't be allowed. 


