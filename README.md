Hello Graal
=======================

This is "Hello Graal" java example for GraalVM.

The structure ``Hello`` package is like this: ::

  com/
  |-- hello
  |   `-- Graal.java
  |-- LICENSE
  |-- manifest.txt
  `-- README.md

Compile class
-------------

For compile the main class for package, execute the follow command: ::

  javac -d build src/com/hello/Graal.java

This generate the ``Graal.class`` file into ``hello`` directory.

Run class
---------

For run the main class for package, execute the follow command: ::

   java -cp ./build com.hello.Graal

This show the ``hello graal`` message.

Create a JAR file
-----------------

For pack the main class for package as a JAR file, execute the follow command: ::

  jar cfvm Hello.jar manifest.txt -C build .

  jar tf Hello.jar

  META-INF/
  META-INF/MANIFEST.MF
  com/
  com/hello/
  com/hello/Graal.class

Run a JAR file
--------------

For run the JAR file packed, execute the follow command: ::

  java -jar Hello.jar

This show the ``Hello world`` message.

Create a native image
--------------

Run the native-image command: ::

  native-image -jar Hello.jar


Reference
=========

- `java - How to run a JAR file - Stack Overflow <http://stackoverflow.com/questions/1238145/how-to-run-a-jar-file>`_.

- `jar - Creating a JAR File https://docs.oracle.com/javase/tutorial/deployment/jar/build.html`_.

- `Setting an Application's Entry Point (The Java™ Tutorials > Deployment > Packaging Programs in JAR Files) <http://docs.oracle.com/javase/tutorial/deployment/jar/appman.html>`_.

- `GraalVM - How to create a native-image <https://www.graalvm.org/reference-manual/native-image/>`_.
