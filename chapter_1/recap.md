# Values, Types, Operators

## Data
Data can be read, modified, or created. This way of thinking about data informs the way apps are created (as you can create, delete, edit/update content). 

There's a lot of data in a computer's memory. There's even more if you include the computer's hard-disk. 

> A typical computer has 30 billion bits

*Whoa, what's a bit?* 

Before we answer that, think about the cells in our body. We have a lot of them flowing about. Our bodies intelligently allocate the amount of cells that are available and make tissues, organs, and organ-systems out of them. 

 Not all organ systems are the same (some are for breathing, some for digesting food). But they're all made of cells.

 *Now back to bits* 

Data is stored in binary units called bits. 

Bits describe things in terms of two. Something can be *true or false*, a *high-signal or weak-signal*, *on or off*. 

Bits are stored in binary units. Numbers can be expressed in bits. 

Think of the number 15. If we were to express it as a decimal unit, we'd do the following procedure:

> 15 is the result of 10 available numbers in the "tens" place, plus 10 available numbers in the "ones" place. Each base in the decimal system moves up by a power of 10. 

As you move up in base, there's additional "room" for numbers by a factor of that base. 

> 115 is the result of 100 available numbers in the "hundreds" place, plus 10 available numbers in the "tens" place, plus 10 available numbers in the "ones" place. 

How does this look like in binary? 

Now let's take 15 and describe it in the binary system. Whereas each factor in the decimal-number system is of a base of 10, each factor in binary is of a base of 2. 

Binary asks the following questions: In the 0 place is there room for a number? If so, 

> 1111 

There are 4 bits of avaialble "space" to get to 15 in binary. 

Data is allocated and stored in the amount of space that's available in working memory and the hard-disk. A computer has more than 30 billion bits for allocating this data.

### JavaScript makes use of this data
JavaScript groups all this data and assigns them a type of role. Some data type serves as text, some will serve as numbers for doing math operations, some will be used as true/false operators for doing conditional logic, some will be used as data-structures for storing complex data, and some will take inputs and spit out outputs in the form of a function. 

There's only so much space to go around for each type of data. 

> Every value has to be stored somewhere, and if you want to use a gigantic amount of them at the same time, you might run out of memory. 

Data is recycleable. If you're not using a piece of data-type, it will be recycled for other values to use. 

#### Numbers 

Javascript has 64 bits of storage available for a number type. There are 2^64 different numbers that can be represented in JS. 

64 bits is a lot of storage for numbers- out of these 64 bits, there are bits allocated for negative, and decimal numbers as well.

> Many numbers lose some precision when only 64 bits are available to store them.

##### You can do math operations

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

#### String 

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

#### Boolean 

Boolean is a fancy-word for a value that gives two possibilities: "yes/no", "true/false". It's binary in nature. 

In JavaScript (and I believe in all computer programming languages...), boolean values can be computed to yield `true` or `false` values.

```
3<2
// false
```

```
Infinity >= 3
// true
```
```
"Apple != "Orange"
//true
```
```
"Apple == "Orange"
//false
```
##### You can use logical operators to output boolean values

Can one statement be true while another false? What would happen if both were false? 

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
 




