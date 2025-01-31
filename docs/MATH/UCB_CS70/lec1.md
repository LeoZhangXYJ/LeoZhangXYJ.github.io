# Lec1
## Note0
### Significant Sets
- $\mathbb{N}$ denotes the set of all natural numbers {0,1,2,3...}
- $\mathbb{Z}$ denotes the set of all integer numbers {...,-2,-1,0,1,2,...}
- $\mathbb{Q}$ denotes the set of all rational numbers $\left\{\frac{a}{b} \mid a, b \in \mathbb{Z}, b \neq 0\right\}$
- $\mathbb{R}$ denotes the set of all real numbers.
- $\mathbb{C}$ denotes the set of all complex numbers.

### Set Notation Examples
- Empty set: $\emptyset$
- Element of: $a \in A$
- Not an element of: $b \notin B$
- Subset: $A \subseteq B$
- Proper subset: $A \subset B$
- Union: $A \cup B$
- Intersection: $A \cap B$
- Set difference: $A \setminus B$
- Cartesian product: $A \times B$
- Power set: $\mathcal{P}(A)$
- Cardinality: If $A = \{1, 2, 3, 4\}$ then $|A|$ is 4
- For all: $\forall$
- There exists: $\exists$

## Note1
### Proposition
Propositions are statements that are true or false.  
**Propositions should not include fuzzy terms**
- Conjunction: $P \land Q$ (P and Q)
- Disjunction: $P \lor Q$ (P or Q)
- Negation: $\neg P$ (not P)

#### Law of the Excluded Middle
- Tautology: a propositional form that is always true ($P \lor \neg P$)
- Contradiction: a propositional form that is always false ($P \land \neg P$)

### Truth Table
A function table that lists all inputs and outputs.  
Example:

| P   | $\neg$P |
| --- | ------- |
| T   | F       |
| F   | T       |

### Implication
$P \implies Q$ (P implies Q). This is the same as "If P, then Q".  
P -> hypothesis of the implication  
Q -> conclusion  

| P   | Q   | $P \implies Q$ | $\neg P \lor Q$ |
| --- | --- | -------------- | -------------- |
| T   | T   | T              | T              |
| T   | F   | F              | F              |
| F   | T   | T              | T              |
| F   | F   | T              | T              |

So $(P \implies Q) \equiv (\neg P \lor Q)$.  
What's more, if both $P \implies Q$ and $Q \implies P$, then we say "P if and only if Q" (abbreviated "P iff Q"). We write $P \iff Q$.
- Contrapositive: $\neg Q \implies \neg P$
- Converse: $Q \implies P$  
PS: $(P \implies Q) \equiv (\neg Q \implies \neg P)$, these two forms are logically equivalent, we can think of them as "meaning the same thing".

### Quantifiers
Two quantifiers:  
- For all: $\forall$
- There exists: $\exists$  
PS: $\forall x \forall y \equiv \forall y \forall x \equiv \forall x,y$

### Much Ado About Negation
1. De Morgan's Law
	1. $\neg (P \land Q) \equiv (\neg P \lor \neg Q)$
	2. $\neg (P \lor Q) \equiv (\neg P \land \neg Q)$
2. About quantifiers
	1. $\neg (\forall x P(x)) \equiv \exists x \neg P(x)$
	2. $\neg (\exists x P(x)) \equiv \forall x \neg P(x)$

So it has a "flip" attribute.  
$\neg (\forall x \exists y P(x,y)) \equiv \exists x \neg (\exists y P(x,y)) \equiv \exists x \forall y \neg P(x,y)$

## Lecture Note
### Intro
1. Discrete -> separate and distinct
2. Proofs: T or F $\iff$ Program: 1 or 0

### Propositional Logics
1. $1 + 1 = 2$ √
2. The angles of a triangle sum to 180°. √
3. Berkeley is an interesting city. ×  
   'Interesting' is a fuzzy word, it can't be defined exactly.

## Reviews
### DIS 0A
1. $(\exists x \in \mathbb{R}) (x \notin \mathbb{Q})$ is true because $\pi$ is an irrational number.  
   $\mathbb{R}$ means real numbers, you can find it on the number line.  
   $\mathbb{Q}$ means rational numbers, it can be expressed as the ratio of two integers, $\frac{a}{b}$.  
   So transcendental numbers all satisfy $(\exists x \in \mathbb{R}) (x \notin \mathbb{Q})$, such as $\pi$ and $e$.
2. $\forall x \exists y P(x,y) \implies \exists y \forall x P(x,y)$ is not always true.

<iframe src="../DIS/dis0a.pdf" width="100%" height="600px" style="border: none;" title="DIS0A">
This browser does not support PDFs
</iframe>


### HW 00
Convert the English sentences into propositional logic.  
To express the word 'unique', we can use two statements connected with an 'and':
1. A solution exists.
2. Two solutions have to be the same.

Example:  
For every real number $k$, there is a unique real solution to $x^3 = k$.  
$(\forall k \in \mathbb{R}) [ (\exists x \in \mathbb{R})(x^3 = k) \land (\forall y,z \in \mathbb{R}) ( ((y^3 = k) \land (z^3 = k)) \implies (y = z))]$  
$(\exists x \in \mathbb{R})(x^3 = k)$ -> a solution exists.  
$(\forall y,z \in \mathbb{R}) ( ((y^3 = k) \land (z^3 = k)) \implies (y = z))$ -> Two solutions have to be the same.

<iframe src="../HW/hw00.pdf" width="100%" height="600px" style="border: none;" title="HW00">
This browser does not support PDFs
</iframe>
