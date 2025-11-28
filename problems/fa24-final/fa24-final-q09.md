# BEGIN PROB

\[(8 points)\] You work for Amazon and are implementing a book genre
classifier to determine whether a book is science fiction (sci-fi),
romance or thriller based on details of the plot. You have a dataset of
18 books and 4 features {"Happy conclusion\","Spaceships\","Murder
investigation\","Sidekick\" } to train a Naïve Bayes classifier.

::: center
  --------- ---------- -------- ---------- ------- ------------
   Book #    Genre     Murder   Sidekick   Happy   Spaceships
      1       sci-fi      No       Yes       Yes       Yes
      2       sci-fi      No       Yes       Yes        No
      3       sci-fi      No        No       Yes       Yes
      4       sci-fi      No       Yes       No        Yes
      5       sci-fi     Yes       Yes       No        Yes
      6       sci-fi      No       Yes       Yes       Yes
      7       sci-fi      No       Yes       Yes       Yes
      8       sci-fi      No        No       No        Yes
      9       sci-fi      No       Yes       No        Yes
     10       sci-fi     Yes       Yes       No        Yes
     11      romance      No        No       Yes       Yes
     12      romance      No       Yes       Yes        No
     13      romance      No       Yes       Yes        No
     14      romance     Yes        No       Yes        No
     15      romance      No        No       Yes        No
     16      romance     Yes       Yes       Yes        No
     17      thriller    Yes       Yes       No         No
     18      thriller    Yes        No       Yes        No
     19      thriller    Yes       Yes       No        Yes
     20      thriller    Yes       Yes       Yes        No
  --------- ---------- -------- ---------- ------- ------------
:::

# BEGIN SUBPROB

($\times$`<!-- -->`{=html}8) A new book has been released which has
'Happy conclusion\", "sidekick\" but not "Spaceships\" or "murder
investigation\". Is this book a sci-fi, thriller or romance? Use the
Naive Bayes Classifier without smoothing. Be sure to clearly state your
prediction as one of the three genres. *Show all your calculations.*

# BEGIN SOLUTION


We estimate the following probabilities from the table:

$$\begin{aligned}
P(\text{Happy} \,|\,\text{romance})         & = 6/6=1     \\
P(\text{sidekick} \,|\,\text{romance})      & = 3/6=1/2   \\
P(\text{No Murder} \,|\,\text{romance})     & = 4/6=2/3   \\
P(\text{No Spaceships} \,|\,\text{romance}) & = 5/6       \\
P(\text{romance})                             & = 6/20=3/10 \\[1em]
P(\text{Happy} \,|\,\text{sci-fi})          & = 5/10      \\
P(\text{sidekick} \,|\,\text{sci-fi})       & = 8/10=4/5  \\
P(\text{No Murder} \,|\,\text{sci-fi})      & = 8/10=4/5  \\
P(\text{No Spaceships} \,|\,\text{sci-fi})  & = 1/10      \\
P(\text{sci-fi})                              & = 10/20=1/2 \\[1em]
P(\text{No Murder} \,|\,\text{thriller})    & = 0/4
\end{aligned}$$

$$\begin{aligned}
& P(\text{romance} \mid \text{Happy,Sidekick, No Murder, No Spaceships}) \\
& \qquad \propto P(\text{Happy}\mid\text{romance}) \times P(\text{sidekick}\mid\text{romance}) \\
& \qquad \qquad \times P(\text{No Murder}\mid\text{romance}) \times P(\text{No Spaceships}\mid\text{romance}) \times P(\text{romance}) \\
& \qquad = 1 \cdot \frac{1}{2}  \cdot \frac{2}{3} \cdot \frac{5}{6} \cdot \frac{3}{10} = \frac{1}{2} \cdot \frac{1}{3} \cdot \frac{1}{2} = \frac{1}{12}
\end{aligned}$$

$$\begin{aligned}
& P(\text{sci-fi} \mid \text{Happy,Sidekick, No Murder, No Spaceships}) \\
& \qquad \propto P(\text{Happy}\mid\text{sci-fi}) \times P(\text{sidekick}\mid\text{sci-fi}) \\
& \qquad \qquad \times P(\text{No Murder}\mid\text{sci-fi}) \times P(\text{No Spaceships}\mid\text{sci-fi}) \times P(\text{sci-fi}) \\
& \qquad = \frac{5}{10} \cdot \frac{4}{5} \cdot \frac{4}{5} \cdot \frac{1}{10} \cdot \frac{1}{2} = \frac{4}{5} \cdot \frac{1}{5} \cdot \frac{1}{10} = \frac{2}{125}
\end{aligned}$$

$$\begin{aligned}
& P(\text{thriller} \mid \text{Happy,Sidekick, No Murder, No Spaceships}) \\
& \qquad \propto P(\text{Happy}\mid\text{thriller}) \times P(\text{sidekick}\mid\text{thriller}) \\
& \qquad \qquad \times P(\text{No Murder}\mid\text{thriller}) \times P(\text{No Spaceships}\mid\text{thriller}) \times P(\text{thriller}) \\
& \qquad = 0
\end{aligned}$$

Since the first probability is the largest, our prediction is that the book was romance.

# END SOLUTION

# END SUBPROB




# END PROB