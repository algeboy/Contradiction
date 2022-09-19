
# Don't Contradict Me
`CC-BY James B. Wilson, 2022`

> Proof by contradiction is dangers because if you make a mistake it helps you.     -J.P. Serre.

Many an author and speaker argue indirectly 

What counts as a "contradiction"?  You might have been seen sentences such as this:
\[
    P \vee \neg P
\]
\[
    \neg(P\wedge \neg P)
\]


There are a number of places you may have encountered contradictions in your reasoning and used this to retreat to an early state of assumptions, adjust, and restart.
There are many facts that we can prove, but a mystery sets in when all we can do is prove something cannot be false.  What 


Should we assume therefore that it is true?  Before you decide it will help to consider some situations.

Consider computer programs


> **Theorem (v.1).** The set of real numbers is uncountable.
> **Theorem (v.2).** It is **not** the case that the set of real numbers is countable.



Is this a contradiction or simply 
Reaching a contradiction whether formally or is a sign that something has 


It is understood some claims 

 are difficult to fathom 
There are many books and professors of mathematics who will attempt to support an argument by arguing towards a contradiction.  The warning of J. P. Serre There is a fine distinction to be made here.Others will nurse a position that something false can logically infer something true, which seems to undercut whatever might be really meant by logical inference.

## Review of propositional logic.

### Sequents

We let expressions be denoted by variables $P, Q,P_1,P_2,\ldots$.  We need a way to separate assumptions from conclusions and the following notations introduced by Frege are commonly accepted today.
\[
    P_1,\ldots,P_n\vdash Q
    \qquad
    \begin{array}{c}
    P_1\\
    \vdots\\
    P_n\\
    \hline
    Q
    \end{array}
\]
The **turnstyle** $\vdash$ is read as **leads to** or **entails**.  Gentzen formalized logic to these symbols calling each term a **sequent** as they take place in a sequence.  



### And (Conjunction)

Assume there is a context $\Gamma$ of assumed propositions.

We agree to **introduce** a conjunction symbol $\wedge$ under the following conditions.
\[
    \begin{array}{l}
        \Gamma\vdash P\\
        \Gamma\vdash Q\\
    \hline
        \Gamma \vdash P\wedge Q
    \end{array} (Intro_{\wedge})
\]
We agree to **eliminate** a conjunction symbol $\wedge$ under these conditions.
\[
    \frac{
        \Gamma\vdash P\wedge Q
    }{
        \Gamma\vdash P
    }(Elim_{\wedge-})
    \qquad
    \frac{
        \Gamma\vdash P\wedge Q
    }{
        \Gamma\vdash Q
    }(Elim_{-\wedge})    
\]

## Implication.

We introduce the implication symbol $\Rightarrow$
\[
    \frac{
        \Gamma, (P)\vdash Q
    }{
        \Gamma \vdash P\Rightarrow Q
    }(Intro_{\Rightarrow})
    \qquad
    \begin{array}{l}
    \Gamma \vdash (P \Rightarrow Q)\\
    \Gamma \vdash P\\
    \hline 
    \Gamma\vdash Q
    \end{array}(Elim_{\Rightarrow})
\]
Here $(P)$ means that $P$ may occur any number of times up to and including $0$ times in preceeding $Q$.   So it is said that we **may assume** $P$ to derive $Q$.  If that condition is meet we may now write $P\Rightarrow Q$.

Notice if we omit $P$ we still may rely on any proposition and axioms in the context $\Gamma$ to derive $Q$.  Thus it is not by magic that $Q$ may be derived from the absence of $P$.  In particular one should avoid the impression that 
> false may logically lead to true''.  

Rather it is that
> Context may lead to truth even when combined with false.

The difference between $(P)\vdash Q$ and $P\Rightarrow Q$ is that the former is the actual process of deduction, where as $\Rightarrow$ is merely a symbol representing to the language that a deduction was made.

### Falsity

There is one symbol $\bot$ that is extremal in that it has no introduction, and every elimination.
\[
    \frac{\bot}{~P~}(Elim_{\bot})
\]
If we assign this situation meaning (semantics) then it is declaring that should $\bot$ ever be present then everything follows, both true and false.  So the presence of $\bot$ is a declaration that our logic has failed, all things are true and truth ceases to have meaning.

Fortunately, because $\bot$ has no introduction we are simultaneously declaring that this situation does not happen.  We are in a sense proposing that not all things are true and therefore logic exposes something to be learned.

The symbol $\bot$ is an upside down $\top$ which is used **truth** and hence $\bot$ is called **falsity** or **fallacy**.

### Negation

$\neg P$ is defined to mean
\[
    \Gamma, (P)\Rightarrow \bot
\]

#### $\sqrt{2}$ is irrational

**Fact** $1$ is not the multiple of a prime number.  That is, 
\[
    1=
\]

> **Definition** $x$ is rational if there exist integers $a$ and $b\neq 0$ such that $bx=a$ and $\gcd(a,b)=1$.  We write $x\in\mathbb{Q}$.

> **Definition** $x$ is irrational if it is not rational.

Let $P\equiv \sqrt{2}\in \mathbb{Q}$.  We aim to prove $\neg P$, that is, 
\[
    \Gamma, (\sqrt{2}\in \mathbb{Q})\Rightarrow \bot
\]
As with all implications we begin by assuming the hypothesis, that is $\sqrt{2}\in \mathbb{Q}$.
By definition that means there exists integers $a,b\neq 0$
\[
\begin{aligned}
    b\sqrt{2} & = a;\\
    2 b^2 & = a^2
\end{aligned}
\]
Therefore $a^2$ is even.  Therefore $a$ is even.  Therefore $a^2=4m^2$ for some $m$.  Therefore $b^2=2m^2$.  Therefore $b^2$ is even 
therefore $b$ is even.  Thus $2|\gcd(a,b)=1$.
