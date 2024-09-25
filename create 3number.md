#!/bin/bash

text="Hello from RTU MIREA!"
text_length=${#text}  
line=$(printf "%${text_length}s" | tr ' ' '-')  

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"
![image](https://github.com/user-attachments/assets/d0b5c927-fa87-4166-8be1-b26c8365864f)



