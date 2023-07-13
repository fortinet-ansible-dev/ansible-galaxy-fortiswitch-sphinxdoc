
Release Notes
==============================

|

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