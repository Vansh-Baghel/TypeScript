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

### Type alliases
* We can't store the datatypes in custom name (like variable) by using **type** keyword in place of let, var. 
* With this we can use that name anywhere we want which looks clean. 

### Function types
* We can also use **Function** in place of datatype for any variable or object. 
* Using Function limits us to just the name of function,we can also pass parameters with datatypes. 
* The syntax is to use () which will contain any random name for parameter with datatype and **arrow function** which will have value of the output ka datatype. 
* Using **void** as the output datatype states that function will not **return** any value 

### unknown type
* If we are not sure and want to add any datatype in future, we can use **unknown** type and can check and then write proper datatype after knowing. 

## tsc --init
* This command allows us to view the resources of TS file

### sourceMap
* This lets us get the TS file in inspect .

### outDir and rootDir

* Any newly added files will automatically go in the outDit folder which we might not need everytime.
* **outDir** allows us to specify an external folder for all the JS files
* **rootDir** allows us to mention that the newly added files must nit move to outzDir automatically.

### removeComment
* It doesnt add comment in JS file whenever we added comment in TS file.

### noEmit
* Whenever we dont want the output of TS file in JS file, we use this.
* We can use this whenever we just want to see the output.

### Debuhg in chrome
* We can start debugging in chrome.
* For that , turn sourceMap on. Mark a breakpoint, start debug and select chrome.
* This will help us to use chrome for debugging snd it will take us to the point where that event happened.

### strictNullCheck
* We have to put **!** after using any element from HTML because strict doesnt read the HTML elements.
* Another way is to put the code inside **if** statement with the condition of the variable name which stores that querySelector.
* By putting exclamation mark we say the compiler that we know that this thing exists becuase compiler just see the page code.

# Chp 5 :- Class


## Inheritance
* By using **extends** keyword we can use any object inside another object and it will also inherite all the values of it.
* By using **super** we can have access to the parent class ka constructor.

## Functions/ Methods
* We describe the type of parameter inside the brackets itself, unlike classes where we describe in curly braces.

## Static method imp point
* Cannot use **this** keyword for static methods , we have to specify the className even if that static method is used inside the class itself.

## Abstract Method
* Whenever there is a common method inside a class and we dont want the inherited class to use the exact same method (we need small changes) then we use abstract.
* This doesnt let that method to be inherited , instead we can define it in the class which inherited it.
* It returns the void value, and behave like functions.

## Public, Private and Protected
* These are the terms which we use to control the scope of certain **type** ie which we provide in curly braces to be on safer side.
* **Public** is type of global type.
* **Private** is block scope type.
* **Protected** is too block scope type but the inherited class can also have access to it.
* This lets us to avoid defining the type everywhere.

# Chp 6
## Intersection Types
* We can define more than one inheritance by separating them using **, (comma)**.
* We can describe more than one **type alliase** by separating them with **& (AND operator)** or **| (OR operator)**.
 
## Guards
* If we are using **intersection types** then there is a scenario where some variables/methods represent in one and absent in another simultaneously, then this concept come in.
* We use **in** keyword in **if** condition where we specify the **method name** with the **type** name.

## Type Casting
* Manier times certain property of HTML is not read by the TS file, we need to specify that  property belongs to HTMLthe.
* We use open and close tab and in between we specify it like */<HTMLinputElement/>document.que...* or we use **as** keyword like document.que..() as HTMLinputElement.
 
 ## Function overloading
 * We can specify more than one type on the same function with the output type too.
 * Same function names with different parameters and types, basically including more than one type for same function parameters.
 
 # Chp 7 :- Generics
 
 * It provides better **type** description for **arrays in function & promises**.
 * In **array**, we specify the type using square brackets like **string[]** but we can also specify it using **Array/<string/>** which sometimes is not sufficient. 
 * We don't know the type, and if we use *any* then after creating the variable still the type shown will be any . We want the type to be shown which is specified and also to set as any while assigning it, here generic comes into play. 
 * We can also create generic functions. 

## Creating Generic Function
* While describing objects, we couldn't call it like **function abc(x: object, y:object)** because in this we couldn't describe the type property for the output and input. 
* We need to use generic function by open-close brackets and using **T or U** for the type. 
* This **T or U** will tell that the output will be the intersection,and also the value while calling the function will be of any type. 
* We can also use **extends** to specify the types and can also use opertors for more types. 

## Generic VS union types
* Union is like saying to use anyone of the specified types , and generic is like to use the only one which is specified. 
 * Generic type must be used when we need whole function to have types from  some specified ones. 
 * Union type must be used when we need any of the types throughout the function , like it can keep changing. 

# Chp 8 :- Decorators
> To use decorators, adjust the config. json file and turn **experimentalDecorators** as true. 
> To call decorators, we use **@**.

## Decorator Factory
* Here we use and return a new function inside a function. 
* While calling the decorator, we can pass values as argument's values if use decorator factory. 
