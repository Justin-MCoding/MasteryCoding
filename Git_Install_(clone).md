## Windows Command Prompt vs Linux/macOS Terminal
---
**Windows** runs `Command Prompt (CMD)` and `Powershell` by default. CMD is usually used for routine administrative task and automation. Powershell is an automated command-line shell that includes the functionality of CMD. The biggest difference is that Powershell is object-oriented. _These are proprietary to Windows Operating System._

**Linux/macOS (UNIX)** most run `Bourne Again Shell (BASH)` by defualt. Although not the only command-line interface for UNIX based systems, it is the most common command-line scripting applications.

&nbsp;  
>**These two command interfaces are not the same and are not compatible.**  Current Windows Systems can run a BASH platform by installing the Windows Subsystem for Linux (WSL)_ &nbsp;  &nbsp;  ...see [Install WSL2](https://learn.microsoft.com/en-us/windows/wsl/install)
  
&nbsp;  
## Installing Git via BASH Terminal
---
The most common way to use Git is from UNIX terminal. This allows the user to turn their directory into a **_repository_** (or repo) that allows the user to track changes to a project. 

This section we will install Git (if necessary) and do some one-time configuration.

Use the terminal window to see if Git is already installed.
```
[~]$ which git
/usr/local/bin/git
```

If the result is empty or if it says the command is not found, it means you have to install Git manually. To do this, follow the instructions at [Getting Started - Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  
&nbsp;  
## Verifying the Version
---
The next step is to make sure you have a sufficient version of Git installed, which you can check as follows:
```
[~]$ git --version
git version 2.31.1    # version needs to be at least 2.28.0
```
If the version isn't updated you can follow the [Getting Started - Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) or the following if running a different environment:

&nbsp;  
>**Cloud IDE:** &nbsp; &nbsp; ..._see Git_Install\_\(AWSCloud9)_
```
[~]$ sudo apt update
[~]$ sudo apt upgrade
[~]$ sudo apt autoremove
```

&nbsp;  
>**macOS:**
```
[~]$ brew upgrade git
```

&nbsp;  
>**ChromeOS:**
Follow the Linux instructions after turning on `Linux Developers Environment` (Settings >> Advanced >> Developers >> Turn On)  
... or setup a Cloud IDE using **AWS Cloud9 IDE**

&nbsp;  
## One-Time Global Configuration
---
After installing Git, but before you start your first project you need to run some one-time configurations:
```
[~]$ git config --global user.name <Name>
[~]$ git config --global user.email <email@example.com>
[~]$ git config --global init.defaultBranch main
```
The first two commands allow Git to identify changes in your projects by name and email address, which can be helpful when collaborating with others on projects.

The third command sets the default Git branch name to main, which is the current recommended default. The previous default for the last 15+ years was **_master_** so you may encounter that as well.
  
&nbsp;  
## Creating a Repository Folder
---
Now it's time to start creating a project and put it under **_version control_** with Git.

_For the example we will be setting up a simple website project._
```
[~]$ mkdir repos/
[~]$ cd repos/
[repos]$ 
```
  
&nbsp;  
## Creating a GitHub Account
---
If you don't already have a GitHub account, you can get started by visiting [GitHub](https://github.com/join) and following the instructions.
  
&nbsp;  
## Creating a New Repository
---
1. Click the  `"+" sign` next to your Account Picture.
2. Fill in a repository (repo) name. (i.e "website")
3. Fill in a brief description. (i.e. "A sample website.")
4. Select it as `Public`
5. Check the box `Initialize this repository with a README`
6. Click the button to  `Create Repository`
 
&nbsp;  
## Clone Remote GitHub Repository
---
1. From your GitHub account, click the small downward arrow on the right-side of the green button called `Clone or download` above your repository.
2. Click `Use HTTPS` link to get the URL of your Git repository and copy it to your clipboard.
3. Go back to the terminal and run the following:
```
$ git clone https://github.com/<user>/website.git
```
   
&nbsp;  
## Clone Remote GitHub Repository
---
Use these commands to push the new content to the repo (i.e. website) from the terminal.
```
[website (main) ]$ git add -A
[website (main) ]$ git commit -am "<notes>"
[website (main) ]$ git push
```
The first command adds any new content, the second command commits the added/modified content to the repo with a description, and the final command sends the content to GitHub. 
&nbsp;  
> **NOTE:** _When running the final command you will be prompted to enter your username and password. The username is your GitHub username, but the password is not your GitHub password. Instead it is a **personal access token** you have to create. Use the following resource if you need help. [Creating a Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token). Follow the instructions for **Creating a personal access token (classic)**. Make sure to select `no expiration` and `repo` as the scope._