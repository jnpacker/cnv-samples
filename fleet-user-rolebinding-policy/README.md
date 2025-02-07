# Applying RBAC to ACM managed CNV clusters
OpenShift Virtualization has three predefined roles that you can bind to users or groups.
  * kubevirt.io:view
  * kubevirt.io:edit
  * kubevirt.io:admin

When OIDC is configured, supplying a `RoleBinding` or `ClusterRoleBinding`, with the **subject** and **clusterRole / role** allows the subject access to virtual machines in a namespace or on the cluster. The included policy assigns oidc users as **subjects** in a `clusterRoleBinding` (cluster wide) with the **ClusterRole** permissions of **kubevirt.io:edit**. Subjects are either User or Group objects on the OpenShift cluster. The subject does not need to exist when the `RoleBinding` is defined, and by default, all OIDC's will create the user after authenticating appropriately.

Any cluster that used the OpenShift Virtualization operator policy to deploy itself, by adding the label `acm/cnv-operator-install: "true"` will also receive the `clusterRoleBinding` and **Users** defined in this policy.

### Deploythe policy
```
  oc apply -f ./acm-kubevirt-edit-fleet.yaml
```