# Haldane Model

This repository contains numerical simulations and visualizations of the **Haldane model**,  
focusing on band structure, Chern number, and phase diagram of topological phase transitions.

The Hamiltonian is defines as

$$
H = t_1 \sum_{\langle i, j \rangle} (c_{A,i}^\dagger c_{B,j} + \text{h.c.}) + t_2 \sum_{\langle\langle i, j \rangle\rangle} (e^{i\phi_{ij}} c_{A,i}^\dagger c_{A,j} + e^{i\phi_{ij}} c_{B,i}^\dagger c_{B,j} + \text{h.c.}) + M \left( \sum_{i} c_{A,i}^\dagger c_{A,i} - \sum_{j} c_{B,j}^\dagger c_{B,j} \right)
$$

where:
* $t_1$ is the nearest-neighbor (NN) hopping.
* $t_2 e^{i\phi_{ij}}$ is the complex next-nearest-neighbor (NNN) hopping.This complex hopping acts as an internal, staggered magnetic field. The net magnetic flux through any unit cell is zero, so it's not a simple external B-field.Its primary function is to explicitly break time-reversal symmetry (TRS). By breaking TRS we obtain topological phase in certain condition.
* $M$ is the on-site energy difference between sublattices A and B. This term breaks inversion symmetry and tries to create a trivial gap.

Hamiltonian that is written as $2\times2$ can be rewritten by Pauli Matrixes. If we write the Hamiltonian using the spinor for A, B sublattice, it can written as $H = \sum_{\mathbf{k}} \Psi_{\mathbf{k}}^\dagger H(\mathbf{k}) \Psi_{\mathbf{k}}, \quad \text{where} \quad \Psi_{\mathbf{k}}^\dagger = (c_{A, \mathbf{k}}^\dagger, c_{B, \mathbf{k}}^\dagger)$.

The Momentum space Hamiltonian is written as 

$H(\mathbf{k}) = d_0(\mathbf{k})\sigma_0 + d_x(\mathbf{k})\sigma_x + d_y(\mathbf{k})\sigma_y + d_z(\mathbf{k})\sigma_z$

where:
* $d_0(\mathbf{k}) = 2 t_2 \cos(\phi) \sum_{n=1}^3 \cos(\mathbf{k} \cdot \vec{b}_n)$
* $d_x(\mathbf{k}) = t_1 \sum_{n=1}^3 \cos(\mathbf{k} \cdot \vec{\delta}_n)$
* $d_y(\mathbf{k}) = -t_1 \sum_{n=1}^3 \sin(\mathbf{k} \cdot \vec{\delta}_n)$
* $d_z(\mathbf{k}) = M + 2 t_2 \sin(\phi) \sum_{n=1}^3 \sin(\mathbf{k} \cdot \vec{b}_n)$

Thus the eigenvalue is written as:

$$
E(k) = d_0 \pm \sqrt{d_x^2 + d_y^2 + d_z^2}
$$

We define the Chern number as:

$$
C = \frac{1}{2} \left[ \text{sgn}(d_z(\mathbf{K})) - \text{sgn}(d_z(\mathbf{K}')) \right]
$$

