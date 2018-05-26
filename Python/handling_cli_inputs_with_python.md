# How to handle CLI Input( Arguments ) easily with Python3
I just started developing a project which has to deal with CLI inputs. When I developed in C language environment, it was so hard to parse the args and make some exceptions about them. But in Python, thankfully some other people already developed argument handling part! All we have to do is to "import argparse" in the python code file.


# Pre-Usage
* Install the library using pip( or pip3 )
  * Python2 : pip install optparse
  * Python3 : pip3 install argparse
* Import the library in your Python code
  * Python2 : import optparse
  * Python3 : import argparse 


# Usage
* Basic code flow
  * Create a parser
  * Add arguments
  * parse the arguments

_Below code examples are coded with Python 3_

## Creating a parser
```Python
parser = argparse.ArgumentParser()
```

## Adding arguments
```Python
parser.add_argument("-v", "--verbose", help="Verbose mode, enables detail log")
parser.add_argument("-l", "--log", help="Log file's path")
```

* add_argument() method
  * name or flags - Either a name or a list of option strings, e.g. foo or -f, --foo.
  * action - The basic type of action to be taken when this argument is encountered at the command line.
  * nargs - The number of command-line arguments that should be consumed.
  * const - A constant value required by some action and nargs selections.
  * default - The value produced if the argument is absent from the command line.
  * type - The type to which the command-line argument should be converted.
  * choices - A container of the allowable values for the argument.
  * required - Whether or not the command-line option may be omitted (optionals only).
  * help - A brief description of what the argument does.
  * metavar - A name for the argument in usage messages.
  * dest - The name of the attribute to be added to the object returned by parse_args().



## Parsing arguments
```Python
parser.parse_args()
```


# What this library do for you
* Parser for input arguments
* Allows a developer to easily add the custom arguments
* Creates help page for CLI input
* Handles error for invalid inputs

  
# Reference
* [Python3 argparse Document](https://docs.python.org/3.6/library/argparse.html)
* [Python2 optparse Document](https://docs.python.org/2/library/optparse.html)
* [Python3 argparse Tutorial](https://docs.python.org/3.6/howto/argparse.html)
