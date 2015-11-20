

A quick and dirty, crude set of integration tests to demonstrate and
help define the behavior of ansible inventory host variables.

In the behavior of hosts mentioned explicitly among differnet
inventory sources doesn't appear to be defined.

  ./run_all

will create and inventories/ directory containing inventory subdirs used as fixtures.

Wading through the example_results currently shows inconsistencies between:

* ansible (ADHOC) and ansible-playbook
* top-level job variables and hostvars[hostname]
* variables defined in dynamic inventories vs static (e.g. variables from dynamic inventories 
  can make it into hostvars[hostname] via magic variables).

TODO

* implement the driver in ansible itself (although it is awkward to get stdoutput and variables
  out of an ansible processes).
