**File: Page 1.jpg**

**Shell Scripting Notes**

**What is Shell Script?**

In the simplest terms, a shell script is a file containing a series of commands. The shell reads this file and carries out the commands as though they have been entered directly on the command line.

- Normally, shell scripts have the file extension `.sh`.
- To create a shell script, use a text editor.

**Creating a Shell Script:**

1. Use an editor like `vi` or `gedit` to write the script.
2. After writing the script, set execute permission:

```shell
chmod +x script_name
```

**File Naming Conventions:**

1. A file name can be a maximum of 255 characters.
2. The name may contain alphabets, digits, dots, and underscores.
3. System commands or Linux reserved words cannot be used for file names.
4. Linux is case-sensitive, so file names, variables, and arrays in shell scripts are also case-sensitive.

**Example:**

```shell
Hjbinjoash
stringi=te
Stringi=20
echo "The value of string is $string"
echo "The value of Stringi is $Stringi"
```

---

**File: Page 2.jpg**

**Example:**

```shell
# chmod +x <script_file_name>
chmod 755 <script_file_name>
```

**Note:**

This sets read, write, and execute (7) permission for the owner, for the group, and other permissions are read and execute only (5).

**Execute Your Script:**

- `bash script_file_name`
- `sh script_file_name`
- `./script_file_name`

Linux is case-sensitive, so file names, variables, and arrays used in shell scripts are also case-sensitive.

**Example:**

```shell
Hjbinjoash
stringi=te
Stringi=20
echo "The value of string is $string"
echo "The value of Stringi is $Stringi"
```

---

**File: Page 3.jpg**

**Running Shell Scripts:**

- To execute a shell script, ensure you have execute permission.
- Give execute permissions using `chmod`.

**File Naming Conventions:**

1. A file name can be a maximum of 255 characters.
2. The name may contain alphabets, digits, dots, and underscores.
3. System commands or Linux reserved words cannot be used for file names.
4. Linux is case-sensitive.

**Example:**

```shell
Hjbinjoash
stringi=te
Stringi=20
echo "The value of string is $string"
echo "The value of Stringi is $Stringi"
```

---

**File: Page 4.jpg**

**Comments**

- Comments are used to escape from the code.
- Adding comments makes code more readable.
- Single-line comments are created using `#`.
- Multiline comments can be created using the HERE DOCUMENT feature.

**Example:**

```shell
#!/bin/bash

# This is a basic shell script by shubhan.

echo "Hello, welcome to The DevOps Learning." # It will display the message
```

---

**File: Page 5.jpg**

**Variable Names:**

- Variables must begin with an alphanumeric character or underscore (_).
- Conventionally, environment variables and internal shell variables are capitalized; all other variable names should be lowercase.
- Variable names are case-sensitive.

**System-defined Variables:**

- Created and maintained by the Linux bash shell.
- Defined in CAPITAL LETTERS.
- Many shell inbuilt variables are used for administration and writing shell scripts.

**User-defined Variables:**

- Created and maintained by the user.
- Avoid using all uppercase names.

**Example:**

```shell
#!/bin/bash

trainingCourse="DevOps"

echo "Displaying the user-defined variable (trainingCourse):"
echo "Value is: $trainingCourse"
```

**Command Line Arguments**

- Values passed through the command prompt are command-line arguments.
- No limitation on the number of arguments.
- Separated by space.

**Example:**

```shell
./scriptfile.sh arg1 arg2 arg3
```

**File Name: commandLineArgs.sh**

```shell
#!/bin/bash

echo "Number of arguments on the command line: $#"
echo "Process number of the current process: $$"
echo "Display the 3rd argument on the command line, from left to right: $3"
```

---

**File: Page 6.jpg**

**String Formatting**

Character Description:

- `-n`: Do not output the trailing new line.
- `-e`: Enable interpretation of backslash escaped characters in the string.
- `\a`: Alert (bell).
- `\b`: Backspace.
- `\e`: Suppress trailing new line.
- `\n`: New line.
- `\r`: Carriage return.
- `\t`: Horizontal tab.
- `\\`: Backslash.

**User Interaction using `read` Command:**

- Use the `read` statement to take input from the user.
- `read` command is used to get input from the user, making scripts interactive.

