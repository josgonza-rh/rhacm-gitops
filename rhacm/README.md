## To use the policies on this repo just follow the steps

Issue this command:

```bash
oc apply -k deploy/
```

or

```bash
kubectl apply -k deploy/
```

This will create a namespace called `rhacm-policies` and will deploy the policies stored here:
[policies](grc/policies/CM-Configuration-Management).

### Configuration Management

Policy  | Description | Prerequisites
------- | ----------- | -------------
[Install OpenShift-Gitops](./grc/policies/CM-Configuration-Management/policy-openshift-gitops-operator-patched.yaml) | Use this policy to install the Red Hat OpenShift GitOps (Argo CD) | Requires OpenShift 4.x. Check the [documentation](https://access.redhat.com/documentation/en-us/openshift_container_platform/4.10/html/cicd/gitops) for more information.
[Configuring Managed Clusters for OpenShift GitOps operator and Argo CD](./grc/policies/CM-Configuration-Management/policy-openshift-gitops-operator-patched.yaml) | Register a set of one or more ACM managed clusters to an instance of Argo CD | Requires OpenShift (*)
[Configuring Managed Clusters for OpenShift GitOps operator and Argo CD](./grc/policies/CM-Configuration-Management/policy-label-cluster.yaml) | Adding cluster to **all-openshift-clusters** `ManagedClusterSet` | Just for `local-cluster`

> ![NOTE](../images/note-icon.png) **(*) NOTE**: Only `OpenShift` clusters are registered to an `Argo CD`, not other Kubernetes clusters.
