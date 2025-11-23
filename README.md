this was my third year mini project in college, it can take health parameters (like Glucose levels, Blood Pressure, BMI, etc.) and provide an prediction. It also includes pages for prevention tips and general health risks associated with diabetes.

Features:
Real-time Prediction: Input patient data and get an immediate result.

Educational Content: Dedicated sections for diabetes risks and prevention (/risk, /prevention).

Clean Interface: Simple, easy-to-navigate UI.

Data Preprocessing
Before training the model, I cleaned the data to ensure accuracy:
Handling Missing Values:Columns like Glucose, Blood Pressure, and BMI contained '0' values which were physically impossible. I replaced these zeros with the mean/median of their respective columns.

Train/Test Split: The data was split into training and testing sets to evaluate performance on unseen data.


I chose **Logistic Regression** for this project because it is effective for binary classification problems (Diabetic vs. Non-Diabetic). 

<img width="800" height="600" alt="image" src="https://github.com/user-attachments/assets/f824fb8a-5e3d-4ae6-a243-f109b6a83f86" />

Tech Stack
Backend: Django (Python)
Frontend: HTML, CSS
Dataset : Pima Indians Diabetes Dataset (kaggle) -It contains health metrics for various patients, including pregnancies, glucose levels, blood pressure, skin thickness, insulin, BMI, diabetes pedigree function, and age.
Database: SQLite (Default Django DB)

💻 How to Run Locally
If you want to run this project on your own machine, follow these steps:

Clone the repository

Bash

git clone https://github.com/Rishikabale/DiabetesPredication.git
cd DiabetesPredication
Create a Virtual Environment (Recommended)

Bash

python -m venv .venv
# Windows
.venv\Scripts\activate
# Mac/Linux
source .venv/bin/activate
Install Dependencies

Bash

pip install django pandas scikit-learn numpy
# OR if a requirements.txt exists:
# pip install -r requirements.txt
Run Migrations

Bash

python manage.py migrate
Start the Server

Bash

python manage.py runserver
Open your browser and go to http://127.0.0.1:8000/.

 Future Improvements
There are a few things I plan to add to this project:

Add user authentication (Login/Signup) to save prediction history.

Improve the UI/UX with Bootstrap or Tailwind CSS.

Train the model on a larger dataset for better accuracy.
