# My way of setting up a TypeScript project from local to remote

- **`CORRECTIONS ARE WELCOME`**: If you notice any mistakes or have suggestions, I would appreciate your input.
- Here's my step-by-step guide to set up a basic TypeScript project.

  **`Prerequisites`**:

  1. Node.js and npm: Install Node.js and npm (Node Package Manager) on your machine. You can download them from the official website:. [ Node.js](https://nodejs.org/en)

  **`Setting up a TypeScript Project`**:

  1. **`Set up Local Repository`**

     - Navigate to the parent directory
       ```
       cd path/to/parent/directory
       ```
     - Create a new directory for your project
       ```
       mkdir learning-typescript
       ```
     - Change into the project directory

       ```
       cd learning-typescript
       ```

     - Initialize a new Git repository
       ```
       git init
       ```

  2. **`Create a .gitignore File`**

     - Create a .gitignore file

       ```
       touch .gitignore
       ```

     - Open .gitignore in a text editor and add the following content

       ```gitignore
         # Node.js
         node_modules/

         # TypeScript
         *.tsbuildinfo

         # Visual Studio Code
         .vscode/

         # macOS
         .DS_Store
       ```

       How about pacakge-lock.json in .gitignore?

       That depends on your project and team's preferences. Here are some considerations:

       - **`Include package-lock.json in .gitignore`**:

         - If your project is a library or a package meant to be used by others, it's common to include package-lock.json in .gitignore. This is because consumers of your package will generate their own lock file based on their environment.
         - It reduces the chances of conflicts when multiple developers are working on the project, especially if they have different Node.js versions.

       - **`Do not include package-lock.json in .gitignore`**:
         - If you want to ensure that everyone working on the project uses the exact same dependencies with the same versions, you may choose not to include package-lock.json in .gitignore. This is more common in application projects where consistency in dependencies is crucial.

       Here's an example of how to include package-lock.json in .gitignore:

       ```gitignore
         # Node.js
         node_modules/
         package-lock.json

         # TypeScript
         *.tsbuildinfo

         # Visual Studio Code
         .vscode/

         # macOS
         .DS_Store
       ```

  3. **`Create Your TypeScript Project`**:

     - **`Initialize a TypeScript project`**:
       ```
       npm init -y
       ```
     - **`Install TypeScript as a development dependency`**:

       ```
       npm install --save-dev typescript
       ```

     - **`Create a tsconfig.json file`**:

       ```
       npx tsc --init
       ```

     - **`Update package.json scripts`**:

       ```
        "scripts": {
        "tsc": "tsc"
        }
       ```

       To use TypeScript compiler "npm run tsc index.ts"

  4. **`Make Your Initial Commit`**:

     - Create and switch to a new branch
       ```
       git checkout -b main
       ```
     - Add all files to the staging area
       ```
       git add .
       ```
     - Make your initial commit with a conventional format
       ```
       git commit -m "chore: initial project setup"
       ```

  5. **`Create a Remote Repository on GitHub`**:

     - Go to GitHub and log in to your account.
     - Click on the "+" sign in the top right corner and select "New repository."
     - Fill in the repository name as "learning-typescript."
     - Optionally, add a description, choose public or private visibility, and initialize the repository with a README file if you wish.
     - Click the "Create repository" button.

  6. **`Connect Local Repository to Remote`**:

     - Copy the URL of your newly created repository.
     - It should look like https://github.com/your-username/learning-typescript.git
     - Add the remote repository

       ```
       git remote add origin https://github.com/your-username/learning-typescript.git
       ```

  7. **`Push to Remote Repository`**:

     - Push your code to the remote repository

       ```
       git push origin main
       ```

  8. **`Verify on GitHub`**:

     - Go back to your GitHub repository in the browser and refresh the page. You should see your code there.
