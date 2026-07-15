[README.md](https://github.com/user-attachments/files/30051667/README.md)
# Smart-Lender

![License](https://img.shields.io/badge/license-MIT-green.svg)
![Python](https://img.shields.io/badge/python-3.7%2B-blue.svg)

## Project Overview

**Smart Lender** is a machine learning-based loan approval prediction system that analyzes applicant information such as income, credit history, loan amount, and employment details to predict whether a loan should be approved. The system provides a user-friendly web interface built with Flask and uses advanced machine learning models (including XGBoost) for accurate predictions.

## Features

- ✅ ML-based loan approval prediction
- ✅ User-friendly web interface
- ✅ Real-time prediction API
- ✅ Comprehensive data preprocessing
- ✅ Multiple ML model integration (XGBoost, etc.)
- ✅ Responsive design with Bootstrap
- ✅ Input validation and error handling
- ✅ Detailed prediction results with confidence scores

## Project Structure

```
Smart-Lender/
├── README.md                      # Project documentation
├── LICENSE                        # License file
├── requirements.txt               # Python dependencies
├── Dataset/
│   └── loan_prediction.csv       # Training dataset
├── Flask/
│   ├── app.py                    # Flask application
│   ├── static/
│   │   ├── css/                  # Stylesheets
│   │   ├── images/               # Image assets
│   │   └── js/                   # JavaScript files
│   └── templates/
│       ├── home.html             # Home page
│       ├── input.html            # Prediction input form
│       └── output.html           # Prediction results page
├── Training/
│   └── Loan Prediction using ML.ipynb  # Model training notebook
└── IBM/                          # IBM-related resources (if any)
```

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Python 3.7+** ([Download](https://www.python.org/downloads/))
- **pip** (Python package manager - usually comes with Python)
- **Git** (optional, for cloning the repository)
- **Web Browser** (Chrome, Firefox, Safari, Edge, etc.)

### Check Your Python Installation

Open Command Prompt (Windows) or Terminal (Mac/Linux) and verify:

```bash
python --version
pip --version
```

Both commands should return version numbers.

## Installation Guide (Step-by-Step)

### Step 1: Clone or Download the Repository

**Option A: Using Git (Recommended)**
```bash
git clone https://github.com/yourusername/Smart-Lender.git
cd Smart-Lender
```

**Option B: Download ZIP**
1. Click the **Code** button on GitHub
2. Select **Download ZIP**
3. Extract the ZIP file to your desired location
4. Open Command Prompt/Terminal and navigate to the folder:
   ```bash
   cd path\to\Smart-Lender
   ```

### Step 2: Create a Virtual Environment

A virtual environment keeps project dependencies isolated from your system Python.

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**Mac/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

You should see `(venv)` at the beginning of your terminal prompt when activated.

### Step 3: Install Required Dependencies

Make sure you're in the Smart-Lender directory and the virtual environment is activated, then run:

```bash
pip install -r requirements.txt
```

This will install all required packages listed in `requirements.txt` including:
- Flask
- scikit-learn
- XGBoost
- pandas
- numpy
- And other dependencies

### Step 4: Verify Installation

Check if all packages are installed correctly:

```bash
pip list
```

## Dataset Information

### Dataset Location
- **File:** `Dataset/loan_prediction.csv`
- **Source:** Training dataset for the ML model

### Dataset Features

The dataset includes the following features:
- `Loan_ID` - Unique identifier for each loan application
- `Gender` - Applicant gender (Male/Female)
- `Married` - Marital status (Yes/No)
- `Dependents` - Number of dependents
- `Education` - Education level (Graduate/Undergraduate)
- `Self_Employed` - Self-employment status (Yes/No)
- `ApplicantIncome` - Applicant's monthly income
- `CoapplicantIncome` - Co-applicant's monthly income
- `LoanAmount` - Loan amount requested (in thousands)
- `Loan_Amount_Term` - Loan repayment term (in months)
- `Credit_History` - Credit history status (0/1)
- `Property_Area` - Area type (Urban/Semiurban/Rural)
- `Loan_Status` - Approval status (Y/N) - **Target Variable**

## Training the Model

### Step 1: Open the Training Notebook

Navigate to the Training folder and open the Jupyter notebook:

```bash
cd Training
jupyter notebook "Loan Prediction using ML.ipynb"
```

### Step 2: Run All Cells

1. Click on **Cell** in the menu
2. Select **Run All**
3. Wait for all cells to execute

### Step 3: Model Output

The notebook will:
- Load and explore the dataset
- Perform data preprocessing and feature engineering
- Train multiple ML models
- Evaluate model performance
- Generate the final trained model file

## Running the Flask Application (Step-by-Step)

### Step 1: Navigate to Flask Directory

```bash
cd Flask
```

### Step 2: Start the Flask Server

```bash
python app.py
```

**Expected output:**
```
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
 * Restarting with reloader
 * Debugger is active!
 * Debugger PIN: XXX-XXX-XXX
```

### Step 3: Open the Application

1. Open your web browser (Chrome, Firefox, Safari, etc.)
2. Go to: **http://localhost:5000** or **http://127.0.0.1:5000**
3. You should see the Smart-Lender home page

### Step 4: Stop the Server

To stop the Flask server:
- Press **CTRL+C** in your terminal

## How to Use the Application

### Home Page
1. When you first load the application, you'll see the home page
2. This page explains the Smart-Lender project

### Making a Prediction (Input Form)

1. Navigate to the **Prediction** or **Input** section
2. Fill in all required fields:
   - **Gender:** Select Male/Female
   - **Marital Status:** Select Yes/No
   - **Dependents:** Enter number (0-3+)
   - **Education:** Select Graduate/Undergraduate
   - **Employment:** Select Self-Employed or Not
   - **Income:** Enter applicant's monthly income
   - **Co-applicant Income:** Enter co-applicant income (0 if none)
   - **Loan Amount:** Enter loan amount needed
   - **Loan Term:** Select repayment period (in months)
   - **Credit History:** Select Yes (1) or No (0)
   - **Property Area:** Select Urban/Semiurban/Rural

3. Click **Submit** or **Predict**

### Viewing Results (Output Page)

1. The system will process your inputs
2. You'll see the prediction result:
   - **Loan Approved** or **Loan Rejected**
   - Confidence score (if available)
3. Review the result and make decisions accordingly

## Technologies Used

| Technology | Version | Purpose |
|-----------|---------|---------|
| **Python** | 3.7+ | Programming language |
| **Flask** | 1.1+ | Web framework |
| **Scikit-learn** | 0.24+ | ML algorithms |
| **XGBoost** | 1.3+ | Advanced ML model |
| **Pandas** | 1.1+ | Data manipulation |
| **NumPy** | 1.19+ | Numerical computing |
| **Jupyter** | 1.0+ | Notebook environment |

## Troubleshooting

### Issue: "Python not found"
- **Solution:** Install Python 3.7+ and ensure it's added to PATH

### Issue: "Module not found" error
- **Solution:** Ensure virtual environment is activated and run:
  ```bash
  pip install -r requirements.txt
  ```

### Issue: Flask server won't start
- **Solution:** Check if port 5000 is in use:
  ```bash
  netstat -ano | findstr :5000  # Windows
  lsof -i :5000                 # Mac/Linux
  ```

### Issue: Predictions not working
- **Solution:** Ensure the trained model file exists in the Flask directory

## Model Performance

The model achieves:
- **Accuracy:** ~80-85% (varies by training parameters)
- **Precision & Recall:** Evaluated during training
- **Cross-validation:** Implemented for robustness

## Future Improvements

- [ ] Add more sophisticated feature engineering
- [ ] Implement ensemble methods
- [ ] Add model explainability (SHAP, LIME)
- [ ] Create REST API endpoints
- [ ] Add database integration for storing predictions
- [ ] Implement user authentication
- [ ] Add mobile responsiveness improvements
- [ ] Deploy on cloud platforms (AWS, Heroku, etc.)

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact & Support

For questions or support:
- Open an issue on GitHub
- Contact the project maintainer

## Acknowledgments

- Dataset source: [Kaggle Loan Prediction Dataset](https://www.kaggle.com/datasets)
- Flask documentation: [flask.palletsprojects.com](https://flask.palletsprojects.com)
- Scikit-learn: [scikit-learn.org](https://scikit-learn.org)

---

**Last Updated:** July 2026  
**Status:** Active Development
