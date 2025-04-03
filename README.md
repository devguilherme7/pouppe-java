# Pouppe

## Test Coverage with JaCoCo

This project uses [JaCoCo](https://www.eclemma.org/jacoco/) (Java Code Coverage) to generate test coverage reports,
allowing you to monitor which parts of the code are coverage by tests and ensure system quality.

1. Run the tests: `./gradlew test`
2. Generate the coverage report: `./gradlew jacocoTestReport`
3. Open the reported located at `<subproject>/build/reports/jacoco/jacocoHtml/index.html`.

## Code Style with Checkstyle and Spotless

This project uses **Checkstyle** and **Spotless** to ensure consistent code quality and formatting across the codebase.

### Checkstyle

Checkstyle enforces coding standards by validating the source code against a set of predefined rules.
The rules are configured in the file located at `config/checkstyle/checkstyle.xml` in the root of the project.

To run Checkstyle and verify code compliance:

```shell
./gradlew checkstyleMain
./gradlew checkstyleTest
```

The results will be available in the `build/reports/checkstyle` directory of each subproject.
Both XML and HTML reports are generated to provide detailed insights into any violations detected.

Checkstyle helps maintain consistent code style, making the codebase easier to read and reducing potential errors caused
by style inconsistencies.

### Spotless

Spotless ensures consistent code formatting by automatically applying rules to format your code and remove unused
imports. It is configured to use a custom Eclipse formatter and can automatically organize imports and trim trailing
whitespaces.

To check the formatting without applying fixes, run:

```shell
./gradlew spotlessCheck
```

To fix any formatting issues automatically, run:

```shell
./gradlew spotlessApply
```
