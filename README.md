# package-insttlation
Basic package installation. Use raw tab to see.

vim package-install.yml

---
- hosts: hosts
  remote_user: username 
  sudo: true
  
  tasks:
        - name: ensure a list of packages installed
          yum:
            name: "{{ packages }}"
          vars:
            packages:
            - opensips-snmpstats
            - perl-DBD-MySQL
            state: latest
