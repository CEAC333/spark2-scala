# spark2-scala

## Getting Started

- Twitter Developer Account - https://developer.twitter.com/

## Introduction, and Getting Set Up

**MacOS**

**Step 1: Install Spark**

**Method A: By Hand**

The best setup instructions for Spark on MacOS are at the following link:

https://medium.com/luckspark/installing-spark-2-3-0-on-macos-high-sierra-276a127b8b85

**Method B: Using Homebrew**

An alternative on MacOS is using a tool called Homebrew to install Java, Scala, and Spark – but first you need to install Homebrew itself.

Step by step instructions are at https://www.tutorialkart.com/apache-spark/how-to-install-spark-on-mac-os/

```
cd /usr/local/Cellar/apache-spark/2.4.0/libexec/conf
nano log4j.properties.template log4j.properties
```

Find the line starting with log4j.rootCategory and change the log-level from INFO to ERROR:

```
log4j.rootCategory=ERROR, console
```

Step 2: Install the Scala IDE
Install the Scala IDE from http://scala-ide.org/download/sdk.html

Step 3: Test it out!
cd to the directory apache-spark was installed to and then ls to get a directory listing.
Look for a text file we can play with, like README.md or CHANGES.txt
Enter spark-shell
At this point you should have a scala> prompt. If not, double check the steps above.
Enter val rdd = sc.textFile(“README.md”) (or whatever text file you’ve found) Enter rdd.count()
You should get a count of the number of lines in that file! Congratulations, you just ran your first Spark program!
Hit control-D to exit the spark shell, and close the console window
You’ve got everything set up! Hooray!


