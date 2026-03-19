# AWS-Examples
AWS codebase

# instal AWS
cd ..
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
cd AWS-Examples

# IAM Access key (some region might need to opt-in)
export AWS_ACCESS_KEY_ID=AKIAIOSFODNN7EXAMPLE
export AWS_SECRET_ACCESS_KEY=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
export AWS_DEFAULT_REGION=ap-southeast-1

# Create a .env to store the above env variables and add
AWS_CLI_AUTO_PROMPT=on-partial
# for better cli experience

# Enter "source ./s3/bash-scripts/setup-env" for automatically setup your environment variables

'
# install powershell using these command
#https://learn.microsoft.com/en-us/powershell/scripting/install/install-ubuntu?view=powershell-7.5

# Update the list of packages
sudo apt-get update

# Install pre-requisite packages.
sudo apt-get install -y wget apt-transport-https software-properties-common

# Get the version of Ubuntu
source /etc/os-release

# Download the Microsoft repository keys
wget -q https://packages.microsoft.com/config/ubuntu/$VERSION_ID/packages-microsoft-prod.deb

# Register the Microsoft repository keys
sudo dpkg -i packages-microsoft-prod.deb

# Delete the Microsoft repository keys file
rm packages-microsoft-prod.deb

# Update the list of packages after we added packages.microsoft.com
sudo apt-get update

###################################
# Install PowerShell
sudo apt-get install -y powershell

# Start PowerShell
pwsh
'

# Install AWS Tools in powershell
Install-Module -Name AWS.Tools.Installer

# Powershell would not be able to Identify the AccessToken
# so it will be best to use "aws configure" or enter 
$env:AWS_ACCESS_KEY_ID="..."
$env:AWS_SECRET_ACCESS_KEY="..."
$env:AWS_DEFAULT_REGION="ap-southeast-1"