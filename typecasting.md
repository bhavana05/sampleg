# Type Casting

Converting a data type into another is known as type casting. Sometimes there is a need to convert the data type of one value to another.

#### The typeof Operator:

You can use the JavaScript typeof operator to find the type of a JavaScript variable.
The typeof operator returns the type of a variable or an expression.

**Example:**
```
<!DOCTYPE html>
<html>
<body>
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = 
typeof 0 + "<br>" + 
typeof "john" + "<br>" +
typeof "" + "<br>" +
typeof (3);
</script>
</body>
</html>
```
**Output:**
```
number
string
string
number
```
#### Converting to Boolean

To convert a value to boolean data type, just pass the value to Boolean function.

Syntax:
```
Boolean(value);
```
**Example**
```
<script>
var b = 1;
b = Boolean(b);
document.write(b + " : " + typeof b); //outputs true : boolean
</script>
```
#### Converting to String

To convert a value to string data type, just pass the value to String function.

Syntax:
```
String(value);
```
**Example**
```
<script>
var s = 1;
s= String(s);
document.write(s + " : " + typeof s); //outputs 1 : string
</script>
```
#### Converting to Number

Many times string needs to get converted into numbers. To convert a value to number data type, just pass the value to Number function.

Syntax:
```
Number(value);
```
**Example**
```
<script>
var n1 = true;
var n2 = "1str";
var n3 = "123";
n1 = Number(n1);
n2 = Number(n2);
n3 = Number(n3);
document.write(n1 + " : " + typeof n1); //outputs 1 : number
document.write("<br />");
document.write(n2 + " : " + typeof n2); //outputs NaN : number
document.write("<br />");
document.write(n3 + " : " + typeof n3); //outputs 123 : number
document.write("<br />");
</script>
```
true is represented as 1 in numeric so n1 after conversion stores value 1.
"1str" after conversion doesn't represent a valid number that's why the output is NaN. NaN means not a number. Its a language construct.
"123" after conversion represents valid number 123.

#### ParseInt

parseInt() function is used to convert strings values into numbers. It works differently than Number() function. It doesn't work for boolean or other data-types values. For others values or string that doesn't contain numbers in it, parseInt() will just output NaN. Examples will clear this idea.

Syntax:
```
parseInt(string);
```
**Example**
```
<script>
var n1 = true;
var n2 = "1str";
var n3 = "123";
var n4 = "str123str1";
n1 = parseInt(n1);
n2 = parseInt(n2);
n3 = parseInt(n3);
n4 = parseInt(n4);
document.write(n1 + " : " + typeof n1); //outputs NaN : number
document.write("<br />");
document.write(n2 + " : " + typeof n2); //outputs 1: number
document.write("<br />");
document.write(n3 + " : " + typeof n3); //outputs 123 : number
document.write("<br />");
document.write(n3 + " : " + typeof n4); //outputs 123 : number
document.write("<br />");
</script>
```
#### parseFloat

parseFloat() function is used to convert strings values into floating point numbers. It works similar to parseInt() function with an exception of handling decimal point numbers. For example, 1.23 is represented as 123e-2. parseInt("123e-2") will result in 123 but parseFloat("123e-2") will give 1.23.

Syntax:
```
parseFloat(string);
```
**Example**
```
<script>
var n1 = "123e-2";
var n2 = "1str";
var n3 = "123";
var n4 = "str123str1";
n1 = parseFloat(n1);
n2 = parseFloat(n2);
n3 = parseFloat(n3);
n4 = parseFloat(n4);
document.write(n1 + " : " + typeof n1); //outputs 1.23 : number
document.write("<br />");
document.write(n2 + " : " + typeof n2); //outputs 1: number
document.write("<br />");
document.write(n3 + " : " + typeof n3); //outputs 123 : number
document.write("<br />");
document.write(n3 + " : " + typeof n4); //outputs 123 : number
document.write("<br />");
</script>
```

