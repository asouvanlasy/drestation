---
layout: post
title: "What is a Object-Oriented Programming?"
categories: doc
---

Object-oriented programming (OOP) is a programming paradigm focused on classes and objects.

- Programming paradigms are the ways, techniques or approaches to writing programs.

- Classes are the blueprints for creating objects. They define what the data should be and what a function can do with that data.

- Objects hold the actual data as defined by the blueprint.

## Real-World Example

Here, `Gun` is a class. The class defines what a `Gun` should be and what it should do. In our example, our `Gun` will have a model, ammo, and can shoot.

To demonstrate this with pseudocode (fake code):

```
class Gun {
    // Define what type of data
    string model
    int bullets
    
    // This function subtracts one bullet when fired
    function shoot() {
    }
}
```

## Why OOP?

The main purpose of OOP is to neatly package together data and it's functionality.

The advantage of this is that your code is more organized, reusable and flexible. Real-world things are easier to represent, such as our `Gun`.

Imagine having to create a `Gun` thousands of times, each with different attributes. It would get tiresome to start from scratch each time.

This makes OOP suitable for large-scale and complex programs that are continously updated.

## The Four Pillars of OOP

These are the four major concepts of OOP:

- **Encapsulation:** every part of an object or class can be encapsulated; meaning you can decide which parts should be hidden or visible (for security).

- **Abstraction:** hiding certain details and showing only information deemed essential to the user. This can be thought of as an extension of encapsulation.

- **Polymorphism:** one class can be used to create many objects, all from the same flexible piece of code. The word 'polymorphism' is derived from Greek meaning "many forms".

- **Inheritance:** classes can inherit data from other classes, so more code is reusable resulting in faster development.

### Extending the Gun Example

As seen as before, we defined a `Gun` class. Let's create a `Gun` object.

```
class Main {
    // Create a Gun called ak47
    Gun ak47 = {
        name = 'Kalashnikov'
        bullets = 30
    }

    ak47.shoot() // 29 bullets remain
}
```

Here are some ways we can demonstrate OOP concepts:

- **Encapsulation:** sensitive details about the gun can be hidden. Perhaps it's an new prototype?

- **Abstraction:** show only essential information like how to shoot the gun. In this case, that would be very poor firearm safety.

- **Polymorphism:** a gun can appear in many forms. Our AK-47 is based off the blueprint `Gun` class.

- **Inheritance:** AK-47 takes traits from `Gun`, such as having bullets and shooting.

## What Else?

Most programming languages are a mix of paradigms and exhibit some or all aspects of OOP.

Developers don't band together behind a paradigm like rooting for a sports team. They decide based on what's the best tool for the job.

**Procedural programming** is an alternative paradigm that is based on procedures rather than simulating real-world objects. Instead of focusing on the data, it focuses on how to do the task.

What paradigm you work with usually won't restrict you, as there's always more than one solution.