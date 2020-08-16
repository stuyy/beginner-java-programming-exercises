# Hello, World!

To-Do
-----

    Write a simple program that prints "Hello World" to the console.

---

Summary
-

This is the starting point to programming. Console output is important. It allows us programmers to receive feedback from the code we write, or the code we run. In Java, we can use the `println` method to log output to our console.

`println` is a method that comes from the `PrintStream` object. Don't know what that is? Don't worry.

`System` is a class that is part of Java core, it provides fields and methods that we can use as utilities for our application. 
- The `System` class has a field called `out`, which is a `PrintStream` object. Like mentioned above, `PrintStream` has a method called `println`, which we can call to log output to the console.

I know all of this stuff does not make any sense to the new programmers, but do not worry about this, this explanation is more for programmers who have experience already.

For now, just remember in order to print output to the console, we use the `System.out.println()` method. This method takes in an **argument**. Arguments are input for methods that produce some output. In this case, we pass in a *String literal* `"Hello, World"`, in between the parenthesis.

```System.out.println("Hello World");```

A *string literal* is a fixed value in code, it never changes, it's constant. In this case, we are passing "Hello World", a string literal, as an argument to the `System.out.println` method. That value never changes.

Remember all of our programming statements that need to be executed must be inside the `main` method of our class, assuming we have the file `HelloWorld.java`

```Java
public class HelloWorld {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```

To compile this manually, open up your Windows CMD if on Windows, or Terminal on Mac/Linux, and type:

  `javac HelloWorld.java`

  `java HelloWorld`

Congrats! You wrote your first Java program. Now go ahead and practice. Java can be a tricky language due to all of the early exposure to classes and objects, but don't worry. Just keep practicing console output and remember that whenever you want to print output to the console, you use `System.out.println("Message");`.

---

Additional Info
-

You can also print numeric values:

```

public class HelloWorld {
  public static void main(String[] args) {
    System.out.println("Hello World");
    System.out.println(100);
    System.out.println("I am " + 22 + " years old");
  }
}

```

The `+` in between `"I am "` and `22` is concatenating both `"I am "` and `22` *(both literal values)*, into one String. The result looks like `"I am 22"`, after, it concatenates `"I am 22"` with `" years old"` producing the final String as: `"I am 22 years old"`.

