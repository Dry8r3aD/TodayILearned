#Shell Command, seq
Shell command 'seq' is a linux command which prints out sequences of numbers. Detailed
usage can be found by typing "man seq" in the sell, or linux man page, [man
seq](https://linux.die.net/man/1/seq)

# My usage
I used this command when i need to test my binay's input, by creating a shell
script.
I think this command should be usful to anyone who's developing in linux env.

# Example
```
root@dev# seq 4 10
4
5
6
7
8
9
10
```
```
root@dev# seq 13 10
13
12
11
10
```
```
root@dev# seq -w 0 .05 .1
0.00
0.05
0.10
```

