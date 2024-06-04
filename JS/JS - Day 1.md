# Data Types
### Primitive
	1. String  => any thing in single or double quotes
	2. Number  => negative positive and float any number
	3. Boolean => True or False
	4. Undefinde => declared but not intialized variable
	5. null => Nothing
___
### Non Primitive
	Object

```js
var myvar = 12;
console.log(typeof("this is a string"));

console.log(typeof myvar );
```
___
# Type Coercion

Type coercion refers to the automatic conversion of values from one data type to another, typically performed during operations or comparisons involving different data types.

##  Number To String

```js
var num = 10;
var str = "The answer is " + num;
console.log(str); // "The answer is 10"
```
___
## String To Number

```js
var str = "100";
var num = +str ; //Coercion string to number
console.log(num); //100
```
___
## Comparison Coercion
JavaScript  to automatically tries converted to make them compatible for operations or comparisons.<br>
**Loose equality**: compares only values in case of different data type it tries to convert it.<br>
**Strict Equality :** compares values and datatypes even when the values are equal but in different data types it return false.<br>

Loose Equality `100 == "100"` =>  true<br>
Loose Inequality `10 != "10"` => false<br>
Strict Equality `100 ==="100"` => false<br>
Strict Inequality `100 !== "100"` => true<br>

Falsy values : These values are considered false in comparisons any other values are considered truthy values.
1. false
2. 0
3. null
4. undefined
5. NaN
6. "" or empty string
___
# Type Conversion

Type conversion, also known as type casting, refers to the explicit transformation of a value from one data type to another. It involves intentionally changing the data type of a value using built-in functions or operators provided by the language.
## From String to Number

### Number
```js
var str = "100";
var num = Number(str);
console.log(num); //100 
```
### parseInt
```js
console.log(Number("100")); // 100
console.log(Number("100 ahmed")); //NaN

console.log(parseInt("100")); //100
console.log(parseInt("100 ahmed")); //100

console.log(parseInt("ahmed 100 ahmed")); //NaN
```

### Parse Float
`parseInt(100.55)` => 100<br>
`parseFloat(100.55);` => 100.55<br>

## From number to string
```js
var num =100;
var str = String(num); //"100"
console.log(str);
```

**Resources :** [Coercion and Conversion](https://medium.com/@atuljha2402/understanding-javascript-type-coercion-type-conversion-a2ce84c00331#:~:text=Type%20coercion%20refers%20to%20the,complete%20the%20operation%20or%20comparison.)
___
## Logical Operators
`!  => NOT`<br>
`&& => AND`<br>
`|| => OR`<br>
## Ternary Operator
`condition ? iftrue : ifFalse ;`
___
