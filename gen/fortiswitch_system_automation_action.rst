:source: fortiswitch_system_automation_action.py

:orphan:

.. fortiswitch_system_automation_action:

fortiswitch_system_automation_action -- Action for automation stitches in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and automation_action category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



Requirements
------------
The below requirements are needed on the host that executes this module.

- ansible>=2.15


FortiSwitch Version Compatibility
---------------------------------


.. raw:: html

 <br>
 <table border="1">
 <tr>
 <td></td><td colspan="1">Supported Version Ranges</td>
 </tr>
 <tr>
 <td>fortiswitch_system_automation_action</td>
 <td><code class="docutils literal notranslate">v7.2.1 -> 7.4.3 </code></td>
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
    <li> <span class="li-head">system_automation_action</span> - Action for automation stitches. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">accprofile</span> - Access profile for CLI script action to access FortiSwitch features. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">action_type</span> - Action type. <span class="li-normal">type: str</span> <span class="li-normal">choices: email, alert, cli-script, snmp-trap, webhook</span> </li>
        <li> <span class="li-head">alicloud_access_key_id</span> - AliCloud AccessKey ID. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">alicloud_access_key_secret</span> - AliCloud AccessKey secret. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">alicloud_account_id</span> - AliCloud account ID. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">alicloud_function</span> - AliCloud function name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">alicloud_function_authorization</span> - AliCloud function authorization type. <span class="li-normal">type: str</span> <span class="li-normal">choices: anonymous, function</span> </li>
        <li> <span class="li-head">alicloud_function_domain</span> - AliCloud function domain. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">alicloud_region</span> - AliCloud region. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">alicloud_service</span> - AliCloud service name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">alicloud_version</span> - AliCloud version. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">aws_api_id</span> - AWS API Gateway ID. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">aws_api_key</span> - AWS API Gateway API key. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">aws_api_path</span> - AWS API Gateway path. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">aws_api_stage</span> - AWS API Gateway deployment stage name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">aws_domain</span> - AWS domain. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">aws_region</span> - AWS region. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">azure_api_key</span> - Azure function API key. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">azure_app</span> - Azure function application name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">azure_domain</span> - Azure function domain. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">azure_function</span> - Azure function name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">azure_function_authorization</span> - Azure function authorization level. <span class="li-normal">type: str</span> <span class="li-normal">choices: anonymous, function, admin</span> </li>
        <li> <span class="li-head">email_body</span> - Email body. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">email_from</span> - Email sender name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">email_subject</span> - Email subject. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">email_to</span> - Email addresses. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Email address. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">gcp_function</span> - Google Cloud function name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">gcp_function_domain</span> - Google Cloud function domain. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">gcp_function_region</span> - Google Cloud function region. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">gcp_project</span> - Google Cloud Platform project name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">headers</span> - Request headers. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">header</span> - Request header. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">http_body</span> - Request body (if necessary). Should be serialized json string. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">method</span> - Request method (POST, PUT, GET, PATCH or DELETE). <span class="li-normal">type: str</span> <span class="li-normal">choices: post, put, get, patch, delete</span> </li>
        <li> <span class="li-head">minimum_interval</span> - Limit execution to no more than once in this interval (in seconds). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">port</span> - Protocol port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">protocol</span> - Request protocol. <span class="li-normal">type: str</span> <span class="li-normal">choices: http, https</span> </li>
        <li> <span class="li-head">script</span> - CLI script. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">snmp_trap</span> - SNMP trap. <span class="li-normal">type: str</span> <span class="li-normal">choices: cpu-high, mem-low, syslog-full, test-trap, fsStitchTrap1, fsStitchTrap2, fsStitchTrap3, fsStitchTrap4, fsStitchTrap5</span> </li>
        <li> <span class="li-head">uri</span> - Request API URI. <span class="li-normal">type: str</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Action for automation stitches.
      fortinet.fortiswitch.fortiswitch_system_automation_action:
          state: "present"
          system_automation_action:
              accprofile: "<your_own_value> (source system.accprofile.name)"
              action_type: "email"
              alicloud_access_key_id: "<your_own_value>"
              alicloud_access_key_secret: "<your_own_value>"
              alicloud_account_id: "<your_own_value>"
              alicloud_function: "<your_own_value>"
              alicloud_function_authorization: "anonymous"
              alicloud_function_domain: "<your_own_value>"
              alicloud_region: "<your_own_value>"
              alicloud_service: "<your_own_value>"
              alicloud_version: "<your_own_value>"
              aws_api_id: "<your_own_value>"
              aws_api_key: "<your_own_value>"
              aws_api_path: "<your_own_value>"
              aws_api_stage: "<your_own_value>"
              aws_domain: "<your_own_value>"
              aws_region: "<your_own_value>"
              azure_api_key: "<your_own_value>"
              azure_app: "<your_own_value>"
              azure_domain: "<your_own_value>"
              azure_function: "<your_own_value>"
              azure_function_authorization: "anonymous"
              email_body: "<your_own_value>"
              email_from: "<your_own_value>"
              email_subject: "<your_own_value>"
              email_to:
                  -
                      name: "default_name_29"
              gcp_function: "<your_own_value>"
              gcp_function_domain: "<your_own_value>"
              gcp_function_region: "<your_own_value>"
              gcp_project: "<your_own_value>"
              headers:
                  -
                      header: "<your_own_value>"
              http_body: "<your_own_value>"
              method: "post"
              minimum_interval: "1296000"
              name: "default_name_39"
              port: "32767"
              protocol: "http"
              script: "<your_own_value>"
              snmp_trap: "cpu-high"
              uri: "<your_own_value>"


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
    If you notice any issues in this documentation, feel free to create a pull request to improve it.
