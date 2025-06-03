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

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributions

Feel free to fork this repo and submit a pull request if you'd like to improve or extend it. Bug fixes, feature additions, and refactoring are welcome.

---

## 👤 Author

**Your Name**
[Linkedin](https://www.linkedin.com/in/dan4o/)
