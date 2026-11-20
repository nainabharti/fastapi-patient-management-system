Patient Management System API

A Patient Management System built using FastAPI, Pydantic, and JSON that provides RESTful API endpoints to manage patient records, including creating, viewing, updating, sorting, and deleting patient information.

Features

- Patient Data Validation: Uses Pydantic models to validate patient information.
- BMI Calculation: Calculates Body Mass Index using patient height and weight.
- Health Assessment: Classifies patients based on BMI into Underweight, Normal, Overweight, and Obese categories.
- View All Patients: Retrieves all stored patient records.
- Search Patient: Retrieves an individual patient using their unique ID.
- Sort Patients: Sorts patient records by height, weight, or BMI in ascending or descending order.
- Create Patient: Adds new patient records while preventing duplicate IDs.
- Update Patient: Updates existing patient information using the PUT method.
- Delete Patient: Removes patient records using their unique ID.
- JSON Storage: Stores patient information in a JSON file.

Technologies Used

- Python
- FastAPI
- Pydantic
- Uvicorn
- JSON

Project Structure

fastAPI-tutorial/
│
├── main.py
├── patients.json
├── requirements.txt
└── README.md

Installation and Setup

1. Clone the Repository

git clone <your-repository-url>

2. Navigate to the Project Directory

cd fastAPI-tutorial

3. Create a Virtual Environment

python -m venv myenv

4. Activate the Virtual Environment

For Windows PowerShell:

myenv\Scripts\Activate.ps1

5. Install Dependencies

pip install -r requirements.txt

Run the Application

Start the FastAPI development server:

uvicorn main:app --reload

Open the following URL in your browser:

http://127.0.0.1:8000

API Documentation

FastAPI automatically generates interactive API documentation.

- Swagger UI: http://127.0.0.1:8000/docs
- ReDoc: http://127.0.0.1:8000/redoc

You can test all API endpoints directly through Swagger UI.

API Endpoints

HTTP Method| Endpoint| Description
GET| "/"| Returns the welcome message
GET| "/about"| Provides API information
GET| "/view"| Retrieves all patient records
GET| "/patient/{patient_id}"| Retrieves a specific patient
GET| "/sort"| Sorts patients by height, weight, or BMI
POST| "/create"| Creates a new patient record
PUT| "/edit/{patient_id}"| Updates an existing patient record
DELETE| "/delete/{patient_id}"| Deletes a patient record

BMI Categories

BMI Range| Verdict
Below 18.5| Underweight
18.5 – 24.99| Normal
25 – 29.99| Overweight
30 or above| Obese

Data Storage

Patient records are stored in "patients.json".

The application uses Python's built-in "json" module to read and write patient information.

Future Improvements

- Integrate a database such as SQLite or PostgreSQL.
- Implement authentication and authorization.
- Add more advanced patient search and filtering options.
- Improve error handling and data security.

---

Author: Naina Bharti