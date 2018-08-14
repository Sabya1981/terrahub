# aws_default_vpc_dhcp_options

Provides a resource to manage the default AWS DHCP Options Set in the current region.

Each AWS region comes with a default set of DHCP options. This is an advanced resource, and has special caveats to be aware of when using it. Please read this document in its entirety before using this resource.

The aws_default_vpc_dhcp_options behaves differently from normal resources, in that Terraform does not create this resource, but instead "adopts" it into management.

## input variables

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
|account_id|The id of AWS account.|string||Yes|
|region|This is the AWS region.|string|us-east-1|Yes|
|default_vpc_dhcp_options_netbios_name_servers|List of NETBIOS name servers.|list||Yes|
|default_vpc_dhcp_options_netbios_node_type|The NetBIOS node type (1, 2, 4, or 8). AWS recommends to specify 2 since broadcast and multicast are not supported in their network. For more information about these node types, see RFC 2132.|number|2|No|
|custom_tags|Custom tags.|map||No|
|default_tags|Default tags.|map|{"ThubName"= "{{ name }}","ThubCode"= "{{ code }}","ThubEnv"= "default","Description" = "Managed by TerraHub"}|No|

## output parameters

| Name | Description | Type |
|------|-------------|:----:|
|id|The ID of the DHCP Options Set.|string|
|thub_id|TThe ID of the DHCP Options Set (hotfix for issue hashicorp/terraform#[7982]).|string|