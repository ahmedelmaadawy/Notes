### Regex
Is a Regular expression it's a pattern to be applied 
## How to use in JS
```js
var pattern =/^[A-Z][a-z]{3,8}[0-9]{1,3}$/
/**
//this pattern means that the any string will apply to this pattern must strart with one capital character then 3 to small characters then 1 to 3 numbers
//Ex : Abcde147 => this is valid to this regex
**/
var userName ="Hello123";
if(pattern.test(userName)){
console.log("this userName string is valid");
}else{
console.log("this userName string is not valid");
}
```
## Start and end of a string
`^ => this symbol represents the start it means that the string must start with this pattern to be valid`
`/^123/` => **123444455** is valid
`/^123/` => **010123456** is not valid

---
`$ => this symbol represents the end of the pattern that your string must end with this pattern to be valid`
`/abc$/` => **1234abc** is valid
`/abc$/` => **abc123** is not valid
___
`if nethier of them is in the pattern that means that string is valid whether it starts ,ends or contains this pattern`
`/abc/` => **abc123aa** is valid
`/abc/` => **123aaxabc** is valid
`/abc/` => **aaa123abc123aa** is valid
___
`if the pattern contains both it means your string must start and end with this pattern `
`/^123abc$/` =>**123abc** is the only string valid
___
### Some Rules Of Regex
`/[]/`
- any thing with in a square brackets is only one character
`/[a-z]/`
- Any character in Range from "a" to "z"
- single character
`/[a-zA-Z]/`
- any character form "a" to "z" capital or small
- just one character
`/[abc]/`
- contains "a" or "b" or "c"
- single character
`/[0-9]/`
- any number from 0 to 9 
- works the same as characters
___
### Repeating
`/[a-z]{2}/`
- any two characters from a to z
`/[a-z]{1,3}/`
- one or two or three characters from a to z is valid
- a => is valid
- ah => is valid
- acc => is valid
___
### Examples
`/^[A-Z][a-z]{3,8}$/` 
- First character is capital
- then 3 to 8 characters
`/[A-Z][a-z]/`
- first character capital
- second character is small
`/[A-Z][a-z]{3-8}/`
- first character is capital 
- then 3 to 8 small characters
`/[\s]/`
- this represents space
`/\d/`
- numbers from 0 to 9
`/\w/`
- this represents any character
`/^[A-Z][a-z]{3,8}/`
- the pattern must start with this expression
`/^[A-Z][a-z]{3,8}$/`
- dollar sign means the pattern must end with this expression
`/^web(design|developer)$/`
- the string must starts with 'web'
- then contains 'design' or 'developer'
- ROUND brackets is grouping
`/[0-9]{0,1}/`
- this means can be one number or no number
`/^01[0125][0-9]{8}$/`
- Egyptian phone number
`/./`
- Any character
`/\./`
- the dot character

### To test Regex
[Regex Test site](https://regex101.com/)
