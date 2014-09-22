```
How to compile your .java using an external jar:
(This assumes the .java file has 'package com.my.somepkg' at the top.)

Assume /home/user/code/java/ExternalJar is the "root" directory of this project.

To compile .java:
javac -cp ".;C:\cygwin\home\user\bin\junit4.10\junit-4.10.jar"
com/my/somepkg/MyTestRunner.java

To run .class:
java -cp ".;C:\cygwin\home\user\bin\junit4.10\junit-4.10.jar"
com.my.somepkg.MyTestRunner

If not package is specified, then it assumes current directory. 
And you can omitt path to .java and .class files respectively.

javac ...same as above... MyTestRunner.java
java ...same as above... MyTestRunner


Note:
* In Windows, you need to use ; (semi-colon) to seperate multiple paths.
* Also, use \ (back slash) instead of / (forward slash) for sub directories.
* You don't have to be in "root" directory to compile .java , but you have 
  to be in "root" directory to run .class file.
* In Linux, you need to use : (semicolon) and / (forwardslash) respectively
* This also assumes you have file junit-4.10.jar located in 
  C:\cygwin\home\user\bin\junit4.10\ directory
```
