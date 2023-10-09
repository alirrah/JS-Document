# javaScript for beginners

## what is javaScript?
one of the most popular language in world and fastest between other languages.

salary of javaScript dveloper 72000 per year

work as
front-end developer
back-end developer
full-stack developer

what can you do with it?
for a long tiime javaScript only use in webbrowers to make interactive web pages

work as toy language

full web/mobile apps 

real-time networking apps

cammand-lin tools

games

where does javascript code run?

run only in broswer
and all broswer has javaScript Engine that can excute javaScript code

javaScript Engine:
firefox: spidermonkey
chrome: v8

node is cpp program that include google, javaScript Engine ,... and with this can run avaScript code outside of broswer and that mean can javaScript in back-end

between javaScript vs ECMAScript?

ECMAScript is Specification but javaScript is programming lanuage 

last version of ECMAScript is ES2015/ES6

run javaScript code in broswer:

open your chrome
right click on empty area 
click on inspect -> open chrome developer tools
select console -> this javaScript console

```js
console.log('Hello Wolrd');
2 + 2;
alert('yo');
```

## we need a code editor:
vs code
sublime text
atom

we use vs code

we can download node to run js code but it`s not nessary becuase we can excute js code in broswer

## to run code we need Script element
we can write in two place:

1. in head section
2. at end of body section -> best option

two reason is best:
* run code from top to bottom -> if javaScript in head may broswer become busy and page not load -> bad user experinse
* javaScript code almost code in html part

but it`s not always
sometimes must put it in head section

```html
<script>
    console.log('hello world');
</script>
```

statement is a pis of code that express an action to be carry out

at the and of each statement we have ; 

string is secuns of characters


comment start with //

comment not excute and only show others why we write this codes

## in real application with millon lines of js code, so we write js code in spreate files

```html
<script src="ADDRESS"></script>
```

EX:

```html
<script src="index.js"></script>
```

## to run js code with node
open terminal or cmd
and head it to the folder
and write node ADDRESS

EX:

```bash
node index.js
```

## variable is the most discotion fundumental concept at any programming language

we use a variable to store data temporarily in the computer memory

we store our data somewhere and give that memory location a name and with this name we can read data at given location in the future

perviously, before ES6 we use var to declare variable but in ES6 the best practice is let to declare variable

by dafualt when we declare varible the value is undefined
so we should initialized it

```js
let name = 'Mosh';
```

rule of variable name
1. can not be a rreserved keyword
2. should be meaningful
3. can not start with a number
4. can not contain space or hyphen

js is case-sensitive

```js
let firstName = 'Alireza';
```

to declare multipy variable:

1. 

```js
let name = 'mosh', age = 12;
```

2. 

```js
let name = 'mosh';
let age = 12;
```

two is better

## we can chanage variable value whenever we want

```js
let age = 10;
age = 13;
```

but if we want to can not chage the value we use constants

the value of constant can not change

```js
const interestRate = 0.3;
```

## what type of value can assign to a variable


we have two type of vriable in js:
1. primitives/ value types
2. reference types

in primitive catgories we have:
1. String

```js
let name = 'Mosh';
```

2. Number

```js
let age = 30;
```

3. Boolean

```js
let isApproved = false;
let isGo = true;
```

4. undefined
default value when we not initialzied

```js
let firstName = undefined;
```

5. null

```js
let lastName = null;
```

we use null when we want to clear value of variable

## js is dynamic programming


we have two types of programming language:
1. static
type of variable set and can not chanage the type of variable in future

2. dynamic
type of variable not set and can chanage type of variable in runtime

we can check the type of variable with typeof in js

typeof NAMEVARIABLE

```js
typeof name
```

with ctrl + l we can clear console

in js we do not have two type of number(interage and float)

## in the reference type we have:

1. Object
when we dela with multipy variables we use object

```js
let person = {
  name: 'mosh',
  age: 30
};
```

