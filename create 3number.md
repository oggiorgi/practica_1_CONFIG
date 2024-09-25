#!/bin/bash

text="Hello from RTU MIREA!"
text_length=${#text}  
line=$(printf "%${text_length}s" | tr ' ' '-')  

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"


![image](https://github.com/user-attachments/assets/460c89d4-56a1-4f40-8555-99354a861a34)




