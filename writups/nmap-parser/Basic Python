Objective
Create a simple Python script to read an Nmap output file
and identify lines that represent open ports.

Analyzed file
scan.txt (result of an Nmap scan)

Example line:
22/tcp open ssh

Approach
- Open the file in read mode
- Read the file line by line
- Filter only lines that contain "/"
- Print those lines to the terminal

Code used
```python
file = open("scan.txt", "r")
for line in file:
    if "/" in line:
        print(line)
file.close()
Result
The script correctly displayed the open ports:

22/tcp

80/tcp

443/tcp

What I learned
How to read files in Python
How to use a for loop to iterate through lines
Using if statements to filter content
The importance of indentation in Python
