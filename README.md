---

⚠️ **IMPORTANT NOTICE** ⚠️

**Repository is archived and unmaintained.** I personally don't need it anymore,
as instead of using a dedicated Ansible Role I switched to installing
kubectx / kubens via asdf. So no reason to keep this role around.

- <https://github.com/trallnag/asdf-kubectx>
- <https://github.com/trallnag/ansible-role-asdf-plugin>

---

[![primary](https://github.com/trallnag/ansible-role-kubens/actions/workflows/primary.yaml/badge.svg)](https://github.com/trallnag/ansible-role-kubens/actions/workflows/primary.yaml)
[![role](https://img.shields.io/ansible/role/55314)](https://galaxy.ansible.com/trallnag/kubens)
[![quality](https://img.shields.io/ansible/quality/55314)](https://galaxy.ansible.com/trallnag/kubens)
[![downloads](https://img.shields.io/ansible/role/d/55314?label=downloads)](https://galaxy.ansible.com/trallnag/kubens)

# Ansible Role `trallnag.kubens`

Ansible role that installs the Go version of [`kubens`](https://github.com/ahmetb/kubectx).

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/kubens).

## Scope

In:

* Install a single version of kubens to a global location.

Out:

* Set up tab completion.

## Special Requirements

None.

## Special Dependencies

None.

## Role Variables

Check out [`meta/argument_specs.yaml`](meta/argument_specs.yaml).

## Examples

Here is a minimal Playbook:

```yaml
- name: Playbook
  hosts: myhost
  remote_user: myuser
  vars:
    rolespec_validate: true
  roles:
    - name: trallnag.kubens
      vars:
        kubens_version: 0.9.4
        kubens_arch: x86_64
```
