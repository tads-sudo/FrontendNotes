# TypeScript compilation

- Is a superset of JavaScript that adds static typing to the language

- When you write TypeScript code, you need to compile it into JavaScript before running it in a browser or a Node.js environment

- Here are the basic steps for TypeScript compilation:

  1. **`Create a TypeScript File`**: Write your code in a file with a .ts extension. For example, you can create a file named app.ts with the following content:

     ```typescript
     function greet(name: string): string {
       return `Hello, ${name}!`;
     }

     console.log(greet("TypeScript"));
     ```

  2. **`Compile TypeScript Code`**: Open a terminal, navigate to the directory containing your TypeScript file, and run the following command to compile the TypeScript code:

     ```
     tsc app.ts
     ```

     This command tells the TypeScript compiler (tsc) to compile the app.ts file. After running this command, you should see a new file named app.js in the same directory.

  3. **`Run the JavaScript Code`**: Now that you have the compiled JavaScript code, you can run it using a JavaScript runtime. For example, if it's a Node.js application, you can run:

     ```
     node app.js
     ```

     If you are working with a browser, you can include the compiled JavaScript file in an HTML file and open it in a web browser.

- **`CUSTOMIZE THE COMPILATION PROCESS`**: by configuring a tsconfig.json file, which allows you to specify compiler options and other settings for your TypeScript project.
