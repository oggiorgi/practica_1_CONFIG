#!/bin/bash

text="Hello from RTU MIREA!"
text_length=${#text}  
line=$(printf "%${text_length}s" | tr ' ' '-')  

echo "+${line}+"
echo "| ${text} |"
echo "+${line}+"



![image](https://github.com/user-attachments/assets/019cd5f5-69f1-4355-907b-bc88bd6c648e)



