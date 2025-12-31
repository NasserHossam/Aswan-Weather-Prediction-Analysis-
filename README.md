☀️ Solar Power Forecasting & Weather Pattern Analysis (Aswan, Egypt)
📌 Project Overview

This project focuses on predicting solar power output levels (Low / Medium / High) using historical weather data from Aswan, Egypt, one of the highest solar radiation regions in the world.
Due to climate variability, accurate solar forecasting is essential for grid stability, energy planning, and renewable integration.

The project applies a complete data science pipeline, including preprocessing, statistical validation, dimensionality reduction, and multiple machine learning models, with a strong emphasis on model comparison and interpretability.

🧠 Objectives

Analyze the relationship between meteorological factors and solar power output

Apply statistical tests to validate feature significance

Reduce feature dimensionality using PCA, LDA, and SVD

Train and compare machine learning and neural network models

Identify the most accurate and robust model for solar power classification

📂 Dataset Description

Location: Aswan, Egypt

Records: 398 observations

Features:

Date

Average Temperature

Dew Point

Humidity

Wind Speed

Atmospheric Pressure

Target Variable:

Solar Power Output (PV)

Categorized into Low / Medium / High

⚙️ Methodology
1️⃣ Data Preprocessing

Missing value checks (none found)

Outlier handling using box plots

Min-Max normalization (Wind, Pressure)

Feature binning:

Temperature → Low / Medium / High

Humidity → Low / Medium / High

Label encoding for categorical features

2️⃣ Statistical Analysis

Used to validate feature relevance:

Chi-Square Test → Dependency between temperature and solar output

ANOVA → Differences in solar output across humidity levels

T-Test & Z-Test → Sample representativeness

✔️ Strong correlations confirmed between Temperature, Pressure, Humidity, and solar output.

3️⃣ Feature Reduction

PCA:

2 components explain ~66.4% of variance

LDA:

Maximizes class separability

SVD:

Extracts latent weather patterns

4️⃣ Machine Learning Models

The following models were trained using 80/20 split and 10-Fold Cross-Validation:

Naive Bayes (Gaussian)

Decision Tree (Entropy – ID3/C4.5)

K-Nearest Neighbors (Manhattan Distance)

Feed-Forward Neural Network (FFNN)

Recurrent Neural Network (RNN)

PCA / LDA / SVD based classifiers

📊 Results Summary
Model	Accuracy
Decision Tree (Entropy)	98.75% ✅
FFNN	97.50%
RNN	96.25%
KNN	93.75%
SVD-Based Classifier	92.50%
LDA Classifier	92.50%
Naive Bayes	90.00%
PCA Classifier	83.75%

🔹 Key Finding:
The Decision Tree (Entropy) achieved the highest accuracy, while Naive Bayes proved highly effective for binned weather data, demonstrating that simpler models can outperform complex ones when preprocessing is done correctly.

🏆 Key Contributions

Developed a comparative solar forecasting framework tailored to Aswan’s climate

Demonstrated the effectiveness of probabilistic models on discretized data

Validated meteorological feature significance using rigorous statistical testing

Achieved near-perfect classification accuracy using interpretable models

🚀 Future Work

Expand dataset to multiple years for seasonal modeling

Move from classification to regression (kW prediction)

Implement hybrid CNN-LSTM models

Deploy model on IoT edge devices (e.g., Raspberry Pi) for real-time forecasting

🛠️ Technologies Used

Python

NumPy, Pandas

Scikit-Learn

Matplotlib, Seaborn

TensorFlow / Keras

📁 Repository Structure
├── Project.ipynb
├── AswanData_weatherdata.csv
├── Final Documentation.pdf
├── README.md

👤 Author

Nasser Hossam Hamed

📚 References

Key references are included in the Final Documentation PDF, covering:

ANN, SVM, LSTM, Ensemble Learning

Solar forecasting benchmarks

Renewable energy forecasting research
