## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | ~> 0.12.20 |
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | ~> 2.14.0 |
| <a name="requirement_template"></a> [template](#requirement\_template) | ~> 2.2.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | ~> 2.14.0 |
| <a name="provider_null"></a> [null](#provider\_null) | n/a |
| <a name="provider_tls"></a> [tls](#provider\_tls) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [azurerm_availability_set.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/availability_set) | resource |
| [azurerm_backup_protected_vm.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/backup_protected_vm) | resource |
| [azurerm_disk_encryption_set.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/disk_encryption_set) | resource |
| [azurerm_key_vault_access_policy.cmk](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/key_vault_access_policy) | resource |
| [azurerm_key_vault_access_policy.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/key_vault_access_policy) | resource |
| [azurerm_key_vault_key.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/key_vault_key) | resource |
| [azurerm_key_vault_secret.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/key_vault_secret) | resource |
| [azurerm_linux_virtual_machine.linux_vms](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/linux_virtual_machine) | resource |
| [azurerm_managed_disk.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/managed_disk) | resource |
| [azurerm_network_interface.linux_nics](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/network_interface) | resource |
| [azurerm_network_interface.windows_nics](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/network_interface) | resource |
| [azurerm_network_interface_application_gateway_backend_address_pool_association.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/network_interface_application_gateway_backend_address_pool_association) | resource |
| [azurerm_network_interface_application_security_group_association.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/network_interface_application_security_group_association) | resource |
| [azurerm_network_interface_backend_address_pool_association.linux_nics_with_internal_backend_pools](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/network_interface_backend_address_pool_association) | resource |
| [azurerm_network_interface_backend_address_pool_association.windows_nics_with_internal_backend_pools](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/network_interface_backend_address_pool_association) | resource |
| [azurerm_network_interface_nat_rule_association.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/network_interface_nat_rule_association) | resource |
| [azurerm_virtual_machine_data_disk_attachment.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_machine_data_disk_attachment) | resource |
| [azurerm_virtual_machine_extension.blob_custom_script](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_machine_extension) | resource |
| [azurerm_virtual_machine_extension.custom_script](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_machine_extension) | resource |
| [azurerm_virtual_machine_extension.log_analytics](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_machine_extension) | resource |
| [azurerm_virtual_machine_extension.network_watcher](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_machine_extension) | resource |
| [azurerm_virtual_machine_extension.storage](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_machine_extension) | resource |
| [azurerm_virtual_machine_extension.vm_insights](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_machine_extension) | resource |
| [azurerm_windows_virtual_machine.windows_vms](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/windows_virtual_machine) | resource |
| [null_resource.dependency_modules](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [tls_private_key.this](https://registry.terraform.io/providers/hashicorp/tls/latest/docs/resources/private_key) | resource |
| [azurerm_client_config.current](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/client_config) | data source |
| [azurerm_resource_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/resource_group) | data source |
| [azurerm_storage_account.custom_script_storage_account](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/storage_account) | data source |
| [azurerm_storage_account.diagnostics_storage_account](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/storage_account) | data source |
| [azurerm_storage_account_sas.diagnostics_storage_account_sas](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/storage_account_sas) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_administrator_login_password"></a> [administrator\_login\_password](#input\_administrator\_login\_password) | Specifies the password associated with the local administrator account | `string` | `null` | no |
| <a name="input_administrator_user_name"></a> [administrator\_user\_name](#input\_administrator\_user\_name) | Specifies the name of the local administrator account | `string` | n/a | yes |
| <a name="input_app_security_group_ids_map"></a> [app\_security\_group\_ids\_map](#input\_app\_security\_group\_ids\_map) | Specifies the Map of network interfaces Application Security Group Id's | `map(string)` | `{}` | no |
| <a name="input_application_gateway_backend_pool_ids_map"></a> [application\_gateway\_backend\_pool\_ids\_map](#input\_application\_gateway\_backend\_pool\_ids\_map) | Specifies the Map of network interfaces Application Gateway Backend Address Pool Id's | `map(string)` | `{}` | no |
| <a name="input_application_gateway_backend_pools"></a> [application\_gateway\_backend\_pools](#input\_application\_gateway\_backend\_pools) | Specifies the Map of Application Gateway Backend Address Pool Names by Application Gateway Name | `map(list(string))` | `{}` | no |
| <a name="input_availability_sets"></a> [availability\_sets](#input\_availability\_sets) | Map containing availability set configurations | <pre>map(object({<br>    name                         = string<br>    platform_update_domain_count = number<br>    platform_fault_domain_count  = number<br>  }))</pre> | `{}` | no |
| <a name="input_dependencies"></a> [dependencies](#input\_dependencies) | Specifies the modules that the Virtual Machine Resource depends on. | `list(any)` | `[]` | no |
| <a name="input_diagnostics_sa_name"></a> [diagnostics\_sa\_name](#input\_diagnostics\_sa\_name) | The name of diagnostics storage account | `string` | n/a | yes |
| <a name="input_key_vault_id"></a> [key\_vault\_id](#input\_key\_vault\_id) | The Id of the Key Vault to which all secrets should be stored | `string` | n/a | yes |
| <a name="input_law_workspace_id"></a> [law\_workspace\_id](#input\_law\_workspace\_id) | Log analytics workspace resource workspace id | `string` | n/a | yes |
| <a name="input_law_workspace_key"></a> [law\_workspace\_key](#input\_law\_workspace\_key) | Log analytics workspace primary shared key | `string` | n/a | yes |
| <a name="input_lb_backend_address_pool_map"></a> [lb\_backend\_address\_pool\_map](#input\_lb\_backend\_address\_pool\_map) | Map of network interfaces internal load balancers backend pool id's | `map(string)` | `{}` | no |
| <a name="input_lb_nat_rule_map"></a> [lb\_nat\_rule\_map](#input\_lb\_nat\_rule\_map) | Map of network interfaces to LB NAT rules | `map(string)` | `{}` | no |
| <a name="input_linux_image_ids"></a> [linux\_image\_ids](#input\_linux\_image\_ids) | Specifies the Map of image Id's from which the Virtual Machines should be created. | `map(string)` | `{}` | no |
| <a name="input_linux_vm_nics"></a> [linux\_vm\_nics](#input\_linux\_vm\_nics) | n/a | <pre>map(object({<br>    name                          = string<br>    subnet_name                   = string<br>    internal_dns_name_label       = string<br>    enable_ip_forwarding          = bool<br>    enable_accelerated_networking = bool<br>    dns_servers                   = list(string)<br>    nic_ip_configurations = list(object({<br>      name      = string<br>      static_ip = string<br>    }))<br>  }))</pre> | n/a | yes |
| <a name="input_linux_vms"></a> [linux\_vms](#input\_linux\_vms) | Map containing Linux VM objects | <pre>map(object({<br>    name                             = string<br>    vm_size                          = string<br>    zone                             = string<br>    assign_identity                  = bool<br>    lb_backend_pool_names            = list(string)<br>    vm_nic_keys                      = list(string)<br>    avaialability_set_key            = string<br>    lb_nat_rule_names                = list(string)<br>    app_security_group_names         = list(string)<br>    app_gateway_name                 = string<br>    disable_password_authentication  = bool<br>    source_image_reference_publisher = string<br>    source_image_reference_offer     = string<br>    source_image_reference_sku       = string<br>    source_image_reference_version   = string<br>    storage_os_disk_caching          = string<br>    managed_disk_type                = string<br>    disk_size_gb                     = number<br>    write_accelerator_enabled        = bool<br>    recovery_services_vault_key      = string<br>    enable_cmk_disk_encryption       = bool<br>    custom_data_path                 = string<br>    custom_data_args                 = map(string)<br>    diagnostics_storage_config_path  = string<br>    custom_script = object({<br>      commandToExecute   = string<br>      scriptPath         = string<br>      scriptArgs         = map(string)<br>      fileUris           = list(string)<br>      storageAccountName = string<br>    })<br>  }))</pre> | `{}` | no |
| <a name="input_managed_data_disks"></a> [managed\_data\_disks](#input\_managed\_data\_disks) | Map containing storage data disk configurations | <pre>map(object({<br>    disk_name                 = string<br>    vm_key                    = string<br>    lun                       = string<br>    storage_account_type      = string<br>    disk_size                 = number<br>    caching                   = string<br>    write_accelerator_enabled = bool<br>    create_option             = string<br>    os_type                   = string<br>    source_resource_id        = string<br>  }))</pre> | `{}` | no |
| <a name="input_recovery_services_vaults"></a> [recovery\_services\_vaults](#input\_recovery\_services\_vaults) | Map of recovery services vaults | `map(any)` | `null` | no |
| <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name) | Specifies the name of the Resource Group in which the Virtual Machine should exist | `string` | n/a | yes |
| <a name="input_sa_bootdiag_storage_uri"></a> [sa\_bootdiag\_storage\_uri](#input\_sa\_bootdiag\_storage\_uri) | Azure Storage Account Primary Queue Service Endpoint. | `string` | n/a | yes |
| <a name="input_subnet_ids"></a> [subnet\_ids](#input\_subnet\_ids) | Map of network interfaces subnets | `map(string)` | `{}` | no |
| <a name="input_vm_additional_tags"></a> [vm\_additional\_tags](#input\_vm\_additional\_tags) | A mapping of tags to assign to the resource | `map(string)` | `{}` | no |
| <a name="input_windows_image_id"></a> [windows\_image\_id](#input\_windows\_image\_id) | Specifies the Id of the image which this Virtual Machine should be created from | `string` | `null` | no |
| <a name="input_windows_vms"></a> [windows\_vms](#input\_windows\_vms) | Map containing windows vm's | <pre>map(object({<br>    name                             = string<br>    vm_size                          = string<br>    zones                            = string<br>    assign_identity                  = bool<br>    subnet_name                      = string<br>    lb_backend_pool_name             = string<br>    source_image_reference_publisher = string<br>    source_image_reference_offer     = string<br>    source_image_reference_sku       = string<br>    source_image_reference_version   = string<br>    storage_os_disk_caching          = string<br>    managed_disk_type                = string<br>    disk_size_gb                     = number<br>    write_accelerator_enabled        = bool<br>    disk_encryption_set_id           = string<br>    internal_dns_name_label          = string<br>    enable_ip_forwarding             = bool<br>    enable_accelerated_networking    = bool<br>    dns_servers                      = list(string)<br>    custom_data_path                 = string<br>    custom_data_args                 = map(string)<br>    static_ip                        = string<br>  }))</pre> | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_linux_vm_id_map"></a> [linux\_vm\_id\_map](#output\_linux\_vm\_id\_map) | n/a |
| <a name="output_linux_vm_identity_map"></a> [linux\_vm\_identity\_map](#output\_linux\_vm\_identity\_map) | n/a |
| <a name="output_linux_vm_ids"></a> [linux\_vm\_ids](#output\_linux\_vm\_ids) | n/a |
| <a name="output_linux_vm_names"></a> [linux\_vm\_names](#output\_linux\_vm\_names) | n/a |
| <a name="output_linux_vm_private_ip_address"></a> [linux\_vm\_private\_ip\_address](#output\_linux\_vm\_private\_ip\_address) | n/a |
| <a name="output_linux_vm_public_ip_address"></a> [linux\_vm\_public\_ip\_address](#output\_linux\_vm\_public\_ip\_address) | n/a |
| <a name="output_linux_vm_resource_group_names"></a> [linux\_vm\_resource\_group\_names](#output\_linux\_vm\_resource\_group\_names) | - - Linux VM's - |
| <a name="output_windows_vm_ids"></a> [windows\_vm\_ids](#output\_windows\_vm\_ids) | n/a |
| <a name="output_windows_vm_names"></a> [windows\_vm\_names](#output\_windows\_vm\_names) | n/a |
| <a name="output_windows_vm_private_ip_address"></a> [windows\_vm\_private\_ip\_address](#output\_windows\_vm\_private\_ip\_address) | n/a |
| <a name="output_windows_vm_public_ip_address"></a> [windows\_vm\_public\_ip\_address](#output\_windows\_vm\_public\_ip\_address) | n/a |
| <a name="output_windows_vm_resource_group_names"></a> [windows\_vm\_resource\_group\_names](#output\_windows\_vm\_resource\_group\_names) | - - Windows VM's - |
