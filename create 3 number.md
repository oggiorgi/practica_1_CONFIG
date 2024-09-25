#!/bin/bash

text="Hello from RTU MIREA!"
text_length=${#text}  
line=$(printf "%${text_length}s" | tr ' ' '-')  

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"


![image](https://github.com/user-attachments/assets/392a1ebc-5b42-4e1e-9327-c77a79f1f225)
