# CodingBestPractices
This repositories contain the different coding best practices which i have learned by working in  different projects or by reading different books and blogs.


## Ternary operator

It will save you lines of code, very easily. This tip is working on almost all the modern languages and even older ones. The goal is to reduce a traditional if-else conditional statement into a one-liner.

**Common Way**

```javascript
let x = 3;

if(x > 1)
  console.log('X is above 1');
else 
  console.log('X is below 1');
  
// => X is above 1
```
**Ternary operator way**

```javascript
// First way
let x = 3;
let sentence = (x > 1) ? 'X is above 1':'X is below 1';
console.log(sentence);

// => X is above 1

// Second shorter way, less-readable
console.log( (x > 1) ? 'X is above 1':'X is below 1' ); // Without a temporary variable

// The syntax is always the same, no matter the language

// (conditional statement) ? result-if-true : result-if-false

// You can even chain the ternary operators

console.log( 
    (x > 1) ? 
      (x > 2) ? 'X is above 2':'X is below 2' 
      :'X is below 1'
  );

// => X is above 2

```

The point is :

-First, you get 4 lines turned into a one-liner not that hard to read.

-Second, it can be used in return statements because it is parsed as an expression.

-Finally, you can concatenate ternary operator expressions even if it’s not readable at all (You should refrain from doing it in production code).


## Logical negation operator

Lines of code saved, like always. But this time, readability will be improved ! What’s more ?

Let’s see how one would implement a basic light switch.

**Common Way**

```javascript
var lightPlugged = false;

function switchLight() 
{
  if(lightPlugged == false)
    lightPlugged = true;
  else 
    lightPlugged = false;
}

console.log( lightPlugged ? 'Light is on':'Light is off');
// => Light is off

switchLight();

console.log( lightPlugged ? 'Light is on':'Light is off');
// => Light is on

```

**Logical Negation Way**

```javascript
var lightPlugged = false;

function switchLight() 
{
  lightPlugged = !lightPlugged;
}

console.log( lightPlugged ? 'Light is on':'Light is off');
// => Light is off

switchLight();

console.log( lightPlugged ? 'Light is on':'Light is off');
// => Light is on
```




