# How to set up your Windows PC using this repo

## Prerequisites

Make sure you have [Chocolatey](https://chocolatey.org/) installed on your system. Chocolatey serves as a package manager for Windows, streamlining the installation process of various software packages. You can confirm its installation status by accessing PowerShell and executing the command choco. If Chocolatey is not installed, execute the following command in PowerShell with administrative privileges:
```bash
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
By executing this command, Chocolatey will be installed on your system, enabling seamless software management.
> [!TIP]
> To optimize the installation process and automate responses to prompts, you have the option to enable a feature within Chocolatey. This feature allows for automatic acceptance of prompts by typing "y." Execute the following command in PowerShell to activate this feature:
> ```bash
> choco feature enable -n=allowGlobalConfirmation
> ```
## Getting started

Once the prerequisites are in place, you can initiate the installation process for the desired package using Chocolatey. Follow these steps meticulously:
1. Open PowerShell as an administrator.
2. Create a directory `C:\choco-packages\SAY10s-PC` on your disk.
```bash
mkdir C:\choco-packages\SAY10s-PC
```
3. Download the [SAY10s-PC.nupkg](https://github.com/SAY10s/PC-Setup/blob/main/SAY10s-PC.1.0.0.nupkg) file from the repository and place it within the newly created directory (C:\choco-packages\SAY10s-PC).
4. Execute the installation command in PowerShell to install the applications contained within the package. Utilize the following command:
```bash
choco install SAY10s-PC --version="1.0.0" --source="C:\choco-packages\SAY10s-PC;https://community.chocolatey.org/api/v2/"
```
5. There you go! You've successfully installed all basic apps.
