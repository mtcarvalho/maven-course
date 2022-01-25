# Apache Maven: Beginner to Guru

[Udemy course](https://www.udemy.com/course/apache-maven-beginner-to-guru/) code repository.

## System Requirements

- IntelliJ or Eclipse or NetBeans IDE
- Java 11 or Higher Required 
- Must have JDK Installed
    Oracle or OpenJDK is okay. Oracle licensing of Java **does** permit for development use.
- Apache Maven 3.6.0 or Higher Required

Check environment with below commands:

```
java --version  // java 11
javac --version // javac 11
mvn --version   // maven 3.6.0 or higher
```

### Section 02: Getting Started

#### Highlights

- In this section, it is showed a minimal version of `pom.xml` file.

- Below are maven coordinates:

    ```
    <groupId>guru.springframework</groupId>
    <artifactId>hello-world</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    ```

#### Commands

`javac HelloWorld.java` compiles the source code to `HelloWorld.class` bytecode file

`java HelloWorld` runs the code

`jar cf myjar.jar HelloWorld.class` packages the bytecode class file to a jar file

`java -classpath myjar.jar HelloWorld` executes the java class file out of the jar file

- Commands after adding lib folder

`javac -classpath ./lib/* HelloWorld.java` includes everything in `lib` folder when compiling the source code

`java -classpath "./lib/*;/." HelloWorld` picks everything in lib and root folder, and runs the code

- Commands after adding `pom.xml` file

`mvn clean` clean out the environment

`mvn package` says there is no sources to compile. It creates a `target` folder without `.class` files.

`mvn clean` again deletes the `target` folder.

To compile the app:

```
mkdir src/main/java
mv HelloWorld.java ./src/main/java
mvn clean package
mvn clean
```