# Mattermost-Setup-With-Ansible

## Why
After looking for automation tools found Ansible, so decided to teach myself how to use Ansible. This is one of the scripts I created.

## What
This script will instantiate:
- RDS instance with postgres installed
- EC2 instance
    - connect to the RDS 
    - install and setup Nginx
    - install and configure Mattermost
    
Once script is done the EC2 instance will be hosting your personal Mattermost site. Mattermost is like Slack.

## How to Run
__Was ran and tested with Ansible 2.4__

1. In order to be able to run the playbook you must have:
    - An AWS user with prorammatic access
    - An AWS key pair set up with your machines personal ssh key, [instructions](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#how-to-generate-your-own-key-and-import-it-to-aws)

2. Update the all file under group_vars to contain the correct variale names.

3. Run playbook with command:
`AWS_ACCESS_KEY_ID='<Your access key id>' AWS_SECRET_ACCESS_KEY='<Your secret access key>' ansible-playbook provision-aws-mattermost.yml`

4. Once playbook is done you can view the mattermost website by going to the ip address of the ec2 instance that the playbook created
