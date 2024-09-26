# cyberspace014
malware-analysis simple BASH script  https://github.com/14mb1v45h/cyberspace014.git

This script checks for malware using 5 functions
signatures 
suspicious_strings 
printable_strings
behavior
simulation

Explanation of each function

Signatures:- This function compares SHA-256 hash values of a file to known malware hash values. An array is created which holds multiple strings of known malware SHA-256 values, then the sha256sum command is used to find the hash value of the file to compare with the array. If there is a match then it prints that it’s a known malware.
Suspicious_strings:- This function has a list of known patterns ie strings and uses grep command to find lines with the listed keywords.
Printable_Strings:- This function has an array of keywords like HTTP,HTTPS,Python,bin,bash etc which could potentially cause harm by running harmful scripts, connecting to malicious websites etc,it uses grep command to find lines with them.
Behavior:- This function checks for behaviors which are used to connect, read, write and execute malicious content. If a match of these keywords are found it prints the line.
Simulation:- This function is used to start simulation, i.e to execute the malicious file in a sandbox or a controlled environment. It uses another tool called firejail which runs the malicious file under conditions like safe mode, no network mode, no super user permissions etc as required by the user. This function is executed only when the user wants to run it/test it using user input.


copyright@iambivash2024

