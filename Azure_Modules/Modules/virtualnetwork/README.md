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
| [azurerm_network_security_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/network_security_group) | resource |
| [azurerm_route_table.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/route_table) | resource |
| [azurerm_subnet.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/subnet) | resource |
| [azurerm_subnet_network_security_group_association.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/subnet_network_security_group_association) | resource |
| [azurerm_subnet_route_table_association.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/subnet_route_table_association) | resource |
| [azurerm_virtual_network.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_network) | resource |
| [azurerm_virtual_network_peering.destination_to_source](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_network_peering) | resource |
| [azurerm_virtual_network_peering.source_to_destination](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_network_peering) | resource |
| [null_resource.dependency_modules](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [azurerm_resource_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/resource_group) | data source |
| [azurerm_virtual_network.destination](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/virtual_network) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_app_security_group_ids_map"></a> [app\_security\_group\_ids\_map](#input\_app\_security\_group\_ids\_map) | Specifies the Map of Application Security Group Id's | `map(string)` | `{}` | no |
| <a name="input_dependencies"></a> [dependencies](#input\_dependencies) | Specifies the modules that the Infrastructure Resources depends on. | `list(any)` | `[]` | no |
| <a name="input_location"></a> [location](#input\_location) | Network resources location if different that the resource group's location. | `string` | `""` | no |
| <a name="input_net_additional_tags"></a> [net\_additional\_tags](#input\_net\_additional\_tags) | Additional Network resources tags, in addition to the resource group tags. | `map(string)` | `{}` | no |
| <a name="input_net_location"></a> [net\_location](#input\_net\_location) | n/a | `string` | `""` | no |
| <a name="input_network_ddos_protection_plan"></a> [network\_ddos\_protection\_plan](#input\_network\_ddos\_protection\_plan) | Network network ddos protection plan parameters. | `any` | `[]` | no |
| <a name="input_network_security_groups"></a> [network\_security\_groups](#input\_network\_security\_groups) | The network security groups with their properties. | <pre>map(object({<br>    name = string<br>    tags = map(string)<br>    security_rules = list(object({<br>      name                                         = string<br>      description                                  = string<br>      protocol                                     = string<br>      direction                                    = string<br>      access                                       = string<br>      priority                                     = number<br>      source_address_prefix                        = string<br>      source_address_prefixes                      = list(string)<br>      destination_address_prefix                   = string<br>      destination_address_prefixes                 = list(string)<br>      source_port_range                            = string<br>      source_port_ranges                           = list(string)<br>      destination_port_range                       = string<br>      destination_port_ranges                      = list(string)<br>      source_application_security_group_names      = list(string)<br>      destination_application_security_group_names = list(string)<br>    }))<br>  }))</pre> | `{}` | no |
| <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name) | The Azure resource group where your resources will be created | `string` | n/a | yes |
| <a name="input_rgname"></a> [rgname](#input\_rgname) | Network resources location if different that the resource group's location. | `string` | `""` | no |
| <a name="input_route_tables"></a> [route\_tables](#input\_route\_tables) | The route tables with their properties. | <pre>map(object({<br>    name                          = string<br>    disable_bgp_route_propagation = bool<br>    routes = list(object({<br>      name                   = string<br>      address_prefix         = string<br>      next_hop_type          = string<br>      next_hop_in_ip_address = string<br>      azure_firewall_name    = string<br>    }))<br>  }))</pre> | `{}` | no |
| <a name="input_subnets"></a> [subnets](#input\_subnets) | The virtal networks subnets with their properties. | <pre>map(object({<br>    name              = string<br>    vnet_key          = string<br>    nsg_key           = string<br>    rt_key            = string<br>    address_prefixes  = list(string)<br>    pe_enable         = bool<br>    service_endpoints = list(string)<br>    delegation = list(object({<br>      name = string<br>      service_delegation = list(object({<br>        name    = string<br>        actions = list(string)<br>      }))<br>    }))<br>  }))</pre> | `{}` | no |
| <a name="input_virtual_networks"></a> [virtual\_networks](#input\_virtual\_networks) | The virtal networks with their properties. | <pre>map(object({<br>    name          = string<br>    address_space = list(string)<br>    dns_servers   = list(string)<br>  }))</pre> | `{}` | no |
| <a name="input_vnet_peering"></a> [vnet\_peering](#input\_vnet\_peering) | Vnet Peering to the destination Vnet | <pre>map(object({<br>    destination_vnet_name        = string<br>    destination_vnet_rg          = string<br>    vnet_key                     = string<br>    allow_virtual_network_access = bool<br>    allow_forwarded_traffic      = bool<br>    allow_gateway_transit        = bool<br>    use_remote_gateways          = bool<br>  }))</pre> | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_map_nsg_ids"></a> [map\_nsg\_ids](#output\_map\_nsg\_ids) | n/a |
| <a name="output_map_subnet_ids"></a> [map\_subnet\_ids](#output\_map\_subnet\_ids) | n/a |
| <a name="output_map_subnets"></a> [map\_subnets](#output\_map\_subnets) | n/a |
| <a name="output_map_vnet_ids"></a> [map\_vnet\_ids](#output\_map\_vnet\_ids) | n/a |
| <a name="output_map_vnets"></a> [map\_vnets](#output\_map\_vnets) | n/a |
| <a name="output_network_security_group_ids"></a> [network\_security\_group\_ids](#output\_network\_security\_group\_ids) | NSGs |
| <a name="output_private_endpoint_subnets"></a> [private\_endpoint\_subnets](#output\_private\_endpoint\_subnets) | n/a |
| <a name="output_private_endpoint_vnets"></a> [private\_endpoint\_vnets](#output\_private\_endpoint\_vnets) | n/a |
| <a name="output_subnet_ids"></a> [subnet\_ids](#output\_subnet\_ids) | Subnets |
| <a name="output_subnets_with_serviceendpoints"></a> [subnets\_with\_serviceendpoints](#output\_subnets\_with\_serviceendpoints) | n/a |
| <a name="output_vnet_ids"></a> [vnet\_ids](#output\_vnet\_ids) | VNets |
| <a name="output_vnet_locations"></a> [vnet\_locations](#output\_vnet\_locations) | n/a |
| <a name="output_vnet_names"></a> [vnet\_names](#output\_vnet\_names) | n/a |
| <a name="output_vnet_peering_dest_to_source"></a> [vnet\_peering\_dest\_to\_source](#output\_vnet\_peering\_dest\_to\_source) | n/a |
| <a name="output_vnet_peering_source_to_dest"></a> [vnet\_peering\_source\_to\_dest](#output\_vnet\_peering\_source\_to\_dest) | VNet Peering |
| <a name="output_vnet_rgnames"></a> [vnet\_rgnames](#output\_vnet\_rgnames) | n/a |
