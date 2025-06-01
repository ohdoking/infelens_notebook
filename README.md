
# 🔍 Infelens: AI Inference Energy & Runtime Estimation

Infelens is a Jupyter Notebook-based project that builds a predictive pipeline to estimate energy consumption, runtime, and CO₂ emissions of large language model (LLM) inference on various hardware configurations. This is part of the Challenge: **"AI Inference Runtime & Power Estimation"**.

---

## 🚀 Project Features

- 📊 Predicts runtime, energy, and CO₂ impact of LLM inference
- 🧠 Trained using multiple regression models, with XGBoost as the final estimator
- 🔧 Uses both AI model metadata and hardware specifications as input features
- 📈 Outputs metrics like MAE, RMSE, and R² for performance validation

---

## 🛠 Installation Guide

### 1. Clone the Repository

```bash
git clone https://github.com/ohdoking/infelens_notebook.git
cd infelens_notebook
```

### 2. Install Jupyter Notebook

```bash
pip3 install jupyter
```

### 3. Set a Jupyter Password

To avoid token login and use a password instead:

```bash
jupyter notebook password
```

Enter your desired password when prompted.

### 4. Start the Notebook (Optional: as root)

```bash
jupyter notebook --allow-root
```

---

## 📁 Project Structure

```
infelens_notebook/
│
├── infelens_energy_pipeline.ipynb    # Main notebook
├── data/                             # Input datasets
├── output/                           # Output predictions and results
└── README.md                         # You're here!
```

---

## 📌 Inputs and Outputs

### Inputs:
- Model: `model_name`, `huggingface_model`, `hidden_size`, `num_layers`, `vocab_size`, `seq_length`, `num_params_B`, `model_type`
- Hardware: `hardware_gpu`, `Manufacturer`, `Memory (GB)`, `TDP (W)`, `CUDA Cores`, `FP32 TFLOPS`, `Architecture`, `hardware_ram_GB`
- Others: `total_prompts`

### Outputs:
- `average_runtime`
- `average_energy`
- `average_co2`

---

## 🧠 Model

Final model used: **XGBoost Regressor (Multi-output)**  
Features:
- Fast training & low compute requirements
- Excellent performance on small and medium-sized datasets
- Regularization & early stopping to prevent overfitting

---

## 📞 Contact

For questions or contributions, open an issue or reach out via GitHub.

---
