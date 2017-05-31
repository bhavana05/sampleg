	The PHP Hypertext Preprocessor (PHP) is a programming language that allows web developers to create dynamic content that interacts with databases. PHP is basically used for developing web based software applications.This PHP tutorial covers all the topics of PHP such as introduction, control statements, functions, array, string, file handling, form handling, regular expression, date and time, object-oriented programming in PHP, math, PHP mysql, PHP with ajax, PHP with jquery and PHP with XML.

Common uses of PHP:
PHP performs system functions, i.e. from files on a system it can create, open, read, write, and close them.
PHP can handle forms, i.e. gather data from files, save data to a file, through email you can send data, return data to the user.
You add, delete, modify elements within your database through PHP.
Access cookies variables and set cookies.
Using PHP, you can restrict users to access some pages of your website.
It can encrypt data.

Web Development:
	PHP is widely used in web development now a days. Dynamic websites can be easily developed by PHP. But you must have the basic the knowledge of following technologies for web development as well.
HTML 
CSS 
JavaScript 
AJAX 
XML and JSON 
JQuery 
PHP example:
	The PHP file must be save with .php extension. As PHP is embedded in HTML, means that in amongst your normal HTML you'll have PHP statements like this:

html>
   <head>
      <title></title>      
   </head>
   <body>
      <?php
         echo "<h1>Hello World</h1>";
      ?>
   </body>
</html>

It will produce following result:

Hello World

PHP tags:
	The PHP parsing engine needs a way to differentiate PHP code from other elements in the page. The mechanism for doing so is known as 'escaping to PHP'. There are four ways to do this
The most common tag:
<?php [code here] ?>
Another version is this one, which is the same kind of tags used for e.g. blocks of JavaScript code:
<script language=”php”> [code here] </script>
Those two options are always available. However, a lot of PHP installations are set up to allow the short version as well:
<? [code here] ?>
On some servers, ASP style tags have been enabled. They look like this:
<% [code here] %>

Commenting PHP code:
	A comment is the portion of a program that exists only for the human reader and stripped out before displaying the programs result. There are two commenting formats in PHP. 
Single-line comment:
	They are generally used for short explanations or notes relevant to the local code. 
 Example:
   <?
   # This is a comment, and
   # This is the second line of the comment
   // This is a comment too. Each style comments only
   ?>
Multi-line comment:
      They are generally used to provide pseudocode algorithms and more detailed explanations when necessary. The multiline style of commenting is the same as in C. Here are the example of multi lines comments.
Example:
	<?
   	/* This is a comment with multiline
      	Author : Mohammad Mohtashim
      	Purpose: Multiline Comments Demo
      	Subject: PHP
   	*/
      	?>

PHP variables
	A variable in PHP is a name of memory location that holds data. A variable is a temporary storage that is used to store data temporarily.
In PHP, a variable is declared using $ sign followed by variable name. 
Syntax of declaring a variable in PHP is given below:
    $variablename=value;
PHP Data types:
	PHP has a total of eight data types which we use to construct our variables −
Integers − are whole numbers, without a decimal point, like 4195.
Doubles − are floating-point numbers, like 3.14159 or 49.1.
Booleans − have only two possible values either true or false.
NULL − is a special type that only has one value: NULL.
Strings − are sequences of characters, like 'PHP supports string operations.'
Arrays − are named and indexed collections of other values.
Objects − are instances of programmer-defined classes, which can package up both other kinds of values and functions that are specific to the class.
Resources − are special variables that hold references to resources external to PHP (such as database connections).
Variable scope:
	Scope can be defined as the range of availability a variable has to the program in which it is declared. PHP variables can be one of four scope types:
1. Local variables:
	A variable declared in a function is considered local; that is, it can be referenced solely in that function. Any assignment outside of that function will be considered to be an entirely different variable from the one contained in the function.
2. Functional parameters:
	Function parameters are declared after the function name and inside parentheses. They are declared much like a typical variable.
3. Global variables:
	In contrast to local variables, a global variable can be accessed in any part of the program. However, in order to be modified, a global variable must be explicitly declared to be global in the function in which it is to be modified. This is accomplished, conveniently enough, by placing the keyword GLOBAL in front of the variable that should be recognized as global. Placing this keyword in front of an already existing variable tells PHP to use the variable having that name. 
4. Static variables:
	The final type of variable scoping that I discuss is known as static. In contrast to the variables declared as function parameters, which are destroyed on the function's exit, a static variable will not lose its value when the function exits and will still hold that value should the function be called again.
Variable Naming:
	Rules for naming a variable is 
Variable names must begin with a letter or underscore character.
A variable name can consist of numbers, letters, underscores but you cannot use characters like + , - , % , ( , ) . & , etc.
Constant:
	A constant is a name or an identifier for a simple value. A constant value cannot change during the execution of the script. By default, a constant is case-sensitive.To define a constant you have to use define() function and to retrieve the value of a constant, you have to simply specifying its name.You can also use the function constant() to read a constant's value if you wish to obtain the constant's name dynamically.
Constant function example:
<?php
   define("MINSIZE", 50);
   echo MINSIZE;
   echo constant("MINSIZE"); // same thing as the previous line
?>

Operator Types:
PHP language supports following type of operators.
Arithmetic Operators 
Comparison Operators 
Bitwise Operators 
Logical Operators 
String Operators 
Incrementing/Decrementing Operators 
Array Operators 
Type Operators 
Execution Operators 
Error Control Operators 
Assignment Operators 
We can also categorize operators on behalf of operands. They can be categorized in 3 forms:
Unary Operators: works on single operands such as ++, -- etc. 
Binary Operators: works on two operands such as binary +, -, *, / etc. 
Ternary Operators: works on three operands such as "?:". 

| Operator | Description | Example |
| ----------  |  ------------- |   --------- |
| +| adds |A+B|

Operator
Description
Example
+
Adds two operands
A + B will give 30
-
Subtracts second operand from the first
A - B will give -10
*
Multiply both operands
A * B will give 200
/
Divide numerator by de-numerator
B / A will give 2
%
Modulus Operator and remainder of after an integer division
B % A will give 0
++
Increment operator, increases integer value by one
A++ will give 11
--
Decrement operator, decreases integer value by one
A-- will give 9
















