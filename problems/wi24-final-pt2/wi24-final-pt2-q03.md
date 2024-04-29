# BEGIN PROB

<i>Originally Problem 3 on the Winter 2024 Final Part 2</i>

With the help of the Alien from Bayesian Galaxy, Issac
built a Little Hadron Collider in his garage to continue testing some
fundamental principles of nature. The alien set up a fixed target at one
end of the collider, and ask Issac to shoot quarks from the other end.
Everytime the quark hit the target, the Alien will tell Issac whether a
new hadron is formed or not. Due to the energy limitation in Issac's
garage, he could only generate up, down, top, and bottom quarks (Strange
and Charm quark would have consumed too much energy). For each quark
Issac created, he has a record of:

-   the type \[up, down, top, bottom\]

-   the state \[particle, antiparticle\]

-   the color charge \[red, green, blue\], and

-   the outcome \[hadron formed, hadron not formed\]

Issac created 10 quarks, and these 10 quarks are recorded in the table
below.

::: center
  **type**   **state**      **color**   **Formed Hadron**
  ---------- -------------- ----------- -------------------
  down       particle       green       formed
  top        particle       red         formed
  top        antiparticle   blue        formed
  up         particle       red         formed
  up         antiparticle   blue        formed
  bottom     antiparticle   red         not formed
  down       antiparticle   blue        not formed
  down       particle       blue        not formed
  top        particle       green       not formed
  up         antiparticle   green       not formed
:::

Since the alien is from Bayesian galaxy, they want Issac to develop a
Naive Bayes classifier to predict whether he'll be successful in forming
a hadron under the following quark conditions:

-   the type is up

-   the state is particle

-   the color is blue

# BEGIN SUBPROB

(4 points) Naive Bayes predicts that, given a up-particle-blue quark,
the probability a hadron formed is k times the probability a hadron is
not formed, for an integer value of k. What is k?

( ) 1
( ) 2
( ) 3
( ) 4

# BEGIN SOLUTION

3

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

(4 points) What would be the value of k if you change up quark in the
previous collision to top quark, but keep everything else the same (i.e.
top-particle-blue quark)?

( ) 1
( ) 2
( ) 3
( ) 4

# BEGIN SOLUTION

3

# END SOLUTION

# END SUBPROB

# END PROB