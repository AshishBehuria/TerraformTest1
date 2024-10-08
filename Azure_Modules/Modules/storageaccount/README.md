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
| [azurerm_key_vault_access_policy.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/key_vault_access_policy) | resource |
| [azurerm_key_vault_key.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/key_vault_key) | resource |
| [azurerm_key_vault_secret.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/key_vault_secret) | resource |
| [azurerm_storage_account.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_account) | resource |
| [azurerm_storage_account_customer_managed_key.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_account_customer_managed_key) | resource |
| [azurerm_storage_blob.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_blob) | resource |
| [azurerm_storage_container.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_container) | resource |
| [azurerm_storage_queue.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_queue) | resource |
| [azurerm_storage_share.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_share) | resource |
| [azurerm_storage_table.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_table) | resource |
| [null_resource.dependency_modules](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [null_resource.dependency_sa](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [null_resource.this](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [azurerm_client_config.current](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/client_config) | data source |
| [azurerm_resource_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/resource_group) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_blobs"></a> [blobs](#input\_blobs) | Map of Storage Blobs | <pre>map(object({<br>    name                   = string<br>    storage_account_name   = string<br>    storage_container_name = string<br>    type                   = string<br>    size                   = number<br>    content_type           = string<br>    source_uri             = string<br>    metadata               = map(any)<br>  }))</pre> | `{}` | no |
| <a name="input_containers"></a> [containers](#input\_containers) | Map of Storage Containers | <pre>map(object({<br>    name                  = string<br>    storage_account_name  = string<br>    container_access_type = string<br>  }))</pre> | `{}` | no |
| <a name="input_dependencies"></a> [dependencies](#input\_dependencies) | Specifies the modules that the Storage Account Resource depends on. | `list(any)` | `[]` | no |
| <a name="input_file_shares"></a> [file\_shares](#input\_file\_shares) | Map of Storages File Shares | <pre>map(object({<br>    name                 = string<br>    storage_account_name = string<br>    quota                = number<br>  }))</pre> | `{}` | no |
| <a name="input_key_vault_id"></a> [key\_vault\_id](#input\_key\_vault\_id) | The ID of the Key Vault from which all Secrets should be sourced | `string` | n/a | yes |
| <a name="input_queues"></a> [queues](#input\_queues) | Map of Storages Queues | <pre>map(object({<br>    name                 = string<br>    storage_account_name = string<br>  }))</pre> | `{}` | no |
| <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name) | The name of the resource group in which to create the storage account | `string` | n/a | yes |
| <a name="input_sa_additional_tags"></a> [sa\_additional\_tags](#input\_sa\_additional\_tags) | Tags of the SA in addition to the resource group tag. | `map(string)` | `{}` | no |
| <a name="input_storage_accounts"></a> [storage\_accounts](#input\_storage\_accounts) | Map of storage accouts which needs to be created in a resource group | <pre>map(object({<br>    name            = string<br>    sku             = string<br>    account_kind    = string<br>    access_tier     = string<br>    assign_identity = bool<br>    cmk_enable      = bool<br>    network_rules = object({<br>      bypass                     = list(string) # (Optional) Specifies whether traffic is bypassed for Logging/Metrics/AzureServices. Valid options are any combination of Logging, Metrics, AzureServices, or None.<br>      default_action             = string       # (Required) The Default Action to use when no rules match from ip_rules / virtual_network_subnet_ids. Possible values are Allow and Deny.<br>      ip_rules                   = list(string) # (Optional) One or more IP Addresses, or CIDR Blocks which should be able to access the Key Vault.<br>      virtual_network_subnet_ids = list(string) # (Optional) One or more Subnet ID's which should be able to access this Key Vault.<br>    })<br>    enable_large_file_share = bool<br>  }))</pre> | `{}` | no |
| <a name="input_tables"></a> [tables](#input\_tables) | Map of Storage Tables | <pre>map(object({<br>    name                 = string<br>    storage_account_name = string<br>  }))</pre> | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_blob_ids"></a> [blob\_ids](#output\_blob\_ids) | n/a |
| <a name="output_blob_urls"></a> [blob\_urls](#output\_blob\_urls) | n/a |
| <a name="output_container_ids"></a> [container\_ids](#output\_container\_ids) | n/a |
| <a name="output_depended_on_sa"></a> [depended\_on\_sa](#output\_depended\_on\_sa) | n/a |
| <a name="output_file_share_ids"></a> [file\_share\_ids](#output\_file\_share\_ids) | n/a |
| <a name="output_file_share_urls"></a> [file\_share\_urls](#output\_file\_share\_urls) | n/a |
| <a name="output_primary_access_keys"></a> [primary\_access\_keys](#output\_primary\_access\_keys) | n/a |
| <a name="output_primary_access_keys_map"></a> [primary\_access\_keys\_map](#output\_primary\_access\_keys\_map) | n/a |
| <a name="output_primary_blob_endpoints"></a> [primary\_blob\_endpoints](#output\_primary\_blob\_endpoints) | n/a |
| <a name="output_primary_blob_endpoints_map"></a> [primary\_blob\_endpoints\_map](#output\_primary\_blob\_endpoints\_map) | n/a |
| <a name="output_primary_connection_strings"></a> [primary\_connection\_strings](#output\_primary\_connection\_strings) | n/a |
| <a name="output_primary_connection_strings_map"></a> [primary\_connection\_strings\_map](#output\_primary\_connection\_strings\_map) | n/a |
| <a name="output_sa_ids"></a> [sa\_ids](#output\_sa\_ids) | n/a |
| <a name="output_sa_ids_map"></a> [sa\_ids\_map](#output\_sa\_ids\_map) | n/a |
| <a name="output_sa_names"></a> [sa\_names](#output\_sa\_names) | n/a |
