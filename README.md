# Human Activity Recognition using mHealth Sensor Data

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=for-the-badge\&logo=python\&logoColor=white)
![Sklearn](https://img.shields.io/badge/Scikit--Learn-Ensemble-F7931E?style=for-the-badge\&logo=scikit-learn\&logoColor=white)
![mHealth](https://img.shields.io/badge/Dataset-mHealth-E74C3C?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-2ecc71?style=for-the-badge)

### Classifying 12 Human Physical Activities from Wearable Sensor Data

</div>

---

## Objective

Wearable devices collect continuous streams of accelerometer and gyroscope readings from the human body. The challenge is determining which activity a person is performing using only sensor measurements.

This project classifies **12 human physical activities** using data collected from body-worn sensors. The solution has practical applications in healthcare monitoring, fitness tracking, rehabilitation systems, and activity-aware intelligent devices.

---

## Activities Detected

| ID | Activity                  |
| -- | ------------------------- |
| 1  | Standing Still            |
| 2  | Sitting and Relaxing      |
| 3  | Lying Down                |
| 4  | Walking                   |
| 5  | Climbing Stairs           |
| 6  | Waist Bends Forward       |
| 7  | Frontal Elevation of Arms |
| 8  | Knees Bending (Crouching) |
| 9  | Cycling                   |
| 10 | Jogging                   |
| 11 | Running                   |
| 12 | Jump Front & Back         |

---

## Dataset

| Property         | Detail                                  |
| ---------------- | --------------------------------------- |
| Source           | mHealth Dataset                         |
| Sensors          | Accelerometer and Gyroscope             |
| Sensor Locations | Left Ankle and Right Wrist              |
| Axes             | X, Y, Z for each sensor                 |
| Subjects         | Multiple Participants                   |
| Challenge        | Highly Imbalanced Activity Distribution |

---

## Project Pipeline

```text
Dataset
   │
   ├── Data Cleaning
   ├── Feature Engineering
   ├── Exploratory Data Analysis
   ▼
Data Transformation
(Encoding • Scaling)
   │
   ▼
Model Development
(7 Classification Models)
   │
   ▼
Performance Evaluation
(Accuracy • Precision • Recall • F1)
   │
   ▼
Hyperparameter Tuning
(GridSearchCV)
   │
   ▼
Activity Classification
```

---

## Why Multiple Models?

Instead of relying on a single algorithm, the project compares the performance of seven machine learning classifiers:

| Model                     | Purpose                              |
| ------------------------- | ------------------------------------ |
| Logistic Regression       | Baseline Linear Classifier           |
| K-Nearest Neighbors       | Distance-Based Classification        |
| Support Vector Classifier | High-Dimensional Pattern Recognition |
| Gaussian Naive Bayes      | Probabilistic Baseline               |
| Decision Tree             | Interpretable Classification         |
| Random Forest             | Ensemble Learning                    |
| Gradient Boosting         | Sequential Ensemble Optimization     |

This comparative approach helps identify which algorithm best captures patterns in wearable sensor data.

---

## Data Preprocessing

The dataset underwent multiple preprocessing steps before training:

* Checked for missing values and duplicates
* Balanced the dominant "None" activity class through downsampling
* Removed extreme sensor noise using percentile-based clipping
* Encoded categorical labels using LabelEncoder
* Applied RobustScaler to handle remaining outliers
* Split data into training and testing sets

---

## Exploratory Data Analysis

EDA focused on understanding activity-specific movement patterns captured by wearable sensors.

### Analysis Performed

* Activity distribution visualization
* Sensor-wise time-series analysis
* Histogram-based feature distribution analysis
* Subject-level movement pattern exploration
* Sensor signal comparison across activities

### Key Observations

* Static activities such as standing and sitting showed low sensor variance.
* Dynamic activities such as jogging and running generated high-frequency oscillations.
* Ankle-mounted sensors provided strong signals for locomotion-based activities.
* Distinct movement signatures were visible across different activity classes.

---

## Model Evaluation

Each model was evaluated using:

| Metric           | Description                          |
| ---------------- | ------------------------------------ |
| Accuracy         | Overall prediction correctness       |
| Precision        | Quality of positive predictions      |
| Recall           | Ability to identify true activities  |
| F1 Score         | Balance between Precision and Recall |
| Confusion Matrix | Detailed class-wise performance      |

These metrics provided a comprehensive understanding of model performance across all activity classes.

---

## Results

The models successfully learned activity-specific motion patterns from wearable sensor data.

### Highlights

* Accurate classification of daily human activities
* Strong separation between static and dynamic actions
* Improved performance through data balancing and feature scaling
* Hyperparameter optimization using GridSearchCV enhanced model effectiveness

---

## Technology Stack

| Category                | Tools               |
| ----------------------- | ------------------- |
| Programming Language    | Python              |
| Data Analysis           | Pandas, NumPy       |
| Data Visualization      | Matplotlib, Seaborn |
| Machine Learning        | Scikit-Learn        |
| Model Optimization      | GridSearchCV        |
| Development Environment | Jupyter Notebook    |

---

## Project Structure

```text
human_activity_recognition/
│
├── human_action_detection__1__Niyati_Joshi.ipynb
├── README.md
└── mhealth_raw_data.csv
```

---

## Getting Started

```bash
# Open the notebook

jupyter notebook human_action_detection__1__Niyati_Joshi.ipynb
```

---

## Applications

* Healthcare Monitoring
* Fitness Tracking
* Human Activity Recognition Systems
* Rehabilitation Support
* Smart Wearable Devices
* Movement Analytics

---

## Key Insight

Human Activity Recognition is fundamentally a pattern recognition problem where sensor signals capture unique movement signatures. By combining preprocessing, feature engineering, and ensemble learning techniques, machine learning models can effectively distinguish between a wide range of physical activities.

---

## Author

**Niyati Joshi**

Machine Learning • Data Analytics • Predictive Modeling

---

<div align="center">

*Every movement tells a story. This model learns to read it.*

</div>
