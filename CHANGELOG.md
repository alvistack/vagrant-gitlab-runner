# Vagrant Box Packaging for GitLab Runner

## YYYYMMDD.Y.Z - TBC

### Major Changes

  - Install dependencies with package manager
  - Upgrade minimal Ansible community package support to 4.5.0

## 20210718.1.1 - 2021-07-18

### Major Changes

  - Upgrade minimal Ansible community package support to 4.2.0

## 20210602.1.1 - 2021-06-02

### Major Changes

  - Initialize with `verify.yml` with first start
  - Upgrade minimal Ansible support to 4.0.0

## 20210313.1.1 - 2021-03-13

### Major Changes

  - Bugfix [ansible-lint `namespace`](https://github.com/ansible-community/ansible-lint/pull/1451)
  - Bugfix [ansible-lint `no-handler`](https://github.com/ansible-community/ansible-lint/pull/1402)
  - Bugfix [ansible-lint `unnamed-task`](https://github.com/ansible-community/ansible-lint/pull/1413)

## 20210116.1.0 - 2021-01-16

### Major Changes

  - Support [QEMU Guest Agent](https://wiki.qemu.org/Features/GuestAgent)
  - Support [VirtualBox Guest Additions](https://www.virtualbox.org/manual/ch04.html)

## 20210114.1.0 - 2021-01-14

### Major Changes

  - Migrate base Vagrant box from `generic/*` to `alvistack/*`

## 20201214.1.1 - 2020-12-14

### Major Changes

  - Add VirtualBox provider
  - Change GIT tag as per Vagrant Box naming and versioning limitation

## 13.6.0-4alvistack1 - 2020-11-23

  - Ubuntu 20.04 based
  - Base box running by [Vagrant Libvirt Provider](https://github.com/vagrant-libvirt/vagrant-libvirt)
  - Provision by [Ansible](https://www.ansible.com/) and [Molecule Vagrant Plugin](https://github.com/ansible-community/molecule-vagrant)
