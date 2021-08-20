---
title: The Henkin style proof of the completeness of predicate logic
date: 2020-04-07 19:01:03
tags:
  - 邏輯
  - 學院
categories: philosophy
mathjax: true
---

述詞邏輯完備性的證明。

<!--more-->

# The Semantics

## Definition 1: Structure

A $\left\langle\mathcal{I},\mathcal{J,}K,\eta,\zeta\right\rangle$-***structure*** $\mathcal{M}$ is a complex of the form $\mathcal{M} = \left\langle A,\ \ R = \left\{ r_{i} \middle| i\mathcal{\in I} \right\},\ \ F = \left\{ f_{j} \middle| j \in \mathcal{J} \right\},\ \ \left\{ e_{k} \middle| k \in K \right\} \right\rangle$, with associated functions $\eta:\mathcal{I} \rightarrow \mathbb{N}^{+}$ and $\zeta\mathcal{:I \rightarrow}\mathbb{N}^{+}$, where

* $A$ is a non-empty set, called the ***domain*** of $\mathcal{M}$;
* for each $i \in \mathcal{I}$, $r_{i}$ is a $\eta(i)$-ary relation on $A$;
* for each $j\mathcal{\in J}$, $f_{j}$ is a $\zeta(j)$-ary function defined on $A^{\zeta(j)}$ (the $\zeta(j)$-power Cartesian product of $A$) to $A$;
* for each $k \in K$, $e_{k} \in A$.

## Definition 2: Language

A ***language*** $\mathcal{L}$ of the type $\left\langle \mathcal{I},\mathcal{J},K,\eta,\zeta \right\rangle$ is defined to be the set sequences consisting of the elements of the following sets: $\left\{ \neg,\  \rightarrow ,\ \forall, = ,\left( , \right),v_{n}\ ,P_{i}\ ,F_{j}\ ,c_{k} \middle| n\mathbb{\in N},\ \ i\mathcal{\in I},\ \ j \in \mathcal{J}\mathrm{,}\mathrm{\ }k \in K \right\}$ with associated formation rules as shown below.

**Terms:** the set $\mathcal{T}$ of terms is defined as:

* (T1) $v_{n} \in \mathcal{T}$ for any $n\mathbb{\in N}$.
* (T2) $c_{k}\mathcal{\in T}$ for any $k \in K$.
* (T3) If $\tau_{1},\ \tau_{2},\ldots,\tau_{m} \in \mathcal{T}$, $F_{j}\left( \tau_{1},\ \tau_{2},\ldots,\tau_{m} \right)\mathcal{\in T}$, where $\zeta\left( j \right) = m$.
* (T4) All elements of $\mathcal{T}$ are generated as in (T1) - (T3).

**Atomic formulae:** the set $\mathcal{A}$ of atomic formulae is defined
as:

* (A1) If $\tau,\ \iota \in \mathcal{T}$, then $\tau = \iota \in \mathcal{A}$.
* (A2) If $\tau_{1},\ \tau_{2},\ldots,\tau_{m}\mathcal{\in T}$, $P_{i}\left( \tau_{1},\ \tau_{2},\ldots,\tau_{m} \right)\mathcal{\in A}$, where $\eta\left( i \right) = m$.
* (A3) All elements of $\mathcal{A}$ are generated as in (A1) - (A2).

**Formulae:** the set $\mathcal{F}$ of formulae is defined as:

* (F1) $\mathcal{A} \subset \mathcal{F}$.
* (F2) If $\phi \in \mathcal{F}$, then $\neg\phi \in \mathcal{F}$.
* (F3) If $\phi,\ \theta\mathcal{\in F}$, then $\phi \rightarrow \theta\mathcal{\in F}$.
* (F4) If $\phi \in \mathcal{F}$ and $n\mathbb{\in N}$ then $\forall v_{n}\phi \in \mathcal{F}$.
* (F5) All elements of $\mathcal{F}$ are generated as in (F1) - (F4).

## Definition 3: Assignment

An ***assignment*** $\varsigma$ of a structure $\mathcal{M =}\left\langle A,R,F,\left\langle e_{k} \right\rangle \right\rangle$ is a function defined on $\mathbb{N}$ to $A$.

