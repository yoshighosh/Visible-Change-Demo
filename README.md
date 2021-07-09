# Visible Change: Changing the Footprint

This app uses Python to handle web stuff.

# Building for development

Prerequisites: Python 3

Building follows the general procedure found [here](https://docs.microsoft.com/en-us/azure/app-service/containers/quickstart-python)

Bash:

    python3 -m venv venv
    source venv/bin/activate
    pip install -r app/requirements.txt
    FLASK_APP=app/main.py flask run

Windows powershell:

    py -3 -m venv env
    env\scripts\activate
    pip install -r app\requirements.txt
    Set-Item Env:FLASK_APP ".\app\main.py"
    flask run

For simplicity, windows users can enable powershell scripts by opening powershell as administrator and running:

    Set-ExecutionPolicy RemoteSigned

Then run

    setup-env-dev.ps1
    flask run

Mac and Linux users can use the bash script. First make it executable:

    chmod +x setup-env-dev.sh

Then run

    setup-env-dev.sh
    FLASK_APP=app/main.py flask run
