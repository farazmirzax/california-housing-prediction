# California Housing Price Prediction

A complete end-to-end machine learning project that predicts California housing prices using the famous California Housing Dataset. This project demonstrates the full ML workflow from data exploration to model deployment.

## 📊 Project Overview

This project builds a regression model to predict median house values in California districts based on various features like location, house age, number of rooms, and proximity to the ocean. The project follows best practices for ML development including:

- Data exploration and visualization
- Feature engineering
- Multiple model comparison
- Hyperparameter tuning
- Model evaluation and validation

## 🎯 Key Results

- **Best Model**: Random Forest Regressor
- **Final RMSE**: ~$47,000 on test set
- **Model Performance**: Evaluated using 10-fold cross-validation
- **Optimization**: Grid search for hyperparameter tuning

## 📁 Project Structure

```
california-housing-project/
├── main.ipynb                          # Main project notebook
├── notebooks/
│   └── 01_data_exploration.ipynb      # Data exploration experiments
├── datasets/
│   └── housing/
│       └── housing.csv                # California housing dataset
├── images/
│   └── end_to_end_project/            # Generated visualizations
├── my_california_housing_model.pkl    # Trained model (saved)
├── requirements.txt                    # Python dependencies
└── README.md                          # Project documentation
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- pip (Python package installer)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/california-housing-project.git
cd california-housing-project
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

### Running the Project

1. Start Jupyter Notebook:
```bash
jupyter notebook
```

2. Open `main.ipynb` and run all cells sequentially

The notebook will:
- Download and load the California Housing dataset
- Perform exploratory data analysis
- Create train/test splits with stratified sampling
- Engineer new features
- Train and compare multiple models (Linear Regression, Decision Tree, Random Forest)
- Perform hyperparameter tuning with GridSearchCV
- Evaluate the final model on the test set
- Save the trained model to disk

## 🔍 Methodology

### 1. Data Acquisition
- Automated download from GitHub repository
- Stored locally in `datasets/housing/`

### 2. Exploratory Data Analysis
- Statistical summaries
- Correlation analysis
- Geographic visualization
- Distribution analysis

### 3. Data Preprocessing
- Stratified train-test split (80/20)
- Handling missing values with median imputation
- Feature engineering (e.g., rooms per household, bedrooms per room)
- Feature scaling with StandardScaler
- One-hot encoding for categorical features

### 4. Model Training
Tested multiple algorithms:
- Linear Regression (baseline)
- Decision Tree Regressor
- Random Forest Regressor (best performer)

### 5. Model Evaluation
- Cross-validation (10-fold)
- RMSE as primary metric
- Grid search for hyperparameter optimization

### 6. Model Deployment
- Model serialization using joblib
- Ready for production deployment

## 📈 Features Used

**Input Features:**
- `longitude`, `latitude` - Location coordinates
- `housing_median_age` - Median age of houses
- `total_rooms`, `total_bedrooms` - Number of rooms
- `population`, `households` - Demographics
- `median_income` - Median income in the area
- `ocean_proximity` - Categorical feature (proximity to ocean)

**Engineered Features:**
- Rooms per household
- Bedrooms per room
- Population per household

**Target Variable:**
- `median_house_value` - Median house value in the district

## 🛠️ Technologies Used

- **Python 3.x**
- **NumPy** - Numerical computing
- **Pandas** - Data manipulation and analysis
- **Matplotlib** - Data visualization
- **Scikit-learn** - Machine learning algorithms and tools
- **Jupyter Notebook** - Interactive development environment

## 📊 Model Performance

| Model | RMSE (Cross-Validation) |
|-------|------------------------|
| Linear Regression | ~$69,000 |
| Decision Tree | ~$71,000 |
| Random Forest | ~$47,000 |

## 💾 Saved Model

The trained Random Forest model is saved as `my_california_housing_model.pkl` and can be loaded for predictions:

```python
import joblib
model = joblib.load("my_california_housing_model.pkl")
predictions = model.predict(new_data_prepared)
```

## 📝 Future Improvements

- [ ] Add more feature engineering techniques
- [ ] Experiment with ensemble methods (XGBoost, LightGBM)
- [ ] Create a web interface for predictions
- [ ] Deploy model as REST API
- [ ] Add confidence intervals to predictions
- [ ] Implement automated model retraining pipeline

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- Dataset source: [Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow](https://github.com/ageron/handson-ml2) by Aurélien Géron
- California Housing dataset from StatLib repository

## 📧 Contact

For questions or feedback, please open an issue in the repository.

---

**Note**: This is an educational project demonstrating machine learning best practices. The model predictions are for learning purposes only.