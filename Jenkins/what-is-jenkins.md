t is Jenkins?
Today for my TIL, I want to write about the software called Jenkins. Jenkins is a software tool for CI, the Continuous integration. (I will do TIL about the CI another day)

# Download
	You can download the Jenkins tool here. [https://jenkins.io](https://jenkins.io)

	When downlaoding, you'll have two options. One, downloading LTS verison, two, downloaing weekly release version. I recommend LTS version unless you're just testing your toy project.

# Installation
	A server is required for you to install a CI server of your own. Looks like several enviroment is supported, such as Mac, Windows, Linux (Gentoo, Debian/Ubuntu, RedHat/Fedora/CentOS), FreeBSD, OpenBSD, OpenSUSE, and even the docker. I think running a CI tool for personal project is also a good idea.


# Jenkins Experience
	I use and manage Jenkins & Coverity for my developement devision in my company. And from my experience, Jenkins is really a attractive CI tool to use. One of the best thing about Jenkins is that it has lots of plugins, and can work with Code Review tools like [Gerrit](https://www.gerritcodereview.com), or colaboration tools like [Slack](https://www.slack.com/). We can calculate the code coverage (how much the code is covered by the unit test) using [cppcheck](http://cppcheck.sourceforge.net) too.

