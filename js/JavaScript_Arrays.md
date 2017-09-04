# JavaScript Arrays
```javascript
var cars = ["Saab", "Volvo", "BMW"];
```

```javascript
var cars = [
	"Saab",
	"Volvo",
	"BMW
];
```

## Access the Element of an Array
```javascript
var name = cars[0];
vars[0] = "Opel"'
```
```javascript
var cars = ["Saab", "Volvo", "BMW"];
document.getElementById("demo").innerHTML = cars[0];
```
Access the Full Array
```javascript
var cars = ["Saab", "Volvo", "BMW"];
document.getElementById("demo").innerHTML = cars;
```
> Saab,Volvo,BMW

```javascript
var fruits, text, fLen, i;

fruits = ["Banana", "Orange", "Apple", "Mango"];
fLen = fruits.length;
text = "<ul>";
for (i = 0; i < fLen; i++) {
    text += "<li>" + fruits[i] + "</li>";
}
text += "</ul>";
document.getElementById("demo").innerHTML = text;
```
> * Banana
> * Orange
> * Apple
> * Mango

