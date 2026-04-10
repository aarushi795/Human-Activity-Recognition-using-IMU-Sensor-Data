# Human Activity Recognition using IMU Sensor Data

## Overview
This project focuses on analyzing and visualizing IMU (Inertial Measurement Unit) sensor data to understand and differentiate human activities. It uses multiple real-world datasets and statistical + dimensionality reduction techniques to extract meaningful insights.

## Datasets Used
1. **WISDM Dataset**
   - 5,000+ instances, 46 features
   - Activities: Walking, Jogging, Sitting, Standing, Upstairs, Downstairs
   - Features include statistical measures like mean, std, skewness, kurtosis

2. **MHEALTH Dataset**
   - Multi-sensor (accelerometer, gyroscope, ECG, EMG, magnetometer)
   - 12 activities including running, cycling, jumping
   - Data collected from 10 subjects

3. **UCI HAR Dataset**
   - 10,000+ instances, 561 features
   - Smartphone-based IMU data
   - Activities: Walking, Sitting, Standing, Laying, etc.

---

## Workflow

### 1. Data Preprocessing
- Cleaned ARFF and log files
- Converted categorical labels
- Removed missing values
- Structured datasets into pandas DataFrames

### 2. Statistical Analysis (ANOVA)
- Performed ANOVA test to identify important features
- Key findings:
  - WISDM: `YABSOLDEV`, `YSTANDDEV`, `RESULTANT`
  - MHEALTH: `acc_x`, `gyro_y`, `emg_2`
  - UCI HAR: entropy and acceleration-based features

👉 These features strongly differentiate between activity classes

---

### 3. Dimensionality Reduction (PCA)
- Reduced high-dimensional data to 2D
- Observations:
  - Jogging forms clear clusters
  - Sitting & Standing overlap
  - Walking & stair activities partially overlap

---

### 4. Data Visualization
Used multiple plots:
- PCA scatter plots
- Pairplots
- Boxplots
- Bar charts for sensor means
- Feature distribution plots

---

## Key Insights

### Activity Patterns
- **Jogging / Running** → high variance, clearly separable  
- **Walking / Stairs** → moderate overlap  
- **Sitting / Standing** → low motion, hard to distinguish  

### Sensor Importance
- Accelerometer & gyroscope → most informative  
- EMG → captures muscle activity  
- ECG → reflects intensity of activity  
- Magnetometer → less significant but useful for orientation  

### Feature Behavior
- Dynamic activities show:
  - higher variance
  - stronger sensor signals  
- Static activities:
  - low variance
  - clustered near origin  

---

## Tools & Technologies
- Python (Pandas, NumPy)
- Scikit-learn (PCA, preprocessing)
- SciPy (ANOVA)
- Matplotlib & Seaborn (visualization)
- Google Colab

---

## Limitations
- Overlap between similar activities (e.g., sitting vs standing)
- No advanced ML model used (focus is analysis)
- Sensor noise and variability across users

---

## Future Work
- Apply classification models (SVM, Random Forest, Deep Learning)
- Real-time activity recognition system
- Feature selection optimization
- Sensor fusion improvements

---

## Conclusion
This project demonstrates how statistical analysis and visualization can effectively extract patterns from IMU sensor data and differentiate human activities, forming a strong foundation for activity recognition systems.

---

## Author
Aarushi Mayekar
B.Tech Robotics & AI
