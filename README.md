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