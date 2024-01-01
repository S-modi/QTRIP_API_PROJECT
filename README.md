QTrip API Automation Suite
This project is an extension of the existing TestNG-based framework for automated testing of QTrip. It includes API tests using RestAssured to validate various functionalities.

Table of Contents
Background
Prerequisites
Installation
Test Cases
Test Case 1: User Registration and Login
Test Case 2: City Search API
Test Case 3: Reservation
Integration with TestNG Framework
Contributing
License
Background
This project extends the existing TestNG-based framework for automated testing of QTrip. The goal is to include API tests using RestAssured to validate the functionality of the QTrip API.

Prerequisites
Before running the API tests, ensure you have the following prerequisites:

Postman for manually executing test cases
RestAssured library
TestNG framework
Java SDK
Installation
Follow these steps to set up and install the API automation suite:

Clone the repository to your local machine.
Install Postman for manual test case execution.
Install RestAssured library and TestNG framework in your project.
Ensure the Java SDK is installed on your machine.
Test Cases
Test Case 1: User Registration and Login
Steps:

Use the register API to register a new user.
Use the Login API to log in using the registered user.
Validate that the login was successful.
Verify that the token and user id are returned for login.
Expected Result:

The Register API should return a status code 201.
After successful login, status code 201 must be returned. The response body should contain: Success = true.
Flow:

Group:
API Tests

Note:
While registering users, ensure the username is universally unique.

Test Case 2: City Search API
Steps:

Search for "beng" using the cities search API.
Verify the count of results being returned.
Expected Result:

After a successful search, the status code must be 200.
The result should be an array of length 1. The description should contain "100+ Places".
Flow:

Group:
API Tests

Validations:

Status code should be 200.
Result should be an array of length 1.
Response JSON Schema validation.
Test Case 3: Reservation
Steps:

Create a new user using API and log in.
Perform a booking using a POST call.
Ensure that the booking goes fine.
Expected Result:

On a successful booking, status code 200 should be returned.
Perform a GET Reservations call for the user and ensure that the successful booking is listed there.
Group:
API Tests

Validations:

Status code should be 200 for a successful booking.
Check if the reservation is available in the /api/v1/reservations call.
Integration with TestNG Framework
Describe how the API automation suite has been integrated into the existing TestNG framework. Include information on how to run both UI and API tests together, and any modifications made to the existing framework.

Contributing
To contribute to this project, follow the guidelines in the CONTRIBUTING.md file.

License
This project is licensed under the MIT License.
