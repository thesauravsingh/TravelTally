# Travel Tracker Web App

This is a simple web application built with Node.js and Express.js for tracking visited countries. Users can add countries they have visited, and the application will display the total number of visited countries along with a list of them. The application supports multiple users, each with a customizable color for visited countries.

## Prerequisites

Before running this application, make sure you have the following installed:

- Node.js (https://nodejs.org/)
- PostgreSQL (https://www.postgresql.org/)

## Installation

1. Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/travel-tracker.git
Navigate to the project directory:
bash
Copy code
cd travel-tracker
Install dependencies using npm:
bash
Copy code
npm install
Set up the PostgreSQL database:
Create a database named world.
Import the provided SQL dump file to create necessary tables and data.
Configuration
Before running the application, you need to configure the PostgreSQL connection settings. Modify the db object in index.js with your database credentials:

javascript
Copy code
const db = new pg.Client({
  user: "your_username",
  host: "localhost",
  database: "world",
  password: "your_password",
  port: 5432,
});
Usage
To start the server, run:

bash
Copy code
npm start
The server will start running at http://localhost:3000. You can access the application in your web browser.

Features
Add Visited Countries: Users can add countries they have visited.
Display Visited Countries: The application displays the total number of visited countries and lists them on the home page.
Multiple Users: Support for multiple users with individual lists of visited countries.
Custom Colors: Each user can set a custom color for their visited countries.
Error Handling: Graceful handling of errors such as invalid country names or duplicate entries.
API Endpoints
GET /: Home page displaying the total number of visited countries and the list of visited countries.
POST /add: Add a new visited country for the current user.
POST /user: Switch between users or add a new user.
POST /new: Create a new user with a custom color.
Contributing
Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature/my-new-feature).
Make your changes and commit them (git commit -am 'Add some feature').
Push to the branch (git push origin feature/my-new-feature).
Create a new Pull Request.
License
This project is licensed under the MIT License - see the LICENSE file for details.
