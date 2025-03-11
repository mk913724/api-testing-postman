# API Testing Using Postman  

This project demonstrates API testing techniques using Postman and Newman. It includes functional and integration testing, automated test execution, and detailed reporting for the **Hotel Booking CRUD REST API**.

---

## Features  

- Comprehensive functional and integration testing for RESTful APIs.  
- Automated tests using Postman collections and Newman.  
- Covers positive, negative, and edge case scenarios.  
- Generates detailed HTML reports for test execution insights.  

---

## Getting Started  

### 1. Clone the Repository  
Clone the project repository to your local machine using the command:  
```bash  
git clone <repository-url>  
```

### 2. Import Postman Collections and Environment Variables  

Import the following files into Postman:  

- **Postman Collection**: `hotel_booking_api_test.postman_collection.json`  
- **Postman Environment**: `Hotel-Booking-Env.postman_environment`  

### 3. Execute API Tests  

Tests can be executed manually within Postman or automatically using Newman.  

---

## Running Tests with Newman  

### Step 1: Install Newman  
Ensure Node.js and npm are installed on your system. Then, install Newman globally:  
```bash  
npm install -g newman  
```

### Step 2: Install the HTML Extra Reporter  
For detailed HTML reports, install the Newman HTML Extra Reporter:  
```bash  
npm install -g newman-reporter-htmlextra  
```

### Step 3: Run the Collection  
Run the API tests using the following command:  
```bash  
newman run hotel-booking-crud-collection.json -e hotel-booking-crud-environment.json -r htmlextra --reporter-htmlextra-export hotel-booking-test-report.html  
```

### Step 4: View the Report  
Open the generated `hotel-booking-test-report.html` file in a web browser to view the test results.

---

## Project Structure  

```plaintext
/collections
  ├── hotel_booking_api_test.postman_collection.json     # Postman collection of API endpoints
  ├── Hotel-Booking-Env.postman_environment.json      # Environment variables (e.g., base_url, auth_token)

/test-cases
  ├── positive-tests.md                        # Positive test cases
  ├── negative-tests.md                        # Negative test cases
  ├── edge-scenarios.md                        # Edge case scenarios

/reports
  ├── report.html           # Detailed test execution report
```

---

## HTML Report Highlights  

The Newman-generated HTML report includes:  

- Execution results: Tests passed, failed, or skipped.  
- Metrics: Response times, status codes, and API performance.  
- Errors: Detailed error messages for failed tests.  
- Visual insights: Charts and data visualization for API performance trends.  

---

## Requirements  

- **Node.js and npm**: For installing and running Newman.  
- **Postman**: Optional, for manual testing and debugging.  

---
