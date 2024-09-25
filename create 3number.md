#!/bin/bash

text="Hello from RTU MIREA!"
text_length=${#text}  
line=$(printf "%${text_length}s" | tr ' ' '-')  

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"


![image](https://github.com/user-attachments/assets/1c58ae00-41e6-4af0-a545-8da9c12060fc)