two ways of work with these prapertese:
1. Dot Notation
```js
person.name
```

2. Brack Notation
```js
person['name']
```

when we know propertes we use dot notation 
but if propertese select in runtime we use brack notation

```js
let selection = 'name';
person[selection]
```

2. Array
use array when we del with list of items

```js
let selectColors = ['blue', 'red'];
```

in array ech element has index and start from zero

```js
selectColors[0]
```

lengeth of array and type of element is dynamic in js

```js
let selectColors = ['red', 'blue'];
selectColors[2] = 1;
```

ARRAYNAME.length return number of elementts

EX: selectColors.length
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

3) Function

function is one of the fundomantal building block in js

funtion basically is set of statement a perporm a task or calculates a value

function greet() {
   console.log('Hello World');
}

greet();

function can have an input 

function greet(name) {
   console.log('Hello ' + name);
}

greet('ali');

ali is argument and name is parameter

function can have multiply parameter

function greet(fistName, lastName) {
   console.log('Hello ' + firstName + ' ' + lastName);
}

if we not pass the argument, js set undefined instead
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

to return a value from function we use return 

function square(number) {
    return number * number'
}

console.log(square(2));
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

in js we have different kind of operators

we use operators along variables to create expressions and with this expressions we can implement logic and algorithms

kind of operators in js:
Arithmetic
Assignment
comparison
logocal
bitwise
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

let`s look at arthmetic operators

+ addition operator
- subtraction operator
* multiptation operator
/ division operator
% remainder operator
** exponesion operator

increment(++)

console.log(++x) 

x += 1
console.log(x)


console.log(x++) 

console.log(x)
x += 1


decrement(--)

console.log(--x) 

x -= 1
console.log(x)


console.log(x--) 

console.log(x)
x -= 1
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

let`s look at assignment operators

= assignment operator
+= additon assignment operator
-= subtraction assignment operator
*= multiptation assignment operator
/= division assignment operator
%= remainder assignment operator
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

let`s look at comparison operators

we use these operators to compere variables

the resualt of comparison operators in boolean

> greater than
>= greater than or equal to
< less than
<= less than or equal to
=== equality
!== not equality
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

equality operators

=== vs  ==

=== strict equality -> same type and value
== lose equality -> convert to same type and then compare


1 === 1 -> true
1 === '1' -> false

1 == 1 -> true
1 == '1' -> true =>that`s what js do '1' == '1'

true == 1 -> true => that`s what js do true == true
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

let`s look at ternary operators or conditionary operators

condition ? value_one : value_two

let type = points > 100 ? 'gold' : 'silver'
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

let`s look at logical operators
we use these opertors to make dission base on multipule condition

kind of logical operators
&& logical and ->be true when both of them true
|| logical or -> be true when at less one of them true
! logical not -> be true when false and reverse
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

the logical operators output in not true or false, it can be a value and it depend on value we passed

false || "ali" => "ali"
false || 1 => 1

Falsy value:
undefined
null
0
false
""
NaN

Truthy is not Falsy

short-circuiting: return the first truthy  value in or
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

let`s look at bitwise oerators

| bitwise or
& bitwise and
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

precedence of operators

it`s hard to memorize it so use parantesize
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

swap to value

let c = a;
a = b;
b = c;
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

in this section we are going to use operators among conditions and statement


conditional statement in js:
if ...else
switch ...case

if hour is between 6am anf 12pm: Good morning!
if it is between 12pm and 6 pm: Good afternoon!
otherwise: Good evening!

if (hour >= 6 && hour < 12) {
    console.log('Good morning!');
} else if (hour >= 12 && hour < 18) {
    console.log('Good afternoon!');
} else {
     console.log('Good evening!');
}

or 

if (hour >= 6 && hour < 12)
    console.log('Good morning!');
else if (hour >= 12 && hour < 18)
    console.log('Good afternoon!');
else
     console.log('Good evening!');
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

switch (role) {
    case 'guest':
        console.log('Guest User');
        break;
    case 'moderator':
        console.log('Moderator User');
        break;
    defulat:
        console.log('Unknown User');
}

break at the end of each statement is nessesary becuase if you do not write it other case will be run.

use if and else for boolean is more commen
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

when we want to do an action n time, use loop

console.log('Hello world');
console.log('Hello world');
console.log('Hello world');
console.log('Hello world');
console.log('Hello world');

it`s ugly.