**Example:**

**File Name: readname.sh**

```shell
#!/bin/bash

echo "Please enter your name:"
read username

echo "The name you entered is $username"
```

---

**File: Page 7.jpg**

**Displaying Special Variables:**

- `$0`: Name of the current shell or program.
- `$#`: Number of arguments on the command line.
- `$$`: Process number of the current process.
- `$n`: nth argument on the command line.
- `$@`: All arguments on the command line (separate words).
- `$*`: All arguments on the command line (single word).
- `$?`: Exit status of the last executed command.

**Example:**

```shell
echo "$0: $0"
echo "$#: $#"
echo "$$: $$"
echo "$1: $1"
```

**Difference between `$*` and `$@`:**

- `$*` treats the collection of arguments as one text string.
- `$@` treats the collection of arguments as separate strings.

---

**File: Page 8.jpg**

**Variable Names:**

- Variables must begin with an alphanumeric character or underscore (_).
- Conventionally, environment variables and internal shell variables are capitalized; all other variable names should be lowercase.
- Variable names are case-sensitive.

**System-defined Variables:**

- Created and maintained by the Linux bash shell.
- Defined in CAPITAL LETTERS.
- Many shell inbuilt variables are used for administration and writing shell scripts.

**User-defined Variables:**

- Created and maintained by the user.
- Avoid using all uppercase names.

**Example:**

**Filename: user_defined_variables.sh**

```shell
#!/bin/bash

trainingCourse="DevOps"

echo "Displaying the user-defined variable (trainingCourse):"
echo "Value is: $trainingCourse"
```

**Command Line Arguments**

- Values passed through the command prompt are command-line arguments.
- No limitation on the number of arguments.
- Separated by space.

**Example:**

```shell
./scriptfile.sh arg1 arg2 arg3
```

**File Name: commandLineArgs.sh**

```shell
#!/bin/bash

echo "Number of arguments on the command line: $#"
echo

 "Process number of the current process: $$"
echo "Display the 3rd argument on the command line, from left to right: $3"
```

---

**File: Page 9.jpg**

**Control Commands**

**if Control Statement:**

**Syntax:**

```shell
if condition
then
  # Display commands list if condition is true
else
  # Display commands list if condition is false
fi
```

**Example:**

**File Name: FindBiggestNumber.sh**

```shell
if [ $1 -ne 3 ]
then
  echo "$0: Number 1 and Number 3 are not given."
  exit 1
fi

if [ $1 -ge $2 ] && [ $1 -ge $3 ]
then
  echo "$1 is the biggest number"
elif [ $2 -ge $1 ] && [ $2 -ge $3 ]
then
  echo "$2 is the biggest number"
elif [ $3 -ge $1 ] && [ $3 -ge $2 ]
then
  echo "$3 is the biggest number"
else
  echo "All three numbers are equal"
fi
```

---

**File: Page 10.jpg**

**Output:**

```shell
Please enter your name: Shubhan Londhe
The name you entered is Shubham Londhe
```

---

**File: Page 11.jpg**

**Loops in Shell Scripting**

**for Loop**

**Syntax:**

```shell
for ((initialization; condition; increment))
do
  commands
done
```

**Example:**

```shell
for ((i = 5; i >= 1; i--))
do
  echo $i
done
```

**Output:**

```shell
5
4
3
2
1
```

---

**File: Page 12.jpg**

**while Loop**

**Syntax:**

```shell
while [ condition ]
do
  commands
done
```

**Example:**

```shell
count=5

while [ $count -gt 0 ]
do
  echo $count
  count=$((count - 1))
done
```

**Output:**

```shell
5
4
3
2
1
```

---

**File: Page 13.jpg**

**Advanced Text Processing Commands**

**grep**

- `grep` is a Unix utility that searches for a pattern in files or data piped to it.
- `egrep` (extended grep) extends `grep` functionality with regular expressions.

**`grep` Options:**

- `-i`: Ignore case during search.
- `-r`: Search recursively.
- `-v`: Invert match (match everything except the pattern).
- `-l`: List files that match the pattern.
- `-L`: List files that do not match the pattern.
- `-n`: Prefix each line of output with the line number within its input file.
- `-A num`: Print num lines of trailing context after matching lines.
- `-B num`: Print num lines of leading context before matching lines.

