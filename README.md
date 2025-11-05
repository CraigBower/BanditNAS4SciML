# BanditNAS: Bandit Neural Architecture Search for Scientific Machine Learning

[![Paper](https://img.shields.io/badge/Paper-ACM%20TAAS-B31B1B.svg)](http://placeholder_link_to_paper.com)
[![Code](https://img.shields.io/badge/GitHub-Code-100000.svg)](https://github.com/your_organization/BanditNAS-SciML)
[![License](https://img.shields.io/github/license/your_organization/BanditNAS-SciML?color=blue)](LICENSE.md)

## 🌟 The Challenge: Adaptive NAS for Scientific ML

Neural Architecture Search (NAS) in **Scientific Machine Learning (SciML)**—such as Physics-Informed Neural Networks (PINNs) and DeepONets—presents unique challenges: the loss landscapes are often **non-stationary**, **noisy**, and **slow to converge**. Traditional pure-exploration multi-armed bandit (MAB) methods like HyperBand and Successive Halving fail because they aggressively prune promising but slow-starting architectures.

We propose **BanditNAS**, a **non-stochastic adaptive MAB algorithm** that explicitly balances **exploration** and **exploitation** to address these issues.

## 🚀 Key Advantages ("Wow Factor")

BanditNAS adapts its exploration strategy based on the adversarial nature of the SciML loss landscape, resulting in significantly improved performance and robustness:

| Feature | Visual Placeholder | Description |
| :--- | :--- | :--- |
| **Adaptive Selection** | *[Animated GIF/Video of $\mathbf{p_t}$ evolution]* | An animation showing the selection probabilities $\mathbf{p_t}$ for a search space $K$ over time $T$. The initially uniform distribution rapidly but smoothly converges, showing the core exploration-to-exploitation transition. |
| **Regret Performance** | *[Plot of Cumulative Regret]* | A log-log plot comparing the cumulative regret of **BanditNAS** (showing lower, theoretically-driven regret) against baselines like HyperBand and EXP3, demonstrating superior theoretical and empirical efficiency. |
| **Robustness** | *[Heatmap/Bar Chart Comparison]* | A plot demonstrating BanditNAS's consistent performance gain across various SciML settings (Noisy Loss, Slow Convergence, Dynamic Optimization). |

## ⚙️ Installation

### Prerequisites
* Python 3.8+
* `pip`

### Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your_organization/BanditNAS-SciML.git](https://github.com/your_organization/BanditNAS-SciML.git)
    cd BanditNAS-SciML
    ```

2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## 🔬 Running Experiments

### 1. Simple Demonstration
For a quick test and to understand the algorithm's mechanics, we recommend running the provided Jupyter notebook:

```bash
jupyter notebook notebooks/simple_banditnas_demo.ipynb
