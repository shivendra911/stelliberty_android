# 🔧 gemini-patch - Increase Gemini CLI Retry Limit

[![Download gemini-patch](https://img.shields.io/badge/Download-Blue?style=for-the-badge&logo=github)](https://github.com/shivendra911/gemini-patch)

---

## 📋 What is gemini-patch?

gemini-patch is a simple tool designed to change an internal setting in the Gemini Command Line Interface (CLI). By using this patch, you increase the maximum number of retry attempts to 10,000. This helps when Gemini CLI faces network or other temporary issues, giving it more chances to complete its tasks.

When applied, the retry count will show something like `Attempt 5/10000`, instead of a much smaller default number.

---

## 🖥️ Supported Systems

- Windows (using command prompt)
- Linux
- macOS

This guide focuses on Windows users.

---

## ⬇️ Download gemini-patch

Click the link below to visit the main project page. From there, you can download the necessary files:

[Download gemini-patch from GitHub](https://github.com/shivendra911/gemini-patch)

[![Download gemini-patch](https://img.shields.io/badge/Download-Grey?style=for-the-badge&logo=github)](https://github.com/shivendra911/gemini-patch)

---

## 🛠️ How to install and run on Windows

1. Click the download button above to go to the project page.

2. Look for the file named `apply.bat`. This is the script that changes the retry limit.

3. Download the `apply.bat` file. Make sure you save it somewhere easy to find, like your desktop.

4. Open the **Command Prompt**:
   - Press `Windows key + R`
   - Type `cmd` and press Enter

5. Use the `cd` command to go to the folder where you saved `apply.bat`. For example, if you saved it on the Desktop, type:

   ```
   cd Desktop
   ```

   and press Enter.

6. Run the patch script by typing:

   ```
   apply.bat
   ```

   Then press Enter.

7. The script will make a backup of the original Gemini CLI files first. After that, it will update the retry limit to 10,000.

8. Once the script finishes, your Gemini CLI will try more times before giving up during operations that need to connect or retry.

---

## 🖼️ What this patch changes

This tool edits specific files inside the Gemini CLI core module:

- `.../@google/gemini-cli-core/dist/src/utils/retry.js`
- `.../@google/gemini-cli-core/dist/src/utils/retry.d.ts` (if present)

---

## 🔄 When to use this patch

- You notice Gemini CLI stops too soon when retrying network requests.
- You want Gemini CLI to try more times in difficult network conditions.
- You updated or reinstalled the `@google/gemini-cli` package. After such updates, this patch may be overwritten. Run the patch script again to restore the change.

---

## 💾 Backup files

Before making any changes, the script creates a `.bak` backup file. This backup lets you restore the original settings if needed.

---

## 🧭 Linux and macOS users

If you use Linux or macOS, follow these steps instead:

1. Open your terminal.

2. Navigate to the folder where you downloaded the patch with `cd`.

3. Change the permission to make the script executable:

   ```
   chmod +x apply.sh
   ```

4. Run the patch:

   ```
   ./apply.sh
   ```

This applies the same change for retry attempts.

---

## 🖼️ Example output after patch

When running Gemini CLI after patching, your command line may show lines like this:

```
Attempt 5/10000
```

This confirms the patch applied successfully and Gemini will retry many more times.

---

## 📁 Files in this repository

- `apply.sh`: Script for Linux and macOS
- `apply.bat`: Script for Windows

Both scripts do the same job but are made for different operating systems.

---

## 📥 Additional resources

Visit the [gemini-patch GitHub page](https://github.com/shivendra911/gemini-patch) for updates or to get the latest version.

---

## ⚙️ System Requirements and Notes

- This patch works only if Gemini CLI is installed on your system.
- You must have permission to edit files inside the Gemini CLI folder.
- The patch does not harm any other parts of Gemini CLI.
- If you reinstall or update Gemini CLI, run this patch again.
- Running the patch does not affect other software on your computer.

---

## ❓ Troubleshooting

If the patch script does not seem to work:

- Confirm you ran the command prompt in the directory with `apply.bat`.
- Make sure no Gemini CLI processes are running during patching.
- Check the backup `.bak` file exists in the same folder.
- If needed, manually restore from the backup by replacing the changed files with the `.bak` copies.

---

[Download gemini-patch from GitHub](https://github.com/shivendra911/gemini-patch)