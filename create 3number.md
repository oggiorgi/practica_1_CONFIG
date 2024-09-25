#!/bin/bash

text="Hello from RTU MIREA!"
text_length=${#text}  
line=$(printf "%${text_length}s" | tr ' ' '-')  

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"


![image](https://github.com/user-attachments/assets/adce2975-f574-404a-b6ba-fdca9c27f2a6)



