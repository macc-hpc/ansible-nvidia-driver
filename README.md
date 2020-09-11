nvidia-driver
=========

Install Nvidia drivers.

Role Variables
--------------

Role has no variables but depends on [yum-repositories](https://github.com/macc-hpc/ansible-yum-repositories) that expects some configuration.

Dependencies
------------

The only dependency is [yum-repositories](https://github.com/macc-hpc/ansible-yum-repositories) aliased to macc.yum-repositories.

Example Playbook
----------------

Running the role

```
- hosts: servers
  vars:
		yum_repositories_urls:
  		- {
    		name: cuda-rhel7-x86_64,
    		description: Nvidia CUDA Drivers,
    		url: https://developer.download.nvidia.com/compute/cuda/repos/rhel7/x86_64,
    		gpgkey: https://developer.download.nvidia.com/compute/cuda/repos/rhel7/x86_64/7fa2af80.pub
  		}
  roles:
     - role: macc.nvidia-driver
```

License
-------

MIT
