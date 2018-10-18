# Ruby Back to Basics
## Introduction
Every day, we control how our life flows. This morning, before you got out of bed, you probably pushed the blanket off. You walked into the bathroom to brush your teeth. Then you sat down at the computer to read this README. When you're hungry, you'll grab a snack. As humans, we use logic to control how our days flow without much thought to the process behind it. Computers need a bit more guidance. Logic and conditional statements in Ruby allow you to control how your program works. Loops allow you to tell a program to repeat a portion of code until a certain condition is met. 

## Learning Goals

- Review Logic and Conditionals
  - If Statements
  - Ternary Operators and Statement Modifiers
  - Case Statements
- Review Looping
  - While Loops
  - Until Loops


### Review Logic and Conditionals
Logic and conditionals is a group name that covers if statements, ternary operators, statement modifiers, and case statements. 

#### If Statements
If statements allow us to check if a certain condition exists, and if it does, to perform a certain action contained within the code block. 
``` money = 20
if money > 10
  going_out_to_lunch = true
end
```

#### else
What happens when we want to check more than one condition? That's where else comes in. 
- Add in more code examples

#### elseif
We all know that with lunch options, we like options. Two choices just aren't going to cut it. How do we set up more options? 
- Code snippets here


#### Ternary Operators
- It's a way of expressing an if and an else statement together on one line
Why use the ternary operator?
- Helps shorten code (show refactor of above if/else statement to ternary operator)
When not to use ternary operator?
- When it adds complexity

#### Statement Modifiers
Statement modifiers are a conditional statement that comes at the end of a statement. 
- Can use both `if` and `unless`
- Show code snippets for both

#### Case Statements
Case statements are similar to if statements in that they allow you to control the flow of your program, and allow you to test multiple conditions, but they are used to test multiple conditions against one value. 
- set a condition
- test against the condition
- write the code examples

### Review Looping
Loops are a way to tell our program to perform a certain part of the code a set number of times until a condition is met. This condition can be hard coded into the method, or more commonly set by the program itself. 

#### `loop`
The code is executed in a loop block:
```
loop do
  puts "This code will loop forever."
end
```
- break keyword
- loop counters (using +=) (I'm not sure if we should even go into these manual loop counters - while loops are so much better)

#### While Loops
While using the `+=` operator in our loops works, it is not a clean as a process as we'd like, and there's a much better way to write them. 
- Code examples

#### Until Loops
Until loops are similar to while loops, but they are the inverse. Until loops will keep executing until a specific condition is true. Another way to think about it is "is not":
- Code example

## Conclusion
- wrap up
## Resources
[Ruby Operators](http://www.techotopia.com/index.php/Ruby_Operators)
[Stack Overflow - Ternary Operators](http://stackoverflow.com/a/4252945)
