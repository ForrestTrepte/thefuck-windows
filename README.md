# thefuck-windows
Setup [nvbn/thefuck](https://github.com/nvbn/thefuck) on windows for PowerShell.

## Run the installation
Prequisites: [install python and pip](https://www.python.org)

Start PowerShell as Administrator

Run `.\install-powershell.ps1`

## Troubleshooting
You may run into the following error:
```
.\install.ps1 : File thefuck-windows\install.ps1 cannot be loaded because running scripts is disabled on
this system. For more information, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.
At line:1 char:1
+ .\install.ps1
+ ~~~~~~~~~~~~~
    + CategoryInfo          : SecurityError: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess
```
To fix this, change your execution policy:
    
    `Set-ExecutionPolicy Unrestricted -Scope CurrentUser`

    Change the execution policy for the current user, because it's also needed to load the `Microsoft.PowerShell_profile.ps1` script.
