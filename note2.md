# Meeting - Mar 2, 2023

## Convert quadratic program to linear program
According to the [paper](https://link.springer.com/article/10.1007/s10288-020-00460-z), we can convert binary quadratic programs to linear programs. 
$$x_ax_b \rightarrow x_{ab}$$

$$
\begin{cases}
x_{ab} \geq x_a + x_b -1,\\
x_{ab} \leq x_{a}\\
x_{ab} \leq x_{b}\\
0 \leq x_{ab} \leq 1
\end{cases}
$$ <br>

These expressions are equivalent when $x_a, x_b \in \\{0,1\\}$ <br>
However, these are not equivalent when $x_a, x_b \in [0,1]$ <br>

For example, when $x_a=0.2, x_b=0.5$, $x_{ab}$ should be 0.1 <br>
However, for the contrains metioned above, $0 \leq x_{ab} \leq 0.2$ <br>
$x_{ab} = 0.1$ is included in the range, but we are unable to get it percisely.

Another example: when $x_a=0.8, x_b=0.8$, $x_{ab}$ should be 0.64 <br>
However, for the contrains metioned above, $0.6 \leq x_{ab} \leq 0.8$ <br>

## Connect to our problem
In our problem, 
$$h_{sp} = X_{sp} \cdot (\sum_{s'=1}^n X_{s'p} \cdot F_{s,s'}) = \sum_{s'=1}^n X_{sp} \cdot X_{s'p} \cdot F_{s,s'} = \sum_{s'=1}^n Y_{sps'p} \cdot F_{s,s'}$$ <br>
We know that, 
$$f(X_{LP\\{0,1\\}}^* , Y_{LP\\{0,1\\} }^* ) = g(X_{QP\\{0,1\\}}^* )$$
$$f(X_{LP[0,1]}^* , Y_{LP[0,1] }^* ) \geq g(X_{QP[0,1]}^* ) \geq g(X_{LP[0,1]}^* )$$ <br>
It is not sure whether
$$g(X_{QP[0,1]}^* ) = g(X_{LP[0,1]}^* )$$
