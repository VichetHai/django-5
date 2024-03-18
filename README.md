# django-5

# VS-Code Configs

Create a folder named is to .vscode and add some files below:

- Create a file name "settings.json" for config vscode.

```
{
    "better-comments.highlightPlainText": true,
    "autoimport.autoComplete": true,
    "bladeFormatter.format.enabled": true,
    "donjayamanne.python-extension-pack": true,
    "blade.format.enable": false,
    "editorconfig.generateAuto": false,
    "indentRainbow.colorOnWhiteSpaceOnly": true,
    "sonarlint.connectedMode.project": {
        "connectionId": "https-sonar-wingmoney-com-9000",
        "projectKey": "wing_digital_api"
    }
}
```

- Create a file name "launch.json" fo launch services and bug.

```
    {
    "version": "0.2.0",
    "configurations": [
        {
            "name": "api debug",
            "type": "debugpy",
            "request": "launch",
            "program": "${workspaceFolder}\\manage.py",
            "args": [
                "runserver"
            ],
            "django": true,
            "justMyCode": true
        },
        {
            "name": "api service",
            "command": "venv && py manage.py runserver",
            "request": "launch",
            "type": "node-terminal"
        },
        {
            "name": "web service",
            "command": "cd /d/wingdigital/wing_digital_web && npm run dev",
            "request": "launch",
            "type": "node-terminal"
        },
        {
            "name": "web dev",
            "command": "cd /d/wingdigital/wing_digital_web && git checkout dev && git fetch --prune && git pull && npm run ilc",
            "request": "launch",
            "type": "node-terminal"
        },
        {
            "name": "web uat",
            "command": "cd /d/wingdigital/wing_digital_web && git checkout uat && git fetch --prune && git pull && npm run ilc",
            "request": "launch",
            "type": "node-terminal"
        },
        {
            "name": "web master",
            "command": "cd /d/wingdigital/wing_digital_web && git checkout master && git fetch --prune && git pull && npm run ilc",
            "request": "launch",
            "type": "node-terminal"
        }
    ]
}
```

- Create a file name "extensions.json" for recommendation extensions.

```
{
    "recommendations": [
        "aaron-bond.better-comments",
        "donjayamanne.python-extension-pack",
        "steoates.autoimport",
        "alefragnani.bookmarks",
        "streetsidesoftware.code-spell-checker",
        "dracula-theme.theme-dracula",
        "oderwat.indent-rainbow",
        "visualstudioexptteam.vscodeintellicode",
        "visualstudioexptteam.intellicode-api-usage-examples",
        "alexcvzz.vscode-sqlite",
        "cardinal90.multi-cursor-case-preserve",
        "njpwerner.autodocstring",
        "pkief.material-icon-theme",
        "ms-python.vscode-pylance",
        "ms-python.debugpy",
        "donjayamanne.python-environment-manager",
        "kevinrose.vsc-python-indent",
        "sonarsource.sonarlint-vscode",
        "ms-python.black-formatter",
        "batisteo.vscode-django",
        "usernamehw.errorlens",
        "eamodio.gitlens",
        "yzhang.markdown-all-in-one",
        "rangav.vscode-thunder-client",
        "wholroyd.jinja"
    ]
}
```