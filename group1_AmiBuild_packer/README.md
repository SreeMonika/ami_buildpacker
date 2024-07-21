# group1_AmiBuild_packer

Ansible playbooks:
1. Blue server
    - with index and configuration file

2. Green Server
    - with index and configuration file

To Provision the playbook please use the following code in packer

provisioner "ansible" {
    playbook_file = "./playbooks/green/greenwebserver.yml"
  }
}

Both server were tested and working fine


Build AMI with Packer:

1. Created Packer configuration for Blue and Green AMIs    

2. Used Ansible playbook from the previous ticket in build provisioners

3. AMI are latest Ubuntu AMI from AWS

4. created AMI in the region with default VPC (Osaka) and then AMI is shared with eu-west-1