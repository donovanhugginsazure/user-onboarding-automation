# User Onboarding Automation Script

## Business Case
Manually creating user accounts during client onboarding is inefficient and prone to typos. This PowerShell script automates local user creation, standardizes username formats, assigns descriptions, and generates a centralized deployment log. It cuts onboarding time down by 90% and ensures perfect data consistency for MSP documentation.

## 🛠️ Technologies Used
* **Language:** PowerShell (v5.1+)
* **Modules:** Microsoft.PowerShell.LocalAccounts
* **Concepts:** Error handling (`try/catch`), logging loops, automation variables.

## 🚀 How to Run and Test This Project
1. Open PowerShell as an **Administrator**.
2. Clone this repository or copy the `OnboardUsers.ps1` script to your machine.
3. Run the script:
   ```powershell
   .\OnboardUsers.ps1
   ```
4. Verify the creation of accounts:
   ```powershell
   Get-LocalUser | Where-Object {\$_.Description -like "*Helpdesk*"}
   ```
5. Check the newly generated `C_OnboardingLog.txt` file in the same directory to view the success and error logs.

## 🧠 Key Learnings
* Developed robust script error handling using `try/catch` blocks to prevent script failure during batch processing.
* Learned how to generate administrative audit trails by piping runtime logs directly to external text files.
