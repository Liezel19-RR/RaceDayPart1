RaceDay

Part 1: System Planning and Database

1. Project Overview

RaceDay is a full-stack web-based event management system designed for the South African running, walking and cycling community.

The system is designed to help Event Organisers manage sporting events and allow Participants to browse and enter events, select categories, and track their personal results.

Part 1 focuses on planning the RaceDay system before application code is developed. The main deliverables are the Entity Relationship Diagram (ERD), API Endpoint Plan and SQL Database Script.

⸻

2. System Roles

Organiser

The Organiser is responsible for managing events on the RaceDay platform.

An Organiser can:

* Create events.
* Edit events.
* Delete events.
* Manage event categories.
* View Participants enrolled in their events.
* Capture Participant finishing times.
* Capture Participant finishing positions.
* View event results.

Participant

The Participant uses RaceDay to find and participate in sporting events.

A Participant can:

* Create an account.
* Log in to the system.
* View and update their profile.
* Browse upcoming events.
* View event information.
* View available event categories.
* Enter an event by selecting a category.
* View their own enrolments.
* Track their personal race results.

The system supports these two distinct roles throughout the RaceDay project.

⸻

3. Part 1 Database Design

The RaceDay database consists of six main entities:

* Users
* Events
* EventTypes
* Categories
* Enrolments
* Results

The database uses primary keys and foreign keys to establish relationships between the entities and maintain data integrity.

Main Relationships

* A User can create multiple Events.
* A User can have multiple Enrolments.
* An EventType can be associated with multiple Events.
* An Event can contain multiple Categories.
* An Event can have multiple Enrolments.
* A Category can be selected by multiple Enrolments.
* An Enrolment can have zero or one Result.

The ERD represents these relationships using appropriate cardinality.

⸻

4. Repository Structure

RaceDay
│
├── docs
│   ├── RaceDay_ERD.png
│   ├── RaceDay_API_Endpoint_Plan.md
│   └── RaceDay_Database.sql
│
├── .github
│   └── workflows
│       └── part1.yml
│
└── README.md

⸻

5. Documentation

Entity Relationship Diagram

The ERD represents the complete RaceDay database design, including:

* Entities
* Attributes
* Primary keys
* Foreign keys
* Relationships
* Cardinality

The ERD is located at:

/docs/RaceDay_ERD.png

The ERD is designed to match the SQL database script.

⸻

API Endpoint Plan

The API Endpoint Plan documents the endpoints planned for the RaceDay system.

The plan covers:

* Authentication
* User Profile
* Events
* Categories
* Event Enrolments
* Results

Each endpoint specifies:

* HTTP Method
* Route
* Description
* Role Required
* Request Body
* Expected Response

The endpoint plan is located at:

/docs/RaceDay_API_Endpoint_Plan.md

The endpoint plan is intended to act as the specification for the API implementation in Part 2.

⸻

SQL Database Script

The SQL Database Script creates and populates the RaceDay database using SQL Server.

The script includes:

* Database creation
* Table creation
* Primary keys
* Foreign keys
* NOT NULL constraints
* UNIQUE constraints
* DEFAULT constraints
* CHECK constraints
* Sample data

The sample data includes:

* At least two Organisers
* At least two Participants
* Three Events
* Categories for each Event
* Sample Enrolments

The SQL script is located at:

/docs/RaceDay_Database.sql

The script is intended to be executed using Microsoft SQL Server Management Studio (SSMS).

⸻

6. How to Run the SQL Database

1. Open Microsoft SQL Server Management Studio (SSMS).
2. Open /docs/RaceDay_Database.sql.
3. Execute the complete SQL script.
4. Confirm that the RaceDay database is created successfully.
5. Expand the RaceDay database.
6. Open the Tables folder.
7. Confirm that the following tables have been created:

Users
Events
EventTypes
Categories
Enrolments
Results

8. Check that the sample data has been inserted successfully.

The SQL script should run without errors on a clean SQL Server instance.

⸻

7. GitHub and CI/CD

GitHub is used for version control and submission of the RaceDay project.

The Part 1 repository contains the planning documents and SQL script inside the /docs folder.

A GitHub Actions workflow is also included to validate the required repository structure.

The workflow is located at:

/.github/workflows/part1.yml

Successful CI/CD Build

The successful GitHub Actions build will be shown below.

CI/CD Screenshot:

Insert screenshot of the successful green GitHub Actions build here.

⸻

8. Part 1 Video Presentation

The Part 1 video presentation explains the planning and database design of the RaceDay system.

The presentation covers:

* ERD design decisions.
* Database entities and relationships.
* Primary and foreign keys.
* Cardinality.
* API endpoint planning.
* Roles and access requirements.
* SQL database design.
* Running the SQL script in SQL Server Management Studio.

YouTube Video

YouTube Link:

Insert the unlisted YouTube video link here.

The video is submitted as an unlisted YouTube video as required by the assessment instructions.

⸻

9. Part 1 Deliverables

Deliverable	Location
ERD	/docs/RaceDay_ERD.png
API Endpoint Plan	/docs/RaceDay_API_Endpoint_Plan.md
SQL Database Script	/docs/RaceDay_Database.sql
GitHub Actions Workflow	/.github/workflows/part1.yml
README	/README.md
Video Presentation	Unlisted YouTube link

⸻

10. Part 1 Completion

Part 1 establishes the foundation for the RaceDay system before application development begins.

The ERD provides the database structure, the API Endpoint Plan defines the functionality that will be implemented later, and the SQL script creates and populates the database.

The planning documents are designed to remain consistent so that the API developed in Part 2 can follow the approved Part 1 plan.