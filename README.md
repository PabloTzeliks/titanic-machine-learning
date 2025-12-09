# Titanic Machine Learning - Kaggle Challenge

A machine learning solution for the famous [Kaggle Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic) competition. This project predicts which passengers survived the Titanic shipwreck using various machine learning techniques and data preprocessing methods.

## 🎯 Challenge Overview

The sinking of the Titanic is one of the most infamous shipwrecks in history. This Kaggle challenge asks participants to build a predictive model that answers the question: "what sorts of people were more likely to survive?" using passenger data (ie name, age, gender, socio-economic class, etc).

## 🛠️ Technology Stack

This project was developed using **Google Colab** and leverages the following Python libraries:

- **Pandas** - Data manipulation and analysis
- **Matplotlib** - Data visualization and plotting
- **Seaborn** - Statistical data visualization
- **Scikit-learn** - Machine learning algorithms and tools
- **NumPy** - Numerical computing
- **Regular Expressions (re)** - Pattern matching and text extraction

## 🚀 Main Implementations

### 1. Data Preprocessing & Feature Engineering

The project includes comprehensive data preprocessing with the following techniques:

- **Title Extraction**: Extracts titles (Mr., Mrs., Miss., etc.) from passenger names using regex
- **Title Grouping**: Groups rare titles into a single category for better model generalization
- **Sex Encoding**: Converts gender to numerical values (male: 0, female: 1)
- **Age Imputation**: Fills missing age values with the median age
- **Family Size Feature**: Creates a new feature combining siblings/spouses and parents/children
- **IsAlone Feature**: Binary flag indicating if the passenger was traveling alone
- **Embarked Handling**: Fills missing embarkation port values with the most frequent port
- **Fare Imputation**: Fills missing fare values with the median fare
- **One-Hot Encoding**: Converts categorical embarkation data into binary columns
- **Feature Selection**: Removes unnecessary columns (PassengerId, Name, Ticket, Cabin, SibSp, Parch)

### 2. Model Training & Evaluation

- **Data Split**: 80/20 train-validation split for model evaluation
- **Algorithm**: Random Forest Classifier with 500 estimators and max depth of 5
- **Metrics**: Accuracy score and confusion matrix for performance evaluation
- **Cross-validation**: Uses validation set to assess model performance before final predictions

### 3. Visualization

- Custom visualizations using Matplotlib and Seaborn
- Confusion matrix heatmap for model evaluation
- Exploratory data analysis plots

### 4. Final Predictions

- Trains final model on complete training dataset
- Generates predictions for test dataset
- Outputs results in Kaggle submission format (CSV)

## 📁 Project Structure

```
titanic-machine-learning/
│
├── TitanicDataset.ipynb    # Main Jupyter notebook with complete implementation
├── README.md               # Project documentation
└── submission_pro.csv      # Generated predictions for Kaggle submission
```

## 🔧 How to Use

### Prerequisites

- Google Colab account (or local Jupyter environment)
- Kaggle account to download the Titanic dataset

### Steps to Run

1. **Download the Dataset**
   - Visit the [Kaggle Titanic Competition page](https://www.kaggle.com/c/titanic)
   - Download `train.csv` and `test.csv`

2. **Upload to Google Drive**
   - Create a folder in your Google Drive (e.g., `/MyDrive/titanic/`)
   - Upload both CSV files to this folder

3. **Open the Notebook**
   - Open `TitanicDataset.ipynb` in Google Colab
   - Or click: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/PabloTzeliks/titanic-machine-learning/blob/main/TitanicDataset.ipynb)

4. **Run the Notebook**
   - Execute all cells sequentially
   - The notebook will mount your Google Drive
   - Ensure the file paths match your Drive structure

5. **Generate Predictions**
   - The notebook will create `submission_pro.csv`
   - Download this file and submit it to Kaggle

## 📊 Model Performance

The Random Forest model with feature engineering provides competitive predictions for the Kaggle competition. Key performance metrics are displayed through:

- Accuracy score on validation set
- Confusion matrix visualization
- Feature importance analysis

## 🎓 Key Learnings

This project demonstrates:

- Effective data preprocessing and feature engineering techniques
- Handling missing data in real-world datasets
- Creating new features from existing data (feature engineering)
- Using ensemble methods (Random Forest) for classification
- Proper train-validation split for model evaluation
- Generating predictions in competition-required format

## 🤝 Contributing

Feel free to fork this repository and submit pull requests for any improvements or alternative approaches to solving the Titanic challenge.

## 📝 License

This project is open source and available for educational purposes.

## 🙏 Acknowledgments

- [Kaggle](https://www.kaggle.com/) for hosting the Titanic competition
- The data science community for sharing knowledge and techniques
- Google Colab for providing free computational resources
