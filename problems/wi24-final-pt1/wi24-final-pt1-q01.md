# BEGIN PROB

Suppose there is a dataset containing $10,000$ integers, the first $2,500$ of them are $3$s, the next $2,500$ of them are $5$s, the next $4,500$ of them are $7$s, and the last $500$ of them are $9$.

# BEGIN SUBPROB

Calculate the median of this dataset.

# BEGIN SOLUTION

$6$

We know there is an even number of integers in this dataset because $10,000 \% 2 = 0$. We can find the middle of the dataset by doing $\frac{10,000}{2} = 5,000$. This means the element in the $5,000$ position and $5,001$ position can give us our median. The element at the $5,000$ position is a $5$ because $2,500 + 2,500 = 5,000$. The element at the $5,001$ position is a $7$ because the next number after $5$ is $7$. We can then plug $5$ and $7$ into the equation:
$$\frac{x_{5,000} + x_{5,001}}{2} = \frac{5 + 7}{2} = 6$$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

How does the mean of this dataset compared to its median?

( ) The mean is larger than the median
( ) The mean is smaller than the median
( ) The mean and the median are equal

# BEGIN SOLUTION

The mean is smaller than the median

We can calculate the mean by doing $$\frac{2,500 * 3 + 2,500 * 5 + 4,500 * 7 + 500 * 9}{10,000} = 5.6$$ Using part A we know that $5.6 < 6$, which means the mean is smaller than the median.

# END SOLUTION

# END SUBPROB

# END PROB