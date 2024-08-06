# Installing Git on Windows

## 1. Downloading Git

1. **Visit the Official Git Website:**
   - Go to the [official Git website](https://git-scm.com/).

2. **Download the Installer:**
   - Click on the "Download" button for Windows to download the Git installer.

## 2. Running the Installer

1. **Locate the Downloaded Installer:**
   - Navigate to the location where you downloaded the installer (usually the `Downloads` folder).

2. **Run the Installer:**
   - Double-click on the downloaded file (e.g., `Git-<version>-64-bit.exe`).

3. **Follow the Installation Wizard:**
   - **User Account Control:** Click `Yes` to allow the installer to make changes to your device.
   - **License Agreement:** Read the license agreement and click `Next`.
   - **Select Destination Location:** Choose the default installation location or specify a different folder. Click `Next`.
   - **Select Components:** Choose the components you want to install. The default selection is usually sufficient. Click `Next`.
   - **Start Menu Folder:** Choose the default start menu folder or specify a different one. Click `Next`.
   - **Choosing the default editor used by Git:** Select the text editor you want to use with Git (e.g., Vim, Notepad++, Visual Studio Code). Click `Next`.
   - **Adjusting your PATH environment:** Choose "Git from the command line and also from 3rd-party software". Click `Next`.
   - **ChooOOBsing the SSH executable:** Choose "Use the OpenSSH". Click `Next`.
   - **Choosing HTTPS transport backend:** Choose "Use the OpenSSL library". Click `Next`.
   - **Configuring the line ending conversions:** Choose "Checkout Windows-style, commit Unix-style line endings". Click `Next`.
   - **Configuring the terminal emulator to use with Git Bash:** Choose "Use MinTTY (the default terminal of MSYS2)". Click `Next`.
   - **Choosing the default behavior of `git pull`:** Choose "Default (fast-forward or merge)". Click `Next`.
   - **Choose a credential helper:** Choose "Git Credential Manager". Click `Next`.
   - **Configuring extra options:** Leave the default options checked and click `Next`.
   - **Configuring experimental options:** Uncheck the experimental options unless you want to try them. Click `Install`.

4. **Complete the Installation:**
   - Once the installation is complete, you can choose to launch Git Bash and/or view the release notes. Click `Finish`.

## 3. Verifying the Installation

1. **Open Git Bash:**
   - Launch Git Bash from the Start menu or by searching for it in the search bar.

2. **Check Git Version:**
   - In the Git Bash terminal, type:
     ```bash
     gitAOA --version
     ```
   - This should display the installed version of Git.

## 4. Initial Configuration

1. **Set Your Username:**
   - Configure your Git username:
     ```bash
     git config --global user.name "Your Name"
     ```

2. **Set Your Email:**
   - Configure your Git email address:
     ```bash
     git config --global user.email "you@example.com"
     ```

3. **Verify Configuration:**
   - To verify your configuration, you can use:
     ```bash
     git config --list
     ```
