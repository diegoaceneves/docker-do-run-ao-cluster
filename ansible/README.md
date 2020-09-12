# Docker do Run ao Cluster
Ansible playbook to deploy a enviroment in AWS.
This playbook create and prepair AWS [EC2] instances.

## To run:
Create a user on [IAM](https://console.aws.amazon.com/iam/home) and export the access_key_id and secret_access_key:

```bash
 $ export AWS_ACCESS_KEY_ID=AKIBX2RXYSXADGWDYDXEH
 $ export AWS_SECRET_ACCESS_KEY=6GDXW3RS2SZDQDSXGHY53D5GNCX24DX6F7D3S2W4
```

Create a MariaDB on [RDS](https://console.aws.amazon.com/rds/home)

Create a [EFS](https://console.aws.amazon.com/efs#/file-systems) storage

Create a [KeyPair](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#KeyPairs:), and save the .pem file at ~/.ssh/

All configs are at [group_vars/all.yml](group_vars/all.yml).

If you don't want to use a custon bashrc file, just remove the include at [roles/prepare_ec2/tasks/main.yml](roles/prepare_ec2/tasks/main.yml)

Create a flag in your ~/.ssh/config
```bash
echo "## AWS" >> ~/.ssh/config
```

Run the playbook:
```bash
ansible-playbook -i hosts playbook.yml
```

The playbook will populate your hosts file with the external IP of created instances and configure ssh client, after this you can access the instances with:
```bash
ssh dockerX
```


## TO DO
* Create a RDS Database
* Create a EFS Storage
* Remove EC2 Instances
* Remove RDS Database
* Remove EFS Storage
