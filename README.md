# BanditNAS: Bandit Neural Architecture Search for Scientific Machine Learning

[![Paper Status: Conditional Acceptance](https://img.shields.io/badge/Paper%20Status-Conditional%20Acceptance%20(ACM%20TAAS)-B31B1B.svg)](http://placeholder_link_to_paper.com)
[![Code](https://img.shields.io/badge/GitHub-Repository-100000.svg)](https://github.com/your_organization/BanditNAS-SciML)
[![License: MIT](https://img.shields.io/github/license/your_organization/BanditNAS-SciML?color=blue)](LICENSE.md)

## 🎯 Abstract

Neural Architecture Search (NAS) for **Scientific Machine Learning (SciML)**—encompassing models like **PINNs, physics-informed GNNs, and DeepONets**—is fundamentally challenged by non-stationary and noisy loss landscapes. Existing **pure-exploration** bandit methods (e.g., HyperBand, Successive Halving) are suboptimal as they prematurely discard promising, yet slow-starting, architectures.

**BanditNAS** introduces a novel **non-stochastic adaptive multi-armed bandit (MAB)** approach. By leveraging a theoretically-grounded, exponentially decaying exploration parameter ($\gamma_t$), BanditNAS explicitly balances exploration and exploitation, proving to be a superior framework for optimization in adversarial and non-convex SciML search spaces.

## 🌟 Core Contributions & Performance

BanditNAS's design directly addresses the non-stationary nature of SciML losses, delivering substantial performance gains across three distinct scientific applications:

| Application Setting | Primary Challenge Addressed | Performance Metric ($\rho(K,T)$) | BanditNAS Result | Baseline Improvement |
| :--- | :--- | :--- | :--- | :--- |
| **PINNs** | **Noisy Validation Losses** | Optimal Pulls Rate | **$\approx 53\%$** | **$+10\%$** over HyperBand |
| **Physics-informed GNNs** | **Slow Convergence & Plateaus** | Optimal Pulls Rate | **$\approx 75\%$** | **$+50\%$** over HyperBand |
| **DeepONets** | **Dynamic Optimization Procedures** | Optimal Pulls Rate | **$\approx 97\%$** | **$+95\%$** over HyperBand |

### Visualization of Adaptive Selection ($\mathbf{p}_t$ Evolution)

The algorithm's power lies in its adaptive probability vector $\mathbf{p}_t$. The visualization below illustrates how $\mathbf{p}_t$ smoothly transitions from uniform exploration to concentrated exploitation.

| Key Mechanism | Visualization | Description |
| :--- | :--- | :--- |
| **Adaptive Selection** | ![BanditNAS p_t Evolution](banditnas_p_t_evolution.gif) | An animation demonstrating the dynamic evolution of the selection probabilities $p_{t,i}$ over time. The **Optimal** arm (highlighted in red) quickly gains probability mass as the exponentially decaying $\gamma_t$ ensures early-stage diversity while rapidly focusing the search. |

***

## ⚙️ Repository Structure

This repository is organized to facilitate both easy demonstration and rigorous replication of the full experimental suite.
