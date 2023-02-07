## Cloud-Based IDE (AWS Cloud9)
---
AWS Cloud9 is a cloud-based integrated development environment (IDE) that lets you write, run, and debug your code with just a browser. It includes a code editor, debugger, and terminal. Cloud9 comes prepackaged with essential tools for popular programming languages, including JavaScript, Python, PHP, and more, so you don’t need to install files or configure your development machine to start new projects. Since your Cloud9 IDE is cloud-based, you can work on your projects from your office, home, or anywhere using an internet-connected machine. Cloud9 also provides a seamless experience for developing serverless applications enabling you to easily define resources, debug, and switch between local and remote execution of serverless applications. With Cloud9, you can quickly share your development environment with your team, enabling you to pair program and track each other's inputs in real time.

[AWS Cloud9 IDE](https://aws.amazon.com/cloud9/)

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
## Update / Upgrade the AWS Cloud9 IDE
---
1. Right-click your **_root folder_** and select the option to `Open Terminal Here`
2. In the terminal type the following:
```
$ sudo apt update
$ sudo apt upgrade
$ sudo apt autoremove
```
If at anytime you get a prompt asking **"Do you want to continue"**, type `Y` and press `Enter`.
  
&nbsp;  
## Install Git on the AWS Cloud9 IDE
---
1. Right-click your **_root folder_** and create a **_new directory_** folder (i.e. website).
2. In the terminal type the following:
```
$ cd website
$ git --version
$ git config --global user.name <Name>
$ git config --global user.email <email@example.com>
```
 
&nbsp;  
## Clone Remote GitHub Repository
---
1. From your GitHub account, click the small downward arrow on the right-side of the green button called `Clone or download` above your repository.
2. Click `Use HTTPS` link to get the URL of your Git repository and copy it to your clipboard.
3. Go back to the terminal and run the following:
```
$ git clone https://github.com/<user>/website.git
```