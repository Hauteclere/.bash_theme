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
10. Install the OhMyPosh CLI themer: `brew install jandedobbeleer/oh-my-posh/oh-my-posh`
    - You also need a Nerd Font. I recommend `ComicShannsMono`, but the OhMyPosh folks recommend `Meslo LGM NF`. Either way, install one with `oh-my-posh font install` (selecting the font of your choice from the menu)
11. Set up Git: https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-git
    - `sudo apt-get install --upgrade git`
    - `git config --global user.name "Your Name"`
    - `git config --global user.email "youremail@domain.com"`
    - Install Git for Windows (linked in the above page). You need to select the correct options here, but it's all the kind of stuff you'd expect. **Recommend doing this as admin!**
    - Link your Linux Git instance to the Windows GCM. The path may depend on what version of Git you have and whether or not you installed it as Admin. For instance, I am a doofus and failed to install Git as admin, so mine ended up here: `git config --global credential.helper "/mnt/c/Users/lavers/Appdata/Local/Programs/Git/mingw64/bin/git-credential-manager.exe"`
12. Clone down this repo!
13. Add the following line to the end of your `.bashrc`: `eval "$(oh-my-posh init bash --config ~/.bash_theme/bash_theme.json)"`
14. Reload your profile: `exec bash`
15. The font will be broken - symbols will be failing to render. To fix this:
    - Download the font you've chosen from the Nerd Fonts website
    - Unzip it
    - Right click on the `.otf` file and select `Install`
    - Open the `settings.json` for your Windows Terminal program
    - Under `"profiles"` -> `"defaults"`, add the following structure:
        ```json
            "font": {
                "face": "ComicShannsMono Nerd Font Mono"
            }
        ```
    - Open a new bash terminal window in Windows Terminal to check it worked.
16. Install Pyenv: `brew install pyenv`
17. Add the following line to your `.bashrc`: `eval "$(pyenv init --path)"` (and restart your bash terminal)
18. Install the latest Python with `pyenv install` 
    -  Run `pyenv --version` to see what version of Python is currently active for you. You may need to set the version you just installed to the global default with `pyenv global 3.10` (Subbing in correct version number).
19. Install postgres with: `sudo apt install postgresql postgresql-contrib`
20. Set postgres password with `sudo passwd postgres` 