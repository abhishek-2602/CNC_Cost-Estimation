CNC Cost Estimation – Data Science Internship Assignment

 Candidate: Abhishek A



 Objective
The aim of this project is to develop a machine learning model that predicts the manufacturing cost of CNC-machined parts using real-world features such as material, dimensions, and complexity. The assignment involves web-based data collection, data preprocessing, feature engineering, visual analysis, and predictive modeling.

 Dataset
- Source: Simulated based on real-world data from Alibaba, Xometry, etc.
- File: `scraped_data.csv`
- Total Records: 100
- Features:
  - `Part_Name` – CNC part name
  - `Material` – Material type (Aluminum, Steel, etc.)
  - `Dimensions_mm` – Dimensions (LxWxH in mm)
  - `Quoted_Cost` – Cost in USD
  - `Cycle_Time_min` – Estimated machining time
  - `Feature_Count` – Number of features (holes, threads, etc.)

---

 Feature Engineering
- `Volume_mm3`: Derived from dimensions
- `Cost_per_mm3`: Normalized cost
- `Cost_per_Feature`: Cost per complexity



 Visualizations
- Scatter Plot (Cost vs Volume)
- Box Plot (Cost by Material)
- Correlation Heatmap
- Actual vs Predicted Cost
- Feature Importance Plot



 ML Model
- Model: RandomForestRegressor
- Inputs: `Volume_mm3`, `Feature_Count`
- Target: `Quoted_Cost`

Evaluation
- MAE: ~ 4.73 USD
- RMSE: ~ 6.10 USD



 Insights
- Volume and feature count strongly affect cost.
- Materials affect pricing distribution.
- More features = higher cycle time & cost.



 Folder Structure:
CNC_Cost_Estimation/
├── CNC_Cost_Estimation.ipynb
├── scraped_data.csv
├── README.md

 Improvements:
- Add tolerance/surface finish data
- Pull real-time CAD data
- Predict cycle time alongside cost

Tools Used
- Python, pandas, numpy
- matplotlib, seaborn
- scikit-learn
- Jupyter Notebook