**Example:**

**Search files containing the word "bash" in the current directory:**

```shell
grep "bash" *
```

---

**File: Page 14.jpg**

**grep (continued)**

**`grep` Examples:**

**Search files NOT containing the word "bash" in the current directory:**

```shell
grep -v "bash" *
```

**Repeat the above search using a case-insensitive pattern match and print the line number that matches the search pattern:**

```shell
grep -i -n "bash" *
```

**Search files not matching a certain name pattern (e.g., "fun"):**

```shell
grep -v -i "fun" *
```

**grep OR**

```shell
grep 'Man\|Sales' employee.txt
```

Output:

```shell
196 Shub Manager Sales $5,608
30 Ankur Sysadmin Technology $7,000
500 Naveen Manager Sales $6,690
```

**grep AND**

```shell
grep -i 'sys.*Tech' employee.txt
```

Output:

```shell
198380 Ankur Sysadmin Technology $7,080
```

**sed**

- `sed` (stream editor) is used to parse and transform information, either from information piped to it or from files.
- `sed` is line-oriented, operates one line at a time, and allows regular expression matching and substitution.

**File: Page 15.jpg**

**`sed` Commands and Flags**

- `s` substitution command.

**Example:**

```shell
sed 's/old_pattern/new_pattern/' filename
```

---

**File: Page 16.jpg**

**`awk`**

**The `awk` text-processing language is useful for tasks such as:**

- Tallying information from text files and creating reports.
- Adding additional functions to text editors like "vi."
- Translating files from one format to another.
- Creating small databases.
- Performing mathematical operations on files of numeric data.

**`awk` has two faces:**

1. It is a utility for performing simple text-processing tasks.
2. It is a programming language for performing complex text-processing tasks.

**How Does `awk` Work**

- `awk` reads the file being processed line by line.
- The entire content of each line is split into columns with space or tab as the delimiter.

- `$0`: Print the entire line.
- `$1`, `$2`, `$3`, ... for each column (if exists).
- `NR`: Number of records (lines).
- `NF`: Number of fields or columns in the current line.

By default, the field delimiter is space or tab. To change the field delimiter, use the `-F` option.

**`awk` Syntax**

```shell
awk pattern {action}
```

- `

pattern` decides when the `action` is performed.
- Most common action is `print`.

**Example:**

**Print file `dosum.sh`:**

```shell
awk "{print $0}" dosum.sh
```

---

**File: Page 17.jpg**

**`awk` Examples**

**Print the list of files that are bash script files:**

```shell
awk '/#!/ {print $0, FILENAME}' *
```

**For Practice Shell scripts, you can refer to this article:**

https://medium.com/@sankad_19852/shell-scripting-exercises-5eb7220c2252

Remove page numbers and check the article for faults and rectify
ChatGPT
I see that you've provided details for each page of the document, including information on shell scripting, file naming conventions, variable usage, control commands, loops, and advanced text processing commands like grep, sed, and awk. Additionally, you've requested that I remove page numbers and check the article for any faults.

Based on the provided information, here's a cleaned-up version of the content without page numbers:

Shell Scripting Notes

What is Shell Script?

In the simplest terms, a shell script is a file containing a series of commands. The shell reads this file and carries out the commands as though they have been entered directly on the command line.

Normally, shell scripts have the file extension .sh.
To create a shell script, use a text editor.
Creating a Shell Script:

Use an editor like vi or gedit to write the script.
After writing the script, set execute permission:
shell
Copy code
chmod +x script_name
File Naming Conventions:

A file name can be a maximum of 255 characters.
The name may contain alphabets, digits, dots, and underscores.
System commands or Linux reserved words cannot be used for file names.
Linux is case-sensitive, so file names, variables, and arrays in shell scripts are also case-sensitive.
Example:

shell
Copy code
Hjbinjoash
stringi=te
Stringi=20
echo "The value of string is $string"
echo "The value of Stringi is $Stringi"
Example:

shell
Copy code
# chmod +x <script_file_name>
chmod 755 <script_file_name>
Note:

