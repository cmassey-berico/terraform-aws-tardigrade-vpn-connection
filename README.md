# terraform-aws-tardigrade-vpn-connection

Terraform module to create a VPN Connection


<!-- BEGIN TFDOCS -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.12 |

## Providers

| Name | Version |
|------|---------|
| aws | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| amazon\_side\_asn | ASN for the Amazon side of the VPN gateway | `string` | `"64512"` | no |
| cgw\_bgp\_asn | BGP ASN of the customer gateway | `string` | `null` | no |
| cgw\_ip\_addresses | List of IP addresses of the customer gateways | `list(string)` | `[]` | no |
| destination\_cidr\_blocks | List of CIDR blocks to route through the VPN Connection | `list` | `[]` | no |
| name | Name tag to associate to all resources that support tags | `string` | `null` | no |
| propagating\_route\_table\_count | Number of route tables in the list of progagating\_route\_table\_ids | `string` | `"0"` | no |
| propagating\_route\_table\_ids | List of Route Table IDs to propagate routes into, from the VPN Gateway | `list` | `[]` | no |
| static\_routes\_only | Boolean used to determine whether the VPN connection uses static routes exclusively. Static routes must be used for devices that don't support BGP | `bool` | `"false"` | no |
| tags | A map of tags to add to any VPN resource that supports tags | `map(string)` | `{}` | no |
| vpc\_id | VPC ID to which the VPN Connection will be attached | `string` | `null` | no |

## Outputs

| Name | Description |
|------|-------------|
| customer\_gateway\_ids | IDs of the Customer Gateways |
| vpn\_connection\_ids | IDs of the VPN Connections |
| vpn\_gateway\_id | ID of the VPN Gateway |

<!-- END TFDOCS -->
