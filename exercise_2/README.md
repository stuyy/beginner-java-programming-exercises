# Variables & Data Types

To Do
-

- Declare a variable of type `int`
- Declare a variable of type `String`
- Declare a variable of type `double`
- Declare a variable of type `boolean`
- Declare a variable of type `char`

# Variables

What are variables? Think of a box, or a container, what do you use them for? You might need to store objects in them, such as books, kitchen utencils, appliances, etc. and then later on you need to retrieve an item from that same box.

This is the same idea with **variables**. They are just containers that hold information for your program. Your program might need to store user info so it can be used later, so it stores it in a variable, e.g:

```Java
String name = "Anson";
System.out.println(name); // Outputs Anson
System.out.println("My name is " + name); // outputs "My name is Anson"
```

First off, let's talk about what we just did in the code snippet above:

We declared a variable called `name`, this is known as the *identifier*, a unique sequence of characters that we can reference later. It is unique, in the sense that we cannot declare another variable with the *same name*.

The variable's *type* is `String`.

# Variable Name Rules & Convention

There are some rules when naming variables:

1) Your variable must start with a letter, it can also start with a `$` or `_` (Underscore)
    - `String $name = "My Name";` would be valid, but `String 123 = "123"` would be invalid.
2) Your variable cannot start with a number.
    - `String 1name = "name";` would be invalid.
3) After the first character, you may have any alphanumeric character after it, you can also have `$` and `_` as well, but you cannot have special characters or spaces in between.

The following variable identifiers are valid:

```Java
String $1name = "My Name";
String name2 = "Your name";
String _name = "Underscore Name";
String valid_name = "Valid Name";
int my_age = 24;
```

The following variable identifiers are invalid:

```Java
String 123; 
String %;
String *name;
String 1name;
String my name;
int my age;
```

### Try it yourself
---
Before we continue, why don't you try declaring a variable of type `int` yourself? Give it a unique name, and assign it a numeric value. Remember, `int` is another data type that holds numeric values, it's short for integer, and it cannot have floating points, e.g: `0.5` is not an integer, thus would be an invalid assignment.

# Data Types

## Strings

A `String` is a sequence of characters, wrapped between double quotes. We have been using String literals up until now, let's declare a couple of String variables and assign them a value.

```Java
String myName = "Anson";
String myCurrentJob = "Garbage Collector";
String myFavoriteFood = "Pizza";
```

We declared three variables, `myName`, `myCurrentJob`, and `myFavoriteFood`. We assigned each variable a String literal value.

We can also re-assign values to variables, too:

```Java
String myName = "Anson";
String myCurrentJob = "Garbage Collector";
String myFavoriteFood = "Pizza";

myName = "Not Anson";
myCurrentJob = "Systems Engineer";
myFavoriteFood = "Sushi";

String myName = "Danny"; // ERROR! Cannot re-declare variables.
```