# Data Types Pt. 2 & Casting

## Widening & Narrowing Conversions
Java is a strongly typed programming language. This means that every value we assign to a variable is checked by the Java compiler to ensure the variable can actually hold such value.

For example,

`int a = 1;`

The Java compiler will check if `1` is valid, which it is, since `1` is an integer and it is within the range of `int` data type.

Try the following:

```Java
double y = 60.7;
int x = y;
```

What is the value of `x`?

You'll notice that the compiler won't even compile, because we have an assignment error.

Integers cannot hold fractional values, e.g: `60.7`.

However, there is a deeper meaning to this. If we attempt to assign an integer to a double, there is a *loss of precision*, which in simple terms, just means that if we try to store a larger value into a variable that cannot hold it, we may lose some parts of it. It's like trying to store everything in a tiny box, you might not be able to, and may lose out on some items.

There is a ranking for numeric data types, these are listed from highest to lowest rank:

```
double
float
long
int
short
byte
```

Java will perform a process called *widening conversion*, which means it will attempt to convert lower ranked data types to higher ranked data types.

Let's declare a variable of type `short`:

`short age = 22;`

We can then declare a variable that has a higher rank, such as `int`

`int intAge;`

Then we can assign the value of `age` to `intAge`

`intAge = age;`

**We can also assign integers to doubles, but not the other way around.**

`double f = intAge; // 22.0`

The value of `f` would be `22.0` and *not* `22`, doubles and floats will always trail a decimal point, in this case it will add a `.0` at the end of `22`.

*Narrowing conversion* is the opposite of *widening conversion*, where we convert a higher ranked data type to a lower ranked data type. The above example of assigning an integer to a double is an example of narrowing conversion. 

Java does not perform narrowing conversions automatically, due to *loss of precision*.

## Casting Data Types

Casting allows you to manually convert a data type to another data type. Casting will ignore consequences from loss of precision.

For example, let's say we really want to convert a `double` to an `int`, we can do so by using the casting operator, which is a set of parenthesis, enclosing the data type we want to cast to.

Example:

```Java
double f = 5.6;
int y = (int)f; // y is 5
```

The `(int)` is the casting operator, it will cast the variable value `f` to an `int`. The value of `y` is `5`. What happened to the floating point, `0.6`? It was *truncated*. Which means the floating point part of the double was lost. This is an example of loss of precision. 

Note: *The original value of `f` is NOT changed*

Let's look at another example with floats:

```Java
float f = 5.6;
```
If we try to run that code, our compiler will throw an error. This is because a *widening conversion* is performed on `5.6`, which converts the data type from a float to a higher rank, `double` in this case.

Therefore, if we want to store `5.6` in a variable of type `float`, we need to cast it. We did this in Episode 4 using a lowercase `f` at the end. This works for literal values and NOT variables.

`float f = 5.6f; // Works because 5.6 is a literal value`

```Java
double someNum = 9.0;
float floatNum = someNumf; // WOULD NOT WORK!
```
```Java
double someNum = 9.0;
float floatNum = (float)someNum; // Correct!
```

# Try it yourself

- Cast an integer to a short
- Cast an integer to a byte
- Cast a double to a float
- Cast a float to a double

