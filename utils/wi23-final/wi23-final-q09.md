# BEGIN PROB

**Naive Bayes Classifier** In the following \"Symptoms\" dataset, the
task is to diagnose whether a person is sick. We use a representation
based on four features per subject to describe an individual person.
These features are \"running nose\", \"coughing\", and \"fever\", each
of which can take the value true ('+') or false ('--').

![Symptoms dataset](Q5a){#fig:my_label width="40%"}

# BEGIN SUBPROB

\[4 points\] What is the predicted class for a person with running nose
but no coughing, and no fever? Use Naive Bayes classifier.

::: responsebox
3.5in We have to compare $$\begin{aligned}
    p_+=P(N,\bar C,\bar F|+)P(+)\quad \text{and}\quad p_-=P(N,\bar C,\bar F|-)P(-).
\end{aligned}$$ $$\begin{aligned}
    &P(+)=\frac35 \quad P(-)=\frac25\quad P(N,\bar C,\bar F|+)=P(N|+)P(\bar C|+)P(\bar F|+)=\frac23\times \frac13\times\frac13=\frac{2}{27}\\
    &P(N,\bar C,\bar F|-)=P(N|-)P(\bar C|-)P(\bar F|-)=\frac12\times \frac12\times 1=\frac{1}{4}.
\end{aligned}$$ Then, $$\begin{aligned}
    p_+=\frac35\times\frac{2}{27}=\frac{2}{45}\quad p_-=\frac25\times\frac{1}{4}=\frac{1}{10}>p_+
\end{aligned}$$ So predicted class is Healthy(-).
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB # BEGIN SUBPROB

\[1 point\] What is the predicted class for a person with running nose,
and fever but no coughing? Use Naive Bayes classifier.

::: responsebox
2 in

Since $P(F|-)=0$, $P(N,\bar C, F|-)=P(N|-)P(\bar C|-)P(F|-)=0$ whereas
$P(F|+)=2/3$. So $p_+>p_-$. So predicted class is Sick(+).
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB # BEGIN SUBPROB

\[3 points\] To deal with cases of unseen feature, we used "smoothing\"
in class. If we use the "smoothing\" method discussed in class, then
what is the probability of a person having running nose, and fever but
no coughing if that person was diagnosed "healthy\"?

::: responsebox
3 in $$\begin{aligned}
          P(N,\bar C, F|-)=P(N|-)P(\bar C|-)P(F|-)=\frac24\times \frac24\times \frac14=\frac{1}{16}.
     
\end{aligned}$$
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

\[2 points\] In part (a), what are the odds of a person being "sick\"
who has running nose but no coughing, and no fever?

::: responsebox
2 in Probability of being sick who has running nose but no coughing, and
no fever, $$\begin{aligned}
         P(+|N,\bar C,\bar F)=\frac{p_+}{P(N,\bar C,\bar F)}=\frac{\frac{2}{45}}{\frac{1}{5}}=\frac29.
     
\end{aligned}$$ $$\begin{aligned}
            \text{Odds of being sick}=\frac{P(+|N,\bar C,\bar F)}{1-P(+|N,\bar C,\bar F)}=\frac27.
        
\end{aligned}$$
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB # BEGIN SUBPROB

\[2 points\] Say someone fit a logistic regression model to a dataset
containing $n$ points $(x_1,y_1),(x_2,y_2),\cdots,(x_n,y_n)$ where
$x_i$s are features and $y_i\in\{-1,+1\}$ are labels. The estimated
parameters are $w_0,~w_1$, that is, given feature $x$, the predicted
probability of belonging to class $y=+1$ is $$\begin{aligned}
        P(y=+1|x)=\frac{1}{1+\exp(-w_0-w_1x)}.
    
\end{aligned}$$ Interpret the meaning of $w_1=1$.

::: responsebox
1.5 in If $x$ is increased by $1$, then the odd of $y=+1$ increases
$\exp(1)=2.718$ times.
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# END PROB