## Definition 4: Semantic Value

For $\tau \in \mathcal{T}$, a structure $\mathcal{M}$ and an assignment $\varsigma$ of $\mathcal{M}$, we define the ***semantic value of $\bm{\tau}$ at at $\bm{\varsigma}$ in $\bm{\mathcal{M}}$***, notated by $\tau^{\mathcal{M}}\left\lbrack \varsigma \right\rbrack$, as:

* (1) *Case 1*: $\tau = v_{n}$, for some $n \in \mathbb{N}$, $\tau^{\mathcal{M}}\left\lbrack \varsigma \right\rbrack = \zeta\left( n \right)$.
* (2) *Case 2*: $\tau = c_{k}$, for some $k \in K$, $\tau^{\mathcal{M}}\left\lbrack \varsigma \right\rbrack = e_{k}$.
* (3) *Case 3*: $\tau = F_{j}\left( \tau_{1},\ldots,\tau_{\zeta(j)} \right)$, for some $j \in \mathcal{J}$ and $\tau_{1},\ldots,\tau_{\zeta\left( j \right)} \in \mathcal{T}$, $\tau^{\mathcal{M}}\left\lbrack \varsigma \right\rbrack = f_{j}\left( {\tau_{1}}^{\mathcal{M}}\left\lbrack \varsigma \right\rbrack,\ldots,{\tau_{\zeta(j)}}^{\mathcal{M}}\left\lbrack \varsigma \right\rbrack \right)$.

## Definition 5: Tarski's Definition of Satisfaction

For a sentence $\phi$ in $\mathcal{L}$, a structure $\mathcal{M}$, and an assignment $\varsigma$ of $\mathcal{M}$, ***the satisfaction of*** $\mathbf{\phi}$ ***at*** $\mathbf{\varsigma}$ ***in*** $\mathcal{M}$, notated by $\mathcal{M} \vDash_{\varsigma}\phi$, is defined by:

* (1) $\phi \in \mathcal{A}$:
  + (a) $\phi$ is the form of $\tau = \iota$: $\tau^{\mathcal{M}}\left\lbrack \varsigma \right\rbrack$ equals to $\tau^{\mathcal{M}}\left\lbrack \iota \right\rbrack$.
  + (b) $\phi$ is the form of $P_{i}\left( \tau_{1},\ \tau_{2},\ldots,\tau_{\zeta(i)} \right)$: $r_{i}\left\langle \tau_{1},\ \tau_{2},\ldots,\tau_{\zeta(i)} \right\rangle \in R$.
* (2) $\phi$ is the form of $\neg\theta$: it is not the case that $\mathcal{M} \vDash_{\varsigma}\theta$.
* (3) $\phi$ is the form of $\theta \rightarrow \psi$: $\mathcal{M} \vDash_{\varsigma}\neg\theta$ or $\mathcal{M} \vDash_{\varsigma}\psi$.
* (4) $\phi$ is the form of $\forall v\theta$: for all $a \in A$, $\mathcal{M} \vDash_{\varsigma(i/a)}\theta$, where $\varsigma(i/a)$ is the assignment defined by

$$\varsigma(i/a)(n) = \begin{cases}\varsigma (j) &\text{if } j \neq n \\ a &\text{if } j = n \end{cases}$$

# The Preparation

## Definition 6: Henkin Theory

$T$ is a ***Henkin theory*** in a language $\mathcal{L}$ iff} for any $\exists x\phi$, there is
a constant $c$ in $\mathcal{L}$ such that $(\exists x\phi \rightarrow \phi(x/c)) \in T$. Such $c$ is called a ***Henkin witness*** in $\mathcal{L}$ of $\exists x\phi$ (notated by $c_{\exists x\phi}$).

## Definition 7: Alphabet Extension

If $\mathcal{L}$ is a language. A language $\mathcal{L}^{+}$ is called an ***alphabet extension*** (or constant extension) of $\mathcal{L}$, *iff* $\mathcal{L}^{+}$ is obtained by numerable steps of adding a new constant to $\mathcal{L}$.

### Property 1

