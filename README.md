# 🌍EnviroCheck - "Breathe Safe, Drink Pure"
## AI-Powered Web App for Air and Water Quality Prediction in India
To empower citizens with better access to vital environmental data, we propose a user-friendly, web-based application. This platform will enable individuals to quickly assess the air quality and water quality of any specific location within India, fostering informed decisions for health and well-being.

### Datasets Used
| Dataset                    | Description                                                                | Source                     |
| -------------------------- | -------------------------------------------------------------------------- | -------------------------- |
| **India Air Quality Data** | Pollution levels across Indian cities (PM2.5, PM10, NO₂, SO₂, O₃)          | Kaggle – hansikasachdeva11 |
| **Water Quality Data**     | Water parameters for potability analysis (pH, hardness, nitrate, fluoride) | Kaggle – shreshthvashisht  |

### ⚙️ Model Development
🔹 Air Quality Models

Regression → Linear, Polynomial, Lasso, Ridge, Random Forest
Classification → Logistic Regression, SVC, Decision Tree, Random Forest, XGBoost
Best Performer: Random Forest Regressor (MSE ↓, R² ↑)

🔹 Water Quality Models

Regression → Linear, Polynomial, Lasso, Ridge, Random Forest, LightGBM, MLP
Best Performer: Random Forest & MLP Regressor (High R², Low MSE)

### 📁 Project Structure
#### Environmental Safety APP/
├── app.py                      # Main Flask app: routing, model loading, prediction logic
├── requirements.txt            # Python dependencies
├── static/
│       ├── image               # images for background 
│       ├── image1
│       ├── image2  
│       ├── style.css           # Styling for main dashboard
│       ├── style1.css          # Styling for air quality pages
│       └── style1.css          # Styling for water quality pages
├── templates/
│   ├── main.html               # Central dashboard with navigation options
│   ├── home1.html              # Air quality input form
│   ├── result1.html            # Air quality prediction output
│   ├── home2.html              # Water quality input form
│   ├── result2.html            # Water quality prediction output
│   └── report.html             # Intro page with Tableau dashboard link
├── models/
│   ├── air_quality_classification # Preprocessing notebooks
│   ├── air_quality_regression
│   ├── water_quality
│   ├── air_reg.pkl             # Trained regression model for AQI
│   ├── air_cls.pkl             # Trained model for health classification
│   └── water_model.pkl         # Trained regression model for WQI
├── deployment/
│   ├── pythonanywhere_config.md # Notes for deploying on PythonAnywhere
├── README.md                   # Project overview and instructions
└── .gitignore                  # Excludes model files, logs, and temp data

### 🚀 Installation & Setup
#### Clone the repository
git clone https://github.com/DSASMPFEB/Environmental-Safety-APP.git
cd Environmental Safety APP

#### Create virtual environment
python -m venv venv
source venv/bin/activate   # On Linux/Mac
venv\Scripts\activate      # On Windows

#### Install dependencies
pip install -r requirements.txt

#### Run Flask app
python app.py

### Web App Demonstration Video Link -
https://drive.google.com/file/d/19PaP4gwL2GAYdHLzbGB4MYCUL9k_S94S/view?usp=drive_link

### 🌐Impact
Empowers citizens with accessible, transparent environmental data
Supports public health decisions through real-time predictions
Scalable & adaptable for future environmental datasets
Integrated visual analytics with Tableau for deeper insights
