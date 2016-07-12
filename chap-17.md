# Chap 17

"Understanding responsibilities is key to good object-oriented design" - Martin Fowler

Objectives:
  - Learn to apply five of the GRASP principles or patterns for OOD.

The critical design tool for software development is a mind well educated in design principles.
It is not the UML or any other technology.

In the UML case, the real point is not the UML, but visual modeling—using a language that allows us to explore more visually
than we can with just raw text.

Responsibility-driven design (RDD) is thinking about how to assign responsibilities to collaborating objects.

During UML drawing, we adopt the realistic attitude (also promoted in agile modeling) that we are drawing the models primarily
to understand and communicate, not to document. Of course, we expect some of the UML diagrams
to be useful input to the definition (or automated code generation with a UML tool) of the code.

## Responsibilities Driven Development

A popular way of thinking about the design of software objects and also larger-scale components[3] is in terms of responsibilities, roles,
and collaborations.
This is part of a larger approach called responsibility-driven design or RDD

Responsibility is an abstraction of what they do. A contract of obligation of a classifier.
These responsibilities are of the following two type: doing & knowing.

- Doing:
  - doing st, like creating obj or calculating
  - initiation action in other objs
  - controlling or coordinating activities in other objs

- Knowing
  - knowing private encapsulated data
  - knowing related objs
  - knowing st can be derive & calculate

  Responsibilities are assigned to classes during OOD.

  Examples:
   - "Sale is responsible for **creating** SalesLineItems" (doing)
   - "Sale is responsible for knowing its total" (knowing)

Big responsibilities take hundreds of classes and methods. Little responsibilities might take 1 method.
A responsibility is not the same thing as a method - it's an abstraction - but methods fullfill responsibilities.

## 5 of 9 GRASP:

- Creator
- Expert
- Low coupling
- High cohension
- Controller


### Creator

#### Problem

#### Solution

Class B handles the responsibiliy to create instance of class A if
- B contains compositely aggregates A
- B records A
- B closely use A
- B has the initializing data for A that will be passed to A when it is created. Thus B is an **Expert** with respect to creating A
