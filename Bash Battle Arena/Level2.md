# Bash Battle Arena Level 2:  

**Mission**: Create a script that outputs the numbers 1 to 10, one number per line.  

**Solution**:  

```bash
#!/bin/bash  
for (( i=1; i<=10; i++ ))
do
    echo "Number: $i"
done
```
