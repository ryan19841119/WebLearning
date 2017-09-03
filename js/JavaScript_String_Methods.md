# Java String Methods

String method help you to work with strings. 

## String Methods and Properties

Primitive values, like "John Doe", cannot have methods or properies (because they are not objects). 

But with JavaScript, methods and properties are also avaliable to primitive values, because JavaScript treats primitive values as objects when executing methods and properties. 

## String Length

The **length** property returns the length of a string. 

## Finding a String in a String

The **indexOf()** method returns the index of (the position of) the **first** occurrence of a specified text in a string:

The **lastIndexOf()** method returns the index of the **last** occurrence of a specified text in a string:

Both the indexOf(), and the lastIndexOf() method return -1 if the text is not found.

> JavaScript count position from zero. <br>
> 0 is the first position in a string, 1 is the second, 2 is the third ...

Both methods accept a second parameter as the starting position for the search. 

> var str = "Please locate where 'locate' occus!"<br>
> var pos = str.indexOf("locate", 15);

## Searching for a String in a String

The **serach()** method search a string for a specified value and returns the position of the match:

## Did You Notice?



