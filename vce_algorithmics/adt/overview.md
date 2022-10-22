# What is an Abstract Data Type (ADT)?

## The role of complexity
Computer science is primarily concerned with **complexity** and creating and implementing techniques for handling it.

As humans, we manage complexity using techniques that allow us to function even in a complex world where we are required to perform complicated actions and manage these in real-time. Take driving a car as an example. How do we make the car move? We push the **accelerator** pedal. It doesn't matter that we don't know how pushing the pedal makes the car move, we are just interested in the result, and any car that has an accelerator will operate in pretty much the same way. The complexity of making a car move is reduced to the push of a pedal.

One of the techniques humans use to manage complexity is to use labels for objects and concepts. Defining all the components that make up the object or concept and treating the assembly of these as a whole allowing for the manipulating of the 'label' in place of its components. This is called a **metaphor** by cognitive psychologists.

Labels can be related to other labels, forming a collection, and these can then be given a new label, forming a hierarchy or tree of concepts, ideas and relationships.

```{prf:example}
:nonumber:
A computer is a **label** we use to describe the millions of components that work together to allow us to watch videos or play games. We don't know what all the components are, nor how they work together to allow the computer to function, we just know what is and is not a computer.
```

This idea of reducing the complexity to a manageable and workable level is a core tenant in computer science.

## Types
A type is a collection of values. A Boolean type is a collection of true and false values and could be defined as a **simple type** as its values do not have any subparts. An Integer is a collection of numbers and is also a simple type, but some types might contain multiple pieces of information, such as a student record. Information such as name, address, grades and course might be included into a record, an **aggregate** or **composite** type.

It is common to hear about types being used in software development and the term is mostly used to describe an object that is a implementation of an abstract term. This implementation of the type in a programming language is where the type is defined along with the operations that can manipulate the type. This is more specifically known as a **data type**.

## Data Types
If we take a type, say an integer, and the operations that manipulate integers, and then we create the implementation of this in a programming language, we will have a built an integer data type. Each programming language will have its own implementation of this data type, but they will all be a representation of the mathematical concept of an integer.

A data type is a physical representation of the logical concept, and is used in the actual code to represent the object and allow operations to be performed on the object's data. Often in programming the terms class, type and data type are used interchangeably to represent the same thing, an implementation in the particular programming language of a mathematical concept or composite structure.

So how do we make a distinction between the logical idea of a data type and all these physical implementations of the idea in different programming languages? How do we reduce the complexity of having to know about how each language works and just focus on using the concept of the data type to look for solutions to problems? This is where abstract data types are used.

## Abstract Data Types (ADT)
An abstract data type is an object whose behaviour is defined by a set of values and a set of operations, without any information about how these are implemented.

Think of an ADT as about the **what** not the **how**. The specification of an ADT tells you the rules that define the interface, the operations that are possible on the interface, the arguments needed for each operation and the type of result the operation returns. 

How the ADT will be implemented in any programming language is up to the developer. We don't need to know how it is going to work, we just need to know what it is and what it can do, and now we are free to think about how we can use this ADT to start representing the parts of a problem we are trying to solve. Hiding these details from the user is known as **abstraction**.

The creation and use of ADTs is done to manage complexity and allows us to solve difficult problems by **abstracting** the complexity of implementing the data type down to just thinking about the operations that are possible and what the data type provides.

```{prf:example}
:nonumber:
Think of driving a car as an ADT. You can steer, accelerate and brake in all cars, but they all do these tasks differently. Some have electric motors and others combustion engines, some have power steering and others steer all four wheels. Some use disk brakes, others drum brakes or regenerative braking. The implementation of these is abstracted from the driver who just uses the interface of steering wheel, accelerator and brake pedals to drive any car. The driver is not required to understand the details of how these all work. The details are deliberately hidden from the driver.
```

ADTs:
- are theoretical in nature
- define what something does, not how it works
- encapsulate a type and the operations possible on this type
- operations are defined with argument types (input) and result types (output)
- the details of how operations work are abstracted from the user
- allows for change in the implementation of the ADT

## Why use ADTs
Using ADTs helps to reduce complexity, but what does this really mean in practice?

1. Fewer bugs
2. Ease of understanding
3. Supports change

**Abstracting** the implementation details of the data type from the user means they can focus on using the ADT to create a solution. 

Using an ADT applies the concept of **modularisation** where the ADT can be isolated, tested and implemented by itself, separate from the whole, and reused where needed.

The ADT is responsible for its own operations and these aren't changed when other parts of the solution change. The internals of the ADT are protected from external interference. It stays consistent and is **encapsulated**.

Consequently, with the details of how the ADT is implemented hidden from the surrounding solution, internal changes in the implementation of the ADT will not impact other parts of the solution, nor will they change the specification of the ADT itself.

Finally, as ADTs do not specify implementation information, they are independent of programming languages and can be used by any programming language that can support them.

```{glossary}
Type
    A collection of values

Data Type
    A type together with operations that can be used to manipulate the type

Abstract Data Type
    The specification of a data type including the type and the operations available on the type, without any implementation information.
```