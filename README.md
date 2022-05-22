# Run OpenVSCode Server on Google Cloud Shell

Install and start [OpenVSCode Server](https://github.com/gitpod-io/openvscode-server) on [Google Cloud Shell](https://cloud.google.com/shell/).

Google Cloud Shell is available at no additional cost for Google Cloud customers and zou get 5 GB of persistent storage.

## 1. Open

Start Google Cloud Shell:

[![Open in Cloud Shell](https://gstatic.com/cloudssh/images/open-btn.png)](https://shell.cloud.google.com/cloudshell/open?cloudshell_git_repo=https://github.com/Cyclenerd/google-cloud-shell-vscode&cloudshell_git_branch=master&cloudshell_tutorial=cloud-shell-tutorial.md)

## 2. Download

Download `code.sh` script:
```bash
curl -O "https://raw.githubusercontent.com/Cyclenerd/google-cloud-shell-vscode/master/code.sh"
```

## 3. Install

Install latest OpenVSCode Server:
```bash
bash code.sh install
```

## 4. Start

Start OpenVSCode Server:
```bash
bash code.sh
```

Open web preview URL:

![Screenshot: Open web preview](./img/google-cloud-shell-open-web-preview.jpg?v1)

![Screenshot: OpenVSCode Settings](./img/openvscode-settings.jpg)

Edit settings (<kbd>Ctrl</kbd> + <kbd>,</kbd>):
```json
{
    "telemetry.enableTelemetry": false,
    "editor.minimap.enabled": false,
    "editor.renderWhitespace": "all",
    "editor.renderControlCharacters": true,
    "editor.fontSize": 14,
    "editor.fontFamily": "'Source Code Pro Medium', 'Source Code Pro', Monaco, 'Courier New', monospace",
    "workbench.colorTheme": "Dracula",
    "editor.acceptSuggestionOnEnter": "smart",
    "workbench.startupEditor": "newUntitledFile",
    "files.eol": "\n",
    "git.enableSmartCommit": true,
    "terminal.integrated.defaultProfile.linux": "tmux",
    "extensions.ignoreRecommendations": true,
    "git.ignoreMissingGitWarning": true,
    "workbench.editor.enablePreview": false,
    "problems.decorations.enabled": false,
    "html.autoClosingTags": false,
    "diffEditor.ignoreTrimWhitespace": false
}
```

## Usage

Help:
```bash
bash code.sh help
```

```text
Usage: code.sh [COMMAND]
COMMAND is one of the following:
        install - install latest OpenVSCode Server
        upgrade - alias for install
        start   - start OpenVSCode Server (127.0.0.1:8080)
        remove  - remove OpenVSCode Server
        help    - displays help (this message)
```

## Contributing

Have a patch that will benefit this project?
Awesome! Follow these steps to have it accepted.

1. Please read [how to contribute](CONTRIBUTING.md).
1. Fork this Git repository and make your changes.
1. Create a Pull Request.
1. Incorporate review feedback to your changes.
1. Accepted!

## License

All files in this repository are under the [Apache License, Version 2.0](LICENSE) unless noted otherwise.