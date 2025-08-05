[![CI](https://github.com/de-it-krachten/ansible-role-cfg2html/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-cfg2html/actions?query=workflow%3ACI)


# ansible-role-cfg2html

Installs cfg2html



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- Red Hat Enterprise Linux 10<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- RockyLinux 10
- OracleLinux 8
- OracleLinux 9
- OracleLinux 10
- AlmaLinux 8
- AlmaLinux 9
- AlmaLinux 10
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Debian 13 (Trixie)
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Fedora 41
- Fedora 42

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>
# cfg2html version
cfg2html_version: 7.2.1

# cfg2html source
cfg2html_source_archive: https://github.com/cfg2html/cfg2html/archive/refs/tags/{{ cfg2html_version }}.tar.gz

# cfg2html root location
cfg2html_root: /opt/cfg2html

# Location where cfg2html will write output to
cfg2html_remote_root: /var/log/cfg2html

# Location where output is stored on central server
cfg2html_local_root: /var/log/cfg2html-central
</pre></code>

### defaults/family-Debian.yml
<pre><code>
# Package name for Debian/Ubuntu
cfg2html_package: cfg2html_7.0.1_all.deb
</pre></code>

### defaults/family-RedHat.yml
<pre><code>
# Package name for RedHat/CentOS/Rocky
cfg2html_package: cfg2html-7.0.1.1.gb8c7a98-1.git202303291751.noarch.rpm
</pre></code>

### defaults/family-Suse.yml
<pre><code>
# Package name for RedHat/CentOS/Rocky
cfg2html_package: cfg2html-7.0.1.1.gb8c7a98-1.git202303291751.noarch.rpm
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'cfg2html'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'cfg2html'
      ansible.builtin.include_role:
        name: cfg2html
</pre></code>
