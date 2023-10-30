# What is a Conventional Commits?

You can visit this website to understand how [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) works.

But, based on my comprehension, Conventional Commits are a standardized format for writing commit messages in version control systems like Git.

The conventional commit format typically follows this pattern:

```
<type>(<scope>): <message>

[optional body]

[optional footer(s)]
```

Here's what each part represents:

- _**Type**_: Describes the purpose of the commit (e.g., feat, fix, chore, docs, style, refactor, perf, test).
- _**Scope**_ (optional): Indicates the component or area of the project that the commit affects.
- _**Message**_: A concise description of what the commit does.
- _**Body**_ (optional): Provides additional context, details, or information about the changes made in the commit.
- _**Footer(s)**_ (optional): Can contain additional information like references to issues or other related tasks.

For example:

```
feat(user-auth): add password reset functionality

Added a new route '/reset-password' to handle password reset requests. Also, implemented the logic for generating and sending reset links to users.

Closes #123

```

In this example:

- **_feat_** is the type, indicating a new feature is being added.
- **_user-auth_** is the scope, specifying that this feature relates to user authentication.
- **_add password reset functionality_** is the message, explaining what the commit does.
- The body provides more detailed information about the changes made in the commit.
- The footer contains a reference to the related issue (in this case, it closes issue #123).

Let's go to the next section to talk about [Types in Conventional Commits](/ConventionalCommits/types-in-conventional-commits.md)
