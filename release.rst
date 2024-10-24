
Release Notes
==============================

|

Release Galaxy 1.2.5
--------------------

Release Targets
^^^^^^^^^^^^^^^

FortiSwitch Galaxy 1.2.5 is based on 1.2.4

Bug Fixes
^^^^^^^^^^^^^^^
- Fix the issue while unsetting allowaccess in `fortiswitch_system_interface`.
- Fix the issue that the session max out while running multiple playboks.

Features
^^^^^^^^^^^^^^^
- Support new version 7.6.0
- Update README.md to satisfy the latest Ansible collection requirements.
- Improve the code logic to send GET request and then POST or PUT request.
- Add `fortiswitch_json_generic` module.
- Support check_mode and diff feature for all the configuration modules.

Release Galaxy 1.2.4
--------------------

Release Targets
^^^^^^^^^^^^^^^

FortiSwitch Galaxy 1.2.4 is based on 1.2.3

Features
^^^^^^^^^^^^^^^
- Support new FortiSwitch versions 7.4.3.
- Update the supported version for the module with version number instead of latest.
- Improve the no_log logic to expose all the non-sensitive data to users.
- Add warning on the document for the module `fortiswitch_system_proxy_arp` to indicate that the module is not used for production purpose.
- Update the required Ansible version to 2.15.
- Support multiple valus for the parameter of `ip6_allowaccess` in the module of `fortiswitch_system_interface`.
- Support Ansible 2.17.

Release Galaxy 1.2.3
--------------------

Release Targets
^^^^^^^^^^^^^^^

FortiSwitch Galaxy 1.2.3 is based on 1.2.2

Features
^^^^^^^^^^^^^^^
- Support new FortiSwitch versions 7.4.2
- Update supported fortiswitch versions and parameters with version ranges instead of fixed versions

Bug Fixes
^^^^^^^^^^^^^^^
- Fix Github issues #6
- Fix errors in sanity-test and ansible-lint

Release Galaxy 1.2.2
--------------------

Release Targets
^^^^^^^^^^^^^^^

FortiSwitch Galaxy 1.2.2 is based on 1.2.1

Features
^^^^^^^^^^^^^^^
- Support new FortiSwitch version 7.4.1.
- Update the requirement.txt file to specify the sphinx_rtd_theme==1.3.0.
- Update Ansible version from 2.9.0 to 2.14.0 in the runtime.yml file.
- Format the contents in the changelog.yaml.

Release Galaxy 1.2.1
--------------------

Release Targets
^^^^^^^^^^^^^^^

FortiSwitch Galaxy 1.2.1 is based on 1.2.0

Features
^^^^^^^^^^^^^^^
- Support new FortiSwitch versions 7.2.4, 7.2.5 and 7.4.0.
- Add a ``readthedocs`` configuration file

Release Galaxy 1.2.0
--------------------

Release Targets
^^^^^^^^^^^^^^^

FortiSwitch Galaxy 1.2.0 is based on 1.1.3

Features
^^^^^^^^^^^^^^^
- Support new FortiSwitch versions 7.2.1, 7.2.2 and 7.2.3.

Release Galaxy 1.1.3
--------------------

Release Targets
^^^^^^^^^^^^^^^

FortiSwitch Galaxy 1.1.3 is based on 1.1.2

Features
^^^^^^^^^^^^^^^
- Support new FortiSwitch versions 7.0.4, 7.0.5 and 7.0.6.

Bug Fixes
^^^^^^^^^^^^^^^
- Fix Github issues #4 and #5.
- Fix errors when deleting an object.
- Fix multiple values issue in the module ``fortiswitch_system_interface``.
- Fix sanity-test errors.

Release Galaxy 1.1.2
--------------------

Release Targets
^^^^^^^^^^^^^^^

FortiSwitch Galaxy 1.1.2 is based on 1.1.1

Features
^^^^^^^^^^^^^^^
- Support check_mode for configuration modules.
- Support Diff feature in check_mode.

Bug Fixes
^^^^^^^^^^^^^^^
- Disable log information for some sensitive parameters.
- Fix bugs in the comparison function.
- Fix member_operation issue.
- Remove invalid value in a list or dict.
- Fix str_obj_has_no_attribute_items issue.


Release Galaxy 1.1.1
--------------------

Release Targets
^^^^^^^^^^^^^^^

FortiSwitch Galaxy 1.1.1 is based on 1.1.0

Bug Fixes
^^^^^^^^^^^^^^^
- Fix redundant state param in the some of the Examples.
- Support multiple values for allowaccess in the module ``fortiswitch_system_interface``.
- Fix unnecessary comprehension for FACT_DETAIL_SUBSETS.
- Add GPLv3 License.
- Use collection version in the doc section.
- Fix import errors in sanity-test.
- Fix no-log-needed errors in sanity-test.
- Fix paramter-list-no-elements errors in sanity-test.
- Support syntax for Python 2.7.
- Fix the issue of empty children in execute schema.
- Add default value for enable_log param and unify the type in both doc and spec.

Release Galaxy 1.1.0
--------------------

Release Targets
^^^^^^^^^^^^^^^

Support execute schema

Features
^^^^^^^^^^^^^^^
- Support backup, restore and other features.

Release Galaxy 1.0.1
--------------------

Release Targets
^^^^^^^^^^^^^^^

Support more FSW versions: 7.0.1, 7.0.2 and 7.0.3

Features
^^^^^^^^^^^^^^^
- Support more FSW versions: 7.0.1, 7.0.2 and 7.0.3

Release Galaxy 1.0.0
--------------------

Release Targets
^^^^^^^^^^^^^^^

It is the initial release of fortiSwitch Ansible Project.

Features
^^^^^^^^^^^^^^^
- Support all the Configuration Modules and Monitor Modules.
- Support FortiSwitch 7.0.0.
- Support fact retrieval feature, ``fortios_monitor_fact`` and ``fortios_log_fact``.
- Support Exporting playbook for configuration modules.