Repos
=========

This role copies (COPR) repo files from the URL they are hosted to /etc/yum.repos.d

In a silverblue installation, rpm-ostree can then also source these to layer packages on top of the base image.

For instance: https://copr.fedorainfracloud.org/coprs/g/eduvpn/eduvpn-client/ has the links for the Fedora EduVPN repos.


Requirements
------------

- ansible.builtin.get_url


Example Playbook
----------------

```yaml
---
- name: Install EduVPN COPR repo
  ansible.builtin.get_url:
  url: "https://copr.fedorainfracloud.org/coprs/g/eduvpn/eduvpn-client/repo/fedora-{{ dist_version }}/group_eduvpn-eduvpn-client-fedora-{{ dist_version }}.repo"
  dest: /etc/yum.repos.d 
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
