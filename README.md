# Goose Weather
The goal of this repository is to provide an easy to launch self-hosted weather application.

## Information

## Quick start
### Prerequisites
- python3 >= 3.10.12
    - See [docs](https://www.python.org/downloads/) for installation downloads for your OS.  Some OSs allow python installation through their package manager.  For example with Ubuntu:
    ```
    apt install python3.10
    ``` 
- git
    - See [docs](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) for installation on your OS.
- (optional) venv (python standard library virtual envirnment tool)
    - See [docs](https://docs.docker.com/engine/) for installation on your OS.  Some python3 installations do not come with `venv` module by default and you will need to install it separately. For example with Ubuntu:
    ```
    apt install python3.10-venv
    ```
### Process
- Clone the repository
    ```
    git clone https://github.com/gooseops/goose_weather.git
    ```
- Change directory to cloned repository
    ```
    cd goose_weather
    ```
- (optional) If you want to avoid adding pip packages to your system level pip, you can create a virtual environment that will keep all pip packages local to this directory which makes cleanup a bit easier.
    ```
    python3 -m venv .venv && source .venv/bin/activate
    ```
- Ensure pip exists
    ```
    python -m ensurepip --upgrade
    ```
- Install pip packages
    ```
    pip install -r requirements.txt
    ```
- Run the server with `gunicorn`
    ```
    gunicorn -w 4 'app:app'
    ```
## Launching with Docker
- Work in progress
## Launching on Kubernetes
- Work in progress
<!-- ### Manifest
### Helm -->
