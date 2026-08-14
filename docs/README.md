# Project Documentation

## Automated Student Intervention Attendance System

This project was developed as an Industry Capstone Project at Griffith University to automate and standardise student attendance capture.

## System Workflow

The solution consists of three main Power Automate workflows:

### 1. Event Organiser Flow

The Event Organiser submits event information through Microsoft Forms.

The Power Automate flow:

1. Captures the organiser's form response.
2. Retrieves the event details.
3. Automatically generates a unique Event ID.
4. Generates the student attendance link.
5. Generates a unique QR code for the event.
6. Generates a manual attendance link as a fallback.
7. Stores the event information in the Event Database.
8. Sends the required event information to the organiser by email.

### 2. QR Attendance Flow

Students scan the event-specific QR code to access the attendance form.

The flow:

1. Captures the student attendance submission.
2. Retrieves the submitted student information.
3. Identifies the associated event.
4. Retrieves the corresponding event information.
5. Stores the attendance record in the Attendance Database.

This design avoids requiring students to manually enter the Event ID or Event Name, reducing the risk of incorrect event information.

### 3. Manual Attendance Flow

A manual attendance process is provided as a fallback when QR-based attendance cannot be used.

The flow retrieves the relevant event information and stores the manual attendance record in the Attendance Database.

## Reporting and Analytics

Power BI was used to analyse attendance data and develop interactive dashboards.

The dashboards provide insights into:

- Total events
- Total attendees
- Guest attendance
- QR attendance
- Manual attendance
- QR adoption rate
- Attendance by campus
- Top events by attendance
- Attendance trends across academic periods
- Campus participation by trimester

## Technologies Used

- Microsoft Forms
- Power Automate
- Microsoft Excel
- SharePoint
- Power BI
- QR-based attendance capture
