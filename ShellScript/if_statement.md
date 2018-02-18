# Shell Script, IF/ELSE
Today, I was writing a script for some of my works, which I was doing repeatly. While writng a script, I had to search(google) about shell script's if comparison. Actually this wasn't my sirst time searching about shell script's IF statement, so I thouhg it would be good to write a TIL about it, so I wouldn't have to search it again.


# IF Statement
As same as other programming language, IF statement is also rapidly used in Shell Script. <br/>
It is used to compare numbers or strings, or deal with some file operations too.


## Comparing numbers(integers)
* Unlike other languages like C or Python, we can't use operators like "==" or "!=" fir number comparison.
* Use the operators like below.

### Number compare operators
**Comparison** | **Explanation**
:-----:|:-----:
-eq | equal to
-ne | not equal to
-lt | less than
-le | less than or equal to
-gt | greater than
-ge | greater than or equal to

### Example
* Shell /Version
  * zsh 5.1.1 (x86_64-ubuntu-linux-gnu))

```
 if [ 5 -eq 5 ]
then
    echo "Euqal!"
fi

if [ 5 -ne 6 ]
then
    echo "Not equal!"
fi

if [ 6 -lt 7 ]
then
    echo "6 < 7"
fi

if [ 6 -le 6 ]
then
    echo "6 <= 6"
fi

if [ 6 -le 7 ]
then
    echo "6 <= 7"
fi

if [ 10 -gt 5 ]
then
    echo "10 > 5"
fi

if [ 10 -ge 10 ]
then
    echo "10 >= 10"
fi

if [ 10 -ge 5 ]
then
    echo "10 >= 5"
fi
```
 
### Output
<pre>
Euqal!
Not equal!
6 < 7
6 <= 6
6 <= 7
10 > 5
10 >= 10
10 >= 5
</pre>
 
 
## Comparing strings
* String comparison is more similar to C then comparing numbers.
* Use the operators like below.

### String compare operators
**Comparison** | **Explanation**
:-----:|:-----:
= | equal to
!= | not equal to

### Example
* Shell /Version
  * zsh 5.1.1 (x86_64-ubuntu-linux-gnu))

```bash
if [ "C" = "C" ]
then
    echo "Equal!"
fi

if [ "C" != "Python" ]
then
    echo "Not equal!"
fi
```

### Output
<pre>
Equal!
Not euqal!
</pre>


## File Operations
* Addition to comparing strings and numbers, we can do some file(directory) operations, such as checking if file is readable, or exists.

### File operations
**Operation** | **Explanation**
:-----:|:-----:
-s | file exists and is not empty
-f | file exists and is not a directory
-d | directory exists
-x | file is executable
-w | file is writable
-r | file is readable

# Reference
* [unix-shell-scripting/ifelse-tutorial](http://www.dreamsyssoft.com/unix-shell-scripting/ifelse-tutorial.php)