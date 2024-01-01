# QTrip API Automation Suite

This project is an extension of the existing TestNG-based framework for automated testing of QTrip. It includes API tests using RestAssured to validate various functionalities.

## Table of Contents
- [Background](#background)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Test Cases](#test-cases)
  - [Test Case 1: User Registration and Login](#test-case-1-user-registration-and-login)
  - [Test Case 2: City Search API](#test-case-2-city-search-api)
  - [Test Case 3: Reservation](#test-case-3-reservation)
  - [Test Case 4: New and Duplicate Registrations](#test-case-4-new-and-duplicate-registrations)
- [Integration with TestNG Framework](#integration-with-testng-framework)
- [Contributing](#contributing)
- [License](#license)

## Background

This project extends the existing TestNG-based framework for automated testing of QTrip. The goal is to include API tests using RestAssured to validate the functionality of the QTrip API.

## Prerequisites

Before running the API tests, ensure you have the following prerequisites:

- Postman for manually executing test cases
- RestAssured library
- TestNG framework
- Java SDK

## Installation

Follow these steps to set up and install the API automation suite:

1. Clone the repository to your local machine.
2. Install Postman for manual test case execution.
3. Install RestAssured library and TestNG framework in your project.
4. Ensure the Java SDK is installed on your machine.

## Test Cases

### Test Case 1: User Registration and Login

**Steps:**
1. Use the register API to register a new user.
2. Use the Login API to log in using the registered user.
3. Validate that the login was successful.
4. Verify that the token and user id are returned for login.

**Expected Result:**
1. The Register API should return a status code 201.
2. After successful login, status code 201 must be returned. The response body should contain: `Success = true`.

**Group:**
API Tests

**Note:**
While registering users, ensure the username is universally unique.

### Test Case 2: City Search API

**Steps:**
1. Search for "beng" using the cities search API.
2. Verify the count of results being returned.

**Expected Result:**
1. After a successful search, the status code must be 200.
2. The result should be an array of length 1. The description should contain "100+ Places".

**Group:**
API Tests

**Validations:**
- Status code should be 200.
- Result should be an array of length 1.
- Response JSON Schema validation.

### Test Case 3: Reservation

**Steps:**
1. Create a new user using API and log in.
2. Perform a booking using a POST call.
3. Ensure that the booking goes fine.

**Expected Result:**
1. On a successful booking, status code 200 should be returned.
2. Perform a GET Reservations call for the user and ensure that the successful booking is listed there.

**Group:**
API Tests

**Validations:**
- Status code should be 200 for a successful booking.
- Check if the reservation is available in the /api/v1/reservations call.

### Test Case 4: New and Duplicate Registrations

**Steps:**
1. Register a new user using the register API.
2. Verify the success and status code for the first-time registration.
3. Attempt to register with the same email (duplicate registration).
4. Verify the success, status code, and error message for the duplicate registration.

**Group:**
API Tests

**Validations:**
- Verify successful registration on the first attempt.
- Verify unsuccessful duplicate registration with the correct error message.

## Integration with TestNG Framework

Describe how the API automation suite has been integrated into the existing TestNG framework. Include information on how to run both UI and API tests together, and any modifications made to the existing framework.


