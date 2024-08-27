#core/mathematicalphysics

A transition probability matrix, also known as a stochastic matrix or Markov matrix, is a **square matrix used to describe the transitions of a Markov chain.** It is a key tool for modelling how a system changes between different states over time.

Specifically, each entry $(i,j)$ in a transition probability matrix represents the probability of moving from state $i$ to state $j$ in one time step, denoted $p_{ij}$. The entries must be non-negative real numbers between 0 and 1, and each row must sum to 1, since the system must transition to one of the states in the next step.

For example, consider a simple weather model with two states: “Sunny” and “Rainy”. The transition probability matrix might look like:

$$
P = 
\begin{bmatrix}
0.8 & 0.2\\
0.6 & 0.4
\end{bmatrix}
$$

This means there is an 80% chance of a sunny day being followed by another sunny day, a 20% chance of a sunny day being followed by a rainy day, and so on.

Some key properties and applications of transition matrices include:

- The long-term behaviour of the Markov chain can be studied by taking powers of the transition matrix. The $n$-step transition probabilities $p_{ij}^{(n)}$ are given by the entries of the matrix $P^n$.
- Under certain conditions, the Markov chain will converge to a steady-state distribution $\pi$, which is a row vector satisfying $\pi P = \pi$. This represents the long-run proportion of time the chain spends in each state.
- Transition matrices are used to model stochastic processes in a wide variety of fields, including economics, queueing theory, genetics, and machine learning.
- In finance, transition matrices are used for credit risk modelling to describe the probabilities of firms moving between different credit ratings over time.

So in summary, transition probability matrices provide a concise way to represent and analyse the probabilistic transitions of a system between a finite number of states, which has extensive applications for modelling real-world stochastic processes.
