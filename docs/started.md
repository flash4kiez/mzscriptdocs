---
title: 'Getting Started'
sidebar_position: 1
---

# Install MZscript

1. Open the vscode and add the folder with the bot
2. Open Terminal (Ctrl+Shift+`)
3. Install MZscript
```py
pip install MZscript
```

## Start Bot

1. Create file `main.py`
> This is your main file, from it you will launch the bot
2. We write the code that launches the bot
```py
from MZscript import MZClient # Let's import the class

bot = MZClient() # Create a bot object

bot.add_command( # Create command
    name='!help', # Name command
    code=''' 
$sendMessage[Hi!]
'''
)

bot.run('Token bot') # Launch bot
```
> The most important thing is not to show the bot token to anyone because another person will be able to access your bot

3. How to launch a bot?
- Method 1:

You are installing the VS Code extension for Python. [Tap](https://marketplace.visualstudio.com/items?itemName=donjayamanne.python-extension-pack). And then in the top right corner, click start.

- Method 2:

Open the terminal and write the command:
```py
python main.py
```