If $\Gamma$ is a consistent set in $\mathcal{L}$, then, for any formula $\exists x\phi$ and $c$ is a
Henkin witness in $\mathcal{L}^{+}\mathcal{( \supset L)}$ (but not in $\mathcal{L}$) of $\exists x\phi$, $\Gamma \cup \left\{ \exists x\phi \rightarrow \phi(x/c) \right\}$ is consistent.

> ***Proof.***
> 
> Suppose $\Gamma \cup \left\{ \exists x\phi \rightarrow \phi(x/c) \right\}$ is inconsistent.
> 
> (⇒) $\Gamma \vdash \neg(\exists x\phi \rightarrow \phi(x/c))$.
> 
> (⇒) $\Gamma \vdash \exists x\phi$ and $\Gamma \vdash \neg\phi(x/c)$.
> 
> (⇒) $\Gamma \vdash \forall x\neg\phi$ since $c$ does not occur in any formula of $\Gamma$ (by rule of Generalization and $\Gamma \vdash \neg\phi(x/c)$).
> 
> (⇒) $\Gamma \vdash \neg\exists x\phi$.
> 
> (⇒) Then $\Gamma$ is inconsistent. A contradiction.

## Definition 8: Deductive Closure

Given $\Gamma$ is a set of sentences in $\mathcal{L}$. $\overline{\Gamma}$ is called a ***deductive closure*** of $\Gamma$ in $\mathcal{L}$, *iff* $\overline{\Gamma} = \left\{ \phi \middle| \Gamma \vdash \phi \right\}$, which $\phi$ is in $\mathcal{L}$.

### Property 2

A set of sentences $\Gamma$ is a consistent, *iff* $\overline{\Gamma}$ is a consistent.

> ***Proof.***
> 
> Trivial.

# The Proof

## Lemma 1: Full Extension

For any consistent set of sentences $\Gamma$ in $\mathcal{L}$, there is a set of sentences $\Sigma$ in $\mathcal{L}^{+}$ such that (1) $\Gamma \subset \Sigma$ and (2) $\Sigma$ is a consistent Henkin theory in $\mathcal{L}^{+}$.

> ***Proof.***
> 
> Given $\Gamma$ is a consistent set in $\mathcal{L}$.
> 
> We define the sequences $\left\langle \Gamma_{n} \right\rangle$ recursively:
> 
>> 1. $\Gamma_{0} = \Gamma$ and $\mathcal{L}_{0}\mathcal{= L}$;
>> 2. $\Gamma_{k} = \Gamma_{k - 1} \cup \left\{ \exists x_{k - 1}\phi_{k - 1} \rightarrow \phi_{k - 1}(x_{k - 1}/c_{\exists x_{k - 1}\phi_{k - 1}}) \right\}$ and $\mathcal{L}_{k} = \mathcal{L}_{k - 1} + \left\{ c_{\exists x_{k - 1}\phi_{k - 1}} \right\}$, where $c_{k - 1}$ is a new Henkin constant of $\exists x_{k - 1}\phi_{k - 1}$.
> 
> Then we define $\Gamma^{*} = \bigcup_{k = 0}^{\infty}\Gamma_{k}$ and$\mathcal{L}^{+} = \bigcup_{k = 0}^{\infty}\mathcal{L}_{k}$.
> 
> By **Property 1**, $\Gamma_{n}$ is consistent for any $n$ (easily proved by induction), and $\left\langle \Gamma_{n} \right\rangle$ is a chain. Therefore, $\Gamma^{*}$ should be consistent unless entail a contradiction. So do $\overline{\Gamma^{*}}$ by **Property 2**.
> 
> For any $\exists x\phi$ such that $\overline{\Gamma^{*}} \vdash \exists x\phi$, there is some $n$ such that $\exists x\phi$ is equal to $\exists x_{n}\phi_{n}$ and $\Gamma^{*}\  \vdash \exists x_{n}\phi_{n} \rightarrow \phi_{n}(x_{n}/c_{\exists x_{n}\phi_{n}})$
> 
> (⇒) $\exists x_{n}\phi_{n} \rightarrow \phi_{n}(x_{n}/c_{\exists x_{n}\phi_{n}}) \in \overline{\Gamma^{*}}$ by definition.
> 
> (⇒) $\overline{\Gamma^{*}}$ is a Henkin theory in $\mathcal{L}^{+}$.

