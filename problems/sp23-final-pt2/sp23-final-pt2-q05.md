# BEGIN PROB

<i>Originally Problem 5 on the Spring 2023 Final Part 2</i>

You're interested in seeing the Milky Way in the night
sky, which you have sometimes been able to do when conditions are right.
For each night that you've attempted to see the Milky Way, you have a
record of:

-   the setting (urban, suburban, or rural),

-   the season (winter, spring, summer, or fall),

-   the time (late night, or early morning), and

-   the outcome (successful, or unsuccessful).

These 12 attempts are recorded in the table below.


  |**setting** &emsp;|  **season** &emsp;|  **time** &emsp;&emsp;&emsp;&emsp;&emsp;    |  **outcome** &emsp; |
  |-------------|------------|---------------|--------------|
  |suburban     |winter      |late night     |successful|
  |rural        |spring      |late night     |successful|
  |urban        |winter      |early morning  |successful|
  |rural        |winter      |early morning  |successful|
  |rural        |summer      |late night     |unsuccessful|
  |urban        |winter      |late night     |unsuccessful|
  |rural        |winter      |early morning  |unsuccessful|
  |rural        |spring      |late night     |unsuccessful|
  |urban        |fall        |early morning  |unsuccessful|
  |suburban     |summer      |late night     |unsuccessful|
  |urban        |winter      |late night     |unsuccessful|
  |rural        |winter      |late night     |unsuccessful|


You want to use a Naive Bayes classifier to predict whether you'll be
successful in seeing the Milky Way under the following conditions:

-   the setting is urban,

-   the season is winter, and

-   the time is late night.

Naive Bayes predicts that, under these conditions, the probability you
are unsuccessful is $k$ times the probability you are successful, for an
integer value of $k$. What is $k$?

( ) $k=1$
( ) $k=2$
( ) $k=3$
( ) $k=4$

# BEGIN SOLUTION

$k=3$

# END SOLUTION

# END PROB