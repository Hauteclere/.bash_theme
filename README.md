# New Computer Setup Log
1. Install Chrome
2. Install LastPass Chrome extension
3. Secure local admin permissions
4. Install WSL by running the command `wsl --install` in Powershell (open as administrator)
5. Update packages with `sudo apt update && sudo apt upgrade`
6. Install Windows Terminal
7. Install VS Code and WSL remote extension: https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode
    - You will need to sort out your other extensions later, but that's up to you
9. Install Homebrew: https://brew.sh/
    - Be careful to follow the post-install instructions including:
        - add brew to the PATH
        - install dependencies
        - install GCC
        - While you're at it, might as well install wget: `brew install wget`
