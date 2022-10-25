# Set ADT

## Description
A **set** is an ADT that is a representation of the mathematical concept of a 'finite set'. It is a collection type object allowing for multiple values to be stored in the ADT. Rather than using it as a storage type for moving objects in and out of the collection, like you might use an array, a set is especially useful when you want to test the membership of a value or compare groups of values with each other.

Many other ADTs could be viewed as being a set with additional operations or rules (axioms) applied to create difference with a standard set ADT. Generally, set ADTs will have operations to perform the algebra of sets, namely operations for: union, intersection, difference and subset.

There are two different common set types encountered. A **static** or **frozen** set is one that does not change after it is created, allowing only querying of the set elements for membership, and a **dynamic** or **mutable** set, which also allows for insertion and deletion of elements after construction.

## Defining Characteristics
Sets:
- Contain unique elements only
- Store elements in no particular order

## Specification

The specification for a set ADT will typically contain operations similar to below:

```{prf:definition}
:nonumber:
:class: adt-specification
:label: Set ADT specification

Name: **Set**<br />
Import: $element, boolean$<br />
Operations:<br />
$new: \space\rightarrow set$<br />
$empty: set \rightarrow boolean$<br />
$add: set$ x $element \rightarrow set$<br />
$member: set$ x $element \rightarrow boolean$<br />
$remove: set$ x $element \rightarrow set$<br />
$union: set$ x $set \rightarrow set$<br />
$intersection: set$ x $set \rightarrow set$<br />
$difference: set$ x $set \rightarrow set$<br />
$subset: set$ x $set \rightarrow set$<br />


```



## Examples
