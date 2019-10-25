# All files and folders in current directory

find .

# All files and folders in the specified directory

find /path/to/dir

# Only directories and exclude files

find . -type d

# Only files and no directories

find . -type f

# Search a file with a know full name

find . -type f -name "filename.txt"

# With partial file name known

find . -type f -name "test*"
# No case-sensitive, we use -iname
find . -type f -iname "test*"

# With a specific extension

find . -type f -name "*.py"

# Filter with metadata e.g. modified in last 15 minutes, modifiled more than 15 minutes ago

find . -type f -mmin -15
find . -type f -mmin +15

## More than a minute but less than five minutes
find . -type -mmin +1 -mmin -5

# Filter with modified with days e.g. modified less than 20 days ago

find . -type f -mtime -20
find . -type f -mtime +20

For access minutes and change minutes, use amin, atime and cmin, ctime, respectively.

# For file search with a certain size

This command finds file with size more than 5 Megabytes.

find . -size +5M

find . -size +5k

find . -size +5G

# Finding empty files that are in the current directory

find . -empty

# Finding files based on the permissions

find . -perm 777

Performing actions on the results, e.g. changing user and group. {} is the placeholder for the results from find command

find . -exec chown ashutosh:www-data {} +

# Changing directory permission to 775 and file permission to 664

find /path/to/dir -type d -exec chmod 775 {} +

find /path/to/file -type f -exec chmod 664 {} +

# Delete all file in current directory with .jpg extension

find . -type f -name "*.jpg" 
Max depth here implies that only the current directory contents will be deleted but not the subdirectories

find . -type f -name "*.jpg"  -maxdepth 1 

find . -type f "*.jpg" -maxdepth 1 -exec rm {} +






