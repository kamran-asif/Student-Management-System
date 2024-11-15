# Student-Management-System
This is a Python-based Student Management System (SMS) built using the Tkinter library for the GUI. The application enables users to manage student records by adding, viewing, updating, deleting, and visualizing data. The application also fetches the user's location, current temperature, and a "Quote of the Day" for an enhanced user experience.

# Features
1. Add Student
Add a student's roll number, name, and marks.
Validations for inputs to ensure correctness.
2. View Students
View all student records stored in the database.
3. Update Student
Update the name and marks of a student based on the roll number.
4. Delete Student
Delete a student record using the roll number.
5. Charts
Visualize student marks using a bar chart.
6. Additional Features
Displays:
Current location (using IP-based geolocation).
Current temperature (using OpenWeatherMap API).
Quote of the Day (from BrainyQuote).

# Prerequisites
Libraries
Ensure the following libraries are installed:

Tkinter: For GUI development.
requests: For fetching API data.
bs4 (BeautifulSoup): For web scraping.
sqlite3: For database operations.
matplotlib: For chart visualization.
You can install these libraries using pip:

bash
Copy code
pip install requests beautifulsoup4 matplotlib

# Setup
Clone or Download the Repository
Download the project files into a directory.

Database Initialization

Create an SQLite database named datab.db.
Create a student table with the following schema:
sql
  Copy code
CREATE TABLE student (
    rno INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    marks INTEGER NOT NULL
);
 Update API Key

Replace "c6e315d09197cec231495138183954bd" with your OpenWeatherMap API key in the temp function:
python
Copy code
a3 = "&appid=" + "YOUR_API_KEY"
Run the Application
Execute the script using Python:

bash
Copy code
python <script_name>.py

# Usage
Add a Student: Navigate to the Add section and provide valid roll number, name, and marks.
View Students: Use the View button to see all stored student data.
Update Student: Navigate to the Update section and modify a student's details using their roll number.
Delete Student: Use the Delete section to remove a student's record.
Charts: View a bar chart of student marks by clicking Charts.
File Structure
bash
Copy code
.
├── main.py              # Main script for the application
├── datab.db             # SQLite database file
└── README.md            # Project documentation

# API Details
1. OpenWeatherMap API
Used to fetch the current temperature for a city.
Get API Key.
2. IPInfo API
Used to fetch the location of the user based on their IP.
No API key required for basic usage.
3. BrainyQuote
Scraped for the "Quote of the Day" using BeautifulSoup.
