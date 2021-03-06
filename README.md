# ansible-role-kubernetes_master

Ansible playbook to automate installing and maintaining kubernetes master nodes.

## Requirements

This role currently requires a working VMware Photon OS server with enabled
Docker environment.

## Role Variables

The following variables are available within the role, with defaults noted:

```yaml
# Container memory limit. Use 512MB, type string, or 0 for unlimited
memory_limit: 0MB

# The name of the kubernetes package to install.
kubernetes_package: kubernetes

# The name of the flannel package to install.
flannel_package: flannel
```

## Example playbook

```yaml
---
- hosts: kubernetes_masters
  sudo: True
  roles:
    - kubernetes_master
  vars:
    - ... forthcoming
```

# License and Copyright
 
Copyright 2015 VMware, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

