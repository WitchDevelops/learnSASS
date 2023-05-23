#SASS concepts
## functions
### `@each` loop
like a `for each` method in JavaScript.
Each loops in Sass iterate on each of the values on a list. The syntax is as follows:
```
@each $item in $list {
  //some rules and or conditions
}
```
The value of $item is dynamically assigned to the value of the object in the list according to its position and the iteration of the loop.

### `@for` loop
For loops in Sass can be used to style numerous elements or assigning properties all at once. They work like any for-loop you’ve seen before.

Sass’s for loop syntax is as follows:
```
@for $i from $begin through $end {
   //some rules and or conditions
}
```
In the example above:

`$i` is just a variable for the index, or position of the element in the list
`$begin` and `$end` are placeholders for the start and end points of the loop.
The keywords `through` and `to` are interchangeable in Sass.

### conditionals
In Sass, `if()` is a function that can only branch one of two ways based on a condition. You can use it inline, to assign the value of a property:

```
width: if( $condition, $value-if-true, $value-if-false);
```
For cases with more than two outcomes, the `@if`, `@else-if`, and `@else` directives allow for more flexibility.

```
@mixin deck($suit) {
 @if($suit == hearts || $suit == diamonds){
   color: red;
 }
 @else-if($suit == clovers || $suit == spades){
   color: black;
 }
 @else{
   //some rule
 }
}
```
The mixin above is a good example for how we would want to handle the coloring of a deck of cards based on a suit condition.
