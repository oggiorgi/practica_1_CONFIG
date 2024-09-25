#!/bin/bash

text="Hello from RTU MIREA!"
text_length=${#text}  
line=$(printf "%${text_length}s" | tr ' ' '-')  

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"

![image](https://github.com/user-attachments/assets/bbfef22e-111c-4478-a66a-bb1cd90a9a42)

