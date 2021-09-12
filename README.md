# InstallationShellScript
Script for automate routine server deployment commands in ubuntu


## How to use:
1. Run this command in linux: 
```shell 
  user$ . install.bin
``` 

## Feel free to hardcode your own variables in!
That way script will be fully independent from user inputs :)

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