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

### 🧩 Project Architecture
#### Frontend

main.html → Dashboard & navigation

home1.html → Air Quality input form

result1.html → Air Quality results

home2.html → Water Quality input form

result2.html → Water Quality results

report.html → Project overview + Tableau link

#### Backend

app.py → Core Flask app

Loads ML models

Handles routing

Processes predictions

Validates inputs & applies classification logic

### 📁 Project Structure

#### Environmental-Safety-APP/

├── app.py                     
├── requirements.txt           

├── static/

│   ├── image/                 
│   ├── image1/                
│   ├── image2/                
│   ├── style.css              
│   ├── style1.css             
│   └── style2.css             

├── templates/

│   ├── main.html              
│   ├── home1.html             
│   ├── result1.html          
│   ├── home2.html             
│   ├── result2.html           
│   └── report.html            

├── models/

│   ├── air_quality_classification  
│   ├── air_quality_regression
│   ├── water_quality
│   ├── air_reg.pkl            
│   ├── air_cls.pkl            
│   └── water_model.pkl        

├── deployment/

│   └── pythonanywhere_config.md  
├── README.md                
└── .gitignore              

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
