# Debugging TypeScript Applicaiton

- Debugging TypeScript applications using source maps is a helpful technique to trace issues in your code and identify the root causes. Source maps allow you to map the generated JavaScript code back to the original TypeScript code, making it easier to debug in the original language.

- Here's a step-by-step guide on how to set up and utilize source maps for debugging in a TypeScript application:

  1.  **`Configure TypeScript Compiler`**: Make sure your tsconfig.json file is configured to generate source maps. Ensure the sourceMap option is set to true.

      **`To do this`**:

      - Let's go inside tsconfig.json.

      - Under compilerOptions property of an object, let's find the _Emit_ section.

      - Then uncomment the "sourceMap" and save it.

      If you don't have a tsconfig.json file, you can create one in the root of your project by typing this on terminal:

      ```
      tsc --init
      ```

  2.  **`Build TypeScript Code`**: Run the TypeScript compiler to generate `index.js.map` which is the source map file.

      ```
      tsc
      ```

      To make debugging more interesting, let's go to step 3.

  3.  **`Back to index.ts file`**: To try debugging, let's write some logic to our index.ts file like this:

      ```typescript
      let age: number = 20;

      if (age < 50) age += 10;
      ```

      After this, go to the first line of the code, If your using vscode, hover your mouse over the left margin, and you'll see a red dot. Click on the red dot to insert the breakpoint.

      When we start debugging, the execution stops right at the line where we place the breakpoint.

      From the point where we place the breakpoint onward, we can execute our code line by line.

  4.  **`Now let's go to the debug panel`**: I assume you're using VSCode as your code editor. In the left panel, hover your mouse over the fourth logo, and you should see the text 'Run and Debug' after hovering. Click on it.

      - You should see the option to '`Create a launch.json file.`' Click on it, and a dropdown menu will appear on your screen. Select '`Node.js`'. This action will create a new file called `launch.json` in your project.

        And this is the content of launch.json looks like:

        ```json
        {
          // Use IntelliSense to learn about possible attributes.
          // Hover to view descriptions of existing attributes.
          // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
          "version": "0.2.0",
          "configurations": [
            {
              "type": "node",
              "request": "launch",
              "name": "Launch Program",
              "skipFiles": ["<node_internals>/**"],
              "program": "${workspaceFolder}/src/index.ts",
              "outFiles": ["${workspaceFolder}/**/*.js"]
            }
          ]
        }
        ```

        This is our launch.json file containing configurations that instruct VSCode on how to debug the application.

        ```json
        "type": "node",
        "request": "launch",
        ```

        This line telling that we're going to use node to launch this program.

        ```json
        "program": "${workspaceFolder}/src/index.ts",
        "outFiles": ["${workspaceFolder}/**/*.js"]
        ```

        Our program begins here. In the source folder, you'll find 'index.ts,' and the output files are stored in our project workspace as files with the 'js' extension.

        **`NOW`** we need to add one more setting called 'preLaunchTask' Set this between the 'program' and 'outFiles' configurations.

        Like this:

        ```json
        "program": "${workspaceFolder}/src/index.ts",
        "preLaunchTask": "tsc: build - tsconfig.json",
        "outFiles": ["${workspaceFolder}/**/*.js"]
        ```

        With this setting, we instruct VSCode to utilize the TypeScript compiler for building our application, utilizing the TypeScript configuration file.

  5.  **`Let's go back to any.ts`**:

      - To start debugging:

        - We can go to the debug panel and click on `Launch Program` or use the shortcut by pressing f5.
        - After pressing it, our program started, and the execution stopped right at the line where we set the breakpoint.
        - On the top, we have a bunch of tools for executing our code.

          we have:

          - **`Step Over`**: For executing 1 line.
          - **`Step Into`**: We are stepping into a function. If you don't have functions in your code currently, this feature may not be useful.
          - **`Step Out`**: This is useful for stepping out to the function.
          - **`restart`**
          - **`Stop`**

          In the tooltip, if you hover over each tool, you can see its corresponding shortcut.

        - The shortcut for stepping over a line is f10, let's press that. The 2nd line of the code was executed.

        - Now on the left panel, under `VARIABLES`, you can see all the variables that are detected in the debugging session. So under `Local` we have age that is set to 20. As we execute each line you'll see the value of this variable getting updated.
        - If there's something that you don't see in the in the `variables window`, you can go to the `watch window` and insert a watch.

        - We're going to watch the '`age`' variable, and its current value is 20.

        - Let's step over the line by pressing F10. Now, we're on the next line.

        - let's step over again. The age code updated but because program terminated, we don't see its value anymore.

        - But if you add one extra line on the code, let say:

          ```typescript
          let age: number = 20;

          if (age < 50) age += 10;
          console.log(age);
          ```

          then let's start the debugging one more time by pressing f5.

        - step over 3 times, and now age is 30.

- This is how debugging a TypeScript application works in VSCode. It's very useful when things go wrong as we can start debugging our program and execute it line by line.
