:source: fortiswitch_switch_qos_qos_policy.py

:orphan:

.. fortiswitch_switch_qos_qos_policy:

fortiswitch_switch_qos_qos_policy -- QOS egress policy in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch_qos feature and qos_policy category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



Requirements
------------
The below requirements are needed on the host that executes this module.

- ansible>=2.11


FortiSW Version Compatibility
-----------------------------


.. raw:: html

 <br>
 <table>
 <tr>
 <td></td>
 <td><code class="docutils literal notranslate">v7.0.0 </code></td>
 <td><code class="docutils literal notranslate">v7.0.1 </code></td>
 <td><code class="docutils literal notranslate">v7.0.2 </code></td>
 <td><code class="docutils literal notranslate">v7.0.3 </code></td>
 </tr>
 <tr>
 <td>fortiswitch_switch_qos_qos_policy</td>
 <td>yes</td>
 <td>yes</td>
 <td>yes</td>
 <td>yes</td>
 </tr>
 </table>
 <p>



Parameters
----------


.. raw:: html

    <ul>
    <li> <span class="li-head">enable_log</span> - Enable/Disable logging for task. <span class="li-normal">type: bool</span> <span class="li-required">required: false</span> <span class="li-normal">default: False</span> </li>
    <li> <span class="li-head">member_path</span> - Member attribute path to operate on. <span class="li-normal">type: str</span> </li>
    <li> <span class="li-head">member_state</span> - Add or delete a member under specified attribute path. <span class="li-normal">type: str</span> <span class="li-normal">choices: present, absent</span> </li>
    <li> <span class="li-head">state</span> - Indicates whether to create or remove the object. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> <span class="li-normal">choices: present, absent</span> </li>
    <li> <span class="li-head">switch_qos_qos_policy</span> - QOS egress policy. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">cos_queue</span> - COS queue configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">description</span> - Description of the COS queue. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">drop_policy</span> - COS queue drop policy. <span class="li-normal">type: str</span> <span class="li-normal">choices: taildrop, weighted-random-early-detection</span> </li>
            <li> <span class="li-head">ecn</span> - Update frame IP ECN field in lieu of packet drop. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">max_rate</span> - Maximum rate (kbps). 0 to disable. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">max_rate_percent</span> - Maximum rate (% of link speed). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">min_rate</span> - Minimum rate (kbps). 0 to disable. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">min_rate_percent</span> - Minimum rate (% of link speed). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">name</span> - COS queue ID. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">weight</span> - Weight of weighted round robin scheduling. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">wred_slope</span> - Slope of WRED drop probability. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">name</span> - QOS policy name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">rate_by</span> - COS queue rate by kbps or percent. <span class="li-normal">type: str</span> <span class="li-normal">choices: kbps, percent</span> </li>
        <li> <span class="li-head">schedule</span> - COS queue scheduling. <span class="li-normal">type: str</span> <span class="li-normal">choices: strict, round-robin, weighted</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - hosts: fortiswitch01
      collections:
        - fortinet.fortiswitch
      connection: httpapi
      vars:
       ansible_httpapi_use_ssl: yes
       ansible_httpapi_validate_certs: no
       ansible_httpapi_port: 443
      tasks:
      - name: QOS egress policy.
        fortiswitch_switch_qos_qos_policy:
          state: "present"
          switch_qos_qos_policy:
            cos_queue:
             -
                description: "<your_own_value>"
                drop_policy: "taildrop"
                ecn: "disable"
                max_rate: "7"
                max_rate_percent: "8"
                min_rate: "9"
                min_rate_percent: "10"
                name: "default_name_11"
                weight: "12"
                wred_slope: "13"
            name: "default_name_14"
            rate_by: "kbps"
            schedule: "strict"
    


Return Values
-------------
Common return values are documented: https://docs.ansible.com/ansible/latest/reference_appendices/common_return_values.html#common-return-values, the following are the fields unique to this module:

.. raw:: html

    <ul>

    <li> <span class="li-return">build</span> - Build number of the fortiSwitch image <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 1547</span></li>
    <li> <span class="li-return">http_method</span> - Last method used to provision the content into FortiSwitch <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: PUT</span></li>
    <li> <span class="li-return">http_status</span> - Last result given by FortiSwitch on last operation applied <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 200</span></li>
    <li> <span class="li-return">mkey</span> - Master key (id) used in the last call to FortiSwitch <span class="li-normal">returned: success</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: id</span></li>
    <li> <span class="li-return">name</span> - Name of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: urlfilter</span></li>
    <li> <span class="li-return">path</span> - Path of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: webfilter</span></li>
    <li> <span class="li-return">serial</span> - Serial number of the unit <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: FS1D243Z13000122</span></li>
    <li> <span class="li-return">status</span> - Indication of the operation's result <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: success</span></li>
    <li> <span class="li-return">version</span> - Version of the FortiSwitch <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: v7.0.0</span></li>
    </ul>

Status
------

- This module is not guaranteed to have a backwards compatible interface.


Authors
-------

- Link Zheng (@chillancezen)
- Jie Xue (@JieX19)
- Hongbin Lu (@fgtdev-hblu)
- Frank Shen (@frankshen01)
- Miguel Angel Munoz (@mamunozgonzalez)


.. hint::
    If you notice any issues in this documentation, you can create a pull request to improve it.
