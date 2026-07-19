# Very Strong Big Busy Beaver (VSBBB)

**VSBBB** is an uncomputable function that extends the standard Busy Beaver by introducing transfinite time complexity and ordinal-indexed towers. It serves as the foundational core for the **Rud function hierarchy**.

## Formal Definition

The value of `VSBBB` on the `n`-th level is defined in three phases.

### Phase 1: Base States (Z)

Define a computable integer `Z` using Knuth's up‑arrow notation: `Z = 3 ↑↑↑ 3`. This is a power tower of 3s of height `3 ↑↑ 3 = 3^(3^3) = 7625597484987`. So: `Z = 3^(3^(...^3))` (7625597484987 times).

### Phase 2: n-fold Busy Beaver

Let `Σ(x)` denote the standard Busy Beaver function. Define the `n`-fold iteration: `Σ^(n)(x) = Σ(Σ(...Σ(x)...))` (n times). Apply it to `Z`: `A = Σ^(n)(Z)`. This yields an uncomputable number belonging to the `n`-th tier of the arithmetic hierarchy.

### Phase 3: Transfinite Tower

Construct a transfinite exponential tower of height `ω^n`, where `ω` is the first infinite ordinal: `VSBBB = f_{ω^n}(A)` using the fast-growing hierarchy `f_α`. Equivalently, in tower notation: `VSBBB = A^(A^(...^A))` (ω^n times), where the tower is understood as the limit of finite towers of heights 1, 2, 3, ... as the height approaches `ω^n`.

## Why It Grows So Fast

The base `A` is **uncomputable** due to the iterated Busy Beaver. The height `ω^n` is **transfinite**, meaning it goes beyond finite iteration. This places `VSBBB` at level `f_{ω^n}` in the fast‑growing hierarchy, exceeding Fish number 4 for sufficiently large `n`.

## Proof of Growth

For any computable function `f`, there exists `n` such that `VSBBB(n) > f(n)`: (1) `Σ(x)` grows faster than any computable function; (2) `Σ^(n)(Z)` is an `n`-fold iteration, so it dominates `f` for large `n`; (3) the transfinite tower `f_{ω^n}` places `VSBBB` beyond any finite-iteration function.

## Relation to the Rud Function

`VSBBB` is a **component** of the **Rud function**: `Rud(n) = [CBB, CBB, (CBB), (CBB)]`, where `CBB` is built from `VSBBB` via ordinals and self-application.

## License

This work is dedicated to the public domain (CC0). Use freely, but please credit the author when citing.

**Author:** [PB2o137]  
**Date:** 2026
