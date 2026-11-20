# Automation Exercise – API Testing Project

## 1. Project Overview

This project demonstrates manual API testing using **Postman** and **JavaScript test scripts** on the Automation Exercise practice website.

The objective is to validate REST API endpoints, verify HTTP status codes and application response codes, test positive and negative scenarios, and document test cases and execution results.

## 2. Application Under Test

- **Website:** https://automationexercise.com/
- **API Documentation:** https://automationexercise.com/api_list
- **Base URL:** `https://automationexercise.com`

## 3. Tools and Technologies

- **Postman** – API testing and request execution
- **JavaScript** – Writing test scripts in Postman's Tests section
- **REST APIs** – GET, POST, PUT and DELETE methods
- **JSON** – Request and response validation
- **GitHub** – Project documentation and version control
- **Microsoft Excel** – Test cases, execution reports and bug reports

## 4. Project Structure

```text
API-Testing-Project/
│
├── README.md
│
├── Postman-Collection/
│   └── Automation-Exercise-API-Testing.postman_collection.json
│
├── Test-Cases/
│   └── Automation_Exercise_API_Test_Cases.xlsx
```

## 5. Test Scenarios Covered

A total of **10 API test scenarios** were created and executed.

| Test Case ID | API Endpoint | Method | Test Scenario |
|---|---|---|---|
| API001 | `/api/productsList` | GET | Verify products list retrieval |
| API002 | `/api/productsList` | POST | Verify unsupported HTTP method |
| API003 | `/api/brandsList` | GET | Verify brands list retrieval |
| API004 | `/api/brandsList` | PUT | Verify unsupported HTTP method |
| API005 | `/api/searchProduct` | POST | Search products using a valid parameter |
| API006 | `/api/searchProduct` | POST | Search products with a missing parameter |
| API007 | `/api/verifyLogin` | POST | Verify login using valid credentials |
| API008 | `/api/verifyLogin` | POST | Verify login when email is missing |
| API009 | `/api/verifyLogin` | DELETE | Verify unsupported HTTP method |
| API010 | `/api/verifyLogin` | POST | Verify login using invalid credentials |

## 6. Testing Approach

The following validations were performed using JavaScript assertions in Postman:

- HTTP status code validation
- JSON response format validation
- Application response code validation
- Response body and message validation
- Array and object structure validation
- Mandatory field validation
- Positive and negative test scenarios
- Response time checks

### Important Testing Observation

The application sometimes returns HTTP status `200` even when an API operation is unsupported or the application-level operation fails.

For example:

- Unsupported methods return HTTP `200` with application response code `405`.
- Invalid login credentials return HTTP `200` with application response code `404`.

Therefore, both the HTTP status and the application-level response code were validated separately.

## 7. Test Execution Results

The following results were recorded from the Postman Collection Runner execution:

| Metric | Result |
|---|---:|
| Total API Requests | 10 |
| Iterations | 1 |
| Assertions Passed | 32 |
| Assertions Failed | 0 |
| Skipped Assertions | 0 |
| Errors | 0 |
| Total Execution Time | 6.296 seconds |
| Average Response Time | 506 ms |

**Execution Result: All 32 assertions passed.**

The detailed results and supporting screenshots are included in the Test Execution Report.

## 8. Test Case Documentation

The Excel test case document includes:

- Test Case ID
- Module and endpoint
- HTTP method
- Test scenario
- Preconditions
- Test steps
- Test data
- Expected result
- Actual result
- Execution status


## 9. How to Run the Collection

1. Download and install Postman.
2. Download the Postman collection from the `Postman-Collection` folder.
3. Import the collection into Postman.
4. Set the required environment variables.
5. Open the collection and select **Run**.
6. Execute all 10 requests using Collection Runner.
7. Review the test results and assertion status.

### Required Variables

The login tests use environment variables:

| Variable | Purpose |
|---|---|
| `validEmail` | Email address of a disposable practice account |
| `validPassword` | Password of that practice account |
| `invalidEmail` | Email address for negative login testing |
| `invalidPassword` | Password for negative login testing |

**Security Note:** Actual login credentials should never be committed to GitHub. Use Postman environment variables and do not share or export sensitive values.

## 10. Project Scope and Limitations

- Testing was performed through publicly available API endpoints.
- No access to the application's internal backend or database was available.
- The project focuses on functional API testing using Postman.
- No Python, Pytest, Playwright or CI/CD automation framework was implemented as part of this project.

## 11. Skills Demonstrated

- REST API Testing
- Postman
- JavaScript Test Scripts
- HTTP Methods and Status Codes
- JSON Validation
- Positive and Negative Testing
- API Test Case Design
- Test Execution and Reporting
- Git and GitHub

## 12. References

- [Automation Exercise Website](https://automationexercise.com/)
- [Automation Exercise API Documentation](https://automationexercise.com/api_list)
- [Postman Documentation](https://learning.postman.com/)

---

**Project Type:** Manual API Testing  
**Application:** Automation Exercise  
**Testing Tool:** Postman  
**Scripting Language:** JavaScript
