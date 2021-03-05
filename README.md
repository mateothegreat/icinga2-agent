# Delete AWS VPC

This role will deploy the icinga2 monitoring agent.
## Example Usage

Add the following to a file like `playbook.yaml`:

```yaml
- hosts: all
  roles:
    - role: "mateothegreat.icinga2_agent"
      vars:
        icinga2_agent:
          master:
            host: "1.1.1.1"
            user: "centos"
            key: "~/.ssh/some-sshkey.pem"
            cert: |
              $ANSIBLE_VAULT;1.1;AES256
              633....     # Release elastic ip address(es) for any NAT gateway(s).
```

Run with `ansible-playbook -i <your inventory file> playbook.yaml`.
