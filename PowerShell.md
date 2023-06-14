# PowerShell Cheat Sheet

This is a WIP and not complete yet...

## Basics

|Command|Description|
|:---|:---|
|```$PSVersionTable```|Prints a table with your current PowerShell's version information.|

## Environment Variables

Note that environment variables are _not_ case sensitive in Windows.

|Command|Description|
|:---|:---|
|```dir Env:```|Prints out all environment variables. (Not case sensitive)|
|```[System.Environment]::GetEnvironmentVariables()```|Prints out all the environment variables using the .NET function ```GetEnvironmentVariables()``` inside the ```System.Environment``` class. |

## Formatting

|Command|Description|
|:---|:---|
|```Format-Table```|Formats output of a command as a table with selected properties of the object in each column. Use the **Property** parameter to select the properties you want to display. |

Example: to display all environment variables with line-wrapping:

```powershell
dir Env: | Format-Table -Wrap
```

Output (showing only a few environment variables; in real-life, this list would be a lot bigger):

```powershell
Name                           Value
----                           -----
ALLUSERSPROFILE                C:\ProgramData
COLORTERM                      truecolor
CommonProgramFiles             C:\Program Files\Common Files
CommonProgramFiles(x86)        C:\Program Files (x86)\Common Files
CommonProgramW6432             C:\Program Files\Common Files
COMPUTERNAME                   MSI
ComSpec                        C:\WINDOWS\system32\cmd.exe
configsetroot                  C:\WINDOWS\ConfigSetRoot
DriverData                     C:\Windows\System32\Drivers\DriverData
GIT_EDITOR                     "c:\Users\<username>\AppData\Local\Programs\Microsoft VS Code\resources\app\extensions\git\dist\git-editor.sh"
NUMBER_OF_PROCESSORS           12
OS                             Windows_NT
```

Notice how the value for GIT_EDITOR was fully displayed by PowerShell instead of cutting off the text with an ellipses "..." at the end of the line.

Another example (choosing properties to display):

```powershell
Get-Service | Format-Table -Property Name, Status, DisplayName
```

Output (showing only first few lines):

```powershell
Name                       Status  DisplayName
----                       ------  -----------
AarSvc_168460              Stopped Agent Activation Runtime_168460
AJRouter                   Stopped AllJoyn Router Service
ALG                        Stopped Application Layer Gateway Service
AppIDSvc                   Stopped Application Identity
Appinfo                    Running Application Information
```

Advanced example (adding your own calculated values to the table):

```powershell
 Get-Process chrome | Format-Table ProcessName, @{Label="TotalRunningTime"; Expression={(Get-Date) - $_.StartTime}} 
```

Output:

```powershell
ProcessName TotalRunningTime
----------- ----------------
chrome      01:29:19.3938160
chrome      1.16:52:19.0100961
```
