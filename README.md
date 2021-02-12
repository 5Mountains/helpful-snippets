## Helpful Snippets

This repository contains useful hints, snippets of ```html```, ```css``` and ```js``` to help refresh memory (:

### HTML

***

text semantics:
```
<q>Some important text</q>
<address>Who said</address>
```
```<blockquote>Some text</blockquote>```

```<time datetime="01.01.2020">My Birthday</time>```
```
<pre>
  <code>
    if(a > b) {
      return a;
    } else {
      return b;
    }
  </code>
</pre>
```
Non semantic highlights:
```
<b>Bold text</b>

<i>Italic text</i>

<tt>Typing text</tt>

<s>Deleted text</s>
```
Semantic highlights:
```
<strong>Some text</strong>

<em>Some text</em>

<small>Some text</small>

<big>Some text</big>

<mark>Some text</mark>

<del>Some text</del>

<ins>Some text</ins>
```
Some 'status bars':
```
<label for="download">Downloading progress:</label>
<progress id="download" value="32" max="100"></progress>
```
```
<label for="fuel">Fuel level:</label>
<meter id="fuel" value="2" min="0" max="10">2 out of 10</meter><br>
```
### JS

***

Converting decimal number ```const num = 1```,

into **binary**:
```const bin = num.toString(2);```

or, into **octal**:
```const oct = num.toString(8);```

or, into **hexadecimal**:
```const hex = num.toString(16);```

but, the result will be **```string```** and in order to convert it into a number (if it needs), there are several options: ```Number()```, ```parseInt()``` or just put  before result **```+```**.

How to join 2 arrays into 1 array:
```
const num1 = [1, 2, 3, 4];
const num2 = [5, 6, 7, 8];
const allNum1 = num1.concat(num2);
const allNum2 = [...num1,...num2];
```
result for both will be [1, 2, 3, 4, 5, 6, 7, 8];

***

### TypeScript

##### Basics
all these consts can be sign only to their set type, in other case will be error;

- boolean:

`const isCompleted: boolean = true | false;`

- string:

``const isString: string = 'word' | `There is some ${word}`;``

- numbers:

```
const isNull: number = 5;
const decimal: number = 5.25;
const hex: number = 0xf00d;
const binary: number = 0b1010;
const octal: number = 0o744;
```

- null

`const isNull: null = null;`

- undefined

`const isUndefined: undefined = undefined;`

<br>

- Array of numbers/strings - the data type is numbers or string and they will be in array

`const numbersArray: number[] or string[] = [1, 2, 3, 4, 5];`

- Generic type - via keyword Array we set data type and after by keyword number or string we describe data.

`const numbersArray: Array<number> or Array<string> = [1, 2, 3, 4, 5];`

- Tuple type - inside array we define future different data types and then assign the array into a variable.

```
let x: [string, number];
x = ['hey', 55];

or

let y: [string, number] = ['buy', 10];
```

- Any type - for dynamically generated data or when the data can be changed, but this checking is unreliable...

```
let x: [any, any] = ['buy', 10];
let y: Array<any> = [10, 'buy'];
let anyone: any = false;
anyone = 10;
anyone = 'hello';
```

Type - custom way of setting data.   

```
type ID = string | number;

const stringId: ID = "1234";
const numberId: ID = 1234;
```

Enum Type - 
Object Type -



##### Functions
- Void - the describing data type which mean that function doesn't have return statement.
```
function sayHello(name: string): void {
  alert(`Hello dear Sir or Madam ${name}`);
  console.log(`Hello dear Sir or Madam ${name}`);
}
```
- Never - the describing data type which mean that function return Error or function never end.

```
function sayHello(message: string): never {
  throw new Error(message);
}

function infinity(): never {
  while(true) {
    console.log('Greetings')
  }
}
```

- interfaces - 

```
interface Person {
  readonly id: number,
  color?: string,
  size: {
    width
  }
}
```