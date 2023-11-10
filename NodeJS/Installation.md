# Installing Node.js

- To install Node.js, you can follow these general steps. The process may vary slightly depending on your operating system.

  **`Windows`**:

  1. **Download Node.js**:

     - Visit the official Node.js website at [https://nodejs.org/en](https://nodejs.org/en)
     - Click on the "LTS" version (recommended for most users) or "Current" version if you want the latest features.

  2. **Run the Installer**:

     - Once the download is complete, run the installer.
     - Follow the on-screen instructions. The installer will guide you through the process.

  3. **Verify Installation**:

     - Open a command prompt or PowerShell window.
     - Type _node -v_ and press Enter. This should display the installed Node.js version.
     - Type _npm -v_ and press Enter. This should display the installed npm (Node Package Manager) version.

  **`macOS`**:

  1.  **Using Homebrew**:

      - Open Terminal.
      - If you don't have Homebrew installed, you can install it by following the instructions at https://brew.sh/
      - Once Homebrew is installed, run the following commands:

        ```terminal
        brew update
        brew install node
        ```

  2.  **Verify Installation**:

      - Open a terminal window.
      - Type _node -v_ and press Enter. This should display the installed Node.js version.
      - Type _npm -v_ and press Enter. This should display the installed npm version.

  **`Linux (Ubuntu/Debian)`**:

  1. **Using Package Manager**:

     - Open a terminal.
     - Update your package manager's repository information: _sudo apt update_
     - Install Node.js and npm: _sudo apt install nodejs npm_

  2. **Verify Installation**:
     - Open a terminal.
     - Type _node -v_ and press Enter. This should display the installed Node.js version.
     - Type _npm -v_ and press Enter. This should display the installed npm version.
