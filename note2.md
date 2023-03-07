# Meeting - Mar 2, 2023

## Convert quadratic program to linear program
According to the [paper](https://link.springer.com/article/10.1007/s10288-020-00460-z), we can convert binary quadratic programs to linear programs. 
$$x_ax_b \rightarrow x_{ab}$$
$$
\begin{equation}
\chi_{\mathbb{Q}}(x)=
    \begin{cases}
        1 & \text{if } x \in \mathbb{Q}\\
        0 & \text{if } x \in \mathbb{R}\setminus\mathbb{Q}
    \end{cases}
\end{equation}
$$
