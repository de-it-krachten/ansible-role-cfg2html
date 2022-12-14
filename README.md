[![CI](https://github.com/de-it-krachten/ansible-role-cfg2html/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-cfg2html/actions?query=workflow%3ACI)


# ansible-role-cfg2html

Installs cfg2html



## Dependencies

#### Roles
None

#### Collections
- community.general

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- RockyLinux 8<sup>1</sup>
- RockyLinux 9
- OracleLinux 8<sup>1</sup>
- OracleLinux 9<sup>1</sup>
- AlmaLinux 8<sup>1</sup>
- AlmaLinux 9<sup>1</sup>
- Debian 10 (Buster)<sup>1</sup>
- Debian 11 (Bullseye)<sup>1</sup>
- Ubuntu 18.04 LTS<sup>1</sup>
- Ubuntu 20.04 LTS<sup>1</sup>
- Ubuntu 22.04 LTS
- Fedora 35<sup>1</sup>
- Fedora 36<sup>1</sup>
- Alpine 3<sup>1</sup>

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>
# Location where cfg2html will write output to
cfg2html_remote_root: /var/log/cfg2html

# Location where output is stored on central server
cfg2html_local_root: /var/log/cfg2html-central
</pre></code>

### defaults/family-RedHat.yml
<pre><code>
# Package name for RedHat/CentOS/Rocky
cfg2html_package: cfg2html-6.43.2.0.gacc0b2d-1.git202211281609.noarch.rpm
</pre></code>

### defaults/family-Debian.yml
<pre><code>
# Package name for Debian/Ubuntu
cfg2html_package: cfg2html_6.41.1_all.deb
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'cfg2html'
  hosts: all
  become: "yes"
  tasks:
    - name: Include role 'cfg2html'
      ansible.builtin.include_role:
        name: cfg2html
</pre></code>
