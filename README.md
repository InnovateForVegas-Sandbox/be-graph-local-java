# Project Installation Guide

This project includes Apache Jena for parsing DOAP files.

It also includes ANTLR for parsing code files. It can be ignored. It might be useful for parsing GitHub template files and other working directory analysis.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- Java Development Kit (JDK) 21 or higher
> [!NOTE]  
> Please edit the target and compile version in pom.xml if you want to use it on a different java version that you might have installed.
- Apache Maven 3.6.0 or higher

## Getting Started

See [LocalGraphCommand.java](src/main/java/info/project_act/tessellation/cmd/LocalGraphCommand.java) for the entry-point of the CLI application.

### Convert n3 file to RDF

```java
mvn compile exec:java -Dexec.mainClass="info.project_act.tessellation.Main" -Dexec.args="convert -n src/main/resources/doap.n3"
```

## Installation Steps

1. **Clone the repository:**

    ```sh
    git clone https://github.com/InnovateForVegas-Sandbox/be-graph-local-java.git
    cd be-graph-local-java
    ```

2. **Build the project:**

   Navigate to the root directory of the project and run the following command to build the project using Maven:

    ```sh
    mvn clean install
    ```

   This command will compile the project, run the tests, and package the application.

3. **Run the tests:**

   To run the tests, use the following command:

    ```sh
    mvn test
    ```

   This will execute all the unit tests in the project.

## Directory Structure

- `src/main/java`: Contains the main source code.
- `src/test/java`: Contains the test source code.
- `src/main/resources`: Contains the resource files.
- `src/test/resources`: Contains the test resource files.

## Additional Information

- **Dependencies:** All project dependencies are managed through Maven and are specified in the `pom.xml` file.
- **IDE:** It is recommended to use VSCode for development. There are launch commands and recommended extensions included in (.vscode/)[./.vscode]

## Troubleshooting

If you encounter any issues during the installation or build process, please check the following:

- Ensure that the JDK and Maven are correctly installed and configured in your system's PATH.
- Verify that you have the correct versions of JDK and Maven.

For further assistance, please refer to the project's documentation or contact the project maintainers.
