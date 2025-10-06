# Homework 1, Problem 1: Understanding Round-off Error

## Part (a)
If $b \gg a$ and $b \gg c$, then $b^2 \gg 4ac$ and the radical is approximately $b$. Any sigfigs from the $4ac$ contribution will be limited by the orders of magnitude difference between $b^2$ and $4ac$. This poses no problem for the $-b - \sim b$ term, but the $-b+\sim b$ term will be near 0 and will not adequately capture the contribution from the $ac$ term. It may have low sigfigs, or in extreme cases where the contribution from $4ac$ to $b^2$ is under machine precision, it may result in an answer of 0 (wrong, as $x=0$ is not a solution to $ax^2 + bx + c = 0$).

## Part (b)
$$
\begin{align*}
x &= \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}* \frac{-b \mp \sqrt{b^2 - 4ac}}{-b \mp \sqrt{b^2 - 4ac}}\\
&= \frac{b^2 - (b^2 - 4ac)}{2a* (-b \mp \sqrt{b^2 - 4ac})}\\
&= \frac{2c}{-b \mp \sqrt{b^2 - 4ac}}
\end{align*}
$$
This formula should be used only for the top case, and the original formula can be used for the bottom case, when $b \gg a$ and $b \gg c$. 