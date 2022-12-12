# Dictionary or Associative Array ADT

## Description
A **dictionary** is a collection type of ADT that stores each element with an associated key, a key-value pair. In mathematical terms a dictionary or **associative array** is a function with $finite$ domain. The key is 'associated' with the value and acts as a kind of index for the ADT.

## Defining Characteristics
Dictionaries:
- have a key and a value associated with the key
- keys are unique

## Specification

The specification for a dictionary ADT will typically contain operations similar to below:

```{prf:definition}
:nonumber:
:class: adt-specification
:label: Dictionary ADT specification

Name: **Dictionary**<br/>
Import: $key, value, boolean, integer$<br/>
Operations:<br/>
$newDictionary: \space\rightarrow dictionary$<br/>
$empty: dictionary \rightarrow boolean$<br/>
$size: dictionary \rightarrow integer$<br />
$get: dictionary$ x $key \rightarrow value$<br/>
$insert: dictionary$ x $key$ x $value \rightarrow dictionary$<br/>
$remove: dictionary$ x $key \rightarrow dictionary$<br/>




```



## Examples