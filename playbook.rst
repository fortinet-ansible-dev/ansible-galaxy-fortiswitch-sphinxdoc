
Run Your First Playbook
==============================

This document explains how to run your first FortiSwitch Ansible playbook.

--------------

With FortiSwitch Galaxy collection, you are always recommended to run
FortiSwitch module in ``httpapi`` manner. The first step is to prepare your
host inventory with which you can use ``ansible-vault`` to encrypt or
decrypt your secrets for the sake of confidentiality.

Prepare host inventory
~~~~~~~~~~~~~~~~~~~~~~

in our case we create a file named ``hosts``:

::

   [fortiswitches]
   fortiswitch01 ansible_host=192.168.190.130 ansible_user="admin" ansible_password="password"
   fortiswitch02 ansible_host=192.168.190.131 ansible_user="admin" ansible_password="password"

   [fortiswitches:vars]
   ansible_network_os=fortinet.fortiswitch.fortiswitch


Write the playbook
~~~~~~~~~~~~~~~~~~

in the example: ``test.yml`` we are going to modify the fortiSwitch configurations.
device’s hostname:

::

   - hosts: fortiswitch01
     collections:
     - fortinet.fortiswitch
     connection: httpapi
     gather_facts: 'no'
     vars:
       ansible_httpapi_use_ssl: true
       ansible_httpapi_validate_certs: false
       ansible_httpapi_port: 443
     tasks:
     - name: Only https allow access to the device.
       fortiswitch_system_interface:
         state: present
         system_interface:
           name: internal
           vdom: root
           allowaccess:
             - https
             - http
             - ssh
             - ping

there are several options which might need you special care:

-  **connection** : ``httpapi`` is preferred.
-  **collections** : The namespace must be ``fortinet.fortiswitch``
-  **ansible_httpapi_use_ssl** and **ansible_httpapi_port**: by
   default when your fortiSwitch device is licensed, the https is enabled.

Run the playbook
~~~~~~~~~~~~~~~~

::

   ansible-playbook -i hosts test.yml

you can also observe the verbose output by adding option at the tail:
``-vvv``.

.. _FortiSwitch API Spec: https://fndn.fortinet.net/index.php?/fortiapi/44-fortiswitch/
