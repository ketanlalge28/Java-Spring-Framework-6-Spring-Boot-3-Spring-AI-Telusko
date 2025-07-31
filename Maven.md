# Maven - (java)


## What is Maven? 
- Maven is a build automation and project management tool used primarily for Java projects.

- You can absolutely say that Maven is like npm, but for Java — that’s a good comparison.

- Just like npm helps Node.js projects manage packages, dependencies, and scripts, Maven does the same for Java projects, including building and testing.




## Maven vs npm -

| Feature                    | Maven (Java)                       | npm (JavaScript/Node.js)           |
| :------------------------- | :--------------------------------- | :--------------------------------- |
| Language Ecosystem         | Java                               | JavaScript / Node.js               |
| Config File                | `pom.xml`                          | `package.json`                     |
| Manages Dependencies       |   Yes                              |   Yes                              |
| Build Tool                 |   Yes (compiles, tests, packages)  |   No by default (use with tools like Webpack) |
| Installs Libraries From    | Maven Central Repository           | npm Registry                       |
| Runs Scripts               |   Using plugins                    |   Using `scripts` section          |
| Package Format             | `.jar`, `.war`                     | `.js`, `.json`, etc.               |



## What is Effective POM? - (Project Object Model)

- It is the final, fully-resolved version of your pom.xml file that Maven uses to build your project — after combining:

    - Your project's own pom.xml

    - The parent POM (if you inherit one)

    - All default settings from Maven’s Super POM

    - Dependencies, plugins, properties, profiles, etc.



## What is an Archetype in Maven?

- A Maven archetype is like a project blueprint or starter kit — it saves time by giving you a ready-made structure with best practices.



## How Maven Works? 

- It follows this order to resolve dependencies:
    - Check Local Repository (~/.m2/repository on your machine)
    - If Not Found → Check Remote Repositories
    - Download & Cache in Local Repository

- Maven first checks your local system for dependencies. If not found, it goes online (globally) to fetch them.
