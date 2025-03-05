## Installation Guide
### Abstract

This guide walks through the necessary steps to install the SPIKES application on a local machine. It allows the user to run the application on their own machine given the correct dependencies are installed.

This Guide is tested on Windows 11 and Ubuntu 24.04 LTS.

### Requirements
- Git (make sure it is up to date)
- Python 3.13
- Virtual environment

### Setup

1. Open a terminal and navigate to the directory where you want to install the application

    Linux, OSX:
    ```bash
    cd ~/path/to/directory
    ```

    Windows (using PowerShell):
    ```bash
    chdir C:\path\to\directory
    ```

2. Clone the repository
   
    ```bash
    git clone git@github.com:SETIatHCRO/Spikes.git
    ```

    and navigate into the SPIKES directory
   
    Linux, OSX:
    ```bash
    cd Spikes
    ```

    Windows:
    ```bash
    chdir Spikes
    ```

3. Create the needed virtual environment
   
    Linux, OSX:
    ```bash
    python3.13 -m venv .venv
    ```

    Windows (to make sure you are using the correct version of python):

    ```bash 
    C:\path\to\python3.13 -m venv .venv
    # this should be: 
    # C:\Users\YourUsername\AppData\Local\Programs\Python\Python313\python.exe
    # or
    # C:\Program Files\Python313\python.exe for system-wide installations
    ```
  
    and activate it

    Linux, OSX:
    ```bash
    source .venv/bin/activate
    ```

    Windows:

    ```bash
    .venv\Scripts\Activate
    ```

4. Upgrade pip
   
    Linux, OSX:
    ```bash
    pip install --upgrade pip
    ```

    Windows:

    ```bash
    python.exe -m pip install --upgrade pip
    ```

    and install requirements
    
    ```bash
    pip install -r requirements.txt
    ```

5. Deactivate the virtual environment
   
    ```bash
    deactivate
    ```