## Definition 9: Syntactic Complete

A set of sentences in $\mathcal{L}$, $\Gamma$, is ***complete*** *iff*, for any $\phi$ in $\mathcal{L}$, either $\Gamma \vdash \phi$ or $\Gamma \vdash \neg\phi$. If $\Sigma$ is a subset of $\Gamma$, we say $\Gamma$ is a ***complete extension*** of $\Sigma$.

## Lemma 2: Complete Extension

For any consistent set of sentences $\Gamma$ in $\mathcal{L}$, there is a set of sentences $\Sigma$ in $\mathcal{L}$ such that $\Sigma$ is a consistent complete extension of $\Gamma$ in $\mathcal{L}$.

> ***Proof.***
> 
> Given $\Gamma$ is a consistent set in $\mathcal{L}$.
> We define the sequences $\left\langle \Gamma_{n} \right\rangle$ recursively:
> 
>> 1. $\Gamma_{0} = \Gamma$
>> 2. $\Gamma_{k} = \Gamma_{k - 1} \cup \left\{ \phi_{k - 1} \right\}$ if $\Gamma_{k - 1} \cup \left\{ \phi_{k - 1} \right\}$ is consistent, $\Gamma_{k} = \Gamma_{k - 1}$ otherwise, where $\left\langle \phi_{n} \right\rangle$ is the sequence of all sentences in $\mathcal{L}$.
> 
> Then we define $\Gamma^{*} = \bigcup_{k = 0}^{\infty}\Gamma_{k}$.
> 
> Easily check $\Gamma^{*}$ is consistent and complete.

## The Extension Lemma

For any consistent set of sentences $\Gamma$ in $\mathcal{L}$, we can extend $\Gamma$ to a consistent complete Henkin theory in $\mathcal{L}^{+}$.

> ***Proof.***
>
>> So far, we have these two lemmas:
>> 
>> * For any consistent set of sentences $\Gamma$ in $\mathcal{L}$, we can extend $\Gamma$ to a consistent Henkin theory $\Gamma^{*}$ in $\mathcal{L}^{+}$. We can call $\Gamma^{*}$ a ***full-extension*** $\Gamma$.
>> * For any consistent set of sentences $\Gamma$ in $\mathcal{L}$, we can extend $\Gamma$ to a consistent complete set $\Gamma^{*}$ in $\mathcal{L}$. We can call $\Gamma^{*}$ a ***complete-extension*** of $\Gamma$.
> 
> Given $\Gamma$ is a consistent set in $\mathcal{L}$.
> 
> We define the sequences $\left\langle \Gamma_{n} \right\rangle$, $\left\langle \Sigma_{n} \right\rangle$ and $\left\langle \mathcal{L}_{n} \right\rangle$ recursively:
> 
>> 1. $\Gamma_{0} = \Gamma$, $\ \mathcal{L}_{0}\mathcal{= L}$;
>> 2. Define $\Sigma_{n}$ as a full-extension of $\Gamma_{n - 1}$ in $\mathcal{L}_{n}$ (defined as the language defined as the proof of **Lemma 1**), $\Gamma_{n}$ as a compete-extension of $\Sigma_{n}$.
> 
> Then we define $\Gamma^{*} = \bigcup_{k = 0}^{\infty}\Gamma_{k}$, $\Sigma^{*} = \bigcup_{k = 1}^{\infty}\Sigma_{k}$ and $\mathcal{L}^{+} = \bigcup_{k = 1}^{\infty}\mathcal{L}_{k}$.
> 
> We can easily check $\Gamma^{*} = \Sigma^{*}$.
> 
> So $\Gamma^{*}$ is a consistent complete Henkin theory in $\mathcal{L}^{+}$ which contains $\Gamma$.

## The Model Existence Lemma

If a set of sentences $\Gamma$ is a complete consistent Henkin theory in $\mathcal{L}$, then $\Gamma$
has a model.

