### Sample template for Scala project to demonstrate use of Ensime (An Emacs package for Scala development)

### Steps

1. Create a folder named hello_scala
2. Create a file named build.sbt in the folder.

    ``` scala
    name := "Hello Scala"

    version := "1.0"

    scalaVersion := "2.11.2"
    ``` 
    
3. Run command 'sbt' on the project.
4. You will notice a folders named 'project' and 'target' has been created
5. Add file named plugins.sbt in the project folder with followign content

    ``` scala
    resolvers += Resolver.sonatypeRepo("snapshots")

    addSbtPlugin("org.ensime" % "ensime-sbt" % "0.1.5-SNAPSHOT")
    ```

6. run 'sbt console'. It will throw you inside sbt repl console
7. Run 'ensime generate' in the console and it will generate ensime files.
8. Start writing scala code (e.g. Create file named src/main/scala/HelloScala.scala)
9. Type 'M-x ensime' in Emacs with .scala file opened. It should start ensime server.
10. Crack on.
