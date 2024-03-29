# practice.dsc40a.com

Repository containing practice problems for DSC 40A (past exams and discussion). Hosted at practice.dsc40a.com. Before using the repo, make sure you have the following packages installed:

```
- BeautifulSoup4
- pandoc
- lxml
```

### [Here is a walkthrough video](https://www.loom.com/share/cdbc8dcc026c43d6ac48cc2df3f57ea8?sid=202e8678-b073-46ff-91d0-afe775bb2541) of how to edit the site, and [here's another walkthrough video](https://www.loom.com/share/4fb2816102034b14b4b0cd6476091ec3?sid=6529b884-e4c0-4460-8baa-1051c55a4a5f) of how to use the latex-to-practice-site script!

Style guide for writing up problems:

- **Answer:** should be bolded followed by unbolded answer(s), comma separated if it fits on one line, or each answer on a new line if it doesn't fit on one line
- Use () for choose one, [] for select all. Add a space before the text of each answer choice.
- For subsubparts, use numbers followed by period to introduce each question

In translating from Latex to Markdown, there are a few easy find/replace things that help with a lot of things:

\begin{verbatim} --> ```py
\end{verbatim} --> ```
" --> '
\_ --> _
\texttt{ --> `
\textbf{ --> **
\textit{ --> *
\bubble --> ( )
\correctbubble --> ( )
\squarebubble --> [ ]
\correctsquarebubble --> [ ]
\begin{subprobset} -->
\end{subprobset} -->
\begin{subprob} --> # BEGIN SUBPROB
\end{subprob} --> # END SUBPROB
\begin{responsebox} --> # BEGIN SOLUTION
\end{responsebox} --> # END SOLUTION
\begin{soln} --> # BEGIN SOLUTION
\end{soln} --> # END SOLUTION
\bigskip -->
\noindent --> 

Note: ( ) and [ ] need a space between the brackets. There should not be blank lines between options.

To explain up-front:
- All exams are individual (collaboration on exams is never allowed).
- What ( ) and [ ] mean. In their absence, students needed to write out code by hand.
- In-person means on-paper.
- Think of select-all questions as a sequence of true-false questions. Partial credit for these questions was assigned accordingly.
- When taking an exam for practice, we recommend having a copy of the DSC 10 reference sheet open in another tab, as well as a second copy of the exam, so you can access the data descriptions.



