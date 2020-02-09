# Values, Types, Operators

## Data
Data can be read, modified, or created. This way of thinking about data informs the way apps are created (as you can read, create, delete, edit/update content). 

There's a lot of data in a computer's memory. 

> A typical computer has 30 billion bits

*Whoa, what's a bit?* 

Before we answer that, think about the cells in your body. You have [trillions](https://www.wonderopolis.org/wonder/how-many-cells-are-in-the-human-body) of them moving about. Your body intelligently allocates the amount of cells available in order to make tissues, organs, and organ-systems out of them.

Not all organ systems are the same (some are for breathing, some for digesting food). But they're all made of cells.

> In the world of computers, a cell is analogous to a bit

In programming languages, a bit is an atomic unit of data. All of the bits that are available in a computer's working memory is split into chunks of data called *values*. 

Each value has a specific "role" or "type" to play, much like the organ systems in your body. Some values are meant to store numbers, while some store text, and true/false values. Other values are more complex and can store bigger pieces of data as well as input/output operations (called functions).

> There's only so much space to go around for each type of value. Every value has to be stored somewhere, and if you want to use a gigantic amount of them at the same time, you might run out of memory. 

Let's explore these different value types: 

### Numbers 

Javascript has 64 bits of storage available for a number type. There are 2^64 different numbers that can be represented in JS. 

64 bits is a lot of storage for numbers. Out of these 64 bits, there are bits allocated for negative, and decimal numbers as well.

> Many numbers lose some precision when only 64 bits are available to store them.

#### You can do math operations

```
1+1 
```

```
100 + 4 * 11
```

JavaScript even follows the order of operations if you specify it with parens. 

```
(100 + 4) * 11
```

You can also get the remainder of one number divided by another by using the `%` operator. `8 % 4` which will output `0`.

### String 

Strings are represented by the amount of bits that are allocated for text and characters. 

There are 2^16 bits available in JavaScript to describe a character in a text.

Strings can be enclosed by single or double quote marks.

```
'Hello world'
"Hello world" 
```

But I like back-ticks ``string with backticks`` more because you can include "template literals" which can do computations from within and output the string.  

```
`half of 100 is ${100/2}`
```

### Boolean 

Boolean is a fancy-word for a value that gives two possibilities: "yes/no", "true/false". It's binary in nature. 

Booleans can be produced by comparing two values in such a way that the end-result is `true` or `false`.

```
3<2
//is 3 greater than 2? false
```

```
Infinity >= 3
// Is infinity greater than OR equal to 3? true
```
```
"Apple != "Orange"
//Is an apple NOT an orange? true
```
```
"Apple == "Orange"
//Is an apple an orange? false
```
#### You can use logical operators to output boolean values

Can one statement be true *and* another false? What would happen if both were false? 

Can one statement be true *or* another false? Would it make a difference What would happen if one statement were false or the other false as well? 

Logical operators are used to answer those questions and generate boolean values in the process. 

Javascript uses the following logical operators: `and`, `or`, and `not` operators, represented as `&&`, `||`, and `!` respectively. 

```
(3>2) && (2<3)
//true and false gives us false
//Something can't be both true and false at the same time.
```

```
(3>2) && (5>2)
//true and true gives us true
//If one statement were true and the other true, then both statements must be true.
```

```
(2<3) && (5>2)
//false and true gives us false
//Something can't be both true and false at the same time.
```

```
(2<3) && (2<5)
//false and false gives us false
//Two false statements don't make it true. 
```

```
(2<3) || (5>2)
//true or false gives us true
//Something can be both true or false at the same time.
```

```
(2>3) || (5>2)
//false or true gives us true
//Something can be both true or false at the same time.
```
```
(2>3) || (10<2)
//false or false gives us false
//Something can't be both false or false at the same time.
```

> The `!` operator is used to negate a boolean value. `!true` gives us
`false`.

### Empty values

In Javascript, the value `undefined` simply means that there is no explicit value assigned to a variable. 

> Think of a user who's trying to log-in to your app. Your app will have to store their username and make reference to that name throughout the entire time they're logged in.

The best way to do that is to create a `variable` which will remember that user's name during their session. 

`let userName = 'John Doe'`; 

This userName variable has been declared and assigned a value of `"John Doe"`. 

But if the userName variable was declared without an assigned value, then that variable is `undefined`. It's JavaScript's way of saying, "hey, you've declared me I'm ready to take in a value and store it into memory." 

`Undefined` is not necessarily a prgramming error. It's just JavaScript's way of letting the programmer know that there's a value that needs to be assigned to a variable. 

`Null` is the absence of a value.

Here's a great [write-up](https://stackoverflow.com/questions/5076944/what-is-the-difference-between-null-and-undefined-in-javascript) on the difference between `undefined` and `null`

## Automatic Type Conversion

How does JavaScript resolve an operation involving two different value types? 

For example:

```
2 * null 
// null is interpreted as 0 and gives us 0 as a result
```
```
2 * '5'
// the string '5' is interpreted as the number 5 and gives us 10 as a result
```
```
'5' + 1
// this operation is interpreted as a string concatenation outputting a string value of '51' 
```
This method of "interpreting" a value's data-type is known as "type coercion". 

Check this out:

`2 == '2'` gives us `true`, though it should really give us `false`. Numbers and text are not the same value type, afterall; yet JavaScript will "coerce" the string value to a number type, thereby making it `true`. 

What if you want to treat values for what they really are? check this out. new version











