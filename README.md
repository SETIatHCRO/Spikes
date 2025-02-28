# SPIKES: Spectrum Plotter and Interfacing Kit for EMI Scanning

## Requirements:
- Python 3.13
- Virtual environment

## Setup:
1. Clone the repository:
   ```bash
   git clone git@github.com:SETIatHCRO/Spikes.git

2. Create the needed virtual environment
   ```bash
   python3.13 -m venv .venv
   source .venv/bin/activate

3. Upgrade pip and install requirements
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
4. Deactivate the virtual environment
   ```bash
   deactivate

5. Edit Path to .yaml configuration files in backend.py (inside get_yamls() function)
