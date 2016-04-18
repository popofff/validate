# Validate

Simple bash script for validation of all cloudformation scripts in current directory.

The script is extremely handy if you are editing over 50 cloudformation templates at once, like I do.

First of all you should have installed aws cli tools.

The AWS Command Line Interface is a unified tool to manage your AWS services. With just one tool to download and configure, you can control multiple AWS services from the command line and automate them through scripts. You can accomplish this task by executing the following commands:
    
    sudo -i 	
    cd /root/
    wget https://s3.amazonaws.com/aws-cli/awscli-bundle.zip
    unzip awscli-bundle.zip
    ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws
    complete -C '/usr/bin/aws_completer' aws
    ln -s /usr/local/aws/bin/aws_completer /usr/bin/

After that configure your aws profile by editing /home/YOURUSER/.aws/credentials or via 'aws configure' like it's described here:

http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html

After that download validate script or clone the git project.

Move the sript inside the /usr/local/bin/ directory:

sudo mv validate /usr/local/bin/validate

Make the script executable:

sudo chmod +x /usr/local/bin/validate

Usage:

Enter the directory where your templates live and run "validate".
For example you can execute "validate|grep -i error" to filter the errors.
