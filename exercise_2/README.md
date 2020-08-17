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

## Numeric Data Types

We have six numeric data types in Java, these are listed in order of size:

| Type | Size (Bytes)   | Range                           |
|:----:|----------------|---------------------------------|
| byte | 1 byte         | -128 to 127                     |
| short| 2 bytes        | -32,768 to 32,767               |
|int   | 4 bytes        | -2,147,483,648 to 2,147,483,647 |
|long  | 8 bytes        | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| float| 4 bytes        | 1.40129846432481707e-45 to 3.40282346638528860e+38 |
|double|8 bytes         | 4.94065645841246544e-324d to 1.79769313486231570e+308d |

What are these "sizes" for each numeric data type? Basically the size tells us how large or small of a number that can be stored in a variable with said type. 

Bytes are a unit of measurement commonly used for digital information. You've definitely heard of bytes before, e.g: "My harddrive has 1 teraBYTE".

1 byte is 8 bits, a bit is also known as a binary digit. Computers interpret machine code (0's and 1's), this is known as binary.

How do we determine what is the range of numbers a data type can hold? We can take the number of bits, and take 2 and raise it to the number of bits.

For example, the data type `byte` has a size of 1 byte, or 8 bits, if we compute 2^8, the result would be 256. However, all of these numeric data types are `signed`, which means variables of said type can hold both negative AND positive values. The opposite, `unsigned`, means the variable can only hold positive values.

Think of it like this, in the real world, we know any number without a negative *sign* is positive. But once we place a negative *sign* in front of the number, we know it's negative. So *signed* means it can hold both negative and positive values, and *unsigned* means it can hold only positive values.

So the actual range of a byte is -128 to 127, or `(-2^7 to (2^7)-1)`

The reason for the subtraction of 1 from 2^7 is because we include the number 0.

If the `byte` data type was *unsigned*, then the correct range would be 0 to 255. (0 to (2^7)-1)

Hopefully all of this makes sense! You probably won't have to worry about unsigned and signed, as Java does not support unsigned integers. However, if you ever plan on learning C or C++, or any systems programming language, you'll be able to use unsigned and signed numeric data types.

These are a bit advanced, so don't worry too much about it if you're a beginner. Just know that different data types have different sizes. Knowing the size of your variables can be very useful, especially when it comes to memory management, but Java takes care of it for you, compared to a language like C.

## Character Data Type

The `char` data type represents a single character literal. e.g: `'A'` or `'B'`.

`char firstNameInitial = 'A';`

## Boolean Data Type

Booleans only hold two values, `true` or `false`. We will use them when we get to conditional statements.

`boolean isMale = true;`

`boolean isTall = false;`
