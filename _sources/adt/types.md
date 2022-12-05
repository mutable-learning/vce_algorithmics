# ADT Specifications

There are many different ways to write abstract data type specifications, and often you will see these written online in ways that suit or are considered the standard for a particular language that the type will be implemented in.

In this book we will be using a simple syntax to define our ADT specifications and the steps below will outline how this works. Keep in mind that there are other ways you will see specifications written and the important understanding is that the operations of the ADT are clearly defined and understandable.

## Steps to define an ADT specification

Follow the steps below to create your type specification:

### Step 1 - state the type's name
You must clearly define the name of your type. You can do this with a line such as:

```{prf:example}
Name: Array
```

### Step 2 - list any imports
If your specifications for your operations use any other types, list them as imports for this type:

```{prf:example}
Imports: boolean, integer, element
```

### Step 3 - List the type's operations
Each operation the type has should be listed on its own line. 

Start with a label to show the list of operations that make up the type.

Then list each operation where each operation specification has the following components:
- the name of the operation
- a colon after the name
- any types required as input (separated with an *x*)
- an arrow pointing to the right (pointing to the output)
- any types returned as the output

An example of some operations could be:

```{prf:example}
Operations:<br />
createList : $\rightarrow$ List<br />
isEmpty : List $\rightarrow$ boolean<br />
add : List x element $\rightarrow$ List<br />
```

## Example ADT specification
Putting these steps all together, you could create a specification for an **Array** ADT like the example below:

````{margin}
```{note}
The *x* between the input types does not indicate multiplication, it just separates the types.
```
````

```{prf:example}

Name: **Array**<br/>
Import: $element, integer$<br/>
Operations:<br/>
$newArray: \space\rightarrow array$<br/>
$get: array$ x $integer \rightarrow element$<br/>
$set: array$ x $integer$ x $element \rightarrow array$<br/>

```

## Is that all?
The steps and examples listed above are not all that you would need in order to build an implementation of an ADT. One part that would be included normally are the axioms that demonstrate the behaviour of the operations, written in formal language these equations demonstrate the behaviour of the operations when used and provide meaning to each operation. 

Each axiom is an example of behaviour that results in a true state. It proves the operations' behaviour.

For our purposes in VCE Algorithmics we will not include the axia with each ADT. However, an example of how it could look for a Set ADT is given below.

```{prf:example}

Name: **Set**<br/>
Import: $element, boolean, integer$<br/>
Operations:<br/>
$newSet: \space\rightarrow set$<br/>
$addElement: set$ x $element \rightarrow set$<br/>
$remElement: set$ x $element \rightarrow set$<br/>
$hasElement: set$ x $element \rightarrow boolean$<br/>
$size: set \rightarrow integer$<br />

Properties:
- the set has no duplicates
- set items have no order

Axioms:<br/>
// on hasElement and addElement<br/>
$if\ hasElement(S,e)\ then\ addElement(S,e)) = S$<br/>
$hasElement(addElement(S,e),e) = true$<br/>
$if\ hasElement(S,e)\ and\ e \ne f\ then\ hasElement(addElement(S,f),e)$<br/>

// on hasElement and remElement<br/>
$if\ (not\ hasElement(S,e))\ then\ remElement(S,e) = S$<br/>
$hasElement(remElement(S,e),e) = false$<br/>
$if\ hasElement(S,e)\ and\ e \ne f\ then\ hasElement(remElement(S,f),e)$<br/>

// on addElement/remElement and size<br/>
$if\ (not hasElement(S,e))\ then\ size(addElement(S,e)) = size(S) + 1$<br/>
$if\ hasElement(S,e)\ then\ size(remElement(S,e)) = size(S) - 1$<br/>

// on addElement and remElement<br/>
$remElement(addElement(S,e),e) = S$<br/>

```