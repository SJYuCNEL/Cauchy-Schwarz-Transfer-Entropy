# Cauchy-Schwarz-Transfer-Entropy
This repository contains the official implementation for our paper, *Cauchy-Schwarz Divergence Transfer Entropy*, which has been accepted for presentation at **ICASSP 2025**. If you find it helpful, please kindly 🌟star it and cite our 📜paper.

## Overview
<p align="center">
  <img src="https://github.com/zhaozhaoma/Images/blob/main/ICASSP2025/KL%20Divergenc%26%20CS%20Divergence%20Comparison.png" width="500" alt="CS-TE Overview"/>
  <br>
  <em>Figure 1: KL divergence is infinite even though there is an overlap between supp(p) and supp(q), but neither is a subset of the other. CS divergence does not have such constraint.</em>
</p>

<p align="center">
  <img src="https://github.com/zhaozhaoma/Images/blob/main/ICASSP2025/Complex%20Causal%20Relationships.png" width="500" alt="CS-TE Overview"/>
  <br>
  Figure 2: (a) indirect causality from 𝑥 to 𝑧. (b) 𝑥 is a confounder to 𝑦 and 𝑧; (c) synergistic effect (𝑥 and 𝑦 produce a causal effect to 𝑧 greater than the sum of their individual effects).
</p>

This paper introduces Cauchy-Schwarz Transfer Entropy (CS-TE), a novel information-theoretic measure for detecting causality in time series data. By leveraging the Cauchy-Schwarz (CS) divergence, CS-TE provides a closed-form estimator that simplifies computation and extends the capability of traditional Transfer Entropy (TE) to capture more intricate causal relationships. Additionally, we explore a supervised learning approach for Granger causality tests, enhancing the robustness and applicability of causal inference in complex systems.

## Contributions
#### 🚀 Closed-Form Estimator
We develop a Cauchy-Schwarz Transfer Entropy (CS-TE) with a closed-form estimator, enabling efficient and straightforward computation of transfer entropy without the need for complex regression models.

#### 🔗 Multivariate Extensions
We introduce CS-Conditional Transfer Entropy (CS-CTE) and CS-Joint Transfer Entropy (CS-JTE), extending CS-TE to multivariate time series. These extensions allow for the identification of indirect causation and synergistic effects, capturing more comprehensive causal interactions beyond pairwise relationships.

#### 📊 Robust Causal Inference
We Enhance the robustness of causal network analysis by utilizing CS divergence, which offers superior performance in the presence of noise and high-dimensional data, making it suitable for real-world applications.

#### 🤖 Supervised Causality Detection
We Explore the use of classifiers instead of traditional regression models for Granger causality tests. By constructing supervised learning frameworks with features based on CS-TE, the approach simplifies the inference of causal directions without relying on permutation tests.

#### 📈 Empirical Validation
We demonstrate the effectiveness of CS-TE and its extensions on benchmark simulated datasets and real-world stock index data from 14 global markets. The results validate the method’s capability to accurately detect and analyze causal relationships in diverse and complex systems.

## Repository Structure
```
.
├── code_demo/                       
│   └── Code Demo.ipynb               # Jupyter notebook demo
│       ├── CS-TE Core Function Implementation/
│       └── Calculation Example/
├── supplementary_material/           # Additional resources
    ├── Motivation/                   # Motivation of this paper
    ├── Mathematical Proofs/          # Detailed proofs for empirical estimator of CS Divergence
    ├── Casual Network Comparisons/   # Causal network comparison based on 5 different methods
    ├── Experimental Details/         # Including nonlinear test data, Gaussian Kernel Bandwidth, and validation of causal network illustration
    └── Permutation Test/             # Algorithm flow of permutation test

```


> [!NOTE]
> Gaussian kernel bandwidth plays a crucial role in the overall computation. Proper adjustments must be made according to the data characteristics. You can adjust the `eta` parameter in the `compute_causality` function to modify this aspect of the calculation. For more details about Gaussian kernel bandwidth, please refer to our supplementary material.

## Citation
If you find the paper and any resources here helpful, please kindly cite our paper:
```
@article{,
  title={Cauchy-Schwarz Divergence Transfer Entropy},
  author={},
  journal={},
  year={}
}
```






















<!This repository serves as the supplementary material for our paper *Cauchy-Schwarz Divergence Transfer Entropy*.

Please review the [Supplementary Material](https://github.com/zhaozhaoma/Cauchy-Schwarz-Transfer-Entropy/tree/main/Supplementary%20Material) folder, which contains detailed mathematical proofs, experimental details, and comparisons of causal networks generated using different methods.

For sample code related to Cauchy-Schwarz Divergence Transfer Entropy (CS-TE), you can click on the [Code Demo](https://github.com/zhaozhaoma/Cauchy-Schwarz-Transfer-Entropy/tree/main/Code%20Demo) folder to explore the corresponding Jupyter Notebook.>






