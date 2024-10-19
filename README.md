**Student Performance Ranking System**
This is a web-based application developed using Flask that ranks students based on their academic performance and extracurricular activities. The application processes various student-related metrics to predict a performance score using a machine learning model, and displays the top 3 students from each year.

**Table of Contents**
Project Description
Features
Technologies Used
Installation
Usage
Dataset
Model Training
Future Enhancements


**Project Description**

The Student Performance Ranking System ranks students by predicting their overall academic and extracurricular performance. This ranking is based on features such as GPA, core course grades, participation in hackathons, paper presentations, research publications, leadership roles, certifications, workshops attended, internships, attendance, and scholarships.

A HistGradientBoostingRegressor model is used to calculate a score for each student, which is then used to rank students. The top 3 students from each academic year are displayed on the web page.

**Features**
Student Score Calculation: Ranks students using various academic and extracurricular metrics.
Top Students Display: Displays the top 3 ranked students for each academic year.
Machine Learning Model: Uses the HistGradientBoostingRegressor to predict student performance scores.
Data Preprocessing: Handles missing data using imputation and standardizes the feature set using StandardScaler.

**Technologies Used**
Python 3.8+
Flask: Lightweight web framework for Python.
Pandas: Data manipulation and analysis library.
Numpy: Fundamental package for scientific computing.
Scikit-learn: Machine learning library for model building and preprocessing.
HTML/Jinja2: For rendering templates and displaying the top students.

**Installation**
To run this project locally, follow these steps:

**Clone the repository:**

git clone https://github.com/your-username/student-performance-ranking-system.git
Navigate to the project directory:

cd student-performance-ranking-system
Install required dependencies: Create a virtual environment (optional but recommended):

python3 -m venv venv
source venv/bin/activate  # For Linux/macOS
venv\Scripts\activate     # For Windows

**Install dependencies:**


**pip install -r requirements.txt**
Add the student dataset: Ensure that the student_dataset.csv is in the project folder. The dataset should include the following columns:

Cumulative GPA
Core Engineering Course Grades
Hackathon Participation
Paper Presentations
Research Publications
Leadership Roles
Certifications
Workshops Attended
Internships
Attendance Record
Scholarships/Awards
Year

**Run the Flask application:**

**
python app.py**
Access the application: Open a browser and navigate to http://127.0.0.1:5000/ to view the top students.

**Usage**
Once the application is running, it will automatically process the student data, apply machine learning to predict student scores, and display the top 3 students from each year. You can modify the dataset and re-run the application to evaluate new data.

Routes
/: Displays the top students ranked by the predicted score.
Dataset
The dataset used for this project (student_dataset.csv) should contain information about student performance, including both academic and extracurricular activities. Here's an example of the structure:

Cumulative GPA	Core Engineering Course Grades	Hackathon Participation	Paper Presentations	Research Publications	Leadership Roles	Certifications	Workshops Attended	Internships	Attendance Record	Scholarships/Awards	Year
3.8	A,B,A,B,C	National	2	1	President	3	5	2	90	1	3
Model Training
The model used in this project is the HistGradientBoostingRegressor from scikit-learn, which is well-suited for handling tabular data. The following steps are performed for model training:

Feature Engineering: Derived features such as core_course_score, hackathon_score, and leadership_score are created from existing columns.
Data Imputation: Missing values in numerical features are filled using the mean of the respective columns.
Normalization: Numerical features are standardized using StandardScaler.
Model Training: The processed data is used to train a HistGradientBoostingRegressor, which predicts the student performance score based on the input features.
Future Enhancements


User Authentication: Add login and registration functionality for students and administrators.
Dynamic Dataset Upload: Allow users to upload new datasets dynamically from the web interface.
Enhanced Visualizations: Incorporate graphs and charts to display student performance trends over time.
Export Results: Provide an option to download the ranked student list as a CSV or PDF.

Output:
![WhatsApp Image 2024-10-19 at 07 34 47_8b02a972](https://github.com/user-attachments/assets/12266130-84ba-4951-bcbd-7cea18388830)
