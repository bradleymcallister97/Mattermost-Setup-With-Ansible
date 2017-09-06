# Mattermost-Setup-With-Ansible

__Was ran and tested with Ansible 2.4__

1. In order to be able to run the playbook you must have:
    - An AWS user with prorammatic access
    - An AWS key pair set up with your machines personal ssh key, [instructions](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#how-to-generate-your-own-key-and-import-it-to-aws)

2. Update the all file under group_vars to contain the correct variale names.

3. Run playbook with command:
`AWS_ACCESS_KEY_ID='<Your access key id>' AWS_SECRET_ACCESS_KEY='<Your secret access key>' ansible-playbook provision-aws-mattermost.yml`

4. Once playbook is done you can view the mattermost website by going to the ip address of the ec2 instance that the playbook created
