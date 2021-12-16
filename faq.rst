
Frequently Asked Questions (FAQ)
================================

|

**TABLE OF CONTENTS:**
 - `How to export the current settings of a module into a playbook?`_

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
      ansible_httpapi_use_ssl: yes
      ansible_httpapi_validate_certs: no
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


.. _Run Your Playbook: playbook.html
