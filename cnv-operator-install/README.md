# Install OpenShift Virtualization operator in the Fleet

This Policy for Red Hat Advanced Cluster Management for Kubernetes(ACM) includes an Operator policy kind. This policy kind deploys Red Hat operators on clusters managed by ACM (ManagedClusters). ACM uses labels to decide where to apply the Operator policy, which deploys the OpenShift Virtualization operator in this case. This is done by applying the label `acm/cnv-operator-install: "true"` to a ManagedCluster in ACM.

### Deploy the Policy
Apply the policy to the ACM Hub, then add the label `acm/cnv-operator-install: "true"` to the ManagedClusters where you want CNV deployed.
```
oc apply -f ./
```

You may customize the hyperconverged settings in the `policy.yaml` file. Where you will find:
  1. Subscription resource details
  2. ClusterServiceVersion resource details
  3. HyperConverged resource details
  4. HostPathProvisioner resource details
  5. Other status checks that validate the OpenShift Virtualization operator deployed correctly.
  6. NEW resources can be added to policy to customize the deployment of OpenShift Virtualization

To customize any of these resources in the policy, refer to the [OpenShift Virtualization documentation](https://docs.openshift.com/container-platform/4.17/virt/install/installing-virt.html#virt-subscribing-cli_installing-virt).

Note: The policy is keyed to `v4.17.3`
