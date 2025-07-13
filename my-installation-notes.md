## my notes of installation from scratch

0. install wsl2 using powershell as admin
- `wsl install`
1. install from microsoft store or install a container using `wsl install ubuntu` from powershell 
2. clone this repo under windows-host
- at `/User/Erick/github/erick4j`
3. from container, link the folder
- run `ln -s /mnt/c/Users/Erick/github ~/github`
4. in vscode open/add project using container path
- `/home/user-erick/github`
5. (optional) install `uv` for fast Python dependency management
- `pip install uv`
6. configure VS Code to use `uv` for Python dependencies:
   - Open VS Code settings (`Ctrl+,`)
   - Search for "Python: Terminal Activate Environment"
   - Ensure it's enabled
   - Use the terminal to run `uv pip install -r requirements.txt` instead of `pip install -r requirements.txt`
   - For tasks, update your `.vscode/tasks.json` to use `uv pip` commands