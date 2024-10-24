:source: fortiswitch_json_generic.py

:orphan:

.. :

.. _fortiswitch_json_generic:

fortiswitch_json_generic -- Configure Fortinet's FortiSwitch with json generic method.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. contents::
   :local:
   :depth: 1


Synopsis
--------
This module is able to configure a FortiSwitch device by allowing the user to set any category supported by FortiAPI with raw json. All parameters and values included in examples need to be adjusted to datasources before usage.


Requirements
-------------
The below requirements are needed on the host that executes this module.

- install galaxy collection ``fortinet.fortiswitch`` >= 1.2.5


Parameters
----------

.. raw:: html

    <ul>

    <li> <span class="li-head">enable_log</span> - Enable/Disable logging for task. <span class="li-normal">type: bool</span> <span class="li-required">required: False</span> <span class="li-normal">default: False</span> </li>
    <li><span class="li-head">json_generic</span> - json generic <span class="li-normal">default: null</span> <span class="li-normal">type: dict</span></li>
            <ul class="ul-self">
            <li><span class="li-head">dictbody</span> - Body with YAML list of key/value format <span class="li-normal">type: dict</span></li>
            <li><span class="li-head">jsonbody</span> - Body with JSON string format, will always give priority to jsonbody <span class="li-normal">type: str</span></li>
            <li><span class="li-head">method</span> - HTTP methods <span class="li-normal">type: str</span> <span class="li-normal">choices: GET,  PUT,  POST,  DELETE</span></li>
            <li><span class="li-head">path</span> - URL path, e.g./api/v2/cmdb/firewall/address <span class="li-normal">type: str</span></li>
            <li><span class="li-head">specialparams</span> - Extra URL parameters, e.g.start=1&count=10 <span class="li-normal">type: str</span>
            </ul>

    </ul>




Examples
--------

**host**

.. code-block:: yaml+jinja

    [fortiswitches]
    fortiswitch01 ansible_host=192.168.52.177 ansible_user="admin" ansible_password="your_password"

    [fortiswitches:vars]
    ansible_network_os=fortinet.fortiswitch.fortiswitch


**sample1.yml**

.. code-block:: yaml+jinja

    ---
    - hosts: fortiswitches
      connection: httpapi
      collections:
        - fortinet.fortiswitch
      vars:
       ansible_httpapi_use_ssl: true
       ansible_httpapi_validate_certs: false
       ansible_httpapi_port: 443

      tasks:
      - name: test add with string
        fortiswitch_json_generic:
          enable_log: True
          json_generic:
            method: "PUT"
            path: "/api/v2/cmdb/system/global"
            jsonbody: |
              {
                "timezone": "04"
              }
        register: info

      - name: display vars
        debug: msg="{{info}}"




Return Values
-------------
Common return values are documented: https://docs.ansible.com/ansible/latest/reference_appendices/common_return_values.html#common-return-values, the following are the fields unique to this module:

.. raw:: html

    <ul>

    <li><span class="li-return">build</span> - Build number of the fortiswitch image <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: '1547'</span></li>
    <li><span class="li-return">http_method</span> - Last method used to provision the content into FortiSwitch <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 'PUT'</span></li>
    <li><span class="li-return">http_status</span> - Last result given by FortiSwitch on last operation applied <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 200</span></li>
    <li><span class="li-return">mkey</span> - Master key (id) used in the last call to FortiSwitch <span class="li-normal">returned: success</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: id</span></li>
    <li><span class="li-return">name</span> - Name of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: urlfilter</span></li>
    <li><span class="li-return">path</span> - Path of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: webfilter</span></li>
    <li><span class="li-return">revision</span> - Internal revision number <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 17.0.2.10658</span></li>
    <li><span class="li-return">serial</span> - Serial number of the unit <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: FSVMEVYYQT3AB5352</span></li>
    <li><span class="li-return">status</span> - Indication of the operation's result <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: success</span></li>
    <li><span class="li-return">version</span> - Version of the FortiSwitch <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: v7.0.0</span></li>
    </ul>


Authors
-------
- Link Zheng (@chillancezen)
- Jie Xue (@JieX19)
- Frank Shen (@fshen01)
- Hongbin Lu (@fgtdev-hblu)




Warning
-------
It's preferred to use ``FortiSwitch Ansible Collection Included Modules`` unless some features are not available there.