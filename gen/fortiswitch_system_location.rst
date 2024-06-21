:source: fortiswitch_system_location.py

:orphan:

.. fortiswitch_system_location:

fortiswitch_system_location -- Configure Location table in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and location category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_location</td>
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
    <li> <span class="li-head">system_location</span> - Configure Location table. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">address_civic</span> - Configure Location Civic Address. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">additional</span> - Additional location information. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">additional_code</span> - Additional code. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">block</span> - Neighborhood or block. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">branch_road</span> - Branch road name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">building</span> - Building (structure). <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">city</span> - City, township, or shi (JP). <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">city_division</span> - City division, borough, city district, ward, or chou (JP). <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">country</span> - The two-letter ISO 3166 country code in capital ASCII letters eg. US, CA, DK, DE. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">country_subdivision</span> - National subdivisions (state, canton, region, province, or prefecture). <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">county</span> - County, parish, gun (JP), or district (IN). <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">direction</span> - Leading street direction. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">floor</span> - Floor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">landmark</span> - Landmark or vanity address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">language</span> - Language. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">name</span> - Name (residence and office occupant). <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">number</span> - House number. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">number_suffix</span> - House number suffix. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">place_type</span> - Placetype. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">post_office_box</span> - Post office box (P.O. box). <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">postal_community</span> - Postal community name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">primary_road</span> - Primary road name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">road_section</span> - Road section. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">room</span> - Room number. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">script</span> - Script used to present the address information. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">seat</span> - Seat number. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">street</span> - Street. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">street_name_post_mod</span> - Street name post modifier. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">street_name_pre_mod</span> - Street name pre modifier. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">street_suffix</span> - Street suffix. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">sub_branch_road</span> - Sub branch road name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">trailing_str_suffix</span> - Trailing street suffix. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">unit</span> - Unit (apartment, suite). <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">zip</span> - Postal/zip code. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">coordinates</span> - Configure Location GPS Coordinates. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">altitude</span> - +/- Floating point no. eg. 117.47. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">altitude_unit</span> - m ( meters), f ( floors). <span class="li-normal">type: str</span> <span class="li-normal">choices: m, f</span> </li>
            <li> <span class="li-head">datum</span> - WGS84, NAD83, NAD83/MLLW . <span class="li-normal">type: str</span> <span class="li-normal">choices: WGS84, NAD83, NAD83/MLLW</span> </li>
            <li> <span class="li-head">latitude</span> - Floating point start with ( +/- )  or end with ( N or S ) eg. +/-16.67 or 16.67N. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">longitude</span> - Floating point start with ( +/- )  or end with ( E or W ) eg. +/-26.789 or 26.789E. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">elin_number</span> - Configure Location ELIN Number. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">elin_number</span> - Configure Elin Callback Number, 10 to 20 bytes numerial string. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">name</span> - Unique Location Item Name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Configure Location table.
      fortinet.fortiswitch.fortiswitch_system_location:
          state: "present"
          system_location:
              address_civic:
                  additional: "<your_own_value>"
                  additional_code: "<your_own_value>"
                  block: "<your_own_value>"
                  branch_road: "<your_own_value>"
                  building: "<your_own_value>"
                  city: "<your_own_value>"
                  city_division: "<your_own_value>"
                  country: "<your_own_value>"
                  country_subdivision: "<your_own_value>"
                  county: "<your_own_value>"
                  direction: "<your_own_value>"
                  floor: "<your_own_value>"
                  landmark: "<your_own_value>"
                  language: "<your_own_value>"
                  name: "default_name_18"
                  number: "<your_own_value>"
                  number_suffix: "<your_own_value>"
                  place_type: "<your_own_value>"
                  post_office_box: "<your_own_value>"
                  postal_community: "<your_own_value>"
                  primary_road: "<your_own_value>"
                  road_section: "<your_own_value>"
                  room: "<your_own_value>"
                  script: "<your_own_value>"
                  seat: "<your_own_value>"
                  street: "<your_own_value>"
                  street_name_post_mod: "<your_own_value>"
                  street_name_pre_mod: "<your_own_value>"
                  street_suffix: "<your_own_value>"
                  sub_branch_road: "<your_own_value>"
                  trailing_str_suffix: "<your_own_value>"
                  unit: "<your_own_value>"
                  zip: "<your_own_value>"
              coordinates:
                  altitude: "<your_own_value>"
                  altitude_unit: "m"
                  datum: "WGS84"
                  latitude: "<your_own_value>"
                  longitude: "<your_own_value>"
              elin_number:
                  elin_number: "<your_own_value>"
              name: "default_name_45"


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
