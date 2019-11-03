# Useful linux commands

### Getting the count of the number of files in a directory

	ls /path/to/dir | wc -l

### Name of all files to a text file
	ls /path/to/dir >> file_names.txt

### Find and replace texts in a file using Stream EDitor or sed
	sed -i 's/original/new/g' file.txt
	where, -i implies to make changes to original file,
	s is for the substitute command
	original is the text you want to replace
	new is the text with which the orginal has to be replaced
	g is for global occurence for replacing all the matches
	In the above example, we can replace file.txt to *.txt if we want to replace occurence in all files.

### Copy files from a folder based on names in a text file
	rsync -a /source/directory --files-from=/full/path/to/listfile /destination/directory
