# Getting Started

Create vars/aws_credentials.yml with the following variables:
```bash
aws_access_key: <aws access key>
aws_secret_key: <aws secret key>
```

Perform `make install` to install dependencies

```bash
make install
```

To install new roles locally add them to requirements.yml and run

```bash
make install/requirements
```

Create an aws keypair using your ~/.ssh/id_rsa.pub public key

```bash
make keypair/create
```

Terminiating an instance by id

```bash
ansible-playbook ec2.yml --tags terminate -e instance_ids=i-061990aec288b0b0d
```

# References

* https://docs.ansible.com/ansible/devel/modules/ec2_module.html