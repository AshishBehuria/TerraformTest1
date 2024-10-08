## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [azurerm_lb.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/lb) | resource |
| [azurerm_lb_backend_address_pool.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/lb_backend_address_pool) | resource |
| [azurerm_lb_nat_pool.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/lb_nat_pool) | resource |
| [azurerm_lb_nat_rule.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/lb_nat_rule) | resource |
| [azurerm_lb_outbound_rule.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/lb_outbound_rule) | resource |
| [azurerm_lb_probe.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/lb_probe) | resource |
| [azurerm_lb_rule.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/lb_rule) | resource |
| [azurerm_public_ip.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/public_ip) | resource |
| [azurerm_resource_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/resource_group) | data source |
| [azurerm_subscription.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/subscription) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_emptylist"></a> [emptylist](#input\_emptylist) | n/a | `list(string)` | <pre>[<br>  "null",<br>  "null"<br>]</pre> | no |
| <a name="input_lb_additional_tags"></a> [lb\_additional\_tags](#input\_lb\_additional\_tags) | Tags of the load balancer in addition to the resource group tag. | `map(string)` | `{}` | no |
| <a name="input_lb_outbound_rules"></a> [lb\_outbound\_rules](#input\_lb\_outbound\_rules) | Map containing outbound nat rule parameters | <pre>map(object({<br>    name                            = string<br>    lb_key                          = string<br>    protocol                        = string<br>    backend_pool_name               = string<br>    allocated_outbound_ports        = number<br>    frontend_ip_configuration_names = list(string)<br><br>  }))</pre> | `{}` | no |
| <a name="input_load_balancer_nat_pools"></a> [load\_balancer\_nat\_pools](#input\_load\_balancer\_nat\_pools) | Map containing load balancer nat pool parameters | <pre>map(object({<br>    name             = string<br>    lb_key           = string<br>    frontend_ip_name = string<br>    lb_port_start    = number<br>    lb_port_end      = number<br>    backend_port     = number<br>  }))</pre> | `{}` | no |
| <a name="input_load_balancer_nat_rules"></a> [load\_balancer\_nat\_rules](#input\_load\_balancer\_nat\_rules) | Map containing load balancer nat rule parameters | <pre>map(object({<br>    name                    = string<br>    lb_key                  = string<br>    frontend_ip_name        = string<br>    lb_port                 = number<br>    backend_port            = number<br>    idle_timeout_in_minutes = number<br>  }))</pre> | `{}` | no |
| <a name="input_load_balancer_rules"></a> [load\_balancer\_rules](#input\_load\_balancer\_rules) | Map containing load balancer rule and probe parameters | <pre>map(object({<br>    name                      = string<br>    lb_key                    = string<br>    frontend_ip_name          = string<br>    backend_pool_name         = string<br>    lb_protocol               = string<br>    lb_port                   = string<br>    backend_port              = number<br>    enable_floating_ip        = bool<br>    disable_outbound_snat     = bool<br>    enable_tcp_reset          = bool<br>    probe_port                = number<br>    probe_protocol            = string<br>    request_path              = string<br>    probe_interval            = number<br>    probe_unhealthy_threshold = number<br>    load_distribution         = string<br>    idle_timeout_in_minutes   = number<br>  }))</pre> | `{}` | no |
| <a name="input_load_balancers"></a> [load\_balancers](#input\_load\_balancers) | Map containing load balancers | <pre>map(object({<br>    name = string<br>    sku  = string<br>    frontend_ips = list(object({<br>      name        = string<br>      subnet_name = string<br>      static_ip   = string<br>      zones       = list(string)<br>    }))<br>    backend_pool_names = list(string)<br>    enable_public_ip   = bool<br>    public_ip_name     = string<br>  }))</pre> | `{}` | no |
| <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name) | The name of the Resource Group in which to create the Load Balancer | `string` | n/a | yes |
| <a name="input_subnet_ids"></a> [subnet\_ids](#input\_subnet\_ids) | A map of subnet id's | `map(string)` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_frontend_ip_configurations_map"></a> [frontend\_ip\_configurations\_map](#output\_frontend\_ip\_configurations\_map) | n/a |
| <a name="output_pri_lb_backend_ids"></a> [pri\_lb\_backend\_ids](#output\_pri\_lb\_backend\_ids) | n/a |
| <a name="output_pri_lb_backend_map_ids"></a> [pri\_lb\_backend\_map\_ids](#output\_pri\_lb\_backend\_map\_ids) | n/a |
| <a name="output_pri_lb_frontend_ip_configurations"></a> [pri\_lb\_frontend\_ip\_configurations](#output\_pri\_lb\_frontend\_ip\_configurations) | n/a |
| <a name="output_pri_lb_names"></a> [pri\_lb\_names](#output\_pri\_lb\_names) | n/a |
| <a name="output_pri_lb_natpool_map_ids"></a> [pri\_lb\_natpool\_map\_ids](#output\_pri\_lb\_natpool\_map\_ids) | n/a |
| <a name="output_pri_lb_natrule_map_ids"></a> [pri\_lb\_natrule\_map\_ids](#output\_pri\_lb\_natrule\_map\_ids) | n/a |
| <a name="output_pri_lb_private_ip_address"></a> [pri\_lb\_private\_ip\_address](#output\_pri\_lb\_private\_ip\_address) | n/a |
| <a name="output_pri_lb_probe_ids"></a> [pri\_lb\_probe\_ids](#output\_pri\_lb\_probe\_ids) | n/a |
| <a name="output_pri_lb_probe_map_ids"></a> [pri\_lb\_probe\_map\_ids](#output\_pri\_lb\_probe\_map\_ids) | n/a |
| <a name="output_pri_lb_rule_ids"></a> [pri\_lb\_rule\_ids](#output\_pri\_lb\_rule\_ids) | n/a |
