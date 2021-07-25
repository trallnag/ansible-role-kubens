[![role](https://img.shields.io/ansible/role/55314)](https://galaxy.ansible.com/trallnag/kubens)
[![quality](https://img.shields.io/ansible/quality/55314)](https://galaxy.ansible.com/trallnag/kubens)
[![downloads](https://img.shields.io/ansible/role/d/55314?label=downloads)](https://galaxy.ansible.com/trallnag/kubens)

# Ansible Role `trallnag.kubens`

Ansible role that installs [`kubens`][kubens] on Linux.

[kubens]: https://github.com/ahmetb/kubectx

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/kubens).

## Role Variables

```yaml
kubens_version:
  default: 0.9.4
  type: str
  required: false
  description: >-
    Version to use. Only 0.9.0 upwards supported. Check here:
    <https://github.com/ahmetb/kubectx/releases>.

kubens_arch:
  default: x86_64
  type: str
  required: false
  choices: ["x86_64", "arm64", "armhf", "armv7", "ppc64le"]
  description: >-
    Architecture to use.
```

## Example Playbook

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

## Special Requirements

None.

## Special Dependencies

None.

## License

Apache-2.0

## Author Information

Trallnag
