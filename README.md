# ansible

## Roles

### `awx-install`
Role configures a host to install [Ansible AWX](https://github.com/ansible/awx).

* ensures depdencies are met
* clones AWX repository
* templates out `install.yml`

_Note: you need to run Ansible locally on the destination host as root._

### `role.telegraf`
Installs and configures Telegraf for use with Wavefront.

### `role.postboot-ec2facts`
Most Playbooks assume EC2 facts through `ec2.py`. In some use cases, you may need to run Playbooks locally on boot using `ansible-pull` and derive similar facts through `ec2_facts` and user-data.

Sample user-data:

```
{"ansible": {"role": "db", "cluster": "elgon", "mirror": "primary"}}
```
