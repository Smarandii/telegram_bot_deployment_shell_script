# telegram_bot_deployment_shell_script
Script for automate routine of telegram bots deployment on ubuntu serveru


## How to use:
1. Run this commands in linux: 
```shell 
git clone https://github.com/Smarandii/telegram_bot_deployment_shell_script
. install.bin
``` 

## Feel free to hardcode your own variables in!
That way script will be fully independent from user inputs :)
This script should be used in every telegram-bot project that is going to be deployed on ubuntu server. 

```shell
#!/bin/bash
cd /Your/Directory/Here
git clone https://YOUR_TOKEN:x-oauth-basic@github.com/YOUR_USER_NAME/YOUR_REPONAME
ls
echo -e "Press ENTER to continue..."
read tmp
echo -e "Creating a virtual environment..."
cd $REPONAME
python3.9 -m venv env
echo -e "Activating..."
. env/bin/activate
echo -e "Installing requirements..."
pip install -r requirements.txt
echo -e "Press ENTER to run bot.py..."
read tmp
python3.9 bot.py &
disown %1

```
