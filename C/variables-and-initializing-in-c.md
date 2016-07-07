# Variables and Initializing in C

Today at my company, I found a code which intrested me so much. And I thought it would be nice to write down about this in my TIL.

## What I knew untill now about vriable initalization
* When using variable, initialize. __Period.__
* **Example**

```c
#include <stdio.h>

int main ( void )
{
	// This is the part where I initialize my variable
	for ( int i = 0; i < 10; i++ )
	{
		printf( "Hello World \n" );
		printf( "%d \n", i );
	}

	return 0;
}
```
* If I use the variable without the initialization, the variable's inital value would be not what I have expected, because of the garbage value.

## What I experienced today
* Code

```c
#include <stdio.h>

int main ( void )
{
	for ( int i; i < 10; i ++ )
	{
		printf( "Hello World \n" );
		printf( "%d \n", i );
	}

return 0;
}
```
* When I first saw this code, I though this code would never work. (Or at least works very intermittently).
* So I compiled and excuted the binary like below, and something I would have never expected happend.
<code> # gcc std=c99 -c code.c; gcc -o run code.o; ./run  </code>
* This code actually worked just like what I had expected it to work.
<pre>ubuntu@ip-172-31-6-98 # ./run
Hello World
0
Hello World
1
Hello World
2
Hello World
3
Hello World
4
Hello World
5
Hello World
6
Hello World
7
Hello World
8
Hello World
9
</pre>
* This code actually worked with the initialized variable "i"


## Different results from different environment

* Since I have some various environments, such as Debian 6, Debian 8, Gentoo, Mac OS X, etc, i tried the same code to every single environment I have.
* _I'm not sure about the compiler(gcc) version of the environments. I guess I need to check it out_
* Debian 6, Debian 8
	* works perfectly fine
* Gentoo
	* works fine, except when I use -O2 option, it didn't print anything which means variable "i" was filled with the garbage data without initialization.
* Mac OS X
	* Never worked.

## Conclusion?
So my conclusion is that the variable initialization is done by the compiler(gcc), but it varys by the version of the compiler.
**BUT, I doubt that initializing a variable before using is a very important thing to remember when writing a code (At least in C)...
Let's be independent from the specific compiler.**
