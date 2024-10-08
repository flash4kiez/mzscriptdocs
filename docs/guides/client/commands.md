---
title: 'Client Commands'
sidebar_position: 1
---

# Client Commands

The command in mzscript looks something like this
```py
bot.add_command(
    name='!help',
    code='''
$sendMessage[Hello World!]    
'''
)
```
Your bot send to the message channel `Hello World!`

## Aliases

If you want to make the team have different names

You need to move the code into a variable

And then add the variable to the command

`main.py`
```py
code = '''
$sendMessage[Hi!]
'''

bot.add_command(name='!hi', code=code)
bot.add_command(name='!hello', code=code)
```

This is roughly how command names work.

You can do the same in cogs

## Cogs
If you don't want to keep all the commands in `main.py` you need `cogs`

With the help of `cogs` you can load commands from a folder or from another file

### Loading files from a folder

In `main.py` you must write a function that loads the folder with the cogs

```py
bot.load_commands('cogs') # You can specify any name
```
> And most importantly, create this folder

Your project should look something like this:
```
mybot
├── cogs
│   └── hello.py
└── main.py
```

Now in the file `hello.py` we write the command

```py
from MZscript import MZClient
# import and set client argument to MZClient is not nessecary

# but gives you code highlighting
def setup(client: MZClient):
    client.add_command(
    name="!command",
    code="""
$sendMessage[Hello!]
""")

    client.add_command(
    name="!command2",
    code="""
$sendMessage[Hello 2!]
""")
```

This is roughly what the cogs look like in mzscript

You can create many different files in the kogs folder

But to load another folder from a folder kog you need to write such a "loader"

### Loading file cogs

Let's say your bot structure looks like this
```
mybot
├── cogs
│   ├── utils
│   │   └── hello.py
│   └── moderation
│   │   └── ban.py
└── main.py
```

You need to use another function that downloads not a folder with files but the file itself

```py
bot.load_command('cogs.utils.hello')
```
In this case, you need to specify the path to the `hello.py`

Now we will write a loader kog so that we don't have to constantly write a function for different files

You need to add one python module `os` to the `main.py`. It is in python by default

`main.py`
```py
from MZscript import MZClient
import os # A module with which we can work with files

# Load all files from the folder
for folder in os.listdir('cogs'): # We get everything that is in the cogs folder 
    for file in os.listdir(f'cogs/{folder}'): # We get all the files in the folder
        if file.endswith('.py'): # Checking if a file ends in .py
            bot.load_command(f'cogs.{folder}.{file[:-3]}') # We are already loading all the files from the cogs folder

bot.run('Token bot')
```

Now we have all the files from the `cogs` folder loaded