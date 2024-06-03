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
`^ => this symbol represents the start it means that the string must start with this pattern to be valid`<br />
`/^123/` => **123444455** is valid<br />
`/^123/` => **010123456** is not valid<br />

---
`$ => this symbol represents the end of the pattern that your string must end with this pattern to be valid`<br />
`/abc$/` => **1234abc** is valid<br />
`/abc$/` => **abc123** is not valid<br />
___
`if nethier of them is in the pattern that means that string is valid whether it starts ,ends or contains this pattern`<br />
`/abc/` => **abc123aa** is valid<br />
`/abc/` => **123aaxabc** is valid<br />
`/abc/` => **aaa123abc123aa** is valid<br />
___
`if the pattern contains both it means your string must start and end with this pattern `<br />
`/^123abc$/` =>**123abc** is the only string valid<br />
___
### Some Rules Of Regex
`/[]/`<br />
- any thing with in a square brackets is only one character<br />
`/[a-z]/`<br />
- Any character in Range from "a" to "z"<br />
- single character<br />
`/[a-zA-Z]/`<br />
- any character form "a" to "z" capital or small<br />
- just one character<br />
`/[abc]/`<br />
- contains "a" or "b" or "c"<br />
- single character<br />
`/[0-9]/`<br />
- any number from 0 to 9 <br />
- works the same as characters<br />
___
### Repeating
`/[a-z]{2}/`<br />
- any two characters from a to z<br />
`/[a-z]{1,3}/`<br />
- one or two or three characters from a to z is valid<br />
- a => is valid<br />
- ah => is valid<br />
- acc => is valid<br />
___
### Examples
`/^[A-Z][a-z]{3,8}$/` <br />
- First character is capital<br />
- then 3 to 8 characters<br />
`/[A-Z][a-z]/`<br />
- first character capital<br />
- second character is small<br />
`/[A-Z][a-z]{3-8}/`<br />
- first character is capital <br />
- then 3 to 8 small characters<br />
`/[\s]/`<br />
- this represents space<br />
`/\d/`<br />
- numbers from 0 to 9<br />
`/\w/`<br />
- this represents any character<br />
`/^[A-Z][a-z]{3,8}/`<br />
- the pattern must start with this expression<br />
`/^[A-Z][a-z]{3,8}$/`<br />
- dollar sign means the pattern must end with this expression<br />
`/^web(design|developer)$/`<br />
- the string must starts with 'web'<br />
- then contains 'design' or 'developer'<br />
- ROUND brackets is grouping<br />
`/[0-9]{0,1}/`<br />
- this means can be one number or no number<br />
`/^01[0125][0-9]{8}$/`<br />
- Egyptian phone number<br />
`/./`<br />
- Any character<br />
`/\./`<br />
- the dot character<br />
<br />
### To test Regex
[Regex Test site](https://regex101.com/)
