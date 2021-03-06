# Module add-ons

This module is used to configure a list of add-ons to an existing cluster on IBM Cloud Infrastructure.

## Example Usage
```
provider "ibm" {
}

module "classic_kubernetes_worker_pool" {
  source = "../../../modules/configure-cluster/add-ons"

  cluster_name                    = var.cluster_name
  add_ons                         = var.add_ons
}
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name                              | Description                                           | Type   | Default | Required |
|-----------------------------------|-------------------------------------------------------|--------|---------|----------|
| cluster\_name                     | Name of the cluster                                   | string | n/a     | yes      |
| add\_ons                          | List of add_ons to attach to a cluster.               | string | n/a     | yes      |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

NOTE: We can configure the list of add-ons to be attached to a cluster by entering add-on details in input.tfvars.

## Usage

terraform apply -var-file="input.tfvars"

