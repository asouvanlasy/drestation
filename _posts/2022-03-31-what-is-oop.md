---
layout: post
title: "What is a Object-Oriented Programming?"
categories: doc
---

Object-oriented programming (OOP) is a programming concept focused on objects and classes.

- Objects are the building blocks for programs. They hold data that say what they are and what they should do.
- Classes are the blueprints for objects. They *don't* hold data for objects, but they say that data should be.

## Real-World Example

Here, a `Person` is an object. The class defines what a `Person` should be and what they should be able to do. In our example, our `Person` will have a name, age, and be able to talk.

To demonstrate this with pseudocode (fake code):
```
class Person {
    string name = 'Robby'
    number age = 47
    
    method talk {
        say('I can talk!')
    }
}
```

## Why OOP?

The main purpose of OOP is to neatly package together data and functionality, like a program sandwich.

The advantage of this is that your code is more organized, reusable and flexible.
Imagine having to create a `Person` thousands of times, each with different attributes.
It would get tiresome to start from scratch each time. This makes OOP suitable for large-scale and complex programs that are continously updated.

## Pros of OOP

Object-oriented programming popular among developers for being suitable for large and complex programs that are continuously updated. The alternative 