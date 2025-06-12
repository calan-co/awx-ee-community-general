# awx-ee-proxmox
This repo contains a modified AWX Execution Environment (EE) that includes the community.general collection and dependencies for community.general.proxmox. It was created to support the ansible roles and playbook for netbox-proxmox-automation. 

## Prerequisites
Building this image requires ansible-builder and it's dependencies (python3.9+ and {docker, podman}).

### Using Ansible
If you already have Ansible installed, you simply run the included playbook. The below command installs prerequisites locally, podman (by default) and ansible-builder, before building the Containerfile

``` sh
ansible-playbook ansible/playbook.yml
```

### Manually
To install ansible-builder, run the following command:
``` sh
pip install ansible-builder
```

To build, run the following command:
``` sh
ansible-builder build --tag quay.io/calan/awx/ee:24.6.1-community-general --container-runtime <docker or podman> --verbosity 3
```
