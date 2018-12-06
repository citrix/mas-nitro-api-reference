#ns_detail_vlan



Configuration for NS Detail Vlan resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ns_vlan_ip_address</td><td>&lt;String></td><td>Read-write</td><td>VPX IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>network_interfaces</td><td>&lt;network_interface[]></td><td>Read-write</td><td>Network Interfaces.</td></tr><tr><td>if_ipv6_routing</td><td>&lt;String></td><td>Read-write</td><td>VLAN for Network Interface on VM Instance.</td></tr><tr><td>ns_vlan_id</td><td>&lt;Integer></td><td>Read-write</td><td>VLAN Id.<br>Maximum value =</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_detail_vlan?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_detail_vlan: {
"network_interfaces":[{
<b>"port_name":<String_value></b>,
"name_server":<String_value>,
"is_mgmt_ifc":<Boolean_value>,
"gateway":<String_value>,
"vrid_list_ipv6":<String_value>,
"parent_id":<String_value>,
"is_member_ifc":<Boolean_value>,
"vrid_list_ipv4":<String_value>,
"mac_address":<String_value>,
"netmask":<String_value>,
"ip_address":<String_value>,
"id":<String_value>,
"l2_enabled":<Boolean_value>,
"interface_name":<String_value>,
"parent_name":<String_value>,
"vlan_whitelist_array":<String_value[]>,
"mac_mode":<String_value>,
"vlan":<Integer_value>,
"managed_device_id":<String_value>,
"vrid_list_ipv4_array":<String_value[]>,
"receiveuntagged":<Boolean_value>,
"sdx_formation_network_id":<String_value>,
"vrid_list_ipv6_array":<String_value[]>,
"is_vlan_applied":<Boolean_value>,
"vlan_whitelist":<String_value>}],
"if_ipv6_routing":<String_value>,
"ns_vlan_ip_address":<String_value>,
"ns_vlan_id":<Integer_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_detail_vlan":[{
"ns_vlan_ip_address":<String_value>,
"network_interfaces":[{
"device_channel_name":<String_value>,
"is_mgmt_ifc":<Boolean_value>,
"name_server":<String_value>,
"vrid_list_ipv6":<String_value>,
"gateway":<String_value>,
"xen_vf_index":<Integer_value>,
"parent_id":<String_value>,
"vrid_list_ipv4":<String_value>,
"is_member_ifc":<Boolean_value>,
"mac_address":<String_value>,
"parent_channel_id":<String_value>,
"channel_type":<String_value>,
"l2_enabled":<Boolean_value>,
"id":<String_value>,
"ip_address":<String_value>,
"netmask":<String_value>,
"port_name":<String_value>,
"parent_name":<String_value>,
"mac_mode":<String_value>,
"managed_device_id":<String_value>,
"vlan":<Integer_value>,
"receiveuntagged":<Boolean_value>,
"sdx_formation_network_id":<String_value>,
"vlan_whitelist":<String_value>
"interface_name":<String_value>
"vrid_list_ipv4_array":<String_value>
"vrid_list_ipv6_array":<String_value>
"vlan_whitelist_array":<String_value>
"is_vlan_applied":<Boolean_value>}],
"if_ipv6_routing":<String_value>,
"ns_vlan_id":<Integer_value>}]}
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_detail_vlan

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_detail_vlan":[{
"ns_vlan_ip_address":<String_value>,
"network_interfaces":[{
"device_channel_name":<String_value>,
"is_mgmt_ifc":<Boolean_value>,
"name_server":<String_value>,
"vrid_list_ipv6":<String_value>,
"gateway":<String_value>,
"xen_vf_index":<Integer_value>,
"parent_id":<String_value>,
"vrid_list_ipv4":<String_value>,
"is_member_ifc":<Boolean_value>,
"mac_address":<String_value>,
"parent_channel_id":<String_value>,
"channel_type":<String_value>,
"l2_enabled":<Boolean_value>,
"id":<String_value>,
"ip_address":<String_value>,
"netmask":<String_value>,
"port_name":<String_value>,
"parent_name":<String_value>,
"mac_mode":<String_value>,
"managed_device_id":<String_value>,
"vlan":<Integer_value>,
"receiveuntagged":<Boolean_value>,
"sdx_formation_network_id":<String_value>,
"vlan_whitelist":<String_value>
"interface_name":<String_value>
"vrid_list_ipv4_array":<String_value>
"vrid_list_ipv6_array":<String_value>
"vlan_whitelist_array":<String_value>
"is_vlan_applied":<Boolean_value>}],
"if_ipv6_routing":<String_value>,
"ns_vlan_id":<Integer_value>}]}
```







