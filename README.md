PATIENT HEALTH MONITORING SYSTEM
1. INTRODUCTION
The Patient Health Monitoring System is a small Python program that helps store basic health details of patients. The user can add patient information, see all saved patients, check their health using simple rules, and save everything into a text file.

2. OBJECTIVE
The main aim of this project is to create a simple system that can:
•	Record patient information
•	Analyze basic health conditions
•	Display stored patient data
•	Save the data to a file

3.PYTHON CONCEPTS USED:
•	Variables
•	Lists
•	Dictionaries
•	If-else conditions
•	Loops
•	User input (input())
•	File handling (writing to a file)

4. HOW THE SYSTEM WORKS
When the program starts, it shows a menu with the following options:
1.	Add Patient
2.	View Patients
3.	Analyze Health
4.	Save to File
5.	Exit
The user chooses a number, and the program performs that task.
4.1 ADD PATIENT
The user enters:
•	name
•	age
•	blood pressure
•	sugar level
•	temperature
The program saves this information in a dictionary and stores it in a list.
4.2 VIEW PATIENTS
Shows all patients saved in the list.
4.3 HEALTH ANALYSIS
The program checks:
•	If sugar level is above 140 → high sugar
•	If temperature is above 37.5°C → fever
•	If BP is not “120/80” → abnormal BP
This is a simple rule-based analysis.
4.4 SAVE TO FILE
All patient data is written into a text file called patients.txt so the information is not lost.

5. DATA STORAGE
The program stores each patient like this:
{
    "name": "John",
    "age": "30",
    "bp": "120/80",
    "sugar": 130,
    "temp": 36.5
}
All these dictionaries are kept inside a list named patients.
 

6. LIMITATIONS
•	Data is lost when the program closes unless it is saved to the file
•	Only basic health checks
•	No GUI (text-only program)
•	Not meant for real medical use

7. CONCLUSION
This project is a simple Python application that helps beginners practice how to collect data, store it, analyze it, and save it. It shows how Python can be used to build small useful tools.

