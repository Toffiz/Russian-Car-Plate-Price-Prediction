# 🚗 LightGBM Regression with Optuna Hyperparameter Tuning

This project implements a regression pipeline using [LightGBM](https://lightgbm.readthedocs.io/) with [Optuna](https://optuna.org/) for hyperparameter tuning. The primary goal is to predict continuous values (e.g., license plate prices) while optimizing the SMAPE (Symmetric Mean Absolute Percentage Error) metric.

---

## 🔧 Features

- 📊 LightGBM for fast and accurate regression  
- 🔍 Optuna for efficient hyperparameter optimization  
- 🧪 Custom SMAPE metric for evaluation  
- 🧼 Data preprocessing and log-transform support  
- 📈 Train-validation split with early stopping

---

## 📁 Project Structure

```

.
├── data/                  # CSV or Parquet input files
├── models/                # Trained model checkpoints
├── notebooks/             # Jupyter notebooks (EDA, experiments)
├── scripts/
│   ├── train.py           # Main training script
│   ├── utils.py           # Utility functions (SMAPE, preprocessing, etc.)
│   └── optuna\_tune.py     # Optuna objective function
├── requirements.txt
└── README.md

````

---

## 🚀 How to Run

1. **Install dependencies:**

```bash
pip install -r requirements.txt
````

2. **Prepare your data:**

Place your training dataset as a CSV in the `data/` folder. You should have a target column like `price` or similar.

3. **Train the model:**

```bash
python scripts/train.py
```

You can set optional arguments inside the script or refactor it to use CLI options.

---

## ⚙️ Example: Optuna Tuning

To run Optuna for hyperparameter tuning:

```bash
# Inside scripts/train.py or optuna_tune.py
use_optuna = True
n_trials = 100  # Customize as needed
```

After tuning, the best hyperparameters and SMAPE score will be printed.

---

## 📈 Metric

We use **SMAPE** (Symmetric Mean Absolute Percentage Error), which is defined as:

$$
\text{SMAPE} = \frac{100\%}{n} \sum_{i=1}^{n} \frac{|y_{\text{pred},i} - y_{\text{true},i}|}{(|y_{\text{true},i}| + |y_{\text{pred},i}|)/2}
$$

Implemented as a custom metric in LightGBM.

---

## 📦 Dependencies

* lightgbm
* numpy
* pandas
* optuna
* scikit-learn

Install with:

```bash
pip install -r requirements.txt
```

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributions

Feel free to fork this repo and submit a pull request if you'd like to improve or extend it. Bug fixes, feature additions, and refactoring are welcome.

---

## 👤 Author

**Your Name**
[GitHub Profile](https://github.com/yourusername)
