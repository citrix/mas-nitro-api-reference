#mps_agent



Configuration for MPS Agent information resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>deployment_status</td><td>&lt;Boolean></td><td>Read-write</td><td>Deployment status of this node..</td></tr><tr><td>hostname</td><td>&lt;String></td><td>Read-write</td><td>Hostname of the agent.</td></tr><tr><td>down_count</td><td>&lt;Integer></td><td>Read-write</td><td>Shows for how long agent was down, each value of count increases after every 10 seconds.</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Agent state.</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Password.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>tenant</td><td>&lt;String></td><td>Read-write</td><td>Tenant.</td></tr><tr><td>public_key</td><td>&lt;String></td><td>Read-write</td><td>public key for agent.</td></tr><tr><td>platform</td><td>&lt;String></td><td>Read-write</td><td>Platform.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for agent registered with NMX Cloud..</td></tr><tr><td>instance_id</td><td>&lt;String></td><td>Read-write</td><td>Unique ID of device provided by Global Trust Service.</td></tr><tr><td>version</td><td>&lt;String></td><td>Read-write</td><td>version..</td></tr><tr><td>datacenter_id</td><td>&lt;String></td><td>Read-write</td><td>Datacenter Id is system generated key for data center.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Agent IP Address.</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>discovery_time</td><td>&lt;Double></td><td>Read-write</td><td>discovery time.</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>username configured on DB node..<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>certificate</td><td>&lt;String></td><td>Read-write</td><td>Name of ABDP Certificate File.</td></tr><tr><td>connector_ips</td><td>&lt;String></td><td>Read-write</td><td>Comma separated list of connector node IPs..</td></tr><tr><td>bulk_request_ipaddress</td><td>&lt;String></td><td>Read-write</td><td>ABDP IP Address..<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>upgrade_version</td><td>&lt;String></td><td>Read-write</td><td>Represents the next version the agent should upgrade to.</td></tr><tr><td>registered_devices</td><td>&lt;managed_device[]></td><td>Read-write</td><td>List of registered devices..</td></tr><tr><td>bulk_request_port</td><td>&lt;Integer></td><td>Read-write</td><td>Port number for ABDP.</td></tr><tr><td>city</td><td>&lt;String></td><td>Read-write</td><td>City.</td></tr><tr><td>mas_version</td><td>&lt;String></td><td>Read-write</td><td>MAS server's current version.</td></tr><tr><td>url</td><td>&lt;String></td><td>Read-write</td><td>URL of ABDP Certificate File Location.</td></tr><tr><td>country</td><td>&lt;String></td><td>Read-write</td><td>Country.</td></tr><tr><td>region</td><td>&lt;String></td><td>Read-write</td><td>Region.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port number for ABDP Certificate file location.</td></tr><tr><td>zipcode</td><td>&lt;String></td><td>Read-write</td><td>Zipcode of location.<br>Maximum length = 32</td></tr><tr><td>server_time</td><td>&lt;Double></td><td>Read-write</td><td>MAS server's Epoch time.</td></tr><tr><td>loc</td><td>&lt;String></td><td>Read-write</td><td>Location - latitude and longitude.</td></tr><tr><td>agent_msg_router_url</td><td>&lt;String></td><td>Read-write</td><td>URL for router.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps_agent/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps_agent

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mps_agent":[{
"deployment_status":<Boolean_value>,
"hostname":<String_value>,
"down_count":<Integer_value>,
"state":<String_value>,
"password":<String_value>,
"tenant":<String_value>,
"public_key":<String_value>,
"platform":<String_value>,
"id":<String_value>,
"instance_id":<String_value>,
"version":<String_value>,
"datacenter_id":<String_value>,
"name":<String_value>,
"rpt_sample_time":<Double_value>,
"discovery_time":<Double_value>,
"username":<String_value>,
"certificate":<String_value>,
"connector_ips":<String_value>,
"bulk_request_ipaddress":<String_value>,
"upgrade_version":<String_value>,
"registered_devices":[{
"subnet_id":<String_value>,
"manufacturedate":<String_value>,
"is_grace":<Boolean_value>,
"hostname":<String_value>,
"std_bw_config":<Integer_value>,
"gateway_deployment":<Boolean_value>,
"gateway_ipv6":<String_value>,
"ha_master_state":<String_value>,
"instance_available":<Integer_value>,
"vpc_id":<String_value>,
"device_finger_print":<String_value>,
"instance_state":<String_value>,
"region":<String_value>,
"reason":<String_value>,
"name":<String_value>,
"ent_bw_available":<Integer_value>,
"description":<String_value>,
"geo_support":<Boolean_value>,
"is_pooled_license":<Boolean_value>,
"upsince":<String_value>,
"sslvpn_config":<Integer_value>,
"security_group":<String_value>,
"private_dns":<String_value>,
"user_driven":<Boolean_value>,
"zone":<String_value>,
"mastools_version":<String_value>,
"model_id":<String_value>,
"virtualization":<String_value>,
"sysservices":<Double_value>,
"termination_protection":<Boolean_value>,
"ent_bw_total":<Integer_value>,
"vcpu_config":<Integer_value>,
"tenant_id":<String_value>,
"device_uuid":<String_value>,
"netmask":<String_value>,
"do_config":<Boolean_value>,
"autoprovisioned":<Boolean_value>,
"ent_bw_config":<Integer_value>,
"datacenter_id":<String_value>,
"host_id":<String_value>,
"version":<String_value>,
"instance_config":<Integer_value>,
"is_managed":<Boolean_value>,
"key_name":<String_value>,
"discovery_time":<Double_value>,
"instance_mode":<String_value>,
"public_dns":<String_value>,
"instance_total":<Integer_value>,
"is_ha_configured":<Boolean_value>,
"trust_id":<String_value>,
"ipv4_address":<String_value>,
"instance_type":<String_value>,
"profile_name":<String_value>,
"seq_no":<Double_value>,
"std_bw_available":<Integer_value>,
"sysid":<String_value>,
"tenancy":<String_value>,
"servicepackage":<String_value>,
"last_updated_time":<Double_value>,
"cloud":<String_value>,
"encoded_serialnumber":<String_value>,
"plt_bw_total":<Integer_value>,
"uptime":<String_value>,
"private_ip":<String_value>,
"id":<String_value>,
"mgmt_ip_address":<String_value>,
"ipv6_address":<String_value>,
"partition_id":<String_value>,
"license_edition":<String_value>,
"cpu_license_type":<Integer_value>,
"cpufrequncy":<Integer_value>,
"plt_bw_available":<Integer_value>,
"device_family":<String_value>,
"location":<String_value>,
"contactperson":<String_value>,
"ha_sync":<String_value>,
"public_ip":<String_value>,
"ha_ip_address":<String_value>,
"bmcrevision":<String_value>,
"type":<String_value>,
"gateway":<String_value>,
"status":<String_value>,
"systemname":<String_value>,
"config_type":<Integer_value>,
"geo_location":<String_value>,
"node_id":<String_value>,
"isolation_policy":<String_value>,
"ip_address":<String_value>,
"ping_state":<Integer_value>,
"std_bw_total":<Integer_value>,
"display_name":<String_value>,
"ami_id":<String_value>,
"root_device_type":<String_value>,
"ebs_optimized":<Boolean_value>,
"plt_bw_config":<Integer_value>,
"partition_name":<String_value>,
"agent_id":<String_value>,
"sslvpn_total":<Integer_value>,
"serialnumber":<String_value>
"parent_inventory":<Boolean_value>
"provision_request_id":<String_value>
"profile_username":<String_value>
"profile_password":<String_value>
"file_location_path":<String_value>
"sync_operation":<Boolean_value>
"act_id":<String_value>
"file_name":<String_value>
"entity_tag":[{
"prop_value":<String_value>,
"prop_key":<String_value>}]}],
"bulk_request_port":<Integer_value>,
"city":<String_value>,
"mas_version":<String_value>,
"url":<String_value>,
"country":<String_value>,
"region":<String_value>,
"port":<Integer_value>,
"zipcode":<String_value>,
"server_time":<Double_value>,
"loc":<String_value>,
"agent_msg_router_url":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps_agent/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mps_agent":[{
"deployment_status":<Boolean_value>,
"hostname":<String_value>,
"down_count":<Integer_value>,
"state":<String_value>,
"password":<String_value>,
"tenant":<String_value>,
"public_key":<String_value>,
"platform":<String_value>,
"id":<String_value>,
"instance_id":<String_value>,
"version":<String_value>,
"datacenter_id":<String_value>,
"name":<String_value>,
"rpt_sample_time":<Double_value>,
"discovery_time":<Double_value>,
"username":<String_value>,
"certificate":<String_value>,
"connector_ips":<String_value>,
"bulk_request_ipaddress":<String_value>,
"upgrade_version":<String_value>,
"registered_devices":[{
"subnet_id":<String_value>,
"manufacturedate":<String_value>,
"is_grace":<Boolean_value>,
"hostname":<String_value>,
"std_bw_config":<Integer_value>,
"gateway_deployment":<Boolean_value>,
"gateway_ipv6":<String_value>,
"ha_master_state":<String_value>,
"instance_available":<Integer_value>,
"vpc_id":<String_value>,
"device_finger_print":<String_value>,
"instance_state":<String_value>,
"region":<String_value>,
"reason":<String_value>,
"name":<String_value>,
"ent_bw_available":<Integer_value>,
"description":<String_value>,
"geo_support":<Boolean_value>,
"is_pooled_license":<Boolean_value>,
"upsince":<String_value>,
"sslvpn_config":<Integer_value>,
"security_group":<String_value>,
"private_dns":<String_value>,
"user_driven":<Boolean_value>,
"zone":<String_value>,
"mastools_version":<String_value>,
"model_id":<String_value>,
"virtualization":<String_value>,
"sysservices":<Double_value>,
"termination_protection":<Boolean_value>,
"ent_bw_total":<Integer_value>,
"vcpu_config":<Integer_value>,
"tenant_id":<String_value>,
"device_uuid":<String_value>,
"netmask":<String_value>,
"do_config":<Boolean_value>,
"autoprovisioned":<Boolean_value>,
"ent_bw_config":<Integer_value>,
"datacenter_id":<String_value>,
"host_id":<String_value>,
"version":<String_value>,
"instance_config":<Integer_value>,
"is_managed":<Boolean_value>,
"key_name":<String_value>,
"discovery_time":<Double_value>,
"instance_mode":<String_value>,
"public_dns":<String_value>,
"instance_total":<Integer_value>,
"is_ha_configured":<Boolean_value>,
"trust_id":<String_value>,
"ipv4_address":<String_value>,
"instance_type":<String_value>,
"profile_name":<String_value>,
"seq_no":<Double_value>,
"std_bw_available":<Integer_value>,
"sysid":<String_value>,
"tenancy":<String_value>,
"servicepackage":<String_value>,
"last_updated_time":<Double_value>,
"cloud":<String_value>,
"encoded_serialnumber":<String_value>,
"plt_bw_total":<Integer_value>,
"uptime":<String_value>,
"private_ip":<String_value>,
"id":<String_value>,
"mgmt_ip_address":<String_value>,
"ipv6_address":<String_value>,
"partition_id":<String_value>,
"license_edition":<String_value>,
"cpu_license_type":<Integer_value>,
"cpufrequncy":<Integer_value>,
"plt_bw_available":<Integer_value>,
"device_family":<String_value>,
"location":<String_value>,
"contactperson":<String_value>,
"ha_sync":<String_value>,
"public_ip":<String_value>,
"ha_ip_address":<String_value>,
"bmcrevision":<String_value>,
"type":<String_value>,
"gateway":<String_value>,
"status":<String_value>,
"systemname":<String_value>,
"config_type":<Integer_value>,
"geo_location":<String_value>,
"node_id":<String_value>,
"isolation_policy":<String_value>,
"ip_address":<String_value>,
"ping_state":<Integer_value>,
"std_bw_total":<Integer_value>,
"display_name":<String_value>,
"ami_id":<String_value>,
"root_device_type":<String_value>,
"ebs_optimized":<Boolean_value>,
"plt_bw_config":<Integer_value>,
"partition_name":<String_value>,
"agent_id":<String_value>,
"sslvpn_total":<Integer_value>,
"serialnumber":<String_value>
"parent_inventory":<Boolean_value>
"provision_request_id":<String_value>
"profile_username":<String_value>
"profile_password":<String_value>
"file_location_path":<String_value>
"sync_operation":<Boolean_value>
"act_id":<String_value>
"file_name":<String_value>
"entity_tag":[{
"prop_value":<String_value>,
"prop_key":<String_value>}]}],
"bulk_request_port":<Integer_value>,
"city":<String_value>,
"mas_version":<String_value>,
"url":<String_value>,
"country":<String_value>,
"region":<String_value>,
"port":<Integer_value>,
"zipcode":<String_value>,
"server_time":<Double_value>,
"loc":<String_value>,
"agent_msg_router_url":<String_value>}]}
```







