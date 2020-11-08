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
