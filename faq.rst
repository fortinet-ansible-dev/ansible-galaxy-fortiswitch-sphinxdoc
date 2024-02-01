
Frequently Asked Questions (FAQ)
================================

|

**TABLE OF CONTENTS:**
 - `How to export the current settings of a module into a playbook?`_
 - `How to backup full config or default config?`_
 - `Resolution for Ansible Always Sending GET/PUT Requests as POST Requests`_

|

How to export the current settings of a module into a playbook?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We are excited to introduce a powerful module fortiswitch_export_config_playbook to you. It's used to convert the current
settings of a module into a executable playbook.

The following example will show you how fortiswitch_export_config_playbook module works.

**Export the current settings of an interface named internal:**

::

  - hosts: fortiswitch01
    connection: httpapi
    collections:
      - fortinet.fortiswitch
    vars:
      ansible_httpapi_use_ssl: true
      ansible_httpapi_validate_certs: false
      ansible_httpapi_port: 443
    tasks:
    - name: Export multiple palybooks
      fortiswitch_export_config_playbook:
        selectors:
        - selector: system_interface
          params:
            name: "internal"
        output_path: "./"

There will be a new generated playbook called system_interface_playbook.yml at the current path.
Feel free to assign a output_path where you want the playbook is saved.

How to backup full config or default config?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Backup full config or default config:**

::

  - hosts: fortiswitch01
    collections:
    - fortinet.fortiswitch
    connection: httpapi
    vars:
      ansible_httpapi_use_ssl: yes
      ansible_httpapi_validate_certs: no
      ansible_httpapi_port: 443
    tasks:
    - name: 'full config backup'
      fortiswitch_execute_backup_full_config:
        enable_log: yes
        execute_backup_full_config:
          config: test
    - name: 'default config backup'
      fortiswitch_execute_backup_default_config:
        enable_log: yes
        execute_backup_default_config:
          config: test

Resolution for Ansible Always Sending GET/PUT Requests as POST Requests
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We have been inundated with complaints regarding older Ansible versions consistently sending GET/PUT requests as POST requests due to a bug in the ansible.netcommon module. To prevent such issues, please ensure that you have installed the latest Ansible version.

To upgrade to the latest version of ansible.netcommon, use the following command:
ansible-galaxy collection install ansible.netcommon --force

.. _Run Your Playbook: playbook.html
