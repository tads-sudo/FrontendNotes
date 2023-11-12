# Configuring the TypeScript Compiler

- Configuring the TypeScript compiler involves creating a `tsconfig.json` file that contains the compiler options for your TypeScript project.

- This file helps TypeScript understand how to transpile your TypeScript code into JavaScript.

- Here are the steps to configure the TypeScript compiler:

  1. **`Initialize TypeScript in your project`**:

     - If you don't have TypeScript installed, you can install it globally using:

       ```
       npm install -g typescript
       ```

     - Then, navigate to your project directory and run:

       ```
       tsc --init
       ```

       This command creates a tsconfig.json file with default settings.

  2. **`Edit tsconfig.json file`**:

     - Open the tsconfig.json file in your text editor. This file contains various options that control how the TypeScript compiler behaves.

       Here are some common settings:

       - **`compilerOptions`**: This section allows you to configure how TypeScript compiles your code.

         Some important options include:

         - **`target`**: Specifies the ECMAScript target version. For example, "es5", "es6", "es2017", etc.
         - **`module`**: Defines the module system to use. Common choices are "commonjs", "es2015", "amd", etc.
         - **`rootDir`**: Specifies the root directory of input files. TypeScript will consider files under this directory when compiling.
         - **`outDir`**: Specifies the directory where the compiled JavaScript files should be placed.

       - **`strict`**: Enforces strict type checking. Setting "strict": true is recommended for better type safety.

  3. **`Compile TypeScript`**:

     - Run the TypeScript compiler using the following command:

       ```
       tsc
       ```

       This command will compile your TypeScript files according to the settings in the tsconfig.json file.

  4. **`Watch mode`**:

     - To automatically recompile your TypeScript code when changes are made, you can use the watch mode:

       ```
       tsc -w
       ```

       This will watch for changes in your TypeScript files and recompile them automatically.

- Adjust the tsconfig.json settings based on your project requirements. The TypeScript documentation https://www.typescriptlang.org/tsconfig provides detailed information about all available compiler options.
