# The Math Class

## Learning Goals

- Learn about the Java `Math` class
- Discuss the more common math methods used

## Let's do the Math

Let's do some math! But don't worry - we won't have to do the heavy
computations ourselves - Java will! Turns out, Java has something we call the
**Math class** that contains several methods to help us calculate mathematical
functions!

The `Math` class is part of the package called `java.lang` and contains only
static methods. This means that the methods will not depend on an object. In
this lesson, we will review some of the more common methods from the Math
class.

## Minimum and Maximum

Let's say we want to compare two numbers and find the minimum (smallest) and the
maximum (largest) values between them. We can use the Math class to do this!
The `Math` class has a `min()` and a `max()` method that each take two numeric
parameters, (can either be of the data types `int`, `double`, `float`, or
`long`) and will return the same data type based on the parameters taken in.

```java
// min() and max() with int data type
int firstInt = 28;
int secondInt = 4;

int minimum = Math.min(firstInt, secondInt);
System.out.println("The minimum integer is " + minimum);

int maximum = Math.max(firstInt, secondInt);
System.out.println("The maximum integer is " + maximum);
```

Let's break down the new statements involving the `Math` class:

`int minimum = Math.min(firstInt, secondInt);`

We see that the variables `firstInt` and `secondInt` are assigned to 28 and 4
respectively. The `min()` method can be invoked by using dot notation with the
class name: `Math.min()`. By providing the two `int` variables as parameters,
the `Math` class will then find the smaller of the two values and return the
smallest `int`. In this case, it would return the value of `secondInt` or 4.

`int maximum = Math.max(firstInt, secondInt);`

The `max()` method can be invoked the same way with dot notation: `Math.max()`.
By providing the two `int` variables as parameters, the Math class will then
find the larger of the two values and return the largest `int`. In this case, it
would return the value of `firstInt` or 28.

## Absolute Value

Another method of the `Math` class is the absolute value method. Absolute value
is a non-negative value that describes how distant a number is from 0. For
example, 0 has 0 distance from itself so its absolute value would be 0. Whereas
-200 has a distance of 200 from 0. The same can be said for the positive
number 200. Both have an absolute value of 200.

```java
// abs() with int data type
int firstInt = -28;

int absValue = Math.abs(firstInt);
System.out.println("The absolute value of " + firstInt + " is " + absValue);
```

The `abs()` method, which is the absolute value method, takes one parameter.
It can be an `int`, `double`, `float`, or `long`. In this case, it takes in an
`int` so it will return an absolute value of the parameter as an `int`.
Therefore, the expression `Math.abs(firstInt)` will evaluate to 28.

## Ceil and Floor

Sometimes we want to round decimal values to the nearest whole number. This is
where the `ceil()` and `floor()` methods come in from the `Math` class! The
`ceil()` method takes a `double` as a parameter and will perform the
ceiling on it (round the number up). The `floor` method also takes a `double`
as a parameter and will perform the floor on it (round the number down).

```java
double x = 8.25;

double ceilingValue = Math.ceil(x);
System.out.println("The ceiling is " + x);

double floorValue = Math.floor(x);
System.out.println("The floor is " + x);
```

To invoke the `ceil()` method, we can use dot notation: `Math.ceil()` and
provide it the variable `x` which is of type `double`. We then can store the
return value in the `double ceilingValue`. Note that the `ceil()` method returns
a `double`. The expression, `Math.ceil(x)` will then evaluate to 9.0. For the
`floor()` method, we will also make use of dot notation and also provide it the
`double` parameter. We'll store the floor value in the variable `floorValue`.
Again, notice that the `floor()` method also returns a `double`. The floor
expression, `Math.floor(x)` will evaluate to 8.0.

## Random

The `Math` class can even help us generate random numbers! The `random()` method
takes no parameters and will return a `double` greater than or equal to 0.0 and
less than 1.0.

```java
double randomNumber = Math.random();
System.out.println("The random number is " + randomNumber);
```

The `randomNumber` variable will be assigned to a different random number each
time the code is run. An output could look something like this:

```java
The random number is 0.3034966869965544
```

This method is helpful if we want to have the computer generate a random number,
for example, simulating a die roll.

If we were to create a program to simulate a die roll using the `Math.random()`
method, we could do something like this:

```java
int min = 1;
int max = 6;
int range = (max - min) + 1;

// Generate random numbers between 1 and 6
int randomRoll = (int)(Math.random() * range) + min;
```

To get a random integer value using the `random()` method, we need to define a
range first. In this case, we hardcoded the numbers 1 and 6 to define the range
of a standard die. Then we do a little math to ensure that a value between 1 and
6 is returned and cast it as an `int`.

## Power and Exponent

We can also use the `Math` class to raise a number to a certain power.
The `pow()` method takes in two arguments: the base number and the power we
want the base number raised to. For example, `pow(2,4)` would be the same as
2 to 4th power or 2 *2* 2 * 2.

```java
double baseNumber = 3;
double exponent = 2;
double squared = Math.pow(baseNumber, exponent);

System.out.println("Three squared is " + squared);
```

The code above shows how the `Math.pow()` can be used. Notice that the `pow()`
method takes in two parameters of type `double` and also returns a `double`.
The above `Math.pow(baseNumber, exponent)` would evaluate and assign the
`squared` variable to 9.0.

We can also take Euler's number (approximately 2.71) and raise that to a power.
We can do so by using the `Math` class' `exp()` method. The `exp()` method takes
one parameter and that is the power we want to raise e to. For example, `exp(2)`
is the same as e squared or e * e.

```java
double exponent = 3;
double cubed = Math.exp(exponent);

System.out.println("e cubed is " + cubed);
```

Just like the `pow()` method, the `exp()` method will take in a `double` as a
parameter and return a `double`. In the example above, `Math.exp(exponent)`
would evaluate and assign the variable `cubed` to 20.085536923187668.

## Square Root

If we ever want to take a square root of a number, we can do so with the `Math`
class! The `Math.sqrt()` method takes in the number we want to take the square
root of as a parameter and will return a `double` of the evaluated expression.

```java
double x = 36;
double squareRoot = Math.sqrt(x);

System.out.println("The square root of " + x + " is " + squareRoot);
```

Notice how the parameter for the `sqrt()` method is of data type `double`. Let's
take a look at what the code above would print out:

```java
The square root of 36 is 6.0
```

## Resources

- [Oracle Docs JDK 11 Math Class](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html)
