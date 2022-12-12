# Array ADT

## Description
An **array** ADT is a collection type object that models a group of elements of a finite size. Each element in the array is assigned a position in the array with the result being that the elements are ordered within the array. The order of the elements in the array is enforced by the ADT but it is possible for elements to be repeated in the array, with each repetition of an element having its own position in the ordering of all elements.

Arrays usually allow only elements of the same type to be stored within the array, integers for example (all elements would be integers in the array).

## Defining Characteristics
Arrays:
- are of a fixed size
- have elements ordered within the array
- have an index assigned to each element to indicate position in the array


## Specification

The specification for an array ADT will typically contain operations similar to below:

```{prf:definition}
:nonumber:
:class: adt-specification
:label: Array ADT specification

Name: **Array**<br/>
Import: $element, boolean, integer$<br/>
Operations:<br/>
$newArray: \space\rightarrow array$<br/>
$get: array$ x $integer \rightarrow element$<br/>
$set: array$ x $integer$ x $element \rightarrow array$<br/>

```



## Examples