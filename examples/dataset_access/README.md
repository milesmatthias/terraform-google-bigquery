# terraform-google-bigquery multiple_tables
The multiple_tables example uses the root terraform-google-bigquery module
to deploy a single dataset and two tables with basic schemas.
This example is a good reference to understand and test the module usage.

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| dataset\_labels | A mapping of labels to assign to the table | map(string) | n/a | yes |
| expiration | TTL of tables using the dataset in MS | string | `"null"` | no |
| project\_id | Project where the dataset and table are created | string | n/a | yes |
| time\_partitioning | Configures time-based partitioning for this table | string | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| bigquery\_dataset | Bigquery dataset resource. |
| bigquery\_tables | Map of bigquery table resources being provisioned. |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Setup
Update the contents of `terraform.tfvars` to match your test environment.

## Run example
`terraform init`
`terraform plan`
`terraform apply -var-file terraform.tfvars`