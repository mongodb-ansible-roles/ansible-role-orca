Ansible role for orca
==================================

Installs Orca for Windows from SDK

[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-orca/workflows/Molecule%20Test/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-orca/actions?query=workflow%3A%22Molecule+Test%22)
[![GitHub Actions](https://github.com/mongodb-ansible-roles/ansible-role-orca/workflows/Release/badge.svg)](https://github.com/mongodb-ansible-roles/ansible-role-orca/actions?query=workflow%3A%22Release%22)

Description
-----------

The `orca` package on Chocolatey seems to be broken as per the comments on this page:
https://chocolatey.org/packages/orca

The alternative way to install `orca` is from the Windows 10 SDK, which as the `orca` MSI.

Role Variables
--------------

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-------:|:--------:|
| `orca_msi` | Location of the Orca MSI file | string | `D:\Installers\Orca-x86_en-us.msi` | false |
| `win_sdk_dest` | Location of SDK ISO | string | `C:\Users\Administrator` | false |
| `win_sdk_iso` | Filename of SDK ISO | string | `19041.685.201201-2105.vb_release_svc_prod1_WindowsSDK.iso` | false |
| `win_sdk_url` | URL to download Win 10 SDK | string | `https://software-download.microsoft.com/download/pr/{{ win_sdk_iso }}` | false |

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: ansible-role-orca
```

License
-------

[Apache License](LICENSE)
