# JavaScript Numbers

JavaScript has only one type of number. Numbers can be written with or
without decimals.

> var x = 3.14;<br>
> var y = 3;

Extra large or extra small numbers can be written with scientific
(exponent) notation:

> var x = 123e5;		// 12300000<br>
> var y = 123e-5;	// 0.00123<br>


## JavaScript Numbers are Always 64-bit Floating Point

Unlike many other programming languages, JavaScript does not define
different type of numbers, like integers, short, long, floating-point
etc.

JavaScript nubers are always stored as double precision floating point numbers, following the international IEEE 753 standard. 

This format stores numbers in 64 bits, where the number (the fraction) is stored in bits 0 to 51, the exponent in bits 52 to 62, and the sign in bit 63:
 
Value (aka Fraction/Mantissa)|Exponent|Sign
---|---|---
52 bits (0 - 51)|11 bits (52 - 62)|1 bit (63)

## Precision

Integers (numbers without a period or exponent notation) are accurate up to 15 diits. 

> var x = 999999999999999;		// x will be 999999999999999<br>
> var y - 9999999999999999;	// y will be
> 10000000000000000<br>

The maximum number of decimals is 17, but floating point arithmetic is not always 100% accurate:

### Example

> var x = 0.2 + 0.1;		// x will be 0.300000000000000004<br>

To solve the problem above, it helps to multiply and divide:

### Example
> var x = (0.2 * 10 + 0.1 * 10) / 10;		// x will be 0.3

## Adding Numbers and Strings

> WARNING !!<br>
> JavaScript uses the + operator for both addition and concatenation.<br>
> Numbers are added. Strings are concatenated. 

If you add two numbers, the result will be a number:

### Example

> var x = 10;<br>
> var y = 20;<br>
> var z = x + y;		// z will be 30 (a number)

If you add two stirngs, the result will be a string concatenation:

### Example

> var x = "10";<br>
> var y = "20";<br>
> var z = x + y;		// z will be 1020 (a string)

If you add a number and a string, the result will be a string concatenation:

### Example

> var x = 10;<br>
> var y = "20";<br>
> var z = x + y;		// z will be 1020 (a string)

If you add a string and a number, the result will be a string concatenation:

### Example

> var x = "10";<br>
> var y = 20;<br>
> var z = x + y;		// z will be 1020 (a string)

A common mistake is to expect this result to be 30:

### Example

> var x = 10;<br>
> var y = 20;<br>
> var z = "The result is: + x + y;

A common mistake is to expect this result to be 102030:

### Example

> var x = 10;<br>
> var y = 20;<br>
> var z = "30";<br>
> var result = x + y + z;

<br>

> TheJavaScript compiler works from left to right. <br>
> First 10 + 20 added because x and y are both nubers. <br>
> Then 30 + "30" is concatenated because z is a string. 

## Numeric Strings

JavaScript strings can have numeric content:

> var x = 100;		// x is a number<br>
> var y = "100";		// y is a string<br>

JavaScript will try to convert strings to numbers in all numeric operations:

This will work:

> var x = "100";<br>
> var y = "10";<br>
> var z = x / y;		// z will be 10

<br>
This wll also work:

> var x = "100";<br>
> var y = "10";<br>
> var z = x * y;			// z will be 1000

And this will work:

> var> x = "100";<br>
> var y = "10";<br>
> var z = x - y; 		// z will be 90

But this will not work:

> var x = "100";<br>
> var y = "10";<br>
> var z = x + y; 		// z will not be 110 (It will be 100010)

<br>

> In the last example JavaScript uses the + operator to concatenate the strings. 

## NaN - Not a Number

NaN is a JavaScript reserved word indicating that a number is not a legal number. 

Trying to do arithmetic with a non-numberic string will result in N (Not a Number):

### Example

> var x = 100 / "Apple";  // x will be NaN (Not a Number)

However, if the string contains a numeric value, the result will be a number:

### Example

> var x = 100 / "10";  // x will be 10

You can use the global JavaScript function isNaN() to find out if a value is a number:

### Example

> var x = 100 / "Apple";<br>
> isNaN(x);		// returns true because x is Not a Number

Watch out for NaN. If you use NaN in a mathematical operation, the result will also be NaN:

### Example

> var x = NaN;
> var y = 5;
> var z = x + y; 		// z will be NaN

Or the result might be a concatenation:

### Example

> var x = NaN;
> var y = "5";
> var z = x + y; // z will be NaN5

NaN is a number: typeof NaN returns number:

### Example

> typeof NaN; 		// returns "number"

## Infinity

Infinity (or -Infinity) is the value JavaScript will return if you cacluate a number outside the largest possible number. 

### Example

> var myNumber = 2;<br>
> while (myNumber != Infinity) {		//Excute until Infinity<br>
> 		myNumber = myNumber * myNumber;<br>
> }

Division by 0 (zero) also generate Infinity:

### Example

> var x = 2/0;		// x will be Infinity<br>
> var y = -2/0;		// y will be -Infinity

Infinity is a number: typeof Infinity returns number. 

### Example

> typeof Infinity; 		// returns "number"

## Hexadecimal

JavaScript interprets numberic constants as hexadecimal if they are preceded by 0x. 

### Example

> var x = 0xFF;		// x will be 255<br>
<br>
> Never write a number with a leading zero (like 07).<br>
> Some JavaScript versions interpret numbers as octal if they are written with a leading zero. 

By default, JavaScript displays numbers as bae 01 decimals.

But you can use the to String() method to output numbers as base 16 (hex), base 8 (octal), or base2(binary). 

### Example

> var myNumber = 128;
> myNumber.toString(16); // returns 80
> myNumber.toString(8); // returns 200
> myNumber.toString(2); // returns 10000000

## Numbers Can be Objects

Normally JavaScript number are primitive values creted from literals:

