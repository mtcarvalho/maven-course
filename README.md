# Apache Maven: Beginner to Guru

[Udemy course](https://www.udemy.com/course/apache-maven-beginner-to-guru/) code repository.

## System Requirements

- IntelliJ (recommended) or Eclipse or NetBeans IDE
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

### Hello World App

#### Concepts

In a **thin** jar, dependencies are not included. With `mvn clean package`, the dependency is included at compile time, but is not included in the build artifact.

In **fat** jars, it is possible to see the jars (dependencies) listed.

#### Highlights

- Below are maven coordinates:

    ```
    <groupId>guru.springframework</groupId>
    <artifactId>hello-world</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    ```

#### Commands

- Commands to compile, package & run the app

`javac HelloWorld.java` compiles the source code to `HelloWorld.class` bytecode file

`java HelloWorld` runs the code

`jar cf myjar.jar HelloWorld.class` packages the bytecode class file to a jar file

`java -classpath myjar.jar HelloWorld` runs the java class file out of the jar file

- Commands when using lib folder to store jar files (app dependencies)

`javac -classpath ./lib/* HelloWorld.java` includes everything in `lib` folder when compiling the source code

`java -classpath "./lib/*;/." HelloWorld` picks everything in lib and root folder, and runs the code

- Commands when using `pom.xml` file

`mvn package`: creates a `target` folder without `.class` files.  
`mvn clean`: deletes the `target` folder (if exists)

#### Tips & Tricks

- Add dummy files for github sync - it ignores empty directories. Here, we created on `hello-world/src/main/resources/application.properties` and `hello-world/src/test/java/package-info.java`
