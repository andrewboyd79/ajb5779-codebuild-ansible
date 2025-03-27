# ajb5779-codebuild-ansible

Test repository for executing Ansible playbooks using CodePipeline/CodeBuild
- Repository connected to 'ajb5779-codebuild-ansible' CodePipeline
- Uses Parameter store value '/ansible_demo/ansible_private_key' to create ssh key in CodeBuild container/job
- Uses 'aws_ec2' plugin to generate dynamic inventory; needs 'aws_ec2' plugins to be enabled in ansible.cfg 
- Instance should be tagged withe Group: Webservers; Ansible hosts set to look for this tag
- Host key checking has been disabled when using CodeBuild

## CodeBuild needs NAT Gateway created and connected to the Private Subnet (using appropriate RTB)
