# 🖥️ Windows 11 Virtual Machine

> A Windows 11 Virtual Machine with all the essential tools pre-installed, accessible from **Android, Windows, macOS, and Linux**.

---

## ✨ Features

- 🌍 Works on almost every device and operating system
- 📱 No PC required
- 🛠️ Essential tools are already installed
- ⚡ Quick and easy setup
- ☁️ Access your VM from anywhere using a web browser

---

## 📋 Requirements

Before getting started, make sure you have:

- 🔑 GitHub Account
- 📧 Google Account
- 🌐 Any modern web browser
- 🛜 Stable internet connection
- 🖥️ [Chrome Remote Desktop](https://remotedesktop.google.com/access/)

---

## 🚀 How to Use This VM

Follow these steps carefully to set up and access your Windows 11 Virtual Machine.

### 1. Create a GitHub Account
- Go to [https://github.com](https://github.com) and sign up for a free account if you don’t already have one.
- Verify your email address.

### 2. Fork This Repository
1. Open this repository: [https://github.com/GameHavenX94/windows11](https://github.com/GameHavenX94/windows11)
2. Click the **Fork** button at the top-right corner of the page.
3. Select your account as the destination.
4. Wait until the fork is complete. You will now have your own copy of the repository under your GitHub username.

### 3. Enable GitHub Actions (Workflows)
1. Go to **your forked repository**.
2. Click the **Actions** tab at the top.
3. If you see a banner saying workflows are disabled, click **I understand my workflows, go ahead and enable them**.
4. This allows the Win11 workflow to run on your fork.

### 4. Adjust GitHub Actions Settings (Recommended)
To prevent the workflow from stopping too early and to keep logs longer:

1. In your forked repository, go to **Settings** → **Actions** → **General**.
2. Under **Workflow permissions**, make sure **Read and write permissions** is selected (if available).
3. Scroll to **Artifact and log retention** (or similar retention setting) and set it to the maximum allowed (usually **90 days** for public repos).
4. Save the changes.

> **Note:** The workflow itself is configured with a very long timeout so the VM can stay running. Setting a longer retention helps you keep the run logs.

### 5. Get the Chrome Remote Desktop (CRD) PowerShell Code
1. Open [Chrome Remote Desktop – Headless Setup](https://remotedesktop.google.com/headless) in your browser.
2. Sign in with the **same Google Account** you will use to connect later.
3. Click **Begin** → **Next** → **Authorize**.
4. On the next page you will see several command lines.  
   **Copy the Windows (PowerShell) command**. It looks similar to this:

   ```powershell
   & "${Env:PROGRAMFILES(X86)}\Google\Chrome Remote Desktop\CurrentVersion\remoting_start_host.exe" `
   --code="4/XXXX..." `
   --redirect-url="https://remotedesktop.google.com/_/oauthredirect" `
   --name=$Env:COMPUTERNAME
   ```

### 6. Run the Win11 Workflow
1. In your forked repository, go to the **Actions** tab.
2. In the left sidebar, click **Win 11** (or the workflow named “Win 11”).
3. Click the **Run workflow** button (usually on the right).
4. In the input field labeled **Paste Powershell Code**, paste the full CRD PowerShell command you copied earlier.
5. Click **Run workflow**.

### 7. Wait for the VM to Start
- The workflow will start running.  
- First it downloads essential files (this can take a few minutes).  
- Then it starts the Chrome Remote Desktop host with PIN **123456**.  
- After approximately **3–7 minutes**, the VM should be ready.

You can watch the progress in the **Actions** log. Look for the step “Starting Virtual Machine…”.

### 8. Connect to Your Windows 11 VM
1. Open [Chrome Remote Desktop Access](https://remotedesktop.google.com/access/) in any browser (phone, tablet, PC, etc.).
2. Sign in with the **same Google Account** you used to generate the CRD code.
3. You should see a new remote computer appear (usually named after the GitHub runner).
4. Click it and enter the PIN / password:

   **PIN / Password: `123456`**

5. You are now connected to your Windows 11 Virtual Machine!

### Important Notes
- The VM runs on a GitHub Actions Windows runner and will stay online as long as the workflow is running.
- Do **not** cancel the workflow while you are using the VM.
- When you are finished, you can cancel the workflow from the Actions tab to free the runner.
- This is intended for **personal and educational use only**.

---

## ⚠️ Important Notice

- This repository is intended for **personal and educational use only**.
- Do **not** use it for illegal, abusive, or unauthorized activities.
- Please **do not re-upload, sell, or redistribute** this repository without permission from the author.
- If you would like to create a YouTube video featuring this repository, please contact the author first.

---

## 📞 Contact & Support

If you need help or want to report a problem:

- 🐞 **[GitHub Issues](https://github.com/GameHavenX94/windows11/issues)**
- 📺 **[YouTube - R_Editrr](https://youtube.com/@r_editr?si=oQLye4RDC7rjRNqr)**
- 💬 **[Telegram Community](https://t.me/join_Random_editrr)**
- 👥 **[Telegram Discussion](https://t.me/r_editrr_gc)**

---

## ❤️ Support the Project

If you find this repository helpful:

⭐ Star the repository

💲 [Buy Us a Coffee ☕](https://donorbox.org/support-r_editrr)

📝 Report bugs and suggest improvements

Your support helps improve the project!
