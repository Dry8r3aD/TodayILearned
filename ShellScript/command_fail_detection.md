# Detecting command fail in Shell Script
I wanted to run "make" command before I push my commit for review, so it could stop me from pushing not-buildable commit to code review system, gerrit.

So I was googling up some Shell Script options and commands, and ended up with adding "set e" at the top of my pre-push code.

# My usage
I usually use [git review](https://www.mediawiki.org/wiki/Gerrit/git-review) to push commit, but I wanted to run make command before it actually gets pushed. It was an easy job for me to make a shell script which does that, but without this option, "set -e", it just ran through the script and tried to push my commit for review even though code build had failed.

So, I added "set -e" option, and everything worked perfectly.

Of course I could have used git hook, but I wanted more simple way, and not per project, but per build machine(developement machine).

# Example
review.sh (~/.script/review.sh)
```
set -e   
                                                                                                                                                                                                                   
make                                                                                                                                                                                                                        
git review
```

~/.zshrc
```
alias gitr="~/.script/review.sh"
```

