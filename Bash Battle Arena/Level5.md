# Bash Battle Arena Level 5:  

**Mission**: Combine what you've learned! Write a script that:

1. Creates a directory names 'Battlefield'
2. Inside Battlefield, create files named knight.txt, sorcerer.txt, and rogue.txt.
3. Check if knight.txt exists; if it does, move it to a new directory called Archive.
4. List the contents of both Battlefield and Archive.

**Solution**:  

``` bash
battlefield_filepath="/Users/mumin/Battlefield/"

echo "Creating Battlefield directory..."
mkdir -p "$battlefield_filepath"

echo "Creating files..."
touch "$battlefield_filepath"/{knight.txt,sorcerer.txt,rogue.txt}

if [[ -f "/Users/mumin/Battlefield/knight.txt" ]]; then
echo "Creating Archive directory..."
mkdir -p "/Users/mumin/Archive/"
mv "/Users/mumin/Battlefield/knight.txt" "/Users/mumin/Archive/"
echo "File has been moved to Archive"
fi

echo "Battlefield contents:"
ls -l /Users/mumin/Battlefield/

echo "Archive contents:"
ls -l /Users/mumin/Archive/
