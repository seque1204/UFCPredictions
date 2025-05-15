## UFC Fight Outcome Prediction

This project aims to predict UFC fight outcomes using a neural network trained on a cleaned and feature-engineered dataset.

### Dataset
- Source: UFC Historical Data
- Size: 7,439 fights × 95 columns
- Target: Predict fight `winner`, `finish_round`, and `method` (KO/TKO, Submission, or Decision)

### Preprocessing
- Dropped irrelevant or redundant columns based on internal documentation.
- Removed rows with missing values.
- Filtered valid weight classes for both men's and women's divisions.
- Converted `weight_class` to numeric weight in pounds.
- Mapped `winner` from `Red`/`Blue` to binary (0/1).
- One-hot encoded `method` (KO/TKO, Submission, Decision).
- One-hot encoded top 14 referees and stances (Orthodox, Southpaw, Switch), adding "other" categories.
- Final dataset shape: **5559 samples × 66 features**

### Target Variables
- `winner` (0 = Red, 1 = Blue)
- `finish_round`
- `Decision`, `KO_TKO`, `Submission` (one-hot encoding of method)

### Train/Test Split
- 80/20 split using `train_test_split()`
- Applied `MinMaxScaler` for normalization
- No missing values in training or testing sets

### Model Architecture (Keras)
- Model: Sequential with final Sigmoid classification layer
- Optimizer: Adam
- Loss: binary_crossentropy
- Epochs: 12
- Batch size: 32
- Validation split: 20%

### Training Performance 
- Final Validation accuracy: **~72%**
- Visualization: Loss and Accuracy curves plotted using Plotly

### Final Test Accuracy
- Accuracy on test set: **~71.8%**

## 🗺️ Motivation

The goal was to test predictive power of neural networks on a dataset of my interest. This project was completed as part of a university-level course in explainable AI and ML.

---

## 📬 Contact

For questions or collaboration opportunities, feel free to reach out via [GitHub Issues](../../issues) or [LinkedIn]([https://www.linkedin.com/in/YOUR-USERNAME](https://www.linkedin.com/in/josequeira/)).