This sets read, write, and execute (7) permission for the owner, for the group, and other permissions are read and execute only (5).

Execute Your Script:

bash script_file_name
sh script_file_name
./script_file_name
Linux is case-sensitive, so file names, variables, and arrays used in shell scripts are also case-sensitive.

Example:

shell
Copy code
Hjbinjoash
stringi=te
Stringi=20
echo "The value of string is $string"
echo "The value of Stringi is $Stringi"
Running Shell Scripts:

To execute a shell script, ensure you have execute permission.
Give execute permissions using chmod.
File Naming Conventions:

A file name can be a maximum of 255 characters.
The name may contain alphabets, digits, dots, and underscores.
System commands or Linux reserved words cannot be used for file names.
Linux is case-sensitive.
Example:

shell
Copy code
Hjbinjoash
stringi=te
Stringi=20
echo "The value of string is $string"
echo "The value of Stringi is $Stringi"
Comments

Comments are used to escape from the code.
Adding comments makes code more readable.
Single-line comments are created using #.
Multiline comments can be created using the HERE DOCUMENT feature.
Example:

shell
Copy code
#!/bin/bash

# This is a basic shell script by shubhan.

echo "Hello, welcome to The DevOps Learning." # It will display the message
Variable Names:

Variables must begin with an alphanumeric character or underscore (_).
Conventionally, environment variables and internal shell variables are capitalized; all other variable names should be lowercase.
Variable names are case-sensitive.
System-defined Variables:

Created and maintained by the Linux bash shell.
Defined in CAPITAL LETTERS.
Many shell inbuilt variables are used for administration and writing shell scripts.
User-defined Variables:

Created and maintained by the user.
Avoid using all uppercase names.
Example:

shell
Copy code
#!/bin/bash

trainingCourse="DevOps"

echo "Displaying the user-defined variable (trainingCourse):"
echo "Value is: $trainingCourse"
Command Line Arguments

Values passed through the command prompt are command-line arguments.
No limitation on the number of arguments.
Separated by space.
Example:

shell
Copy code
./scriptfile.sh arg1 arg2 arg3
File Name: commandLineArgs.sh

shell
Copy code
#!/bin/bash

echo "Number of arguments on the command line: $#"
echo "Process number of the current process: $$"
echo "Display the 3rd argument on the command line, from left to right: $3"
String Formatting

Character Description:

-n: Do not output the trailing new line.
-e: Enable interpretation of backslash escaped characters in the string.
\a: Alert (bell).
\b: Backspace.
\e: Suppress trailing new line.
\n: New line.
\r: Carriage return.
\t: Horizontal tab.
\\: Backslash.
User Interaction using read Command:

Use the read statement to take input from the user.
read command is used to get input from the user, making scripts interactive.
Example:

File Name: readname.sh

shell
Copy code
#!/bin/bash

echo "Please enter your name:"
read username

echo "The name you entered is $username"
Displaying Special Variables:

$0: Name of the current shell or program.
$#: Number of arguments on the command line.
$$: Process number of the current process.
$n: nth argument on the command line.
$@: All arguments on the command line (separate words).
$*: All arguments on the command line (single word).
$?: Exit status of the last executed command.
Example:

shell
Copy code
echo "$0: $0"
echo "$#: $#"
echo "$$: $$"
echo "$1: $1"
Difference between $* and $@:

$* treats the collection of arguments as one text string.
$@ treats the collection of arguments as separate strings.
Variable Names:

Variables must begin with an alphanumeric character or underscore (_).
Conventionally, environment variables and internal shell variables are capitalized; all other variable names should be lowercase.
Variable names are case-sensitive.
System-defined Variables:

Created and maintained by the Linux bash shell.
Defined in CAPITAL LETTERS.
Many shell inbuilt variables are used for administration and writing shell scripts.
User-defined Variables:

Created and maintained by the user.
Avoid using all uppercase names.
Example:

Filename: user_defined_variables.sh

shell
Copy code
#!/bin/bash

trainingCourse="DevOps"

echo "Displaying the user-defined variable (trainingCourse):"
echo "Value is: $trainingCourse"
Control Commands

if Control Statement:

Syntax:

shell
Copy code
if condition
then
  # Display commands list if condition is true
