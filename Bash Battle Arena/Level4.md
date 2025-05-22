# Bash Battle Arena Level 4:  

**Mission**: Create a script that copies all .txt files from the Arena directory to a new directory called Backup  

**Solution**:  

``` bash
#!/bin/bash

current_directory="/Users/mumin/Arena/"  
new_directory="/Users/mumin/Backup/"  

mkdir -p "$new_directory"  

for file in "$current_directory"*.txt;  
do  
cp -v "$file" "$new_directory"  
done
