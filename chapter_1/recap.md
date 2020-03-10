# Values, Types, Operators

## Data
As humans, we are equipped with the ability to communicate emotions, intent, commands (among many other things) with words in any given language. Whether it's Spanish, French, or Japanese- we use words encoded in that language to express our thoughts and sentiments.  

As for computers, they are neither thoughtful or sentimental- but they are communicative, however. They have ways of listening to certain things and returning other things in order to interact with humans or other computers. 

Whereas the atomic unit of communication for humans are words, computers rely on data as the means of communicating information. Computers can listen to data (think of a user submitting a file) and return it (outputting a piece of data). Data can be read, modified, or created by humans interacting with the computer. This way of thinking about data informs the way computer programs are created.

There's a lot of data in a computer's memory. 

> A typical computer has 30 billion bits in its working memory.

*Whoa, what's a bit?* 

Before we answer that, think about the cells in your body. You have [trillions](https://www.wonderopolis.org/wonder/how-many-cells-are-in-the-human-body) of them moving about. Your body intelligently allocates the amount of cells available in order to make tissues, organs, and organ-systems from them.

Not all organ systems are the same (some are allocated for breathing, some for digesting food). But they're all made of the same clump of cells.

> In the world of computers, a cell is analogous to a bit

In programming languages, a bit is an atomic unit of data. All of the bits that are available in a computer's working memory is split into chunks of data called *values*. 

Each value has a specific "role" or "type" to play, much like the organ systems in your body. Some values are meant to store numbers, while some store text, and true/false values. 

Other values are more complex and can store bigger pieces of data as well as input/output operations (called functions).

> There's only so much space to go around for each type of value. Every value has to be stored somewhere, and if you want to use a gigantic amount of them at the same time, you might run out of memory. 

Let's explore these different value types: 

## Numbers 

Javascript has 64 bits of storage available for a number type. There are 2^64 different numbers that can be represented in the JavaScript programming language. 

64 bits is a lot of storage for numbers. Out of these 64 bits, there are bits allocated for negative, and decimal numbers as well.

> Many numbers lose some precision when only 64 bits are available to store them.

We must treat decimal numbers as approximations and not as precise values.

### You can do math operations

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

## String

Strings are represented by the amount of bits that are allocated for text and characters. 

There are 2^16 bits available in JavaScript to describe a character in a text.

Strings can be enclosed by single or double quote marks.

```
'Hello world'
"Hello world" 
```
Some strings need additional tab spaces, quotation marks, or additional lines.

Say you want to embed quotations and make one text go on top of the other, like this:

```
John said: "Hi, are you going?"
Joan replied: "No, I am not."
```
To achieve this, you can include `escape characters` using the backslash `\n` to create the newline character and `\"` to embed the double quotes. Just like this:

```
let message = "John said: \"Hi, are you going?\" \n Joane replied: \"No I'm staying in.\" ";
```
This looks complicated and really annoying to do. As we say in NYC:

> Ain't nobody got time for memorizing escape characters and using them in strings. Besides, escape characters were an outdated hack that was used for controlling typewriters in the past. #Facts.

I just use back-ticks ``string with backticks`` and express the strings as I wish without having to use those pesky escape characters. 

For example;

```
let text = `John said: "Hey are you going to school?"
Joan said: "Nah, I'm staying in"`;
```
There... no need for those `\n` or `\'` characters.

Besides, backticks allow for us to compute values within a string, using the `${}` syntax, like this:

```
let output = '';
output += `half of 100 is ${100/2}`;
console.log(output);
```
> When you write something inside `${}` its result will be computed, converted to a string, and included at the position. 

Although we can't perform math operations in strings, we can treat strings as values that can be evaluated through the use of `${}`.

One more example: 

```
let d = new Date();
let currentYear = d.getFullYear();
let studentName = "John"; 
let userBio = `${studentName} is a freshman and will graduate in ${currentYear + 4}`;
```

## Boolean 

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
### You can use logical operators to output boolean values

Can one statement be true *and* another false? What would happen if both were false? 

Can one statement be true *or* another false? 

Logical operators are used to answer those questions and generate boolean values in the process. 

Javascript uses the following logical operators: `and`, `or`, and `not` operators, represented as `&&`, `||`, and `!` respectively. 

Some examples:

```
(3>2) && (2<3)
// `true` and `false` gives us `false`
// Something can't be both true AND false at the same time.
```

```
(3>2) && (5>2)
// `true` AND `true` gives us `true`
// If one statement were true AND the other true, then both statements must be true.
```

```
(2<3) && (5>2)
// `false` AND `true` gives us `false`
// Something can't be both `true` AND `false` at the same time.
```

```
(2<3) && (2<5)
// `false` AND `false` gives us `false`
// Two `false` statements don't make it true. 
```

```
(2<3) || (5>2)
// `true` OR `false` gives us `true`
// Something can be both `true` OR `false` at the same time.
```

```
(2>3) || (5>2)
// `false` OR `true` gives us `true`
// Something can be both `true` OR `false` at the same time.
```
```
(2>3) || (10<2)
// `false` OR `false` gives us `false`
// Something can't be both `false` OR `false` at the same time.
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

`Undefined` is not necessarily a programming error. It's just JavaScript's way of letting the programmer know that there's a value that needs to be assigned for that variable. 

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

`2 == '2'` gives us `true`, though it should really give us `false`. Numbers and text are not the same value type, yet JavaScript will "coerce" the string value to a number type, thereby making it `true`. 

>This can get confusing really fast, a number should be a number and a string should be a string. 

We can compare between two values without relying on type coercion by using `===` or `!==` instead of `==` or `!=`. 

```
2 === '2'
// gives us false
```

> "I recommend using the three-character comparison operators defensively to prevent unexpected type conversions from tripping you up." 
-Marijn Haverbeke

## Short-Circuiting of Logical Operators

Short-circuit evaluation uses the logical operators `&&` and `||` to do the following:

1. Convert a set of values into boolean values
2. Evaluate between those sets of boolean values
3. Return a member of that set of values 

Let's demonstrate with an example:

```
let user = 'Agnes' || ''
```

Because a logical `||` is being invoked, the two values ('Agnes' and 'user') are converted into Boolean values. 'Agnes' is converted to `True` and  the empty string `''` is converted to `False`. 

Next, those two values are evaluated. We've learned that `True || False` evaluates to `True`.

No matter what the expression on the right of 'Agnes' is, because 'Agnes' evaluates to `True`, the expression "short-circuits", or stops the evaluation process, and immediately returns 'Agnes'.

Lastly, 'Agnes' is assigned to the `user` variable.

Let's see this example:

```
let user = '' || 'awesome user';
```

What do you think will happen here? 

First, the empty string `''` will convert to `False` and 'awesome user' will convert to `True`. 

We know that `False || True` evaluates to `True`. 

The expression will continue searching over the value that evaluates to `True` and will return it to the `user` variable.

Now `user = awesome user`.
 
testing again!














