# Ruby Back to Basics

## Introduction

Every day, we control how our life flows. This morning, before you got
out of bed, you probably pushed the blanket off. You walked into the
bathroom to brush your teeth. Then you sat down at the computer to
read this README. When you're hungry, you'll grab a snack. As humans,
we use logic to control how our days flow without much thought to the
process behind it. Computers need a bit more guidance. Logic and
conditional statements in Ruby allow you to control how your program
works. Loops allow you to tell a program to repeat a portion of code
until a certain condition is met.

## Learning Goals

- Review Conditionals and Logic
  - If Statements
  - Ternary Operators and Statement Modifiers
  - Case Statements
- Review Looping
  - While Loops
  - Until Loops

## Review Conditionals and Logic

The term 'conditionals' refers to a set of expressions: if statements, ternary
operators, statement modifiers, and case statements. Think of a real life
scenario where you would need to make a decision based on certain
conditions. For example, `if` it's raining outside, you take a rain jacket
or umbrella. In the context of web technology, `if` you're logged in, you
can see content specific to a registered user, if not (or `else`), you may
see a marketing page or log in screen.

In order for conditional statements to function, we always need a logical
statement that evaluates to `TRUE` or `FALSE`. It is either `TRUE` or `FALSE`
that it is raining outside, `TRUE` or `FALSE` that you are logged in to a
website. These logical statements can be comparisons:

```ruby
0 < 1
# => true
5 > 10
# => false
```

Or methods:

```ruby
[].empty?
# => true
[1, 2, 3].include?(4)
# => false
```

Its also possible to use values to derive the 'trueness' or 'falseness'. In
Ruby, anything that is _something_ is considered 'true', sometimes referred to
as 'truthy'. This includes empty hashes and arrays and _any_ number or integer,
including `0`. The only values that evaluate to false on their own are `false`
and `nil`.

## Conditionals

### If Statements

If statements allow us to check if a certain logic condition is true, and if it
is, perform a certain action contained within the code block.

```ruby
money = 20
if money > 10
  going_out_to_lunch = true
end
```

### Else Statements

What happens when we want to check more than one condition? That's where
else comes in.

```ruby
happy_hour = true
if happy_hour
  drinks = market_price * .5
else
  drinks = market_price
end
```

### Elsif

We all know that with lunch options, we like options. Two choices just
aren't going to cut it. How do we set up more options?

```ruby
if vegan && gluten_free
  mood = "thrilled"
elsif vegetarian && gluten_free  
  mood = "satisfied"
elsif gluten_free  
  mood = "content"
else
  mood = "disappointed"
end
```

### Ternary Operators

Ternary operators are a shorthand way of expressing an if/else statement
on one line. This helps shorten the amount of code written. Below, we've
refactored a previous example:

```ruby
happy_hour = true ? market_price * .5 : market_price
```

The ternary operator is most useful in cases where the conditions are
simple, and there are no more than 2 possible outcomes.

### Statement Modifiers

Statement modifiers are a conditional statement that comes at the end of a
statement. It will execute the line of code _if_ the conditional evaluates
accordingly:

```ruby
hot = true
print "Keep oven at 350 degrees" if hot
```

### Unless

The `unless` statement is structured like an `if` statement, but in reverse: The
code block will execute if the conditional evaluates to _false_ rather than true:

```ruby
food = "hot"
unless food == "cold"
   puts "Keep refrigerated or on ice"
end
```

In the above, the text 'Keep refrigerated or on ice' will be displayed because
food is not equal to 'cold.' If there is an `else` statement, it will execute if
the conditional evaluates to _true_:

```ruby
food = "hot"
unless food == "hot"
   puts "Keep refrigerated or on ice"
 else
   puts "Keep oven at 350 degrees"
end
```

This time, 'Keep over at 350 degrees' will be displayed. The `unless` statement
works as a statement modifier as well, allowing us to write the things like
the following:

```ruby
hot = true
print "Keep oven at 350 degrees" if hot
print "Keep refrigerated or on ice" unless hot
```

### Case Statements

Case statements are similar to if statements in that they allow you to
control the flow of your program, and allow you to test multiple
conditions, but they are used to test multiple conditions against one
value. For example:

```ruby
age =  14
case age
when 0 .. 2
   school = "daycare age"
when 3 .. 4
   school = "pre-school age"
when 5 .. 9
   puts "elementary/primary school age"
when 10 .. 13
   puts "middle school age"
when 14 .. 18
   puts "high school age"
when 19 .. 25
   puts "college age"
else
   puts "legal adult"
end
```

The age condition set in this example is being tested against multiple cases
that would determine which school age group a 14 year old might fall into. This
will produce the following result:

```ruby
high school age
```

## Review Looping

Loops are a way to tell our program to perform a certain part of the code a set
number of times until a condition is met. This condition can be hard coded into
the method, or more commonly set by the program itself.

### `loop`

The code is executed in a loop block:

```ruby
loop do
  puts "This code will loop forever."
end
```

The above code is not ideal and will loop continuously. In order to prevent
this, you can set conditions and/or use the break keyword to exit loops based on
certain conditions:

```ruby
i = 0
loop do
  puts "This code will loop forever unless the loop breaks"
  i += 1
  break if i > 4
end
```

This loop will run 5 times before the statement modifier `if i > 4` evaluates to
true and `break` is executed.

### `while`

Using the comparison operators in our loops works, but it is not as clean as a
process as we'd like, and there are much better ways to write them. The `while`
loop is often a better choice. With the `while` loop, _as long as_ a condition
evaluates to true, the loop will continue to fire. The following is valid,
syntactically correct code:

```ruby
i = rand(20)
while i < 20
   puts i
   i += 1
end
```

We could have written this using a standard loop with a break included, but
`while` takes care of that for us.The above code will generate a random number
between 0 and 20 and increment _as long as_ `i` is less than 14. If `i` is
assigned the value 14 to start, it will increment inside the `while` loop until
it reaches 20. In the terminal, the numbers 14 through 19 will be displayed.

Why 19 and not 20? On the very last loop iteration, `i` is incremented to 20,
which causes `i < 20` to evaluate to false, breaking the loop before `puts i`
is executed again.

### Until Loops

Until loops are similar to while loops, but instead are the inverse. Until loops
will keep executing until a specific condition is true. Another way to think
about this concept is "loop while conditional is not true". It loops _until_ the
condition evaluates to true.

```ruby
i = 0
until i == 20
   puts i
   i += 1
end
```

## Conclusion

Conditionals, logic and loops are essential tools for every Ruby programmer.
They are the most common methods for making our programs dynamic and useful.

Both in the programming world and real life, decisions are made and conditions
must be met. We use `if`, `else`, `elsif`, `unless` and `case` statements to
give conditional results and use `while` and `until` statements to iterate until
conditions are met.

## Resources

[Ruby Operators](http://www.techotopia.com/index.php/Ruby_Operators)
[Stack Overflow - Ternary Operators](http://stackoverflow.com/a/4252945)
