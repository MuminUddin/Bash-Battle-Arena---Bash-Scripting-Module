# Bash Battle Arena Level 3  

**Mission**: Write a script that checks if a file named hero.txt exists in the Arena directory. If it does, print Hero found!; otherwise, print Hero missing!  

**Solution**:  

``` bash
file_path="/users/mumin/Arena/hero.txt"

if [[ -f "$file_path" ]]; then

echo "Hero found!"
else
echo "Hero missing!"

fi
