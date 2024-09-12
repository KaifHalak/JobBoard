# Job Board Application

## Overview
This is a full-featured job board application where users can search, filter, and save jobs as well as post job opportunities.

Demo video can be found here --> ![Video](https://kaifhalak.github.io/JobBoard/demo-vid.mp4)


## Note
- The git histories can be found in their respective repos:
    - [jobBoardClient](https://github.com/KaifHalak/jobBoardClient)
    - [jobBoardServer](https://github.com/KaifHalak/jobBoardServer)


## Features

### Users
- User Authentication
- Change Username/Email/Password
- Upload Profile Picture

### Job Listings
- Browse through job postings
- Filter jobs by:
    - Country
    - City
    - Experience Level (in years)
    - Employment Type (e.g., full-time, internship)

- Search jobs using the search bar
- Save jobs to view later
- Create Job Posts

## Technical Details

### Tests
- Unit tests for some validation functions and settings page
- Integration for user authentication

### Custom Logger
- A custom-built logger to handle different levels of logging, including such as Events and Errors

### Security
- Password hashing (+ use of peppers) before storing them into DB
- Rate limiting to prevent DDoS attacks and password-guessing attempts (brute force).
- Session Managemen JWT tokens stored in client-side cookies

### Other
- Global Error handling to properly handle exceptions and errors
- Polling Mechanism: used when users search for jobs to efficiently retrieve relevant data without overloading the server.

## Setup Instructions

- Clone the repository or download the zip file
- Install the dependencies in both folders seperately:
```
cd jobBoardClient
npm i

cd jobBoardServer
npm i

```
- Create a .env file in the jobBoardServer dir and add the following values:

```
SERVER_PORT: 3000
JWT_SECRET: "shhhhh"

DB_HOST: "./jobBoardDB.sqlite3"
```

- Go to the jobBoardClient dir and run the following command:
```
npm run build
```
- Go to the jobBoardServer dir and run the following command:
```
npm run server
```
