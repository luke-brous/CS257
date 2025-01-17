# Shut the Box

Team members (edit these):
1. Luke Broussard
2. Jaylen 
3. Team member 3...

## Before you begin...

There are a few things that you should know about this lab assignment:

1. It is a _pair programming_ activity. Pair programming is a software
   development practice where two programmers sit side-by-side at the same
   computer and work together to develop a program. One programmer is the
   _driver_--they type and edit the code, explaining what they are doing. The
   other programmer is the _navigator_, who should be thinking about the big
   picture, offering advice and suggestions, and __asking questions__. The
   members of a pair programming team should be in __constant conversation__ so
   that they can switch roles at any moment.

2. You will be editing this file using [markdown](https://commonmark.org/help/).
   You will write your answers in this file, and this edited file will be what you submit for your lab submission. 
   You can switch back and forth between viewing and
   editing this file using the "preview" button in the top right of this window.

3. This is a POGIL (Process Oriented Guided Inquiry Learning) activity. It will
   introduce concepts to you through guided inquiry. This pedagogy is proven to
   be extremely effective in helping students to understand topics and materials
   on a deeper level. Throughout the course, we will be using POGIL for lab
   activities.

   POGIL activities are structure where you are guided through the _learning
   cycle_ of exploration, concept invention, and application. This cycle is
   backed by the psychology of learning, and there are numerous studies that
   show that this is more effective than lecture.

4. Each person on the team should have their own copy of this file, but you
   should choose to work in __one__ team member's markdown file. When you are done with
   the lab, this team member should share their file with the rest of the team.

   You should note who you worked with at the top of this file.

## Goals

By the time that you are done with this activity, you and your partner should be
able to:

* declare and create arrays and access their elements,
* use and explain parts of for loops,
* and work more effectively as a team.

## Playing the Game

Run ShutTheBox.java to play the game. It is a one-player game, so you and
your partner should play once or twice before getting together to answer the
questions.

Each person on the team should play the game on their own a few times
(limit yourself to ~5 minutes).

1. Are you done playing and ready to work together as a team?

Yes!

Note that for the rest of these questions, you may need to go back and play the
game again to answer some of the questions to come. But you should do so
__deliberately__, in order to find something out, not just because you got bored
with the conversation or thought you could answer a question better on your own.

2. What constitutes winning a game?

Closing all the levers, all levers are down.

3. What constitutes an illegal move?

Closing a lever that is already closed.

4. Assuming you make no illegal moves but don't win, when does the game end?

Legally closing levers that don't add up to the number that is rolled.

5. If you get a score, how is your score determined?

Sum of the levers that haven't been closed yet.

6. Under what circumstances do you roll a different number of dice?

When the levers, 7,8,9, are all closed.

7. Did all team members reach consensus on your answers to the previous
   questions? 

Yes!

## Stop here and check in with me 

If your team couldn't reach consensus, grab me for a quick discussion. If they
could, keep moving!

8. What is a good strategy for this game? For example, is it better to close the
   levers with smaller or larger numbers first? Why?

The best strategy is to close the levers with the biggest numbers first. 
The longer you can keep the smaller levers the better. That way you
have more options to choose from the longer the game goes.

## Arrays

Now examine the `main` function in the Java file.

9. The line
   
   `int score = 45;`

   declares a variable `score` and gives it an initial value of 45. What is the
   type of the variable declared on the line below?

   `boolean[] closed = new boolean[10];`

It creates a boolean array.

10. In the line
   
   `int roll = StdRandom.uniform(1, 7);`

   the initial value of the variable `roll` is given by the expression
   `StdRandom.uniform(1, 7)`. In the line below, what expression gives the
   initial value of `closed`?

   `boolean[] closed = new boolean[10];`

new boolean[10] creates the closed array with an initial size of 10, with all values 
initialized to 0.

For the next several questions, you will have to temporarily add some code to
the program. You might want to leave a couple of blank lines around your
additions so that you can easily return the program to its original state after
you're done.

11. After the line

   `boolean[] closed = new boolean[10];`

   add:

   `StdOut.println(closed[3]);`

   What does this cause the program to print? (When you run the program, the new
   output will appear after the instructions but before the first run.)

It prints false. 

12. What happens if you print `closed[30]` instead?

It returns an error: Index 30 out of bounds for length 10.

13. What are the limits on the number you can put between the square brackets in
   an array indexing expression like those in the two previous questions?

The limit is from 0-9.

14. What is printed if you add the following two lines?

   ```
   closed[2] = true;
   StdOut.println(closed[2]);
   ```

It prints true.

15. Is `int[]` a valid type?

Yes it is.

## Stop here and check in with me

We might have a discussion here. Raise your hand and I will come to your group. If I ask you to wait here before continuing, your group can
discuss the following question:

16. What syntax would you use to create an array __of arrays__ of booleans
   (_i.e._, a 2-dimensional array)? There are several reasonable guesses.
   Experiment to find one that works.

boolean[][] my_array = new boolean[5][5]

## For loops

Return your program to its original state by deleting any new code that you
added. The undo function in your editor may be useful.

17. A for loop begins with the keyword `for`. How many for loops appear in this
   program?

3 for loops.

Here is a template for a while loop:

```
while (boolean expression) {
  statement
  ...
}
```

An _expression_ is a piece of code that has a value, such as `"hello"` or `x +
5`. More specifically, a _boolean expression_ is an expression with a value of
type boolean, such as `true` or `score == 0`. A _statement_ is a "complete
sentence" of code that does something, like

`StdOut.println("Shut the Box");`

or:

`int score = 45;`

18. Write a template for a for loop, similar to the one for while loops that is
   directly above. Note that there are three parts within the parentheses,
   separated by semicolons. Two of these parts are statements; the other is a
   boolean expression.

for (int i = 0;i < 10;i++) {
   statement

}

19. How many times does the for loop below run?

   ```
   for (int i = 1; i <= 9; i++) {
     StdOut.println(i);
   }
   ```

   You can determine this by adding a println statement in the loop, or putting
   this code in your file.

__answer__

20. What is the value of the local variable `i` on the first pass through the
   loop?

__answer__

21. What is the value of the local variable `i` on the last pass through the
   loop?

__answer__

22. Consider the first part of a for loop within the parentheses (_e.g._, `int i
   = 0`):

   Does it run only once, or every pass through the loop?

   Does it run before or after the statements between the curly braces?

__answer__

23. Consider the second part of a for loop within the parentheses (_e.g._, `i <
   count`):

   Does it run only once, or every pass through the loop?

   Does it run before or after the statements between the curly braces?

__answer__

24. Consider the third part of a for loop within the parentheses (_e.g._, `i++`):

   Does it run only once, or every pass through the loop?

   Does it run before or after the statements between the curly braces?

__answer__

25. How would you modify the loop so that it prints the numbers counting down
   from 9 to 1, instead of up from 1 to 9?

__answer__

26. Did your team have any conflicts while working on this activity? If so, how
   did you resolve them?

__answer__

## Stop here and check in with me

Raise your hand and I will check in with your group. In the meantime,
discuss the following:

27. Could a for loop be placed inside another for loop? If so, how? If not, why
   not?

__answer__


<sub>This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.
It is adapted from “Shut the Box” by Peter Drake.</sub>
