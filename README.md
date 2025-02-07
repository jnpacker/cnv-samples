# cnv-samples
### Samples to use with ACM and Container Native Virtualization:
  * Roll out the OpenShift Virtualization operator to the fleet
  * Manage kubevirt.io:Edit/View/Admin roles on clusters where the OpenShift Virtualization operator is deployed
  * YAML definitions for Virtual Machines (using ephemral and persistent PVC's)

### Index
  * [ACM Operator Policy to install Virtualization](./cnv-operator-install)
  * [RBAC Policies for OpenShift Virtualization users](./fleet-user-rolebinding-policy)
  * [Virtual Machine YAML](./virtual-machines)

### Before you begin
ACM Hub refers to an OpenShift cluster with Red Hat Advanced Cluster Management for Kubernetes installed
CNV refers to Container Native Virtualization from Red Hat
RHOV refers to Red Hat OpenShift Virtualization
Operator Red Hat packaging of containerized sofware for OpenShift
ManagedCluster is an OpenShift or STaR-K8s cluster that has the ACM agent and ACM agent addons running on it (the cluster is managed by ACM).
Virtual Machine is a software based container with an OS running on/in it that mimics a baremetal computer(server).
