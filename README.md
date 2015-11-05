Instructions
------------

Using [Packer](https://packer.io/) and [Ansible](https://github.com/ansible/ansible) to repackage custom AWS EC2 AMIs.

Put this together as I didn't really find great examples for doing exactly what I wanted to. Hopefully this can help others.

1. cp aws-creds-example.json aws-creds.json
  * replace values in aws-creds.json
1. packer build -var-file=aws-creds.json templates/base.json
1. profit

**note:** you may need to remove the subnet_id and the aws_vpc_id
