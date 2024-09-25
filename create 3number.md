#!/bin/bash

text="Hello from RTU MIREA!"
text_length=${#text}  
line=$(printf "%${text_length}s" | tr ' ' '-')  

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"

![image](https://github.com/user-attachments/assets/e8f8f3e0-54a2-4f57-acca-5614a98026cd)



