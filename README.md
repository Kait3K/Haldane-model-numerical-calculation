# Haldane Model

This repository contains numerical simulations and visualizations of the **Haldane model**,  
focusing on band structure, Chern number, and phase diagram of topological phase transitions.

The Hamiltonian is defines as below

$H = t_1 \sum_{\langle i, j \rangle} (c_{A,i}^\dagger c_{B,j} + \text{h.c.}) + t_2 \sum_{\langle\langle i, j \rangle\rangle} (e^{i\phi_{ij}} c_{A,i}^\dagger c_{A,j} + e^{i\phi_{ij}} c_{B,i}^\dagger c_{B,j} + \text{h.c.}) + M \left( \sum_{i} c_{A,i}^\dagger c_{A,i} - \sum_{j} c_{B,j}^\dagger c_{B,j} \right)$

where:
* $t_1$ is the nearest-neighbor (NN) hopping.
* $t_2 e^{i\phi_{ij}}$ is the complex next-nearest-neighbor (NNN) hopping.
* $M$ is the on-site energy difference between sublattices A and B.


