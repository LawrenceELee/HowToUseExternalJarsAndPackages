```
How to compile your .java using an external jar:

* Assume /home/user/code/java/ExternalJar (cygwin path ) is the "root"
  directory of this project.

* Also assumes you have .jar file 'junit-4.10.jar' located in 
  'C:\cygwin\home\user\bin\junit4.10\' directory

(This assumes the .java file has 'package com.my.somepkg' at the top.)

1) Go to "root" directory of your project.

2) To compile .java:
   javac -cp ".;C:\cygwin\home\user\bin\junit4.10\junit-4.10.jar" com/my/somepkg/MyTestRunner.java

3) To run .class:
   java -cp ".;C:\cygwin\home\user\bin\junit4.10\junit-4.10.jar" com.my.somepkg.MyTestRunner

Note: the usage of . (dots) in the class name when running.

If package is not specified, then it assumes current directory. 
Then you can omitt path to .java and .class files respectively.

1) Go to directory where .java file are located.

2) javac ...same as above... MyTestRunner.java

3) java ...same as above... MyTestRunner


Note:
* In Windows, you need to use ; (semi-colon) to seperate multiple paths.
* Also, use \ (back slash) instead of / (forward slash) for sub directories.
* You don't have to be in "root" directory to compile .java , but you have 
  to be in "root" directory to run .class file.
* In Linux, you need to use : (semicolon) and / (forwardslash) respectively
* '-cp <path>' can be omitted if specified in the CLASSPATH 
  system/envirmonment variable.
* If you have multiple jars to list in the classpath and they are all in the
  directory, you can use classpath wildcards (ex. "Test.jar;lib/*")
  Note the use of double quotes to surround classpath, and * not *.jar
  reference: http://stackoverflow.com/q/219585
```
