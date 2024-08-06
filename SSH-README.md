# Installing and Configuring SSH on Windows

## 1. Installing OpenSSH Client on Windows

### Using Windows Settings:
1. **Open Windows Settings:**
   - Press `Win + I` to open Settings, or click on the Start menu and select the gear icon.

2. **Navigate to Apps:**
   - In the Settings window, go to `Apps`.

3. **Manage Optional Features:**
   - Click on `Optional features`.

4. **Add a feature:**
   - Click on `Add a feature` at the top of the Optional features page.

5. **Install OpenSSH Client:**
   - Scroll down the list and find `OpenSSH Client`.
   - Select `OpenSSH Client` and click `Install`.

### Using PowerShell:
1. **Open PowerShell as an Administrator:**
   - Right-click on the Start menu and select `Windows PowerShell (Admin)`.

2. **Install OpenSSH Client:**
   ```powershell
   Add-WindowsCapability -Online -Name OpenSSH.Client*
   ```

## 2. Verifying the Installation

1. **Check SSH version:**
   - Open Command Prompt or PowerShell and type:
     ```powershell
     ssh -V
     ```
   - This should display the version of OpenSSH installed.

## 3. Configuring ssh-agent

1. **Start the ssh-agent service:**
   - Open PowerShell as an Administrator and run:
     ```powershell
     Start-Service ssh-agent
     ```

2. **Configure the service to start automatically:**
   - This ensures that `ssh-agent` starts on system boot.
     ```powershell
     Get-Service ssh-agent | Set-Service -StartupType Automatic
     ```

3. **Add your SSH key to ssh-agent:**
   - Ensure you have an SSH key. If you don't, generate one:
     ```powershell
     ssh-keygen
     ```
   - Add the generated key (or an existing one) to `ssh-agent`:
     ```powershell
     ssh-add C:\Users\yourusername\.ssh\id_rsa
     ```

