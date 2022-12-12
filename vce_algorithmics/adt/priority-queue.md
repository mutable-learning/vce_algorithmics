# Priority Queue ADT

## Description
A **priority queue** is a collection type of object that is very similar to a regular queue ADT but each element also has a ***priority*** associated with it. In this type of queue the element with the higher priority is served before an element with a lower priority. If two or more elements have the same priority the priority queue would usually operate like a regular queue and follow the first in first out rule, but some implementations do not define an order for elements with the same priority.

A priority queue can also be specified as the lowest value priority being the 'highest priority', so that it will be returned first. Operations for priority queues are commonly known by a variety of names, but they must at least support creating the priority queue, checking if it is empty, inserting an element with a priority, and returning an element with the 'highest' priority.

## Defining Characteristics
Priority Queues:
- allow for adding elements with a priority
- will return the element with the *highest* priority first
- priority values can be either min or max to determine the *highest*

## Specification

The specification for a priority queue ADT will typically contain operations similar to below:

```{prf:definition}
:nonumber:
:class: adt-specification
:label: Priority Queue ADT specification

Name: **Priority Queue**<br/>
Import: $element, boolean, integer$<br/>
Operations:<br/>
$newPQueue:    \space\rightarrow pqueue$<br/>
$empty:  pqueue \rightarrow boolean$<br/>
$insert\_with\_priority:   pqueue$ x $element$ x $integer \rightarrow pqueue$<br/>
$get\_maximum\_element:    pqueue \rightarrow pqueue$<br/>
$find\_max:    pqueue \rightarrow element$<br/>


```

## Examples