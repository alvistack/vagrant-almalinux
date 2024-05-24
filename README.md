# Vagrant Box Packaging for AlmaLinux

<a href="https://alvistack.com" title="AlviStack" target="_blank"><img src="/alvistack.svg" height="75" alt="AlviStack"></a>

[![GitLab pipeline
status](https://img.shields.io/gitlab/pipeline/alvistack/vagrant-almalinux/master)](https://gitlab.com/alvistack/vagrant-almalinux/-/pipelines)
[![GitHub
tag](https://img.shields.io/github/tag/alvistack/vagrant-almalinux.svg)](https://github.com/alvistack/vagrant-almalinux/tags)
[![GitHub
license](https://img.shields.io/github/license/alvistack/vagrant-almalinux.svg)](https://github.com/alvistack/vagrant-almalinux/blob/master/LICENSE)
[![Vagrant Box
download](https://img.shields.io/badge/dynamic/json?label=alvistack%2Falmalinux-9&query=%24.boxes%5B%3A1%5D.downloads&url=https%3A%2F%2Fapp.vagrantup.com%2Fapi%2Fv1%2Fsearch%3Fq%3Dalvistack%2Falmalinux-9)](https://app.vagrantup.com/alvistack/boxes/almalinux-9)

AlmaLinux OS is an open-source, community-driven Linux operating system that fills the gap left by the discontinuation of the CentOS Linux stable release. AlmaLinux OS is an Enterprise Linux distro, binary compatible with RHEL®, and guided and built by the community.

As a standalone, completely free OS, AlmaLinux OS enjoys \$1M in annual sponsorship from CloudLinux Inc. and support from more than 25 other sponsors. Ongoing development efforts are governed by the members of the community.

Learn more about AlmaLinux: <https://almalinux.org/>

## Supported Boxes and Respective Packer Template Links

- [`alvistack/almalinux-9`](https://app.vagrantup.com/alvistack/boxes/almalinux-9)
  - [`packer/almalinux-9-libvirt/packer.json`](https://github.com/alvistack/vagrant-almalinux/blob/master/packer/almalinux-9-libvirt/packer.json)
  - [`packer/almalinux-9-virtualbox/packer.json`](https://github.com/alvistack/vagrant-almalinux/blob/master/packer/almalinux-9-virtualbox/packer.json)
- [`alvistack/almalinux-8`](https://app.vagrantup.com/alvistack/boxes/almalinux-8)
  - [`packer/almalinux-8-libvirt/packer.json`](https://github.com/alvistack/vagrant-almalinux/blob/master/packer/almalinux-8-libvirt/packer.json)
  - [`packer/almalinux-8-virtualbox/packer.json`](https://github.com/alvistack/vagrant-almalinux/blob/master/packer/almalinux-8-virtualbox/packer.json)

## Overview

- Packaging with [Packer](https://www.packer.io/)
- Minimal [Vagrant base box
  implementation](https://www.vagrantup.com/docs/boxes/base)
- Support [QEMU Guest
  Agent](https://wiki.qemu.org/Features/GuestAgent)
- Support [VirtualBox Guest
  Additions](https://www.virtualbox.org/manual/ch04.html)
- Support [Vagrant synced folder with
  rsync](https://www.vagrantup.com/docs/synced-folders/rsync)
- Support [Vagrant provisioner with
  Ansible](https://www.vagrantup.com/docs/provisioning/ansible)
- Standardize disk partition with GPT
- Standardize file system mount with UUID
- Standardize network interface with `eth0`

### Quick Start

Once you have [Vagrant](https://www.vagrantup.com/docs/installation) and
[VirtaulBox](https://www.virtualbox.org/) installed, run the following
commands under your [project
directory](https://learn.hashicorp.com/tutorials/vagrant/getting-started-project-setup?in=vagrant/getting-started):

    # Initialize Vagrant
    vagrant init alvistack/almalinux-9

    # Start the virtual machine
    vagrant up

    # SSH into this machine
    vagrant ssh

    # Terminate the virtual machine
    vagrant destroy --force

### Molecule

You could also run our
[Molecule](https://molecule.readthedocs.io/en/stable/) test cases if you
have [Vagrant](https://www.vagrantup.com/) and
[Libvirt](https://libvirt.org/) installed, e.g.

    # Run Molecule on AlmaLinux 9 Stream
    molecule converge -s almalinux-9-libvirt

Please refer to [.gitlab-ci.yml](.gitlab-ci.yml) for more information on
running Molecule.

## Versioning

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub
Release](https://github.com/alvistack/vagrant-almalinux/tags) of this
repository. Thus using these tags will ensure you are running the most
up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab
pipeline](https://gitlab.com/alvistack/vagrant-almalinux/-/pipelines) in
weekly basis. Thus using these tags will ensure you are running the
latest packages provided by the base image project.

## License

- Code released under [Apache License 2.0](LICENSE)
- Docs released under [CC BY
  4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

- Wong Hoi Sing Edison
  - <https://twitter.com/hswong3i>
  - <https://github.com/hswong3i>
