
# QA-Engineer-Take-Home-Evaluation
This document will list the steps a candidate for the QA Engineer position will perform to evaluate skill level, proficiency, and ability to deliver a solution meeting the requirements in a timely manner.

## Requirements
- IDE or Text Editor: Such as Visual Studio Code, PyCharm, or any preferred code editor
- Postman: For manual API testing and initial test case verification

## Task
1. Test Case Design
	- Design test cases for the POST https://mockapi.rapidextras.com/login endpoint considering various scenarios, including edge cases and invalid inputs.
	- Ensure coverage for positive and negative test cases.

2. Automation Script Development
	- Develop automation scripts to test the designed cases.
	- Use tools like Postman, JUnit, Selenium, or any preferred testing framework.
	- The automation script(s) should be able to:
		- Send a POST request to the https://mockapi.rapidextras.com/login endpoint.
		- Validate the response status code.
		- Validate the response body.
		- Validate the response time.
		- Validate the response headers.
		- Validate the response cookies (if any)
		- Validate the response token (if any)

3. Execution and Reporting
	- Run the automation test scripts.
	- Capture and document the output of the automation scripts and provide a detailed report of the test execution results.

## Deliverables:
Place the following deliverables in a repository on your GitHub account along with a README containing your full name and which method or job site you used to reach this repository. Send an invitation to your GitHub repository to Rapid POS at `recruiting.programmer@rapidpos.com`
- Test Case Design Document
- Automation Script(s)
- Test Execution Report

## Evaluation Criteria
- Test Case Design
- Coverage of positive and negative test cases
- Coverage of edge cases
- Coverage of invalid inputs
- Clarity and completeness of the test cases

## Additional Information
- Some responses may be intentionally delayed or incorrect to test the candidate's ability to handle such scenarios.
- Consider edge cases like empty inputs, special characters, and long inputs.

## Username Triggers
- Empty Username or Password:
    -- Any request with an empty username or password will return 400 Bad Request with the message "Username and password are required."
- Invalid Login:
-- Username containing "invalid" (e.g., "invaliduser@example.com") will return 401 Unauthorized.
- Malformed JSON Response:
-- Username containing "malformed" (e.g., "malformeduser@example.com") will return a malformed JSON response.
- Server Error:
-- Username containing "error" (e.g., "erroruser@example.com") will return 500 Internal Server Error.
- Slow Response:
-- Username containing "slow" (e.g., "slowuser@example.com") will introduce a delay of 2 seconds before returning a response.
- Successful Login:
-- Any other valid username will return 200 OK with a JWT token in the response.
