# ntlmaps - Ansible Role

[![GitHub tag](https://img.shields.io/github/tag/unleashedtech/ansible-role-ntlmaps.svg)](https://github.com/unleashedtech/ansible-role-ntlmaps/tags)
[![license](https://img.shields.io/github/license/unleashedtech/ansible-role-ntlmaps.svg)](https://github.com/unleashedtech/ansible-role-ntlmaps/blob/master/LICENSE)

Installs ntlmaps on Debian-based servers.

## Requirements

* [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html) 2.3 or later
* Debian or Ubuntu (modern versions)

## Installation

Add this role to `requirements.yml`:

```yaml
- src: unleashedtech.ntlmaps
  version: 0.1.0 # Check for latest version!
```

Run `$ ansible-galaxy install -r requirements.yml` to install this new role.

## Role Variables

Mandatory variables you will need to set include:

```yaml
# Parent proxy IP/hostname
ntlmaps_parent_proxy: "xx.xx.xx.xx"

# NTLM authentication settings
# You should probably store these in an encrypted vault file!
ntlmaps_auth_nt_domain: "ACMECORP"
ntlmaps_auth_nt_user: "jsmith"
ntlmaps_auth_nt_password: "hunter2"
```

See [`defaults/main.yml`](https://github.com/unleashedtech/ansible-role-ntlmaps/blob/master/defaults/main.yml) for a list of default variables you may want to override.

## Contributing

Pull requests are welcomed. Please preserve backward compatibility!

## License

This role is released under the [MIT License](https://opensource.org/licenses/MIT).
