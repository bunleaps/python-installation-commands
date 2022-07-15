# Python Installation Command

```
===================================
*******       Step 1       ********
===================================
# Go to User Directory
cd ~

# Change Execution Policy Settings
Set-ExecutionPolicy -Scope CurrentUser
* RemoteSigned

# Check List of Execution Policy
Get-ExecutionPolicy -List


===================================
*******       Step 2       ********
===================================
# Connect to WebClient (shares Internet connection settings)
$script = New-Object Net.WebClient

# Check if script is working + options (commands)
$script | Get-Member

# Download & Check Signatures
$script.DownloadString("https://chocolatey.org/install.ps1")

# Install Chocolatey
iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex

# Check if Chocolatey is installed
choco -?

# Update Chocolatey
choco upgrade chocolatey

===================================
*******       Step 3       ********
===================================
# Install Python via Chocolatey
choco install -y python3

# Refresh Environment Vars
refreshenv

# Check if Python is installed
python -V

# Make Sure PIP is installed and upgraded
python -m pip install --upgrade pip
```
