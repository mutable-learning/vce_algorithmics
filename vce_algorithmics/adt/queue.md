# Queue ADT

## Description
A **queue** is a collection type of object that follows the rule of 'first in first out' (**FIFO**). A queue is similar to a list in that it maintains the order of the elements in the queue and allows for adding and removing elements. It is also similar to a stack in the way the elements are manipulated except that in a queue the elements are added to one end and removed from the other, whereas a stack only adds and removes elements to the same end. To add an element to a queue you use the **enqueue** operation, and to remove an element you use the **dequeue** operation. A queue may also define a **peek** operation that returns the value of the element at the front of the queue without modifying it.

## Defining Characteristics
Queues:
- allow for adding at one end and removing of elements at the other end
- follow the first in first out rule (FIFO)
- will have the **front** of the queue containing the most recently added item
- will maintain the order of elements in the order they were added to the queue

## Specification

The specification for a queue ADT will typically contain operations similar to below:

```{prf:definition}
:nonumber:
:class: adt-specification
:label: Queue ADT specification

Name: **Queue**<br/>
Import: $element, boolean$<br/>
Operations:<br/>
$newQueue:    \space\rightarrow queue$<br/>
$empty:  queue \rightarrow boolean$<br/>
$enqueue:   queue$ x $element \rightarrow queue$<br/>
$dequeue:    queue \rightarrow queue$<br/>
$peek:    queue \rightarrow element$<br/>


```

## Examples