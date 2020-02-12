# What is "pretty-format"?
When I use git commands such as git log or git rebase -i (interactive rebase), results are shown specific format that is set as default in Git. But one day, I needed some more information than that. When I was using git rebase -i command, I wanted to see the author's name of the commit, and when it was committed to the repository, in addition to the informations like commit-id and some other stuff.

When using git rebase -i command, only the commit-id and commit's title is shown as defult.

```
pick 2402571 TIL : 2018.09.22
pick 65f6559 Fixed directory issue
pick 731cec2 files were swapped..!
pick 500ec97 Add image path

# Rebase 07c6748..500ec97 onto 07c6748 (4 commands)
```
But I needed some more information of the commits in order to complete the rebase command successfully. So, I searched about showing date and author of the commit along with above's information, and found about the "pretty-format'

It's usually used with the git log command, but since's it's global format in the git, you can use it in the git config to make some customization to the other command's result.

# Usage
* Ex. git log 
```bash
git log --pretty=format:"%H %an <%ae>"
```
  * This shows commit id(hash), author name, and author's email.

* Ex. git rebase -i (Used in the git config)
```bash
[rebase]
  instructionFormat = (%an <%ae>) %s %cd
```
  * (%an <%ae>) %s part is the default format, and i added %cd to print the commit's comitted date.


# Reference
* [Git Pretty Formats](https://git-scm.com/docs/pretty-formats)