loops:
for
while
do ...while
for ...in
for ...of


for (let i = 0; i < 5; i++) {
    console.log('Hello world');
}

for (let i = 5; i >= 0; i--) {
    console.log(i);
}
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

let i = 0;
while(i >= 5) {
    console.log(i);
    i++;
}
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

let i = 0;
do {
    console.log(i);
    i++;
} while (i <= 5);

do ...while is run one time and then check the condition
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

infinite loop 
the loop is excute for ever

while (true) {
    console.log(1);
}
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

for-in loop

cost person = {
   name: 'Mosh',
   age: 30
};

for (let key in person) {
    console.log(key);
    console.log(person[key]);
}

use it to iterate a collection.

better to use in object.
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

for-of loop

const colors = ['red', 'blue', 'yellow'];

for (let color of colors) {
   console.log(color);
}

better to use in array.
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

use break to jump out  of the loop

use continue to skip other lines of code for one step and jump to next iteration
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

return maxium of two number

function max (numberOne, numberTwo) {
    if (numberOne > numberTwo)
        return numberOne;
    return numberTwo;
}

function max (numberOne, numberTwo) {
    return (numberOne > numberTwo) ? numberOne : numberTwo;
}

show is landscape or portrait

functon isLandscape(width, height) {
     return (width > height) ? true : false;
}

functon isLandscape(width, height) {
     return (width > height);
}

divisible by 3 => Fizz
divisible by 5 => Buzz
divisible by both 5 and 3 => FizzBuzz
not divisible by 3 or 5 => input
not a number => Not a number

function fizzBuzz(input) {
    if (typeof input !== 'number')
        return 'Not a number';
    if (input % 3 === 0 && input % 5 === 0) 
        return 'FizzBuzz';
    if (input % 3 === 0)
        return 'Fizz';
    if (input % 5 === 0)
        return 'Buzz';
    return input;
}

for not a number is better to return NaN
typeof Nan is number
so we have:

function fizzBuzz(input) {
    if (typeof input !== 'number')
        return NaN;
    if (input % 3 === 0 && input % 5 === 0) 
        return 'FizzBuzz';
    if (input % 3 === 0)
        return 'Fizz';
    if (input % 5 === 0)
        return 'Buzz';
    return input;
}

under or equal 70 return Ok
for each 5 kilameter you get one point
get more than 12 pionts license suspended

Math.floor() convert float to number

function checkSpeed(speed) {
    if (result < 75)
        return 'Ok';
    let result = Math.floor(speed - 70 / 5);
    if (result >= 12) 
        return 'License suspended';
    return 'Point ' + result;
}

show odd and even number until limit

function showNumber(limit) {
    for(let i = 0; i <= limit; i++) 
        console.log((i % 2 === 0) ? 'EVEN' : 'ODD');
}

get array and return the number of truthy element

function countTruthy(array) {
    let count = 0;
    for (let item of array) 
        if (item)
            count++;
    return count;
}

get objet and show all the properties

function showProperties(obj) {
    for (let item in obj)
        console.log(item, obj.item);
}

function showStar(rows) {
    for(let row = 1; row <= rows; i++) {
        let pattern = '';
        for (let j = 0; j < row; j++)
            pattern += '*';
        console.log(pattern);
    }
}


function isPrime(number) {
     for (let i = number - 1; i > 1; i--) 
         if (number % i === 0)
              return false;
     return true;
}
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////