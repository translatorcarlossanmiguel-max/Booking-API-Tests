# Booking API Tests

Welcome to the **Booking API Tests** repository!  
This project contains a collection of automated API tests for the [Restful Booker API](https://restful-booker.herokuapp.com/), written in Postman and designed to cover both positive and negative scenarios.

> **Note:**  
> As requested, these tests are being executed using both the Postman CLI and Newman. In the future, we will need to decide which tool is best suited for this project and standardize on either Postman CLI or Newman for running our API tests.

These tests help ensure that the API functions as expected and catches regressions early in development.

---

## 🚀 Features

- Comprehensive coverage of booking endpoints
- Positive and negative test cases
- Easy to run locally or in CI/CD
- Generates detailed HTML and CLI reports

---

## 🛠️ Prerequisites

- [Node.js](https://nodejs.org/) installed on your machine
- [Newman](https://github.com/postmanlabs/newman) (the command-line runner for Postman collections)
- (Optional) [Postman CLI](https://learning.postman.com/docs/postman-cli/postman-cli-overview/) for running collections

---

## 📦 Installation

Install Newman globally (if you haven’t already):

```bash
npm install -g newman
```

If you want to use the Postman CLI, refer to the [official documentation](https://learning.postman.com/docs/postman-cli/postman-cli-overview/) for installation steps.

---

## ▶️ Running the Tests

### 1. Run with Newman (default CLI reporter):

```bash
newman run BookingAPI.postman_collection.json -e BookingAPI.postman_environment.json
```

### 2. Run and generate an HTML report with Newman:

```bash
newman run BookingAPI.postman_collection.json \
  -e BookingAPI.postman_environment.json \
  -r cli,html \
  --reporter-html-export ./newman-report.html
```

### 3. Run with Postman CLI (alternative):

```bash
postman collection run BookingAPI.postman_collection.json -e BookingAPI.postman_environment.json
```

- The `-e BookingAPI.postman_environment.json` flag loads the environment variables required for the tests.
- The `-r cli,html` flag tells Newman to output results to both the terminal and an HTML file.
- The `--reporter-html-export ./newman-report.html` flag specifies the path where the HTML report will be saved (in your project root folder).

---

## 📄 Viewing the Report

After running the tests with the HTML reporter, a file named `newman-report.html` will be created in your project’s root directory.

- **To view the report:**  
  Open `newman-report.html` in your web browser.
- **What’s inside:**  
  The report shows a summary of all test runs, including:
  - Total requests/tests run
  - Passed/failed test cases
  - Response times and status codes
  - Detailed logs for any failures

---
Happy Testing! 🚦
