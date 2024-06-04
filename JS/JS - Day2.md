# Functions
## Statement Functions
```js
function add(num1,num2){
	return num1+num2 ;
}
console.log(add(10,20)); // 30
var number1 = 50 ;
var number2 = 100 ;

console.log(add(number1,number2));//150
```

## Expression Functions
```js
var calculator = function(num1,num2){
console.log("sum equals" ,num1+num2);
console.log("multiply equals" ,num1*num2);
console.log("subtraction equals" ,num1-num2);
}

//calling the function
calculator(20,10); //sum equals 30
				   //multiply equals 200
				   //subtraction equals 10
```
___
# Hoisting
JavaScript **Hoisting** refers to the process whereby the interpreter appears to move the declaration of functions, variables, classes, or imports to the top of their scope, prior to execution of the code.
## Variable Hoisting
variable can be used before it has been declared.<br>
But variable Initialization is not hoisted.
```js
x = 5 ;
console.log(x); //5

var x;
```

```js
console.log(x); //x equal UNDEFINED
var x=5;
```

**This is error Don't Use**
```js
console.log(x); //Error X IS UNDEFINED
```

## Function Hoisting
only statement functions are hoisted you can use statement functions before declaration but You can't with expression functions 
```js
add(10,20);//30

function add(a,b){
console.log(a+b);
}
```

**Expression Functions**
```js
add(a,b);//ERROR TypeError: add is not a function

var add =function(a,b){
console.log(a+b);
}
```

___
# Callbacks
A callback is a function passed as an argument to another function.
```js
//This function prints a value in console
function print (value){
console.log(value);
}
function printInDocument(value){
document.writeLn("<h1>Your value is "+value+"<h1>");
}

function add(num1,num2,someFunction){
var sum = num1+num2;
//This is a callback function its passed within the parameter
someFunction(sum);
}

//calling the add function
//this will add the two values then call the print function to print result in console
add(10,20,print);
//this will add the two values then call the printindocument function to print result in your HTML
add(10,20,printInDocument);
```
##### Remember when using callbacks 
**Don't pass Functions Like this** <br>
`add(10,20,print())` => this will cause error<br>

___
# Arrays
## Declaration
```js
var myArray = [];//empty array
var myNums = [1,2,3,4,5,6];
var myNames =["ahmed","salem","mohamed"];
var values =[1,2,"hello",true];

console.log(values[1]); //2
console.log(myNums[0]);//1
```
## Array Length
`myNums.length` =>5

## Add To Array
```js
var arr =[];
arr[2] ="ahmed";
console.log(arr); //[ <2 empty items>, 'ahmed' ]
```

```js
var mynames =["ahmed","mohamed","sayed","salem"];

mynames[6]="ali" ;
//mynames => ["ahmed","mohamed","sayed","salem",2Xempty,"ali"]
```

___
## Array Methods
1. `myarr.push(element)` => Add element to the end of the array
2. `myarr.pop(element)` => Remove element from the end of the array
3. `myarr.shift(element)` =>Remove element from the start of the array
4. `myarr.unshift(element)` =>Add element to the start of the array
5. `myarr.sort()` =>sort the array based on string 
6. `myarr.reverse();` => Reversing an array
7. `myarr.splice(index,number)` =>remove elements from array 
8. `myarr.indexof(element)` => If element exists in array it returns the index of it otherwise returns `-1`
9. `myarr.lastindexof(element)` => If element exists in array but from the last of the array it returns the index of it otherwise returns `-1`
10. `myarr.includes(item)` =>if the item is in the array return `true` else it returns `false`
11. `myarr.slice(startindex,endindex)` =>returns a copy of section of array not including end if didn't provide end index it will slice to the end
12. `myarr.toString()` => Makes all array to one string and separate elements with coma `,`
13. `myarr.join(' ')` => it takes a separator and joins all array
14. `myarr1.concat(myarr2)` => returns an array with joining to arrays together
#### Sort Array
to sort numbers in array it needs specific function `array.sort(compareFunction)`<br>
A function that defines a sort order. The function should return a negative, zero, or positive value, depending on the arguments.

```js
var myNums = [10,2,7,1,0,9];
//sort in ascending order
myNums.sort(function(a,b){return a-b});
console.log(myNums);//[ 0, 1, 2, 7, 9, 10 ]
//sort in descending order
myNums.sort(function(a,b){return b-a});
console.log(myNums);//[ 10, 9, 7, 2, 1, 0 ]

```

___
# String Methods
### Access With Index

```js
let name ="ahmed" ;

console.log(name[1]); //"h"
console.log(name.charAt(1)) //"h"
```
### Length
`name.length` => 5 
### Trim
```js
var name ="    Ahmed ";
console.log(name.trim());//remove spaces before and after
```
### To Upper & To Lower
```js
var name ="Hello" ;

console.log(name.toUppedCase()); //HELLO
console.log(name.toLowerCase()); //hello
```
### Index of
`indexof(Value [mand],Start[opt]0)`

```js
var x = "Hello my world" ;

console.log(x.indexOf("my")); //6
console.log(x.indexOf("my" ,8)); //-1

console.log(x.lastIndexOf("l")); //12

```
### Slice
```js
var x = "hello world";

console.log(x.slice(0,5));//hello
console.log(x.slice(-5); //world
console.log(x.slice(-5 , -3); //wo

```
### Repeat
```js
var name = "hi";

console.log(name.repeat(3)); //hihihi
```
### Split
```js
var str = "Hi My Name Is Ahmed";

console.log(str.split()); //array of char
console.log(str.split(" ")) //["hi" ,"My","Name" ,"Is", "Ahmed"]
```

### Sub-str
```js
var x ="hello world";
console.log(x.substr(0,5));//hello 5 char
```

### Includes
`x.includes("hello",index[opt]);` => true or false

### Starts-with & Ends-With
`x.startsWith("he",index[opt]);`=>true<br>
`x.endsWith("he",length[opt]);`=>false<br>
___
# Math Object
- `Math.round(99.2)` => 99
- `Math.round(99.6)` => 100
- `Math.ceil(99.2)` => 100
- `Math.floor(99.9)` => 99
- `Math.min(10,20,30,40,50)` => 10
- `Math.max(10,20,30,40,50)` => 50
- `Math.pow(2,5)` => 32
- `Math.random()` => random
- `Math.PI`=> 3.14
- `Math.sqrt(100)`=> 10
- `Math.abs(-10)` => 10
___
