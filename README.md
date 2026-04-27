
# Lift Survival Framework

**Wessen Getachew · [@7dview](https://twitter.com/7dview)**  
**[wessengetachew.github.io](https://wessengetachew.github.io/Rh/) · math.NT · April 2026**

---

## What This Is

An original framework in analytic number theory built around a single geometric question: when a coprime residue r ∈ (ℤ/Mℤ)* is reduced mod M+1, does it remain coprime to M+1? Tracking this *lift survival* density across all M reveals a precise limiting constant, a prime-detecting function with exact jump discontinuities, two distinct geometric dynamics on the modular ring sequence, and an exact finite form of the Hardy–Littlewood singular series — all provable from elementary number theory.

---

## Quick Start

**New here?** Start in this order:

1. **[Preprint](https://wessengetachew.github.io/preprint.html)** — read the theorems first (20 min)
2. **[Lift Dynamics](https://wessengetachew.github.io/lift_dynamics.html)** — watch the two geometric structures, open The Math tab
3. **[E(N) Explorer](https://wessengetachew.github.io/EN_explorer-1-2.html)** — see the error term and the O(1/N) conjecture live
4. **[Geometric Canvas](https://wessengetachew.github.io/zmmz_explorer-1.html)** — the full modular ring visualization

The other 12 pages are deeper dives into specific results. Use the site map below when you want them.

---

## Proved Results

### 1. Convergence of the Lift Ratio

For M ≥ 2, define L(M) = φ(M)·φ(M+1)/(M+1) and R(N) = ΣL(M)/Σφ(M). Then:

```
R(N) → C = Π_p (p²−2)/(p²−1) ≈ 0.530711806246…   [OEIS A065469]
```

Algebraic identity: C = ζ(2)·d_FT (OEIS A065474). Equivalently K = ζ(2)·C ≈ 0.872986.

### 2. The Jump Theorem

D(x) = −Σ_{p > x+1} 1/(p²−x−1) is smooth except at x = p−1 for each prime p, where:

```
Δ_p = 1 / p(p−1)   [exact]
```

Recovery formula: p = (1 + √(1+4/s))/2. Discriminant (2p−1)² is always a perfect square.  
Biconditional: 1+4/s is a perfect square ⟺ s = 1/n(n−1) for some integer n ≥ 2.  
D(x) provides the primality filter — composites leave no jump.

### 3. Character-Weighted Extension

For Dirichlet character χ, D_χ(x) jumps by χ(p)/p(p−1) at each prime p. Proved identity:

```
J_χ = Σ_p χ(p)/p(p−1) = Σ_{k≥2} P(k,χ)
```

For Liouville λ: C_λ = ζ(2) exactly. Connects to L-functions and GRH geometrically.

### 4. Primorial Sieve Identity

For admissible constellation H of size k, at every primorial p_max#:

```
R_H(p_max) = C_H(p_max) · M(p_max)^k   [zero error, exact]
```

where C_H = Π_p (1−ν_H(p)/p)/(1−1/p)^k and M = Π_{p≤p_max} (p−1)/p.  
Proof: Chinese Remainder Theorem. Verified to 17# across six constellation types.  
Corollary: Gap-6 pairs = 2 × twin primes exactly at every primorial.

### 5. Farey Sector Formula

```
C(n, N) ~ 3N² / (π²n(n+1))
```

The factor 3/π² encodes ζ(2) = π²/6. Error terms connect to Franel–Landau and RH.

### 6. The Two Lift Dynamics

**±n Equatorial Path:** r = (M±n)/2 — the modular halves of ±n. As M → ∞, angular position θ → π (equator). For n=1, survives the lift iff M+1 = 2p (safe prime condition). These rings are where |E(N)·N| peaks numerically.

**Prime Spiral:** r_p(M) = p mod M. Phase 1 (M ≤ p): encodes p by CRT. Phase 2 (M > p): r = p fixed, θ = 2πp/M → 0. Dropout at M = p (p mod p = 0) = the Jump Theorem discontinuity.

**Intersection Theorem:** The ±1 path meets the prime-p spiral at ring M iff M+1 = 2p — exactly the safe prime rings. Gold intersections in the canvas.

---

## Conjectures (Open)

| # | Conjecture | Status |
|---|-----------|--------|
| C1 | E(N) = O(1/N) | Verified to N=10M, OLS slope −0.9979 |
| C2 | sup\|E(N)·N\| = K = ζ(2)·C | Maxima near K at safe prime rings |
| C3 | Maxima at N = p−1 for safe primes | Pattern confirmed |
| C4 | Complexity wall degrees 2,3,6 for k=1,2,3 | k=1,2 proved; k=3 pending |
| C5 | E(N) changes sign infinitely often | Observed, not proved |
| C6 | E_χ(N) governed by zeros of L(s,χ) on Re=½ | GRH conditional |

---

## Constants

| Symbol | Value | Definition |
|--------|-------|-----------|
| C | 0.530711806246 | Π_p (p²−2)/(p²−1)  [OEIS A065469] |
| K | 0.872986 | ζ(2)·C |
| J | 0.773155 | Σ_p 1/p(p−1) = Σ_{k≥2} P(k) |
| D₀ | 0.452246 | Σ_p 1/(p²−1) |
| T | 0.320909 | Σ_p 1/(p²(p−1)) |
| J₂ | 0.407100 | Twin prime jump sum |
| φ | 1.618034 | Golden ratio — supremum of jump spectrum |

Identities: J = D₀ + T · C = ζ(2)·d_FT · K = ζ(2)·C · C_λ = ζ(2)

---

## The Complexity Wall

| Constellation | k | Degree | Certification |
|--------------|---|--------|---------------|
| Single prime | 1 | 2 | Discriminant = perfect square |
| Twin prime | 2 | 3 | Cubic has rational root |
| Prime triplet | 3 | 6 | Sextic has rational root |

---

## Interactive Pages

All at **[wessengetachew.github.io](https://wessengetachew.github.io)**:

| Page | Description |
|------|-------------|
| `index.html` | Opener — animated prime visualization, navigation hub |
| `lift_dynamics.html` | **Lift Dynamics** — ±n path, prime spiral, both together, lift connections, The Math tab, 4K export, play animations |
| `EN_explorer-1-2.html` | E(N) Explorer — 9 charts, OLS regression, Möbius proof |
| `EN_explorer-updated.html` | Deep Analysis — Jump Theorem checker, 5 panels |
| `zmmz_explorer-1.html` | Geometric Canvas — WebGL rings, 4 views, prime spiral, gap overlay, animations |
| `zeta_explorer.html` | ζ(2) Explorer — 7 charts, gap-class decomposition |
| `gcd_explorer.html` | GCD Coprimality — sieve density visualizer |
| `lift_paper-48.html` | Lift Paper — formal paper + C(x) explorer |
| `k_explorer.html` | K Constant — 5 charts, safe prime analysis |
| `spectral_theory-1.html` | Spectral Theory — all constants, Al-Battani table, complexity wall |
| `dchi_explorer.html` | D_χ Explorer — 6 characters, J_χ, C_χ, compare panel |
| `zeta_lift_bridge.html` | ζ–Lift Bridge — s-plane conformal map, E(N) explicit formula, FFT, zero contributions |
| `complexity_wall.html` | Complexity Wall — discriminant filter, root landscape, degree visualization |
| `sophie_germain.html` | Sophie Germain Primes — SG pairs, safe primes, discriminant map p→2p−1 |
| `wessen_identity.html` | Primorial Sieve Identity — paper with KaTeX, canvas explorer, step-by-step |
| `preprint.html` | HTML Preprint — full paper, all theorems, KaTeX math |

---

## Preprint

**"Prime Detection via a Jump Discontinuity in a Lift-Survival Function"**  
[wessengetachew.github.io/preprint.html](https://wessengetachew.github.io/preprint.html)

MSC 2020: 11N37, 11A25, 11M32, 11M26

---

## What Is Original

**Likely new:**
- Lift survival interpretation of C and its geometric framework
- The Jump Theorem — D(x), exact Δ_p, closed-form recovery, perfect-square biconditional
- Character-weighted D_χ(x) and J_χ series identity
- The two lift dynamics: ±n path and prime spiral with intersection theorem
- Primorial Sieve Identity (exact finite Hardy–Littlewood)
- Complexity wall 2→3→6
- K = ζ(2)·C conjecture with safe prime peak structure

**Reframes classical results:**
- Farey Sector Formula
- ζ(2) gap-class decomposition
- C = ζ(2)·d_FT algebraic identity

**Not proved — honestly labelled:**
- E(N) = O(1/N) and all conjectures above

---

## References

- Hardy, G.H. and Littlewood, J.E. (1923). *Acta Mathematica* 44, 1–70.
- Iwaniec, H. and Kowalski, E. (2004). *Analytic Number Theory*. AMS.
- Montgomery, H.L. and Vaughan, R.C. (2006). *Multiplicative Number Theory I*. Cambridge.
- Sándor, J. and Tóth, L. (1989). *Fibonacci Quarterly* 28(3), 255–258.
- OEIS A065469: https://oeis.org/A065469

---

*Wessen Getachew · @7dview · wessengetachew.github.io*  
*All numerical claims verified computationally. Proved results have complete proofs. Conjectures clearly labelled.*
