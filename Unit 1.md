### Basics of Quantum Information

#### Lesson 1: Single Systems
- single system in isolation

##### 1. Classical Information
Consider a physical system that stores information: let us call it `X`
Assume `X` can be in one of a finite number of `classical states` at each moment
Denote this classical state set by $\sigma$

###### Examples:
- If X is a bit, then its classical state set is $\sigma = \{0,1\}$.
- If X is a six-sided die, then $\sigma=\{1,2,3,4,5,6\}$
- If X is a switch on a standard electric fan, then perhaps $\sigma=\{high, medium,low,off\}$.

There may be `uncertainty` about the classical state of a system, where each classical state has some `probability` associated with it.

For example, if X is a bit, then perhaps it is in the classical state 0 with probability 3/4 and in the classical state 1 with probability 1/4. This is a `probabilistic state` of X
$$
Pr(X=0)=\frac{3}{4} \; and \; Pr(X=1)=\frac{1}{4}
$$
A succinct way to represent this probabilistic state is by a `column vector`
$$
(\frac{\frac{3}{4}}{\frac{1}{4}})
$$
This vector is a `probability vector`
- All entries are nonnegative real numbers.
- The sum of the entries is 1.

###### Dirac notation (first part)
Let $\sum$ be any classical state set, and assume the elements of $\sum$ have been placed in correspondence with the integers 1,...,$|\sum|$

We denote by $\ket{a}$ the `column vector` having a 1 in the entry corresponding to $a \in \sum$, with 0 for all other entries.

###### Example 1:
If $\sum=\{0,1\}$, then
$$
\ket{0} = \begin{pmatrix}1\\0\end{pmatrix} \; and \; \ket{1} = \begin{pmatrix}0\\1\end{pmatrix}
$$

###### Example 2:
If $\sum=\{♣, ♦, ♥, ♠\}$, then we might choose to order these states like this:
♣, ♦, ♥, ♠. This yields
$$
\ket{♣} = \begin{pmatrix}1\\0\\0\\0\end{pmatrix} \;\; \ket{♦} = \begin{pmatrix}0\\1\\0\\0\end{pmatrix} \;\; \ket{♥} = \begin{pmatrix}0\\0\\1\\0\end{pmatrix} \;\; \ket{♠} = \begin{pmatrix}0\\0\\0\\1\end{pmatrix}
$$
Vectors of this form are called `standard basis vectors`. Every vector can be expressed uniquely as a linear combination of standard basis vectors.
$$
\begin{pmatrix}\frac{3}{4}\\\frac{1}{4}\end{pmatrix}=\frac{3}{4}\ket{0}+\frac{1}{4}\ket{1}
$$
###### Measuring probabilistic states
What happens if we `measure` a system X while it is in some probabilistic state?
We see a `classical state`, chosen at random according to the probabilities.
Suppose we see the classical state $a\in\sum$
This changes the probabilistic state of X (from our viewpoint): having recognized that X is in the classical state $a$, we now have
$$
Pr(X=a)=1
$$
 This probabilistic state is represented by the vector $\ket{a}$
###### Example:
Consider the probabilistic state of a bit X where
$$
Pr(X=0)=\frac{3}{4}\;and\;Pr(X=1)=\frac{1}{4}
$$
Measuring X selects (or reveals) a transition, chosen at random
$$
\frac{3}{4}\ket{0}+\frac{1}{4}\ket{1}
$$
###### Deterministic operations
Every function $f:\sum\rightarrow\sum$ describes a `deterministic operation` that transforms the classical state $a$ into $f(a)$, for each $a\in\sum$
Given any function $f:\sum\rightarrow\sum$, there is a (unique) matrix $M$ satisfying
$$
M\ket{a}=\ket{f(a)}\;(for\;every\;a\in\sum)
$$
This matrix has exactly one 1 in each column, and 0 for all other entries:
$$
M(b,a)=\begin{cases}
1 & b = f(a)\\
0 & b \neq f(a)
\end{cases}
$$
The action of this operation is described by `matrix-vector multiplication`
$$
v\mapsto Mv
$$
###### Example:
For $\sum=\{0, 1\}$, there are four functions of the form $f:\sum \rightarrow \sum$

$$
\begin{array}{c|SSS}
  a    & f_1(a) \\
  \hline
  0 & 0 \\
  1 & 0 
\end{array}
\;\;\;\;\;\;\;\;
\begin{array}{c|SSS}
  a    & f_2(a) \\
  \hline
  0 & 0 \\
  1 & 1 
\end{array}
\;\;\;\;\;\;\;\;
\begin{array}{c|SSS}
  a    & f_3(a) \\
  \hline
  0 & 1 \\
  1 & 0 
\end{array}
\;\;\;\;\;\;\;\;
\begin{array}{c|SSS}
  a    & f_4(a) \\
  \hline
  0 & 1 \\
  1 & 1 
\end{array}
$$
Here are the matrices corresponding to these functions:
$$
M_1=\begin{pmatrix} 1 & 1 \\ 0 & 0\end{pmatrix}
\;\;\;\;\;
M_2=\begin{pmatrix} 1 & 0 \\ 0 & 1\end{pmatrix}
\;\;\;\;\;
M_3=\begin{pmatrix} 0 & 1 \\ 1 & 0\end{pmatrix}
\;\;\;\;\;
M_4=\begin{pmatrix} 0 & 0 \\ 1 & 1\end{pmatrix}
$$
##### 2. Quantum Information

###### a. Quantum state vectors
###### b. Standard basis measurements
###### c. Unitary operations

##### Descriptions of quantum information
###### Simplified description
- Quantum states are represented by `vectors;` operations are represented by `unitary matrices`
- Sufficient for an understanding of most quantum algorithms

##### General description
- More general and more broadly applicable
- Quantum states are represented by `density matrices;` allows for a more general class of measurements and operations
- Includes both the simplified description and classical information (including probabilistic states) as special cases

