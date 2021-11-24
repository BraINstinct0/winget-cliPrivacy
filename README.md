# winget-cliPrivacy
Winget build without telemetry
If successful will add modifications to further reduce the amount of data sent to MS or any other party

## Noted telemetry/data leaks
* Sending locale (2 letter) to 
## Plans
Steps to follow: [official guide from MS](https://github.com/microsoft/winget-cli#building-the-client)

Difference: if possible, use Github runner ([`windows-2019`](https://github.com/actions/virtual-environments/blob/main/images/win/Windows2019-Readme.md) seems to be adequate)

- [ ] Enable Developer mode? If necessary: ```reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModelUnlock" /t REG_DWORD /f /v "AllowDevelopmentWithoutDevLicense" /d "1"```
- [X] Install Visual Studio 2019 : already has `C:\Program Files (x86)\Microsoft Visual Studio\2019\Enterprise`
- [ ] workload: `.NET Desktop Development` : (probably should look at Chocolatey if missing)
- [ ] workload: `Desktop Development with C++`
- [ ] workload: `UWP Development`
- [ ] extension: `Microsoft Visual Studio Installer Projects`
- [ ] Build process using github actions - should be triggered on new `published` of microsoft/winget-cli ?
