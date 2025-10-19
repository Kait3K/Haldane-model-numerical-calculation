We use nearest-neighbor vectors
- δ₁ = (a/2,  √3 a/2),  δ₂ = (a/2, -√3 a/2),  δ₃ = (-a, 0)

and next-nearest (same-sublattice) vectors
- b₁ = δ₂-δ₃ = ( 3a/2, -√3 a/2)
- b₂ = δ₃-δ₁ = (-3a/2, -√3 a/2)
- b₃ = δ₁-δ₂ = ( 0,     √3 a)

Define
- g(k) = t₁ ∑_{i=1}^{3} exp(i k·δᵢ)
- f(k) = 2 t₂ ∑_{i=1}^{3} cos(k·bᵢ + φ)

Then the Bloch Hamiltonian can be written as
  H(k) = d₀(k) I + d(k)·σ
with
  d₀(k) = 2 t₂ cosφ ∑_{i} cos(k·bᵢ)
  dₓ(k) = Re g(k) = t₁ ∑_{i} cos(k·δᵢ)
  d_y(k) = -Im g(k) = - t₁ ∑_{i} sin(k·δᵢ)
  d_z(k) = M - 2 t₂ sinφ ∑_{i} sin(k·bᵢ)

Matrix form:
  H(k) =
    [ d₀(k)+d_z(k)      dₓ(k) - i d_y(k) ]
    [ dₓ(k) + i d_y(k)  d₀(k)-d_z(k)    ]

## Energy eigenvalues

  E_±(k) = d₀(k) ± √( dₓ(k)² + d_y(k)² + d_z(k)² )

## Topological phase criterion

  |M| < 3√3 t₂ sinφ  → Chern = ±1 (topological)
  |M| > 3√3 t₂ sinφ  → Chern = 0  (trivial)

