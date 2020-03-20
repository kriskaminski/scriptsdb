


```PowerShell
(Get-ItemProperty "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion")
```
```
## Output

SystemRoot                : C:\Windows
BaseBuildRevisionNumber   : 1
BuildBranch               : 19h1_release
BuildGUID                 : ffffffff-ffff-ffff-ffff-ffffffffffff
BuildLab                  : 18362.19h1_release.190318-1202
BuildLabEx                : 18362.1.amd64fre.19h1_release.190318-1202
CompositionEditionID      : Enterprise
CurrentBuild              : 18362
CurrentBuildNumber        : 18362
CurrentMajorVersionNumber : 10
CurrentMinorVersionNumber : 0
CurrentType               : Multiprocessor Free
CurrentVersion            : 6.3
EditionID                 : Professional
EditionSubManufacturer    :
EditionSubstring          :
EditionSubVersion         :
InstallationType          : Client
InstallDate               : 1570805003
ProductName               : Windows 10 Pro
ReleaseId                 : 1903
SoftwareType              : System
UBR                       : 657
PathName                  : C:\Windows
ProductId                 : 00330-80000-00000-AA393
DigitalProductId          : {164, 0, 0, 0...}
DigitalProductId4         : {248, 4, 0, 0...}
RegisteredOwner           : Krzysiek
RegisteredOrganization    :
InstallTime               : 132152786032380421
PSPath                    : Microsoft.PowerShell.Core\Registry::HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Curren
                            tVersion
PSParentPath              : Microsoft.PowerShell.Core\Registry::HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT
PSChildName               : CurrentVersion
PSDrive                   : HKLM
PSProvider                : Microsoft.PowerShell.Core\Registry
```
## Just build number 
``` PowerShell
(Get-ItemProperty "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion").BuildLabEx -match '^[0-9]+\.[0-9]+' |  % { $matches.Values }
```
## Reference 
[Stack Overflow Reference](https://stackoverflow.com/a/40350410)


