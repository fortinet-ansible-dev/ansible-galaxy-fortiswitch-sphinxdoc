:source: fortiswitch_router_static6.py

:orphan:

.. fortiswitch_router_static6:

fortiswitch_router_static6 -- Ipv6 static routes configuration in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify router feature and static6 category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_router_static6</td>
 <td><code class="docutils literal notranslate">v7.0.0 -> 7.4.3 </code></td>
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
    <li> <span class="li-head">router_static6</span> - Ipv6 static routes configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">bfd</span> - Bidirectional Forwarding Detection (BFD). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">blackhole</span> - Enable/disable black hole. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">comment</span> - comment <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">device</span> - Gateway out interface. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">devindex</span> - devindex <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">distance</span> - Administrative distance (1-255). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dst</span> - Destination IPv6 prefix for this route. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">gateway</span> - Gateway IPv6 address for this route. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">seq_num</span> - entry No. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">status</span> - Status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">vrf</span> - VRF. <span class="li-normal">type: str</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Ipv6 static routes configuration.
      fortinet.fortiswitch.fortiswitch_router_static6:
          state: "present"
          router_static6:
              bfd: "enable"
              blackhole: "enable"
              comment: "comment"
              device: "<your_own_value> (source system.interface.name)"
              devindex: "7"
              distance: "127"
              dst: "<your_own_value>"
              gateway: "<your_own_value>"
              seq_num: "<you_own_value>"
              status: "enable"
              vrf: "<your_own_value> (source router.vrf.name)"


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
