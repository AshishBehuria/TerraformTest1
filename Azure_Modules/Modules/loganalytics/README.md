## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | n/a |
| <a name="provider_null"></a> [null](#provider\_null) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [azurerm_key_vault_secret.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/key_vault_secret) | resource |
| [azurerm_log_analytics_solution.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/log_analytics_solution) | resource |
| [azurerm_log_analytics_workspace.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/log_analytics_workspace) | resource |
| [null_resource.dependency_modules](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [azurerm_resource_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/resource_group) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_dependencies"></a> [dependencies](#input\_dependencies) | Specifies the modules that the Log Analytics Workspace Resource depends on. | `list(any)` | `[]` | no |
| <a name="input_key_vault_id"></a> [key\_vault\_id](#input\_key\_vault\_id) | The Id of the Key Vault to which all secrets should be stored | `string` | n/a | yes |
| <a name="input_law_additional_tags"></a> [law\_additional\_tags](#input\_law\_additional\_tags) | A mapping of tags to assign to the resource. | `map(string)` | `{}` | no |
| <a name="input_name"></a> [name](#input\_name) | Specifies the name of the Log Analytics Workspace | `string` | n/a | yes |
| <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name) | The name of the resource group in which the Log Analytics workspace is created | `string` | n/a | yes |
| <a name="input_retention_in_days"></a> [retention\_in\_days](#input\_retention\_in\_days) | The workspace data retention in days. Possible values range between 30 and 730 | `string` | n/a | yes |
| <a name="input_sku"></a> [sku](#input\_sku) | Specifies the Sku of the Log Analytics Workspace. Possible values are Free, PerNode, Premium, Standard, Standalone, Unlimited, and PerGB2018 | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_law_id"></a> [law\_id](#output\_law\_id) | n/a |
| <a name="output_law_id_map"></a> [law\_id\_map](#output\_law\_id\_map) | n/a |
| <a name="output_law_key"></a> [law\_key](#output\_law\_key) | n/a |
| <a name="output_law_name"></a> [law\_name](#output\_law\_name) | n/a |
| <a name="output_law_workspace"></a> [law\_workspace](#output\_law\_workspace) | n/a |
| <a name="output_law_workspace_id"></a> [law\_workspace\_id](#output\_law\_workspace\_id) | n/a |
