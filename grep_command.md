# Using grep command

###  Finding a string in a text file
	grep 'search_text' filename.txt

### Exact match return

	grep -w 'search_text' filename.txt

grep, by default, is case-sensitive. We may use -i 

	grep -wi 'search_text' filename.txt

### Getting the line number using -n
	grep -win 'search_text' filename.txt

### Getting some surrounding texts using -B with 3 lines above match
	grep -win -B 3 'search_text' filename.txt

### Getting some surrounding texts using -A with 3 lines below match
	grep -win -A 3 'search_text' filename.txt


### Getting some surrounding texts using -C with n lines below and above the match
	grep -win -C 3 'search_text' filename.txt

### Using search in muliple files
	grep -win "search_text" ./*.txt

### Searching within sub-directories using -r
	grep -winr "search_text" ./

If only file names are required without match information use -l

	grep -wirl "search_text" ./

To get the number of matches, use -c

	grep -wirc "search_text" ./

### Using grep as a pipe to another command

	history | grep "some_text"

	history | grep "some_text" | grep "other_text"

## Using grep with regular expression to find phone number
	grep "...-...-...." filename.txt

... implies any kind of character. We can be specific to get only digits.

### We can use perl compatibility using -P command as grep by default used POSIX.

	grep -P "\d{3}-\{3}-\d{4}" filename.txt

The above command, however, will not work on mac environment as Mac uses grep BSD instead of grep GNU.

To install grep GNU on Mac, use Homebrew package manager:

	brew install grep
	

