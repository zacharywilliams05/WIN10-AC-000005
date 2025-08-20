# STIG-Implementation-WIN10-AC-000005
STIG Implementation WIN10-AC-000005

# WIN10-AC-000005
STIG Implementation WIN10-AC-000005

<#
.SYNOPSIS
    This PowerShell script sets the lockout duration to 15 minutes.

.NOTES
    Author          : Zachary Williams
    LinkedIn        : linkedin.com/in/zacharywilliams05/
    GitHub          : github.com/zacharywilliams05
    Date Created    : 2025-08-20
    Last Modified   : 2024-08-20
    Version         : 1.0
    CVEs            : N/A
    Plugin IDs      : N/A
    STIG-ID         : WIN10-AC-000005

.TESTED ON
    Date(s) Tested  : 
    Tested By       : 
    Systems Tested  : 
    PowerShell Ver. : 

.USAGE
    PS C:\> .\__remediation_template(STIG-ID-WIN10-AC-000005).ps1 
#>

```powershell
# Note: You may need to change your execution policy to RemoteSigned before running this script.
# You can do this by running the following command in an elevated PowerShell session:
# Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

# After running the script, you can revert the execution policy back to Restricted by using:
# Set-ExecutionPolicy Restricted -Scope CurrentUser

# Change the lockout duration to 15 minutes using net accounts
$lockoutDuration = 15

# Execute the net accounts command
net accounts /lockoutduration:$lockoutDuration

# Provide feedback to the user
Write-Host "Lockout duration has been set to $lockoutDuration minutes."
```
