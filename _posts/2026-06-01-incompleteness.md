---
layout: post
title: "Gödel's Incompleteness Theorem: It Is About the Medium, Not the Facts"
date: 2026-06-01 15:14:00
---

When I first approached Gödel's incompleteness theorems, I came through the standard route: Gödel numbering, the diagonal lemma, self-referential sentences that encode their own unprovability. The machinery is genuinely impressive, and by the time the theorem emerges from it, it feels like a conjuring trick — something uncanny conjured from symbol manipulation. I came away thinking that something was fundamentally lost, that arithmetic inexplicably leaves a statement in genuine limbo, ambiguous in truth value, neither true nor false.

It took me a long time to understand that impression is completely wrong, and when I talked to other people, I found that the misconception lives in many minds. This is especially the case when we approach the theorem not from the formal paper but via videos, blog posts, and other online media.

## TL;DR

In arithmetic, the truth value of any given statement **IS** fixed, regardless of if we can prove it or not. Most misconceptions stem from the conflation of "truthfulness" and "proof".

## The worry: what does "true but unprovable" even mean?

The usual framing of the theorem is: *there are true statements that cannot be proven*. The natural question is: if we cannot prove something, in what sense is it true?

Take Goldbach's conjecture — the claim that every even number greater than 2 is the sum of two primes. Suppose it is unprovable. Then what?

Here is a simple argument. If Goldbach were *false*, there would exist a specific even number that could not be written as a sum of two primes. That is a finite, concrete counterexample — something we could in principle verify directly. Falsity would be provable. So if Goldbach is unprovable, it cannot be false. It must be true.

But now we have argued for its truth. So what does "unprovable" mean?

## The same gap, made obvious

Before addressing it directly, let us consider a simpler case in a stripped-down arithmetic system.

Robinson Arithmetic (Q) is a real, well-studied formal system. It has axioms for successor, addition, and multiplication — enough to express and verify arithmetic claims — but it has no induction schema.

What Q can do is already impressive: it is Turing complete and can verify any specific numerical claim. Give it 3 + 5 = 5 + 3, it verifies it. Give it 17 + 4 = 4 + 17, it verifies that too. In fact, Q is strong enough that Gödel's incompleteness theorems apply to it directly.

What Q cannot do is prove that a + b = b + a for *all* natural numbers. Without induction, there is no way to bridge from "this works for every specific case I check" to "this works for all cases". The infinitely many instances cannot be collapsed into a single general proof.

And yet nobody concludes from this that commutativity is metaphysically uncertain. The truth value is perfectly determined — addition commutes, full stop.

We can try to apply the same reasoning. If commutativity were false, there would exist two numbers whose sum did not commute, and such a counterexample could be verified by the system. Of course, we know that commutativity is true and no such counterexample exists; therefore, within the system, we can neither prove that commutativity holds (because the system is too weak) nor find any counterexample (because none exists). The statement cannot be approached by Robinson Arithmetic, but its truth value has nothing to do with the system.

In other words, the system just lacks the tools to see it. Once you add induction, commutativity becomes provable, and the reach of the system extends.

This is the exact same structure as the Goldbach situation, but with all philosophical confusion removed. There is no temptation to ask "but is commutativity *really* true if Q cannot prove it?" because the answer is too apparent: the system is limited, and its limitation says nothing about the fact.

Returning to Goldbach: suppose we have established that the conjecture is unprovable in Peano Arithmetic. If it is false, there exists a finite counterexample — something we could in principle exhibit. If it is true, no counterexample exists, but the absence of a counterexample settles nothing on its own, since we cannot search all natural numbers, and the system cannot prove that no counterexample exists.

## Extending reach: transfinite induction

Adding induction to Q gave us Peano Arithmetic, which can prove commutativity and vastly more. But PA has its own ceiling. A striking example is the classical Goodstein's theorem.

Take any natural number — say 4. Write it in hereditary base 2, meaning every number in the representation is also written as a power of 2: 4 = 2². Now replace every 2 with 3 to get a number in base 3: 3³ = 27. Subtract 1 to get 26. Write 26 in hereditary base 3: 2·3² + 2·3 + 2. Replace every 3 with 4: 2·4² + 2·4 + 2 = 42. Subtract 1. Repeat indefinitely, incrementing the base each time.

Now take a slightly larger starting point: 16. In hereditary base 2, this is 2^(2²). The first step replaces every 2 with 3, giving 3^(3³) = 3^27 — a number in the trillions, from a single substitution. After subtracting 1 and rewriting in hereditary base 3, the next substitution produces a number with hundreds of digits. From there the sequence enters territory no computer could store or meaningfully display, growing for a length of time that dwarfs the age of the universe.

Yet Goodstein's theorem says this sequence always eventually reaches 0, for any starting number.

This is a statement purely about natural numbers — no mention of infinity, no exotic objects. And it is true. But it is unprovable in Peano Arithmetic. The standard induction schema, powerful as it is, cannot reach it.

What can prove it is transfinite induction — induction extended to infinite ordinal numbers, reasoning about sequences that go beyond all finite steps. With this stronger tool, Goodstein's theorem follows naturally. The reach of the system extends once again.

The pattern is exactly the same as before. Q lacked the tools to see commutativity. PA lacks the tools to see Goodstein's theorem. Add the right tool, and what was out of reach becomes provable. The ceiling rises.

## Gödel shows the gap is permanent

For any consistent formal system strong enough to do basic arithmetic, there are true sentences beyond its reach. Add more axioms, and the reach extends — but new sentences immediately appear that are again out of reach. The ceiling rises but never disappears.

This is no more mysterious than the Q example. A system has reach. Gödel shows the reach is never total. That's the whole theorem.

## What it would mean to have no gap

A being that perceived the full structure of the natural numbers directly — not through proof, but all at once — would face no incompleteness at all. Gödel's theorem is a theorem about formal systems, about proof as a mechanical procedure. It says nothing about what such a being could know.

Proof is a tool invented by finite minds to approximate a direct vision they don't have. The incompleteness theorems measure precisely how far that tool falls short.

The gap is not in mathematics. The gap is in us.
