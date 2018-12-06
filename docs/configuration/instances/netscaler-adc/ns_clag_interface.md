#ns_clag_interface



Configuration for CLAG Interface resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>channel_id</td><td>&lt;String></td><td>Read-write</td><td>Channel ID if this interface represents a channel (CLA/1, CLA/2 ...).<br>Minimum length = 5<br>Maximum length = 5</td></tr><tr><td>channel_tag_all_vlans</td><td>&lt;Boolean></td><td>Read-write</td><td>If true then all the member interfaces of this channel are tagged. Possible values: true and false.</td></tr><tr><td>channel_ha_monitoring</td><td>&lt;Boolean></td><td>Read-write</td><td>HA-monitoring control for the channel. Possible values: true and false.</td></tr><tr><td>lacp_channel_time</td><td>&lt;String></td><td>Read-write</td><td>LACP time. Possible values: long and short.<br>Minimum length = 4<br>Maximum length = 10</td></tr><tr><td>channel_interface_list</td><td>&lt;ns_clag_node[]></td><td>Read-write</td><td>Array of CLAG nodes that are part of this channel (10/1, 10/4).</td></tr><tr><td>clip</td><td>&lt;String></td><td>Read-write</td><td>Cluster IPAddress.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>channel_alias</td><td>&lt;String></td><td>Read-write</td><td>Alias name for this channel.<br>Minimum length = 4<br>Maximum length = 31</td></tr><tr><td>has_foreign_interfaces</td><td>&lt;Boolean></td><td>Read-write</td><td>Indicates whether CLAG has interfaces from remote SDX. Possible values: true and false.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for CLAG.</td></tr><tr><td>mtu</td><td>&lt;Integer></td><td>Read-write</td><td>MTU value, should be between 1500-9216.<br>Minimum value = 1500<br>Maximum value =</td></tr><tr><td>sync_operation</td><td>&lt;Boolean></td><td>Read-write</td><td>sync operation.</td></tr><tr><td>channel_state</td><td>&lt;String></td><td>Read-only</td><td>Indicates CLA state. Possible values: UP and DOWN.</td></tr><tr><td>lacp_mode</td><td>&lt;String></td><td>Read-only</td><td>LACP mode can be either ACTIVE, PASSIVE, DISABLED. Applicable for channel.</td></tr><tr><td>lacp_channel_mac_address</td><td>&lt;String></td><td>Read-only</td><td>Mac address of the bond on cluster.</td></tr><tr><td>channel_type</td><td>&lt;String></td><td>Read-only</td><td>Channel type to represent the CLAG type.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_clag_interface?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_clag_interface: {
<b>"channel_id":<String_value></b>,
<b>"channel_interface_list":[{
"nodeid":<Integer_value>,
"parent_id":<String_value>,
"id":<String_value>,
"interface_name":<String_value>,
"local_node":<Boolean_value>,
"parent_name":<String_value>}]</b>,
<b>"clip":<String_value></b>,
"channel_tag_all_vlans":<Boolean_value>,
"lacp_channel_time":<String_value>,
"channel_alias":<String_value>,
"id":<String_value>,
"mtu":<Integer_value>,
"channel_ha_monitoring":<Boolean_value>,
"sync_operation":<Boolean_value>,
"has_foreign_interfaces":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_clag_interface":[{
"channel_id":<String_value>,
"channel_tag_all_vlans":<Boolean_value>,
"channel_ha_monitoring":<Boolean_value>,
"lacp_channel_time":<String_value>,
"host_type":<String_value>,
"channel_interface_list":[{
"local_node":<Boolean_value>,
"interface_name":<String_value>,
"parent_name":<String_value>,
"nodeid":<Integer_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"channel_state":<String_value>,
"lacp_mode":<String_value>,
"clip":<String_value>,
"channel_alias":<String_value>,
"has_foreign_interfaces":<Boolean_value>,
"host_ip_address":<String_value>,
"lacp_channel_mac_address":<String_value>,
"id":<String_value>,
"channel_type":<String_value>,
"mtu":<Integer_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_clag_interface/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_clag_interface

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_clag_interface":[{
"channel_id":<String_value>,
"channel_tag_all_vlans":<Boolean_value>,
"channel_ha_monitoring":<Boolean_value>,
"lacp_channel_time":<String_value>,
"host_type":<String_value>,
"channel_interface_list":[{
"local_node":<Boolean_value>,
"interface_name":<String_value>,
"parent_name":<String_value>,
"nodeid":<Integer_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"channel_state":<String_value>,
"lacp_mode":<String_value>,
"clip":<String_value>,
"channel_alias":<String_value>,
"has_foreign_interfaces":<Boolean_value>,
"host_ip_address":<String_value>,
"lacp_channel_mac_address":<String_value>,
"id":<String_value>,
"channel_type":<String_value>,
"mtu":<Integer_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_clag_interface/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_clag_interface":[{
"channel_id":<String_value>,
"channel_tag_all_vlans":<Boolean_value>,
"channel_ha_monitoring":<Boolean_value>,
"lacp_channel_time":<String_value>,
"host_type":<String_value>,
"channel_interface_list":[{
"local_node":<Boolean_value>,
"interface_name":<String_value>,
"parent_name":<String_value>,
"nodeid":<Integer_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"channel_state":<String_value>,
"lacp_mode":<String_value>,
"clip":<String_value>,
"channel_alias":<String_value>,
"has_foreign_interfaces":<Boolean_value>,
"host_ip_address":<String_value>,
"lacp_channel_mac_address":<String_value>,
"id":<String_value>,
"channel_type":<String_value>,
"mtu":<Integer_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_clag_interface/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_clag_interface:{
<b>"id":<String_value></b>,
"channel_tag_all_vlans":<Boolean_value>,
"lacp_channel_time":<String_value>,
"channel_interface_list":[{
"nodeid":<Integer_value>,
"parent_id":<String_value>,
"id":<String_value>,
"interface_name":<String_value>,
"local_node":<Boolean_value>,
"parent_name":<String_value>}],
"channel_alias":<String_value>,
"clip":<String_value>,
"mtu":<Integer_value>,
"channel_id":<String_value>,
"channel_ha_monitoring":<Boolean_value>,
"sync_operation":<Boolean_value>,
"has_foreign_interfaces":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_clag_interface":[{
"channel_id":<String_value>,
"channel_tag_all_vlans":<Boolean_value>,
"channel_ha_monitoring":<Boolean_value>,
"lacp_channel_time":<String_value>,
"host_type":<String_value>,
"channel_interface_list":[{
"local_node":<Boolean_value>,
"interface_name":<String_value>,
"parent_name":<String_value>,
"nodeid":<Integer_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"channel_state":<String_value>,
"lacp_mode":<String_value>,
"clip":<String_value>,
"channel_alias":<String_value>,
"has_foreign_interfaces":<Boolean_value>,
"host_ip_address":<String_value>,
"lacp_channel_mac_address":<String_value>,
"id":<String_value>,
"channel_type":<String_value>,
"mtu":<Integer_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>}]}
```