> ***Proof.***
> 
> Let $\left\{ P_{n} \right\}$ be the set of predicate symbols in $\mathcal{L}$ and $\left\{ c_{n} \right\}$ be the set of all constants in $\mathcal{L}$, $n\mathbb{\in N}$.
> 
> We can define a relation on terms $\sim$ as: $\iota\sim\tau$ *iff* $\Gamma \vdash \iota = \tau$. $\sim$ has these properties:
> 
>> * Reflexivity: For any constant $\iota$, $\Gamma \vdash \iota = \iota$.
>> * Symmetry: For any constant $\iota$ and $\tau$, if $\Gamma \vdash \iota = \tau$, then $\Gamma \vdash \tau = \iota$.
>> * Transitivity: For any constant $\iota$, $\tau$ and $\pi$, if $\Gamma \vdash \iota = \tau$ and $\Gamma \vdash \tau = \pi$, then $\Gamma \vdash \iota = \pi$.
> 
> That is, $\sim$ is an equivalence relation. And we can define an equivalence class by $\left\lbrack \iota \right\rbrack \in \left\{ \iota \right\}/\sim$.
> 
> Let $\mathcal{M =}\left\langle A,\ R = \left\{ r_{i} \middle| i\mathcal{\in I} \right\},F = \left\{ f_{j} \middle| i \in \mathcal{J} \right\},E = \left\{ e_{k} \right\} \right\rangle$ with $\eta\mathcal{:I \rightarrow}\mathbb{N}^{+}$ and $\zeta:\mathcal{J \rightarrow}\mathbb{N}^{+}$:
> 
>> 1. We define $A = \left\{ \left\lbrack c_{n} \right\rbrack \right\}$.
>> 2. Suppose $P_{i}$ is an $k_{i}$-ary relation of $\mathcal{L}$, we define $r_{i}$ and $\eta$ as: $r_{i}\left( \left\lbrack \tau_{1} \right\rbrack,\left\lbrack \tau_{2} \right\rbrack,\ldots,\left\lbrack \tau_{k_{i}} \right\rbrack \right)$ *iff* $P_{i}\left( \tau_{1},\tau_{2},\ldots,\tau_{k_{i}} \right) \in \text{\ Γ}\ $ and $\eta\left( i \right) = k_{i}$.
>> 3. Suppose $F_{j}$ is an $k_{j}$-ary function of $\mathcal{L}$, we define $f_{j}$ and $\zeta$ as: $f_{j}\left( \left\lbrack \tau_{1} \right\rbrack,\left\lbrack \tau_{2} \right\rbrack,\ldots,\left\lbrack \tau_{k_{j}} \right\rbrack \right) = F_{j}\left( \tau_{1},\tau_{2},\ldots,\tau_{k_{j}} \right)$ and $\zeta\left( j \right) = k_{j}$.
>> 4. We define $e_{k} = \left\lbrack c_{k} \right\rbrack$.
> 
> We need to show that, for any $\phi$ in $\mathcal{L}$, $\mathcal{M \vDash}\phi$, *iff* $\Gamma \vdash \phi$. *Note*: we can also define the assignment function $\varsigma\mathbb{:N \rightarrow}A$.
> 
> ***Basis case***: $\phi$ is atomic.
> 
> *Case 1*: $\phi$ is the form of $\tau = \iota$.
> 
>> $\mathcal{M \vDash}\phi$.
>> 
>> (⇔) For any $\varsigma$, $\mathcal{M} \vDash_{\varsigma}\phi$ i.e. $\mathcal{M} \vDash_{\varsigma}\tau = \iota$.
>> 
>> (⇔) For any $\varsigma$, $\tau^{\mathcal{M}}\lbrack\varsigma\rbrack = \iota^{\mathcal{M}}\lbrack\varsigma\rbrack$.
>> 
>> (⇔) For any $\varsigma$, $\tau^{\mathcal{M}}\lbrack\varsigma\rbrack\sim\iota^{\mathcal{M}}\lbrack\varsigma\rbrack$.
>> 
>> (⇔) $\Gamma \vdash \tau = \iota$.
>> 
>> (⇔) $\Gamma \vdash \phi$.
> 
> *Case 2*: $\phi$ is the form of $P(\tau_{1},\tau_{2},\ldots,\tau_{n})$.
> 
>> $\mathcal{M \vDash}\phi$.
>> 
>> (⇔) For any $\varsigma$, $\mathcal{M} \vDash_{\varsigma}\phi$ i.e. $\mathcal{M} \vDash_{\varsigma}P(\tau_{1},\tau_{2},\ldots,\tau_{n})$.
>> 
>> (⇔) For any $\varsigma$, there is some $i$, such that $r_{i}\left( {\tau_{1}}^{\mathcal{M}}\lbrack\varsigma\rbrack,{\tau_{2}}^{\mathcal{M}}\lbrack\varsigma\rbrack,\ldots,{\tau_{n}}^{\mathcal{M}}\lbrack\varsigma\rbrack \right)$.
>> 
>> (⇔) $\Gamma \vdash P(\tau_{1},\tau_{2},\ldots,\tau_{n})$.
>> 
>> (⇔) $\Gamma \vdash \phi$.
> 
> ***Inductive step***: for some $\phi$, we assume that all proper subformulae of $\phi$ hold the result as the inductive hypothesis.
> 
> *Case 1*: $\phi$ is the form of $\neg\psi$. Clearly hold by definition and completeness of $\Gamma$.
> 
> *Case 2*: $\phi$ is the form $\psi \rightarrow \theta$.
> 
>> $\mathcal{M \vDash}\phi$ i.e. $\mathcal{M \vDash}\psi \rightarrow \theta$.
>> 
>> (⇔) $\mathcal{M \vDash \neg}\psi$ or $\mathcal{M \vDash}\theta$.
>> 
>> (⇔) $\Gamma \vdash \neg\psi$ or $\Gamma \vdash \theta$ (by the inductive hypothesis).
>> 
>> (⇔) $\Gamma \vdash \psi \rightarrow \theta$.
>> 
>> (⇔) $\Gamma \vdash \phi$.
> 
> *Case 3*: $\phi$ is the form $\forall x\psi$, and, WLOG, we suppose the variables of $\psi$ is $(\tau_{1},\tau_{2},\ldots,\tau_{n - 1},\ x)$.
> 
>> $\mathcal{M \vDash}\phi$.
>> 
>> (⇔) For any $\varsigma$, $\mathcal{M} \vDash_{\varsigma}\phi$ i.e. $\mathcal{M} \vDash_{\varsigma}\forall x\psi$.
>> 
>> (⇔) For any $\varsigma$ and $\lbrack c\rbrack \in A$, $\mathcal{M} \vDash_{\varsigma(i/\lbrack c\rbrack)}\psi$.
>> 
>> (⇔) For any $\lbrack c\rbrack \in A$, $\Gamma \vdash \psi(\tau_{1},\tau_{2},\ldots,\tau_{n - 1},c)$ (by the inductive hypothesis).
>> 
>> (⇔) $\Gamma \vdash \forall x\psi$.
>> 
>> (⇔) $\Gamma \vdash \phi$.
> 
> So, for any $\phi$ in $\mathcal{L}$, $\mathcal{M \vDash}\phi$, *iff* $\Gamma \vdash \phi$.}

## Completeness Theorem

If $\Gamma \vDash \phi$, then $\Gamma \vdash \phi$ where $\phi$ is a sentence in $\mathcal{L}_{\text{CPL}}$ and $\Gamma$ is a set of sentences in $\mathcal{L}_{\text{CPL}}$.

> ***Proof.***
> 
> Suppose $\Gamma \vDash \phi$ but $\Gamma \nvdash \phi$.
> 
> (⇒) $\Gamma \cup \left\{ \neg\phi \right\}$ is constant.
> 
> (⇒) There is a consistent complete Henkin theory $\Gamma^{*}$ in ${\mathcal{L}_{\text{CPL}}}^{+}$ contains $\Gamma \cup \left\{ \neg\phi \right\}$ (by \textbf{extension lemma}).
> 
> (⇒) There is a model $\mathcal{M}$ such that $\mathcal{M \vDash}\Gamma \cup \left\{ \neg\phi \right\}$ in ${\mathcal{L}_{\text{CPL}}}^{+}$ (by \textbf{model existence lemma}). But it is impossible: if $\Gamma \vDash \phi$ in $\mathcal{L}$, then $\Gamma \vDash \phi$ in $\mathcal{L}^{+}$.
> 
> So, $\Gamma \vdash \phi$.

