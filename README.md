Campus Event Reporting Prototype

## Project Summary

Campus Event Reporting System (Prototype)

Project Description
This project is a Campus Event Reporting System built as part of a Campus Event Management Platform. It allows college staff to create and manage events, and students to register, check in, and give feedback. The system tracks event creation, registrations, attendance, and feedback, and provides reports on:
Event popularity (registrations per event).
Attendance percentage and average feedback.
Student participation across events.
Top active students.
The prototype is implemented with FastAPI and SQLite, featuring:
APIs for events, students, registration, attendance, and feedback.
Reporting endpoints and SQL queries.
Sample database schema and seed data for demonstration

Features

Manager of college wise events.

Register students for events.

Take the attendence and feedback (rate 1-5).

Generate reports:

Event popularity (registrations per event)

Attendance summary and average feedback

Student participation counts

Top active students

Tech Stack

Backend: FastAPI (Python)

Database: SQLite (prototype)

ORM: SQLAlchemy

## Quick Start

First run below commands:-

## First Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate

## And install all the requirements
pip install -r requirements.txt

## Initialize DB with sample data
## Run below command to Seeded sample data
python seed.py

# Run server
python app.py

## Once you run the above command you can see servers like this:-
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:8000
 * Running on http://10.117.83.49:8000
## Server at http://localhost:8000/health

## When you open http://127.0.0.1:8000/health
you can see output like this -

*/

{
  "status": "ok"
}

/*


## You can also try these endpoints

## Try the below reports endpoints [you can directly paste them in browser so can access below reports]:

Event Popularity Report:
http://127.0.0.1:8000/reports/event-popularity

Student Participation Report:
http://127.0.0.1:8000/reports/student-participation

Top Active Students (bonus):
http://127.0.0.1:8000/reports/top-active-students


## Next You Can Export CSV Reports by using below command:
python reports.py
## You can see output like this - 
- Reports exported to docs/reports
This will create a CSV file in your docs/reports


## Notes
- Tech: Flask + SQLite + SQLAlchemy.
- Data model & APIs are in `DESIGN.md`.
- Added AI conversation screenshots to `ai_log/` directory.
