# openshift-day2
This repo serves as a template to managed OpenShift day2 operations with the GitOps and Kustomize. Once cloned you must change it and edit it to align the files with your desired configurations.

## Structure
The repos is divided in 3 parts:
- base
- cluster-overlay
- namespace-overlay

### base
The base folder hosts the template and base resource that generally are used in day2 operations, such as resources to install operators, create machine sets and machine configs.

### overlays
These 2 folders serves as example of how the repos can be used to manage configuration with GitOps and Kustomize.
namespace-overaly contains namespace-wide resources such as machine sets, while cluster-overlay contains cluster-wide resource such as machine configs.

Some subfolders may contains a resource folder in addition to the patches folder. In this case the resource folder is thought to contain the manifest yaml of a resource that already exists in the cluster after installation, but needs to be patched (for example, the DNS Operator instance already exists in the cluster, but may require patching to add some tolerations).
