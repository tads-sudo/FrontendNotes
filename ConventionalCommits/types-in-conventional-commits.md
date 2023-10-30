# Different types

1.  _**feat**_: A new feature introduced to the codebase.

    ```
    git commit -m "feat(user-auth): add email verification process

    Add functionality to send a verification email to users upon registration. This email will contain a link for users to verify their email address.

    Closes #123
    ```

2.  _**fix**_: A bug fix.

    ```
    git commit -m "fix(database): resolve issue with incorrect data retrieval

    The previous implementation was using an outdated query syntax, which resulted in incorrect data being retrieved from the database.

    This commit updates the query to use the correct syntax,
    ensuring accurate data retrieval.

    Fixes #456"
    ```

3.  _**chore**_: Routine tasks, maintenance, or updates.

    ```
    git commit -m "chore(build): update build scripts for better CI integration

    The previous build scripts were causing issues with the continuous
    integration pipeline. This commit updates the scripts to ensure
    smooth integration and deployment.

    Additionally, dependencies have been updated to their latest versions
    to align with best practices.

    Closes #789"
    ```

4.  _**docs**_: Documentation-related changes.

    ```
    git commit -m "docs(readme): update installation instructions

    The installation instructions in the README file were outdated and
    contained incorrect information. This commit corrects and updates
    the instructions to ensure a smooth setup process for new users.

    Additionally, a troubleshooting section has been added to address
    common issues that users might encounter during installation.

    Closes #234"
    ```

5.  _**style**_: Code style changes (e.g., formatting, missing semi-colons).

    ```
    git commit -m "style(css): format stylesheets for consistency

    The CSS files in the project were using a mix of tabs and spaces for
    indentation, leading to inconsistent formatting. This commit applies
    uniform indentation using spaces to improve code readability.

    Additionally, unnecessary blank lines and trailing spaces have been
    removed to ensure a cleaner codebase.

    Closes #567"
    ```

6.  _**refactor**_: Code changes that neither fix a bug nor add a feature.

    ```
    git commit -m "refactor(auth): improve error handling in login process

    The login process previously had limited error handling, making it
    difficult to provide meaningful feedback to users in case of issues.
    This commit refactors the login logic to include better error handling
    and user-friendly error messages.

    Additionally, code redundancy has been reduced by extracting common
    functions and improving code organization.

    Closes #345"
    ```

7.  _**perf**_: Code changes that neither fix a bug nor add a feature.

    ```
    git commit -m "perf(api): optimize database queries for faster response times

    The API was experiencing slow response times due to inefficient
    database queries. This commit addresses the performance bottleneck
    by optimizing the queries, resulting in significantly faster
    response times for API requests.

    Additionally, query execution plans have been reviewed and
    indexes have been added where necessary to further enhance
    performance.

    Closes #678"
    ```

8.  _**test**_: Adding or modifying tests.

    ```
    git commit -m "test(unit): add new unit tests for user service

    New unit tests have been added to cover edge cases and ensure
    comprehensive test coverage for the user service.

    This commit includes tests for user registration, login, and
    password reset functionalities.

    Closes #789"
    ```

9.  _**build**_: Changes related to the build process or external dependencies.

    ```
    git commit -m "build(deps): update Node.js to version 14.0.0

    This commit updates the project's dependencies to use Node.js version 14.0.0. This version includes important security updates and performance improvements.

    Additionally, the package.json file has been updated to reflect the new Node.js version.

    Closes #123"
    ```

10. _**ci**_: Changes to the continuous integration setup and configurations.

    ```
    git commit -m "ci(travis): configure automated deployment after successful builds

    This commit updates the Travis CI configuration to automatically deploy the application to the staging environment after successful builds from the `main` branch.

    Additionally, environment variables have been securely configured in the Travis CI settings to ensure sensitive information is kept private.

    Closes #456"
    ```
