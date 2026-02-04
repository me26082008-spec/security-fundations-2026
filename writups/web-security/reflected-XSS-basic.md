Context:
The test was performed in a PortSwigger lab with the objective of identifying Cross-Site Scripting (XSS) vulnerabilities, following the lab instructions.

XSS Test:
The application's search field was tested using the following 
payload:
<script>alert(1)</script>

Result:
The script was reflected in the application's response and executed in the browser, confirming the presence of a Reflected XSS vulnerability.
Observation:
User input is reflected directly in the page without proper validation or sanitization, allowing the execution of arbitrary JavaScript code.
