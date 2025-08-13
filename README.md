# ❤️⚡ Variational Quantum Classifier – Heart Disease Prediction

## 🎉 Introduction

Welcome to our **Variational Quantum Classifier (VQC)** project! Developed as the **capstone project** for the **Road to Quantum Practitioner** program, organized by **IBM Quantum** and **Freeya Mind Campus**, this project explores how **quantum machine learning** can be applied to predict heart disease using the **UCI Heart Disease dataset**.

We implemented the model using **Qiskit 2.0** to harness the potential of **noisy intermediate-scale quantum (NISQ)** devices, with careful attention to feature selection, optimization strategies, and practical considerations for real-world deployment.

---

## ⚙️ Key Features

### 🔄 Flexible Optimization Options
- **Choice of Optimizers**: 
  - **CMA-ES** (evolutionary strategy) for global optimization
  - **COBYLA** (gradient-free) for faster convergence
- **Tunable Parameters**:
  - Adjustable population size for CMA-ES
  - Customizable iteration limits for both optimizers
  - Configurable shot count for measurement precision

### 💾 Checkpoint System
- Automatic saving of parameters and cost values after each iteration
- Resume training from last checkpoint after interruptions
- Particularly valuable for real quantum hardware runs with long queue times

### 🔬 Experimental Controls
- Switch between real quantum backends and high-performance simulators
- Region selection for IBM Quantum access (us-east or eu-de)
- Reproducibility via fixed random seeds

### 📊 Analysis Tools
- Live cost function tracking during optimization
- Multiple test runs for reliable accuracy estimation
- Statistical reporting (mean, standard deviation, confidence intervals)
- Comparison tool against previous runs

---

## ⚙️ Requirements

* Python 3.10+
* Qiskit 2.0+
* NumPy, Pandas, Matplotlib, Scikit-learn
* Jupyter Notebook
* (Optional) CMA-ES for evolutionary optimization

---

## 🚀 Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/dosqas/r2p-quantum-capstone-project.git
   ```

2. Navigate into the folder:

   ```bash
   cd r2p-quantum-capstone-project
   ```

---

## ▶️ Running the Project

1. Open the Jupyter notebook:

   ```bash
   jupyter notebook
   ```

2. Run through `heart-disease-vqc.ipynb` to train and evaluate the quantum classifier.

---

## 🌟 Implementation Highlights

### Quantum Circuit Design
- **4-Qubit Architecture**: Matches selected clinical features
- **ZZFeatureMap**: For effective classical-to-quantum encoding
- **RealAmplitudes Ansatz**: Optimized for NISQ devices

### Feature Selection
- Clinically relevant features: chest pain type (cp), ST depression (oldpeak), sex (gender), exang (exercise-induced angina)
- Rigorous preprocessing: Normalized to [0,π] for angle encoding
- Correlation-validated feature set

### Hybrid Optimization
- Classical optimization of quantum parameters
- Noise-adaptive CMA-ES variant for hardware runs
- Cost-efficient COBYLA for rapid prototyping

---

## 🛠️ Challenges & Solutions

| Challenge | Our Approach |
|-----------|--------------|
| Limited Qubits | Careful feature selection + dimensionality reduction |
| Noisy Hardware | CMA-ES with noise adaptation + multiple test runs |
| Long Queue Times | Checkpoint system + session management |
| Training Speed | Hybrid classical-quantum optimization |

---

## 🖥️ Project Presentation

For a detailed explanation of our approach, workflow, and results, check out our presentation:  
[📑 View Presentation](presentation/presentation.pdf)

---

## Acknowledgements  

* Special thanks to **IBM Quantum** and **Freeya Mind Campus** for the *Road to Practitioner* program
* Gratitude to the **Qiskit team** for their powerful quantum computing tools
* Heartfelt thanks to our teacher **Tudor Mihoc** for guidance and opportunity
* Appreciation to my teammates **Rodica, Gheorghe, and Adrian** for their collaboration
* Inspired by the quantum computing community's open knowledge sharing

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 💡 Contact

Questions, feedback, or ideas? Reach out anytime at [sebastian.soptelea@proton.me](mailto:sebastian.soptelea@proton.me).

---

## 🔗 Resources
- [Qiskit Documentation](https://qiskit.org/documentation/)
- [UCI Heart Disease Dataset](https://archive.ics.uci.edu/ml/datasets/Heart+Disease)
- [CMA-ES Paper](https://arxiv.org/abs/1604.00772)
