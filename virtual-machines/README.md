# Virtual Machine YAML definitions

Before applying the YAML, make the following changes:
  1. Change the virtual machine name
  2. Set the `password` and `ssh_authorized_keys`(optional) in the `userData` section
  3. Apply the yaml with `oc apply -f`