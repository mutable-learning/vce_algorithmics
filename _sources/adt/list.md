# List ADT

## Description
A **list** ADT is a collection type object that is similar to an array ADT. As with an array, lists store and maintain the order of elements. However, a list ADT allows for a dynamic number of elements, with the list expanding and contracting as needed. Lists also allow for elements to be added to the front, or the end, and also allow for accessing elements using an index or other positional indicator such as next/previous elements.

## Defining Characteristics
Lists:
- are of dynamic size
- have elements ordered within the list

## Specification

The specification for a list ADT will typically contain operations similar to below:

```{prf:definition}
:nonumber:
:class: adt-specification
:label: List ADT specification

Name: **List**<br/>
Import: $element, boolean, integer$<br/>
Operations:<br/>
$new: \space\rightarrow list$<br/>
$empty: list \rightarrow boolean$<br/>
$size: list \rightarrow integer$<br />
$get: list$ x $integer \rightarrow element$<br/>
$set: list$ x $integer$ x $element \rightarrow list$<br/>
$head: list \rightarrow element$<br/>
$tail: list \rightarrow list$<br/>
$prepend: list$ x $element \rightarrow list$<br/>
$append: list$ x $element \rightarrow list$<br/>


```



## Examples
