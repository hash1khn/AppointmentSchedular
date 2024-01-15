Scheduling Desktop Application
Overview
This repository contains the source code for a GUI-based scheduling desktop application developed for a global consulting organization. The application is designed to handle customer records, appointments, scheduling functionalities, and user activity tracking. It utilizes JavaFX SDK for the GUI and MySQL JDBC Driver to interact with the provided MySQL database.

Requirements
Please ensure your development environment includes JavaFX SDK and MySQL JDBC Driver. If using NetBeans IDE, make sure the custom library for JavaFX .jar files is named "JavaFX." For IntelliJ IDEA, the folder where the JavaFX SDK resides will be used as the library name.

Installation and Setup
Clone the repository to your local machine.
Set up your development environment with JavaFX and MySQL JDBC Driver.
Import the project into your IDE.
Usage
1. Log-in Form
Accepts username and password, providing appropriate error messages.
Determines the user's location (ZoneId) and displays it on the form.
Displays the form in English or French based on the user's computer language setting.
Automatically translates error control messages into English or French based on the user's language setting.
2. Customer Record Functionalities
Customer records and appointments can be added, updated, and deleted.
Customer data is collected using text fields (name, address, postal code, phone number).
Auto-generates Customer_ID; first-level division and country data collected using combo boxes.
Displays customer data in a TableView; updates can be performed in text fields.
Custom message displayed when deleting a customer record.
3. Scheduling Functionalities
a. Appointment Management
Enables the user to add, update, and delete appointments.
Custom message displayed with Appointment_ID and type of appointment canceled.
Auto-generates and disables Appointment_ID.
All appointment fields can be updated except Appointment_ID.
Displays original appointment information on the update form in local time zone.
b. Appointment Schedules
User can view appointment schedules by month and week using a TableView.
Allows switching between month and week views with tabs or radio buttons.
Columns: Appointment_ID, Title, Description, Location, Contact, Type, Start Date and Time, End Date and Time, Customer_ID, User_ID.
c. Timezone Handling
Appointment times stored in Coordinated Universal Time (UTC).
Automatically updates appointment times according to the local time zone set on the user's computer.
ET business hours check before storing in UTC.
d. Input Validation and Logical Error Checks
Prevents scheduling appointments outside business hours, overlapping appointments, and incorrect username/password.
Displays custom messages for each error check.
e. Appointment Alerts
Alerts for appointments within 15 minutes of user log-in.
Custom message includes Appointment ID, date, and time.
f. Reports
Displays the following reports in the user interface:
Total number of customer appointments by type and month.
Schedule for each contact, including appointment ID, title, type, description, start date and time, end date and time, and customer ID.
An additional user-defined report.
Lambda Expressions
Two lambda expressions are utilized to enhance code readability and conciseness. Detailed comments are provided in the code to justify their use.

User Activity Tracking
User log-in attempts, dates, timestamps, and success status are recorded in the login_activity.txt file. Each new record is appended to the existing file and saved in the root folder of the application.

Javadoc Comments
Descriptive Javadoc comments are provided for at least 70 percent of the classes and their members throughout the code. An index.html file of the comments is included based on Oracle's guidelines for the Javadoc tool best practices. Each lambda expression is justified in the comments of the method where it is used.
