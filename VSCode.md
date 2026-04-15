# VS CODE EDITOR
#### Disable the parameter Hints (shows function parameter descriptions and overloads)

1. Open the Command Palette (Ctrl+Shift+P / Cmd+Shift+P).
2. Type and select "Preferences: Open User Settings (JSON)".
3. Add or modify the following lines within the `settings.json` file to disable various quick suggestions: <br> 
```
"editor.parameterHints.enabled": false
```

#### Point VS Code Editor to specific path for a Virtual Environment.

1. Create or open the `.vscode/settings.json` file in your project root.
2. Add or update the following entry:
```
{
  "python.defaultInterpreterPath": "path/to/your/venv/bin/python"
}
```
Replace "path/to/your/venv/bin/python" with the actual path to your venv's Python executable.


#### Set Working Directory to Python File path during Debugging/Running.

1. Open the `.vscode/launch.json` file in your project root.
2. Add or update the following entry:
```
"cwd": "${fileDirname}",
"purpose": ["debug-in-terminal"]
```
3. Optionally open the `.vscode/settings.json` file in your project root.
4. Add or update the following entry:
```
"python.terminal.executeInFileDir": true
```