# Missing Person Identification and Search System

## Overview

The **Missing Person Identification and Search System** is an AI-assisted application developed to help manage missing-person cases and identify possible matches from submitted images or sightings.

The system uses facial landmark detection and machine learning techniques to compare facial features from registered cases with those obtained from public submissions. It provides separate interfaces for authorized users and the general public, making it easier to register cases, submit sightings, manage records, and review potential matches.

---

## Key Objectives

* Digitize the process of registering and managing missing-person cases.
* Reduce the need for manual comparison of photographs.
* Extract facial features from uploaded images using AI-based face detection.
* Compare registered cases with publicly submitted sightings.
* Provide a centralized dashboard for monitoring case information.
* Allow authorized users to manage cases based on their assigned roles.
* Store and organize case-related information in a structured database.

---

## How the System Works

### 1. Registering a Missing Person

An authorized user can register a new missing-person case by entering the required details and uploading an image.

The system processes the uploaded image and detects facial landmarks. The extracted facial information is converted into numerical data that can later be used for comparison with other records.

### 2. Managing Cases

Registered cases are available through the main application dashboard.

Depending on the assigned role, users can perform actions such as:

* Registering new cases
* Viewing case records
* Managing existing cases
* Monitoring case status
* Initiating the face-matching process

### 3. Public Sighting Submission

A separate public interface allows users to submit information about a possible sighting.

The user can provide relevant details and upload an image or video. The system processes the submitted visual data and extracts facial information when a detectable face is available.

### 4. AI-Based Face Matching

The system compares facial landmark data from registered missing-person cases with the facial data obtained from public submissions.

A K-Nearest Neighbors (KNN) based approach is used to identify potential similarities between the available facial feature vectors.

Potential matches can then be reviewed to assist in determining whether the sighting may be related to an existing case.

### 5. Case Monitoring

The application dashboard provides an overview of registered cases and their current status.

Location-related information can also be visualized to provide a better understanding of the geographical distribution of cases.

---

## Features

| Feature                     | Description                                                           |
| --------------------------- | --------------------------------------------------------------------- |
| Missing Person Registration | Allows authorized users to create and maintain missing-person records |
| Facial Landmark Detection   | Extracts facial landmark information from uploaded images             |
| AI-Based Matching           | Uses machine learning to identify possible facial matches             |
| Public Submission Portal    | Allows the public to submit possible sightings                        |
| Image Processing            | Processes uploaded images for facial information                      |
| Video Processing            | Extracts relevant frames and facial data from uploaded videos         |
| Case Management             | Supports viewing, updating, and managing case records                 |
| Role-Based Access           | Provides different permissions for different types of users           |
| Case Status Tracking        | Helps monitor the progress and status of registered cases             |
| Location Visualization      | Displays geographical information related to cases                    |
| Database Storage            | Stores application data using SQLite                                  |
| Email Notifications         | Supports notifications when configured in the application             |

---

## Technology Stack

The project is built using the following technologies:

* **Python** – Core programming language
* **Streamlit** – Web application interface
* **MediaPipe** – Facial landmark detection and face processing
* **scikit-learn** – Machine learning and KNN-based matching
* **SQLite** – Local database storage
* **SQLModel** – Database modelling and interaction
* **OpenCV** – Image and video processing
* **Folium** – Location and map visualization

---

## Installation

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the Project Directory

```bash
cd <your-project-folder>
```

### 3. Install the Required Dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Application

### Run the Main Application

```bash
streamlit run Home.py
```

### Run the Public Submission Portal

```bash
streamlit run mobile_app.py
```

> Make sure the required files and dependencies are properly configured before running the application.

---

## Face Matching Process

The facial comparison process generally follows these steps:

1. An image is uploaded to the application.
2. The system checks whether a face is detected.
3. Facial landmarks are extracted from the detected face.
4. The landmark data is converted into a numerical feature representation.
5. The extracted information is stored or compared with existing records.
6. The KNN-based algorithm identifies the closest available matches.
7. Potential matches are made available for review.

The quality of the matching process can be influenced by:

* Image quality
* Lighting conditions
* Face orientation
* Visibility of facial features
* Resolution of the uploaded image

---

## User Roles

The application supports role-based access for authorized users.

| Role            | General Access                                                  |
| --------------- | --------------------------------------------------------------- |
| Administrator   | Can access broader system functions and manage cases            |
| Authorized User | Can register and access cases according to assigned permissions |

> For security, passwords should be stored securely and should not be uploaded directly to a public repository.

---

## Database

The project uses **SQLite** for storing application-related data.

The database may contain information such as:

* Missing-person case details
* Case status
* Facial feature information
* Public sighting submissions
* Location-related details
* Application user information

The database helps organize and manage records required for the registration and matching process.

---

## Email Configuration

If email notifications are enabled, mail server credentials can be configured using environment variables.

Example configuration:

```text
SMTP_HOST
SMTP_PORT
SMTP_USER
SMTP_PASSWORD
```

> Sensitive credentials should not be hard-coded or uploaded to a public repository.

---

## Project Structure

```text
project-folder/
│
├── Home.py
├── mobile_app.py
├── requirements.txt
│
├── scripts/
│   └── Helper scripts and utilities
│
├── resources/
│   └── Application resources and stored files
│
├── assets/
│   └── Application assets and screenshots
│
└── Configuration and database files
```

The exact project structure may vary depending on the configuration and version of the application.

---

## Limitations

The system may be affected by several factors, including:

* Low-quality images
* Poor lighting conditions
* Partially visible faces
* Side-facing faces
* Changes in appearance
* Similar-looking individuals
* Limited comparison data

For this reason, the system should be considered a tool for identifying **potential matches** and should not be used as the sole basis for final identification.

---

## Future Enhancements

Possible future improvements include:

* Improving facial matching accuracy
* Adding more advanced deep-learning models
* Supporting larger and more scalable databases
* Adding advanced search and filtering functionality
* Implementing secure cloud-based storage
* Adding real-time notifications
* Improving geographical analysis and reporting
* Enhancing authentication and application security
* Improving video-based face detection
* Developing a dedicated mobile application

---

## Disclaimer

This project is developed for educational and learning purposes. Any images or data used for testing and demonstration should be handled responsibly and in accordance with applicable privacy and data-protection requirements.

The application is intended to assist in identifying potential matches and should not replace appropriate human verification or official identification procedures.
