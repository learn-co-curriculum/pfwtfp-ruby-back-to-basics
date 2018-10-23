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
- Review Logic and Conditionals
  - If Statements
  - Ternary Operators and Statement Modifiers
  - Case Statements
- Review Looping
  - While Loops
  - Until Loops


### Review Logic and Conditionals
Logic and conditionals is a group name that covers if statements, ternary
operators, statement modifiers, and case statements. Think of a real life
scenario where you would need to make a decision based on certain
conditions. For example, `if` it's raining outside, you take a rain jacket
or umbrella. In the context of web technology, `if` you're logged in, you
can see content specific to a registered user, if not (or `else`), you may
see a marketing page or log in screen.

#### If Statements
If statements allow us to check if a certain condition exists, and if it
does, to perform a certain action contained within the code block.
``` money = 20
if money > 10
  going_out_to_lunch = true
end
```

#### else
What happens when we want to check more than one condition? That's where
else comes in.
``` happy_hour = true
if happy_hour
  drinks = market_price * .5
else 
  drinks = market_price
end
```
#### elseif
We all know that with lunch options, we like options. Two choices just
aren't going to cut it. How do we set up more options?
``` 
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

#### Ternary Operators
Ternary operators are a shorthand way of expressing an if/else statement
on one line. This helps shorten the amount of code written. Below, we've
refactored a previous example:

```
happy_hour = true ? market_price * .5 : market_price
```
The ternary operator is most useful in cases where the conditions are
simple, and there are no more than 2 possible outcomes.

#### Statement Modifiers
Statement modifiers are a conditional statement that comes at the end of
a statement. It will execute the code `if` conditional is false. If the
conditional is true, code specified in the else clause is executed.

The standard `unless` statement looks like the following:
```
food = "hot" 
unless food == "hot"
   puts "Keep refrigerated or on ice"
 else
   puts "Keep oven at 350 degrees"
end
```
And `unless` modifier can also use both `if` and `unless`.

```
hot = true
print "Keep oven at 350 degrees" if hot
print "Keep refrigerated or on ice" unless hot
```

#### Case Statements
Case statements are similar to if statements in that they allow you to
control the flow of your program, and allow you to test multiple
conditions, but they are used to test multiple conditions against one
value. For example:
```
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
The age condition set in this example is being tested multiple cases that
would determine which school age group a 14 year old might fall into.
This will produce the following result:
```
high school age
```

### Review Looping
Loops are a way to tell our program to perform a certain part of the
code a set number of times until a condition is met. This condition
can be hard coded into the method, or more commonly set by the program
itself. 

#### `loop`
The code is executed in a loop block:
```
loop do
  puts "This code will loop forever."
end
```
The above code is not ideal and will loop continuously. In order to
prevent this, you can set conditions and/or use the break keyword to exit
loops based on certain conditions.

#### While Loops
While using the comparison operators in our loops works, it is not a
clean as a process as we'd like, and there's a much better way to
write them. The do in this case is optional. The following is valid,
syntactically correct code:
```
i = rand(20)
while i < 20
   break if i == 13
   puts i
   i += 1
end
```
The above code will generate a random number between 0 and 20 and
increment until 20. Let's say that 13 is an unlucky number, so we will
break the loop when `i` reaches that value. If we get 14 as our result,
it will continue to increment until it reaches 20.

#### Until Loops
Until loops are similar to while loops, but instead are the inverse.
Until loops will keep executing until a specific condition is true.
Another way to think about this concept is "is not". It is a similar
concept as the `unless` conditional. It loops until a true condition
is met.
```
i = 0
until i == 20
   puts i
   i += 1
end
```

## Conclusion
These Ruby basics are an essential tool used to create loops and 
conditions that give results based on certain criteria. Both in the
programming world and real life, decisions are made and conditions
must be met. We use `if`, `else`, `elsif`, and `case` statements to
give conditional results and `while` and` until` statements to iterate 
until conditions are met. 

## Resources
[Ruby Operators](http://www.techotopia.com/index.php/Ruby_Operators)
[Stack Overflow - Ternary Operators](http://stackoverflow.com/a/4252945)