else
  # Display commands list if condition is false
fi
Example:

File Name: FindBiggestNumber.sh

shell
Copy code
if [ $1 -ne 3 ]
then
  echo "$0: Number 1 and Number 3 are not given."
  exit 1
fi

if [ $1 -ge $2 ] && [ $1 -ge $3 ]
then
  echo "$1 is the biggest number"
elif [ $2 -ge $1 ] && [ $2 -ge $3 ]
then
  echo "$2 is the biggest number"
elif [ $3 -ge $1 ] && [ $3 -ge $2 ]
then
  echo "$3 is the biggest number"
else
  echo "All three numbers are equal"
fi
Output:

shell
Copy code
Please enter your name: Shubhan Londhe
The name you entered is Shubham Londhe
Loops in Shell Scripting

for Loop

Syntax:

shell
Copy code
for ((initialization; condition; increment))
do
  commands
done
Example:

shell
Copy code
for ((i = 5; i >= 1; i--))
do
  echo $i
done
Output:

shell
Copy code
5
4
3
2
1
while Loop

Syntax:

shell
Copy code
while [ condition ]
do
  commands
done
Example:

shell
Copy code
count=5

while [ $count -gt 0 ]
do
  echo $count
  count=$((count - 1))
done
Output:

shell
Copy code
5
4
3
2
1
Advanced Text Processing Commands

grep

grep is a Unix utility that searches for a pattern in files or data piped to it.
egrep (extended grep) extends grep functionality with regular expressions.
grep Options:

-i: Ignore case during search.
-r: Search recursively.
-v: Invert match (match everything except the pattern).
-l: List files that match the pattern.
-L: List files that do not match the pattern.
-n: Prefix each line of output with the line number within its input file.
-A num: Print num lines of trailing context after matching lines.
-B num: Print num lines of leading context before matching lines.
Example:

Search files containing the word "bash" in the current directory:

shell
Copy code
grep "bash" *
grep (continued)

grep Examples:

Search files NOT containing the word "bash" in the current directory:

shell
Copy code
grep -v "bash" *
Repeat the above search using a case-insensitive pattern match and print the line number that matches the search pattern:

shell
Copy code
grep -i -n "bash" *
Search files not matching a certain name pattern (e.g., "fun"):

shell
Copy code
grep -v -i "fun" *
grep OR

shell
Copy code
grep 'Man\|Sales' employee.txt
Output:

shell
Copy code
196 Shub Manager Sales $5,608
30 Ankur Sysadmin Technology $7,000
500 Naveen Manager Sales $6,690
grep AND

shell
Copy code
grep -i 'sys.*Tech' employee.txt
Output:

shell
Copy code
198380 Ankur Sysadmin Technology $7,080
sed

sed (stream editor) is used to parse and transform information, either from information piped to it or from files.
sed is line-oriented, operates one line at a time, and allows regular expression matching and substitution.
sed Commands and Flags

s substitution command.
Example:

shell
Copy code
sed 's/old_pattern/new_pattern/' filename
awk

The awk text-processing language is useful for tasks such as:

Tallying information from text files and creating reports.
Adding additional functions to text editors like "vi."
Translating files from one format to another.
Creating small databases.
Performing mathematical operations on files of numeric data.
awk has two faces:

It is a utility for performing simple text-processing tasks.
It is a programming language for performing complex text-processing tasks.
How Does awk Work

awk reads the file being processed line by line.

The entire content of each line is split into columns with space or tab as the delimiter.

$0: Print the entire line.

$1, $2, $3, ... for each column (if exists).

NR: Number of records (lines).

NF: Number of fields or columns in the current line.

By default, the field delimiter is space or tab. To change the field delimiter, use the -F option.

awk Syntax

shell
Copy code
awk pattern {action}
pattern decides when the action is performed.
Most common action is print.
Example:

Print file dosum.sh:

shell
Copy code
awk "{print $0}" dosum.sh
awk Examples

Print the list of files that are bash script files:

shell
Copy code
awk '/#!/ {print $0, FILENAME}' *
For Practice Shell scripts, you can refer to this article:

https://medium.com/@sankad_19852/shell-scripting-exercises-5eb7220c2252

