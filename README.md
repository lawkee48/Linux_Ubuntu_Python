# Linux_Ubuntu_Python

## Install Python
### Option 1: Using apt (Easier)
Check if python is installed in the system:
```
python --version
```
If not, then continue. Update and Refresh Repository Lists: 
```
sudo apt update && sudo apt upgrade
```
Install Supporting Software:
- The software-properties-common package gives you better control over your package manager by letting you add PPA (Personal Package Archive) repositories)
```
sudo apt install software-properties-common
```
Add Deadsnakes PPA:
- Deadsnakes is a PPA with newer releases than the default Ubuntu repositories) and Refresh the package lists again
```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
```
Install Python 3 and check if it is successfully installed:
```
sudo apt install python3.8
python --version
```
### Option 2: From Source Code (Latest Version)
Update Local Repositories:
```
sudo apt update
```
Compiling a package from source code requires additional software, install them: 
```
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev wget
```
Download the Latest Version of Python Source Code
```
cd ~/Downloads
wget https://www.python.org/ftp/python/3.7.6/Python-3.7.6.tgz
```
Extract Compressed Files
```
tar -xf Python-3.7.6.tgz
```

Before installation, Test System and Optimize Python:
- The ./configure command evaluates and prepares Python to install on your system. Using the --optimization option speeds code execution by 10-20%.
```
cd python-3.8.3
./configure --enable-optimizations
```
Install a Second Instance of Python (recommended)
```
sudo make altinstall
```
or Overwrite Default Python Installation (optional)
```
sudo make install
```
Verify Python version:
```
python --version
```



Reference:
How to Install Python 3 on Ubuntu 18.04 or 20.04. https://phoenixnap.com/kb/how-to-install-python-3-ubuntu
