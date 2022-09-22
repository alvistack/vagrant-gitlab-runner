# Vagrant Box Packaging for GitLab Runner

<a href="https://alvistack.com" title="AlviStack" target="_blank"><img src="/alvistack.svg" height="75" alt="AlviStack"></a>

[![Gitlab pipeline status](https://img.shields.io/gitlab/pipeline/alvistack/vagrant-gitlab-runner/master)](https://gitlab.com/alvistack/vagrant-gitlab-runner/-/pipelines)
[![GitHub tag](https://img.shields.io/github/tag/alvistack/vagrant-gitlab-runner.svg)](https://github.com/alvistack/vagrant-gitlab-runner/tags)
[![GitHub license](https://img.shields.io/github/license/alvistack/vagrant-gitlab-runner.svg)](https://github.com/alvistack/vagrant-gitlab-runner/blob/master/LICENSE) -[![Vagrant Box download](https://img.shields.io/badge/dynamic/json?label=alvistack%2Fgitlab-runner-15.4&query=%24.boxes%5B%3A1%5D.downloads&url=https%3A%2F%2Fapp.vagrantup.com%2Fapi%2Fv1%2Fsearch%3Fq%3Dalvistack%2Fgitlab-runner-15.4)](https://app.vagrantup.com/alvistack/boxes/gitlab-runner-15.4)

GitLab is a complete DevOps platform, delivered as a single application. This makes GitLab unique and makes Concurrent DevOps possible, unlocking your organization from the constraints of a pieced together toolchain. Join us for a live Q\&A to learn how GitLab can give you unmatched visibility and higher levels of efficiency in a single application across the DevOps lifecycle.

Learn more about GitLab: <https://about.gitlab.com/>

## Supported Boxes and Respective Packer Template Links

  - [`alvistack/gitlab-runner-15.4`](https://app.vagrantup.com/alvistack/boxes/gitlab-runner-15.4)
      - [`packer/gitlab-runner-15.4-libvirt/packer.json`](https://github.com/alvistack/vagrant-gitlab-runner/blob/master/packer/gitlab-runner-15.4-libvirt/packer.json)
      - [`packer/gitlab-runner-15.4-virtualbox/packer.json`](https://github.com/alvistack/vagrant-gitlab-runner/blob/master/packer/gitlab-runner-15.4-virtualbox/packer.json)
  - [`alvistack/gitlab-runner-15.3`](https://app.vagrantup.com/alvistack/boxes/gitlab-runner-15.3)
      - [`packer/gitlab-runner-15.3-libvirt/packer.json`](https://github.com/alvistack/vagrant-gitlab-runner/blob/master/packer/gitlab-runner-15.3-libvirt/packer.json)
      - [`packer/gitlab-runner-15.3-virtualbox/packer.json`](https://github.com/alvistack/vagrant-gitlab-runner/blob/master/packer/gitlab-runner-15.3-virtualbox/packer.json)

## Overview

  - Packaging with [Packer](https://www.packer.io/)
  - Minimal [Vagrant base box implementation](https://www.vagrantup.com/docs/boxes/base)
  - Support [QEMU Guest Agent](https://wiki.qemu.org/Features/GuestAgent)
  - Support [VirtualBox Guest Additions](https://www.virtualbox.org/manual/ch04.html)
  - Support [Vagrant synced folder with rsync](https://www.vagrantup.com/docs/synced-folders/rsync)
  - Support [Vagrant provisioner with Ansible](https://www.vagrantup.com/docs/provisioning/ansible)
  - Standardize disk partition with GPT
  - Standardize file system mount with UUID
  - Standardize network interface with `eth0`

### Quick Start

Once you have [Vagrant](https://www.vagrantup.com/docs/installation) and [VirtaulBox](https://www.virtualbox.org/) installed, run the following commands under your [project directory](https://learn.hashicorp.com/tutorials/vagrant/getting-started-project-setup?in=vagrant/getting-started):

    # Initialize Vagrant
    vagrant init alvistack/gitlab-runner-15.4
    
    # Start the virtual machine
    vagrant up
    
    # SSH into this machine
    vagrant ssh
    
    # Terminate the virtual machine
    vagrant destroy --force

### Molecule

You could also run our [Molecule](https://molecule.readthedocs.io/en/stable/) test cases if you have [Vagrant](https://www.vagrantup.com/) and [Libvirt](https://libvirt.org/) installed, e.g.

    # Run Molecule on GitLab Runner 15.4
    molecule converge -s gitlab-runner-15.4-libvirt

Please refer to [.gitlab-ci.yml](.gitlab-ci.yml) for more information on running Molecule.

## Versioning

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub Release](https://github.com/alvistack/vagrant-gitlab-runner/tags) of this repository. Thus using these tags will ensure you are running the most up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab pipeline](https://gitlab.com/alvistack/vagrant-gitlab-runner/-/pipelines) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
