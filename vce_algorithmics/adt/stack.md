# Stack ADT

## Description
A **stack** is a collection type of object that follows the rule of 'last in first out' (**LIFO**). A stack is similar to the list ADT with the added rule that elements can only be added or removed from one end of the stack. Elements can be added to the stack with the **push** operation, and removed from the stack with the **pop** operation. An additional operation known as **top** or **peek** can return the value of the most recently added element without altering the stack.

## Defining Characteristics
Stacks:
- allow for adding and removing of elements to one end only
- will have the most recently added item will also being the one removed first (LIFO)
- will have the **top** of the stack containing the most recently added item
- will maintain the order of elements in the order they were added to the stack

## Specification

The specification for a stack ADT will typically contain operations similar to below:

```{prf:definition}
:nonumber:
:class: adt-specification
:label: Stack ADT specification

Name: **Stack**<br/>
Import: $element, boolean$<br/>
Operations:<br/>
$newStack:    \space\rightarrow stack$<br/>
$empty:  stack \rightarrow boolean$<br/>
$push:   stack$ x $element \rightarrow stack$<br/>
$pop:    stack \rightarrow stack$<br/>
$top:    stack \rightarrow element$<br/>


```



## Examples
