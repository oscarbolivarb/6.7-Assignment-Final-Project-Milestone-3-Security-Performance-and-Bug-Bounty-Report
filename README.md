# 6.7-Assignment-Final-Project-Milestone-3-Security-Performance-and-Bug-Bounty-Report

Introduction 

This report summarizes the security, performance and bugs in the MedSched appointment scheduling system. The purpose of this assignment was to identify any defects, verify the system behavior and document any finding using GitHub. Some tools were used such as Postman to test the API responses and Apache JMeter was to obtain a basic performance test.
Security and Defect Finding

Issue #1: Appointment form accepts empty patient’s name 
During the test an appointment request was accepted even when the patient’s name field was left empty. This could result in incomplete and invalid information being added to the system. 

Severity: Medium 

Impact: if there is missing patient information this could cause problems and make appointment records harder to manage. 

Evidence: Patient Name.png

Issue #2: Invalid endpoint returns a 404 error message 
An invalid API endpoint was tested using Postman. The system returned a 404 error message, which showed that the invalid requests was handled correctly.

Severity: low

Impact: The system prevents users from accessing endpoints that do not exist, which helps avoid errors and unexpected behaviors.

Evidence: Postman 404 error.png

Issue #3 System Performance Tested with 10 users
An apache JMeter was used to simulate how 10 users would access the system at the same time. The test was completed without any errors.

Test Settings
•	10 users
•	Ramp-up period was 10 seconds
•	One test cycle 

Results 
•	10 requests completed
•	0% error rate 
•	Average response time was about 127 ms. 

Evidence 
Summary Report.png
View Result Tree.png

Bug Tracking 
GitHub issues were used to record and organize the findings from the test. Each issue was included in the description, steps to reproduce the problem and the screenshot as evidence. This helps keep the testing process organized. 

Conclusion
The testing was completed during this assignment to help evaluate the quality of the MedSched system. One validation problem was found, the API responses were tested with Postman and the performance test showed that the system can handle multiple users without a problem. Also GitHub was used to document and track the results easily. 

References
Apache Software Foundation. (2026). Apache JMeter. https://jmeter.apache.org/
Postman, Inc. (2025). Postman learning center. https://learning.postman.com/

