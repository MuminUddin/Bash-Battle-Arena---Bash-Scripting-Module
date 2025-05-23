# Bash Battle Arena Level 6:  

**Mission:** Write a script that accepts a filename as an argument and prints the number of lines in that file. If no filename is provided, display a message saying 'No file provided'.  

**Solution:**  

``` bash
#!/bin/bash
print_file() {
    local file_name="$1"
    local line_count=0
    while IFS= read -r line; do
    (("$line_count++"))
    echo "Number of line: $line_count"
    done < "$file_name"
}

if [[ $# -eq 0 ]]; then
echo "No file provided" >&2
exit 1
fi

print_file
