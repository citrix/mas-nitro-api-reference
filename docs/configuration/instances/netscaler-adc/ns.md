#ns



Configuration for NetScaler resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>gateway_deployment</td><td>&lt;Boolean></td><td>Read-write</td><td>Is this device acting as Gateway..</td></tr><tr><td>std_bw_config</td><td>&lt;Integer></td><td>Read-write</td><td>Standard Bandwidth running.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NS IP Address for this managed device.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>gateway_ipv6</td><td>&lt;String></td><td>Read-write</td><td>Gateway IPv6 Address.</td></tr><tr><td>instance_available</td><td>&lt;Integer></td><td>Read-write</td><td>Instance license available.</td></tr><tr><td>device_finger_print</td><td>&lt;String></td><td>Read-write</td><td>Fingerprint/thumb-print from UMS public certificate for SSL communication.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of managed device.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>mastools_version</td><td>&lt;String></td><td>Read-write</td><td>Mastools version if the device is embedded agent.</td></tr><tr><td>ent_bw_total</td><td>&lt;Integer></td><td>Read-write</td><td>Enterprise Bandwidth Total.</td></tr><tr><td>ssh_port</td><td>&lt;Integer></td><td>Read-write</td><td>SSH port of the container..</td></tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>Netmask of managed device.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>ent_bw_config</td><td>&lt;Integer></td><td>Read-write</td><td>Enterprise Bandwidth configured.</td></tr><tr><td>datacenter_id</td><td>&lt;String></td><td>Read-write</td><td>Datacenter Id is system generated key for data center.</td></tr><tr><td>instance_config</td><td>&lt;Integer></td><td>Read-write</td><td>Instance license running.</td></tr><tr><td>instance_mode</td><td>&lt;String></td><td>Read-write</td><td>Denotes state- primary,secondary,clip,clusternode.</td></tr><tr><td>discovery_time</td><td>&lt;Double></td><td>Read-write</td><td>discovery time.</td></tr><tr><td>number_of_ssl_cores_up</td><td>&lt;Integer></td><td>Read-write</td><td>Number of SSL Cores Up.</td></tr><tr><td>std_bw_available</td><td>&lt;Integer></td><td>Read-write</td><td>Standard Bandwidth Available.</td></tr><tr><td>instance_name</td><td>&lt;String></td><td>Read-write</td><td>NetScaler CPX Instance Name.</td></tr><tr><td>plt_bw_total</td><td>&lt;Integer></td><td>Read-write</td><td>Total Platinum Bandwidth.</td></tr><tr><td>host_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Host IPAddress where VM is provisioned.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the managed devices.</td></tr><tr><td>ipv6_address</td><td>&lt;String></td><td>Read-write</td><td>IPv6 Address.</td></tr><tr><td>mgmt_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Management IP Address for this Managed Device.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>plt_bw_available</td><td>&lt;Integer></td><td>Read-write</td><td>Platinum Bandwidth Available.</td></tr><tr><td>is_clip</td><td>&lt;Boolean></td><td>Read-write</td><td>Is Clip.</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Device Family.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of device, (Xen | NS).<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>throughput</td><td>&lt;Double></td><td>Read-write</td><td>Assign throughput in Mbps to VM Instance.</td></tr><tr><td>ns_observationdomainid</td><td>&lt;String></td><td>Read-write</td><td>ns_observationdomainid.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>gateway</td><td>&lt;String></td><td>Read-write</td><td>Default Gateway of managed device.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>http_port</td><td>&lt;Integer></td><td>Read-write</td><td>HTTP port of the container..</td></tr><tr><td>iscco</td><td>&lt;Boolean></td><td>Read-write</td><td>Is CCO.</td></tr><tr><td>isolation_policy</td><td>&lt;String></td><td>Read-write</td><td>Isolation Policy of the Device.</td></tr><tr><td>provision_request_id</td><td>&lt;String></td><td>Read-write</td><td>Value is set only if the instance was provisioned from MAS.</td></tr><tr><td>lb_role</td><td>&lt;String></td><td>Read-write</td><td>LB role performed by the device: North-South (Ingress or server), or East-West (client).</td></tr><tr><td>license</td><td>&lt;String></td><td>Read-write</td><td>Feature License for NetScaler Instance, needs to be set while provisioning (standard, enterprise, platinum, SWG).<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>https_port</td><td>&lt;Integer></td><td>Read-write</td><td>HTTPS port of the container..</td></tr><tr><td>domain_name</td><td>&lt;String></td><td>Read-write</td><td>Domain name of VM Device.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>snmp_port</td><td>&lt;Integer></td><td>Read-write</td><td>SNMP port of the container..</td></tr><tr><td>image_name</td><td>&lt;String></td><td>Read-write</td><td>Image Name, This parameter is used while provisioning VM Instance with XVA image, template_name is given priority if provided along with image_name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>hostname</td><td>&lt;String></td><td>Read-write</td><td>Assign hostname to managed device, if this is not provided, name will be set as host name .<br>Minimum length = 1<br>Maximum length = 256</td></tr><tr><td>pre_auth_key</td><td>&lt;String></td><td>Read-write</td><td>Shared secret that used for orchestration deployment.</td></tr><tr><td>ent_bw_available</td><td>&lt;Integer></td><td>Read-write</td><td>Enterprise Bandwidth configured.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Description of managed device.<br>Minimum length = 1<br>Maximum length = 512</td></tr><tr><td>geo_support</td><td>&lt;Boolean></td><td>Read-write</td><td>Is this device configured to support GEO location..</td></tr><tr><td>sslvpn_config</td><td>&lt;Integer></td><td>Read-write</td><td>sslvpn license maximum.</td></tr><tr><td>sysservices</td><td>&lt;Double></td><td>Read-write</td><td>System Services.</td></tr><tr><td>num_pes</td><td>&lt;Integer></td><td>Read-write</td><td>Total number of PEs.</td></tr><tr><td>burst_priority</td><td>&lt;Integer></td><td>Read-write</td><td>Burst Priority of the VM Instance..</td></tr><tr><td>routable</td><td>&lt;Boolean></td><td>Read-write</td><td>Whether the device is reachable or not.</td></tr><tr><td>autoprovisioned</td><td>&lt;Boolean></td><td>Read-write</td><td>Device is auto-provisioned or not.</td></tr><tr><td>is_managed</td><td>&lt;Boolean></td><td>Read-write</td><td>Is Managed.</td></tr><tr><td>number_of_cpu</td><td>&lt;Integer></td><td>Read-write</td><td>Number of CPU that is assigned to VM Instance.</td></tr><tr><td>instance_total</td><td>&lt;Integer></td><td>Read-write</td><td>Instance license.</td></tr><tr><td>is_ha_configured</td><td>&lt;Boolean></td><td>Read-write</td><td>Is HA configured.</td></tr><tr><td>trust_id</td><td>&lt;String></td><td>Read-write</td><td>Device ID obtained from trust service.</td></tr><tr><td>ipv4_address</td><td>&lt;String></td><td>Read-write</td><td>IPv4 Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>profile_name</td><td>&lt;String></td><td>Read-write</td><td>Device Profile Name that is attached with this managed device.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>backplane</td><td>&lt;String></td><td>Read-write</td><td>Backplane Interface.<br>Minimum length = 1</td></tr><tr><td>servicepackage</td><td>&lt;String></td><td>Read-write</td><td>Service Package Name of the device.</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Node State.<br>Minimum length = 1<br>Maximum length = 32</td></tr><tr><td>task_id</td><td>&lt;String></td><td>Read-write</td><td>Task Id used by Triton to identify NS.</td></tr><tr><td>last_updated_time</td><td>&lt;Double></td><td>Read-write</td><td>Last Updated Time.</td></tr><tr><td>partition_id</td><td>&lt;String></td><td>Read-write</td><td>ID of admin partition.</td></tr><tr><td>customid</td><td>&lt;String></td><td>Read-write</td><td>Custom ID.</td></tr><tr><td>number_of_ssl_cores</td><td>&lt;Integer></td><td>Read-write</td><td>Assign number of ssl virtual functions to VM Instance.</td></tr><tr><td>number_of_ssl_cards</td><td>&lt;Integer></td><td>Read-write</td><td>Number of SSL Cards.</td></tr><tr><td>max_burst_throughput</td><td>&lt;Double></td><td>Read-write</td><td>Maximum burst throughput in Mbps of VM Instance.</td></tr><tr><td>config_type</td><td>&lt;Integer></td><td>Read-write</td><td>Configuration Type. Values: 0: IPv4, 1: IPv6, 2: Both.<br>Maximum value =</td></tr><tr><td>cmd_policy</td><td>&lt;String></td><td>Read-write</td><td>true if you want to allow shell/sftp/scp access to NetScaler Instance administrator.<br>Minimum length = 1<br>Maximum length = 1024</td></tr><tr><td>node_id</td><td>&lt;String></td><td>Read-write</td><td>Node identification of a device.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address for this managed device.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>number_of_cores</td><td>&lt;Integer></td><td>Read-write</td><td>Number of cores that are assigned to VM Instance.</td></tr><tr><td>display_name</td><td>&lt;String></td><td>Read-write</td><td>Display Name for this managed device. For HA pair it will be A-B, and for Cluster it will be CLIP.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>std_bw_total</td><td>&lt;Integer></td><td>Read-write</td><td>Standard Bandwidth.</td></tr><tr><td>partition_name</td><td>&lt;String></td><td>Read-write</td><td>NS Admin Partition Name.<br>Maximum length = 512</td></tr><tr><td>plt_bw_config</td><td>&lt;Integer></td><td>Read-write</td><td>Platinum Bandwidth configured.</td></tr><tr><td>sslvpn_total</td><td>&lt;Integer></td><td>Read-write</td><td>sslvpn license.</td></tr><tr><td>agent_id</td><td>&lt;String></td><td>Read-write</td><td>Agent Id.</td></tr><tr><td>formation_instance_id</td><td>&lt;String></td><td>Read-write</td><td>This property is deprecated;ltbr;gtFormation Instance Id that this VM is Part of.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>save_config</td><td>&lt;Boolean></td><td>Read-write</td><td>Should config be saved first in case instance is rebooted while modify.</td></tr><tr><td>num_ports</td><td>&lt;Integer></td><td>Read-write</td><td>Number of CPX Ports to be exposed.</td></tr><tr><td>profile_username</td><td>&lt;String></td><td>Read-write</td><td>User Name specified by the user for this Netscaler Instance..<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>profile_password</td><td>&lt;String></td><td>Read-write</td><td>Password specified by the user for this Netscaler..<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>start_port</td><td>&lt;Integer></td><td>Read-write</td><td>Port assignment will be started from this value.</td></tr><tr><td>EULA</td><td>&lt;Boolean></td><td>Read-write</td><td>Value will be set to true if end user accepts EULA.</td></tr><tr><td>file_location_path</td><td>&lt;String></td><td>Read-write</td><td>File Location on Client for upload/download.<br>Minimum length = 1</td></tr><tr><td>file_name</td><td>&lt;String></td><td>Read-write</td><td>File name which contains comma separated instances to be discovered.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>LS_IP</td><td>&lt;String></td><td>Read-write</td><td>License server IP address.</td></tr><tr><td>entity_tag</td><td>&lt;property_map[]></td><td>Read-write</td><td>Array of tag_name and tag_value pair assocaited with an entity.</td></tr><tr><td>clusterid</td><td>&lt;Integer></td><td>Read-only</td><td>Cluster Id.</td></tr><tr><td>manufacturedate</td><td>&lt;String></td><td>Read-only</td><td>Manufacture Date.</td></tr><tr><td>instance_state</td><td>&lt;String></td><td>Read-only</td><td>State of device, UP only if device accessible.</td></tr><tr><td>diskavail</td><td>&lt;Integer></td><td>Read-only</td><td>NS Disk Available(MB).</td></tr><tr><td>virtualization</td><td>&lt;String></td><td>Read-only</td><td>paravirtual(PV) or Hardware Virtual Machine(HVM) (if hosted on AWS).</td></tr><tr><td>termination_protection</td><td>&lt;Boolean></td><td>Read-only</td><td>If termination_protection is enabled, instance can't be terminated unless it is disabled (if hosted on AWS).</td></tr><tr><td>vcpu_config</td><td>&lt;Integer></td><td>Read-only</td><td>Number of vCPU allocated for the device.</td></tr><tr><td>clip</td><td>&lt;String></td><td>Read-only</td><td>Cluster IP Address.</td></tr><tr><td>device_uuid</td><td>&lt;String></td><td>Read-only</td><td>Device UUID.</td></tr><tr><td>version</td><td>&lt;String></td><td>Read-only</td><td>Device Version.</td></tr><tr><td>health</td><td>&lt;String></td><td>Read-only</td><td>Node Health.</td></tr><tr><td>public_dns</td><td>&lt;String></td><td>Read-only</td><td>Public DNS of the managed device.</td></tr><tr><td>instance_type</td><td>&lt;String></td><td>Read-only</td><td>Instance type indicates the size of the managed device which is a combination of CPU, memory, storage, and networking capacity.</td></tr><tr><td>disksize</td><td>&lt;Integer></td><td>Read-only</td><td>NS Disk Size(MB).</td></tr><tr><td>sysid</td><td>&lt;String></td><td>Read-only</td><td>System ID.</td></tr><tr><td>nodeid</td><td>&lt;Integer></td><td>Read-only</td><td>Node Id.</td></tr><tr><td>tenancy</td><td>&lt;String></td><td>Read-only</td><td>default or dedicated. Dedicated means -&gt; running on a single tenant (if hosted on AWS).</td></tr><tr><td>vm_state</td><td>&lt;String></td><td>Read-only</td><td>State of Virtual Machine (Running | Halted).</td></tr><tr><td>uuid</td><td>&lt;String></td><td>Read-only</td><td>UUID of VM Instance.</td></tr><tr><td>encoded_serialnumber</td><td>&lt;String></td><td>Read-only</td><td>Encoded Serial Number.</td></tr><tr><td>ssl_virtual_functions</td><td>&lt;String></td><td>Read-only</td><td>SSL Virtual Functions assigned to VM Instance.</td></tr><tr><td>cpufrequncy</td><td>&lt;Integer></td><td>Read-only</td><td>CPU Frequency (MHZ).</td></tr><tr><td>http_req</td><td>&lt;Double></td><td>Read-only</td><td>HTTP Requests/second.</td></tr><tr><td>ha_sync</td><td>&lt;String></td><td>Read-only</td><td>HA Synchronization State.</td></tr><tr><td>ha_ip_address</td><td>&lt;String></td><td>Read-only</td><td>Peer IP Address.</td></tr><tr><td>node_state</td><td>&lt;String></td><td>Read-only</td><td>Node State of NetScaler Instance.</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Status of managed device.</td></tr><tr><td>systemname</td><td>&lt;String></td><td>Read-only</td><td>Device System Name.</td></tr><tr><td>geo_location</td><td>&lt;String></td><td>Read-only</td><td>Geo location of the managed device.</td></tr><tr><td>ns_memory_usage</td><td>&lt;Double></td><td>Read-only</td><td>Memory Usage (%).</td></tr><tr><td>instance_id</td><td>&lt;String></td><td>Read-only</td><td>Id of CPX instance.</td></tr><tr><td>serialnumber</td><td>&lt;String></td><td>Read-only</td><td>Device Serial Number.</td></tr><tr><td>subnet_id</td><td>&lt;String></td><td>Read-only</td><td>in which the instance was launched. Subnet is a Range of IP addresses in a VPC (if hosted on AWS).</td></tr><tr><td>ha_master_state</td><td>&lt;String></td><td>Read-only</td><td>Master State (Primary/Secondary).</td></tr><tr><td>vpc_id</td><td>&lt;String></td><td>Read-only</td><td>VPC ID of the managed device.</td></tr><tr><td>region</td><td>&lt;String></td><td>Read-only</td><td>Region in which the managed device is hosted.</td></tr><tr><td>reason</td><td>&lt;String></td><td>Read-only</td><td>Reason of failure for this managed device.</td></tr><tr><td>virtual_functions</td><td>&lt;String></td><td>Read-only</td><td>Virtual Functions assigned to VM Instance.</td></tr><tr><td>ns_total_tx</td><td>&lt;Double></td><td>Read-only</td><td>Total Tx of NetScaler Instance in Mbits.</td></tr><tr><td>upsince</td><td>&lt;String></td><td>Read-only</td><td>Upsince of managed device.</td></tr><tr><td>security_group</td><td>&lt;String></td><td>Read-only</td><td>virtual firewall that controls the traffic for one or more managed devices (if hosted on AWS).</td></tr><tr><td>private_dns</td><td>&lt;String></td><td>Read-only</td><td>Private DNS of the managed device.</td></tr><tr><td>zone</td><td>&lt;String></td><td>Read-only</td><td>Zone in which the managed device is hosted.</td></tr><tr><td>model_id</td><td>&lt;String></td><td>Read-only</td><td>Device Model Id.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant ID.</td></tr><tr><td>ns_mgmt_cpu_usage</td><td>&lt;Double></td><td>Read-only</td><td>Management CPU Usage (%).</td></tr><tr><td>port_range</td><td>&lt;String></td><td>Read-only</td><td>NetScaler CPX Exposed Port Range.</td></tr><tr><td>do_config</td><td>&lt;Boolean></td><td>Read-only</td><td>Do default config for managed device.</td></tr><tr><td>host_id</td><td>&lt;String></td><td>Read-only</td><td>Host ID.</td></tr><tr><td>system_hardwareversion</td><td>&lt;String></td><td>Read-only</td><td>System Hardware Version.</td></tr><tr><td>ns_tx</td><td>&lt;Double></td><td>Read-only</td><td>Out Throughput of NetScaler Instance in Mbps.</td></tr><tr><td>key_name</td><td>&lt;String></td><td>Read-only</td><td>name of the S3 bucket in which managed device is stored (if hosted on AWS).</td></tr><tr><td>is_swg</td><td>&lt;Boolean></td><td>Read-only</td><td>Boolean to indicate whether a VM is SWG.</td></tr><tr><td>diskused</td><td>&lt;Integer></td><td>Read-only</td><td>NS Disk Used(MB).</td></tr><tr><td>cloud</td><td>&lt;String></td><td>Read-only</td><td>Cloud on which the managed device is hosted.</td></tr><tr><td>uptime</td><td>&lt;String></td><td>Read-only</td><td>Uptime of device.</td></tr><tr><td>private_ip</td><td>&lt;String></td><td>Read-only</td><td>Private IP of the managed device.</td></tr><tr><td>cpu_license_type</td><td>&lt;Integer></td><td>Read-only</td><td>VCPU license 0 = No VCPU License, 1 = VCPU Pool license.</td></tr><tr><td>location</td><td>&lt;String></td><td>Read-only</td><td>Device Location.</td></tr><tr><td>contactperson</td><td>&lt;String></td><td>Read-only</td><td>Device contact person.</td></tr><tr><td>public_ip</td><td>&lt;String></td><td>Read-only</td><td>Public IP of the managed device.</td></tr><tr><td>ns_cpu_usage</td><td>&lt;Double></td><td>Read-only</td><td>CPU Usage (%) of NetScaler Instance.</td></tr><tr><td>bmcrevision</td><td>&lt;String></td><td>Read-only</td><td>BMC Firmware Version.</td></tr><tr><td>ns_rx</td><td>&lt;Double></td><td>Read-only</td><td>In Throughput of NetScaler Instance in Mbps.</td></tr><tr><td>vm_description</td><td>&lt;String></td><td>Read-only</td><td>Description.</td></tr><tr><td>diskperusage</td><td>&lt;Integer></td><td>Read-only</td><td>NS Disk Utilization (%).</td></tr><tr><td>ami_id</td><td>&lt;String></td><td>Read-only</td><td>AMI ID of the managed device (if hosted on AWS).</td></tr><tr><td>root_device_type</td><td>&lt;String></td><td>Read-only</td><td>contains the image used to boot the managed device (if hosted on AWS).</td></tr><tr><td>ebs_optimized</td><td>&lt;Boolean></td><td>Read-only</td><td>AWS offers consistent and low-latency performance if EBS optimized is true.</td></tr><tr><td>ns_total_rx</td><td>&lt;Double></td><td>Read-only</td><td>Total Rx of NetScaler Instance in Mbits.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr><tr><td>diff_exists</td><td>&lt;Boolean></td><td>Read-only</td><td>Indicates whether config diff exists for this instances or not.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[REBOOT](#r)| [UNMANAGE](#unm)| [GET (ALL)](#get-all)| [GET](#get)| [MANAGE](#m)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###reboot







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns/id_value&lt;String&gt;?action=reboot;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{"ns": { }}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>}
```







###unmanage







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns/id_value&lt;String&gt;?action=unmanage;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{"ns": { }}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>}
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns":[{
"clusterid":<Integer_value>,
"is_grace":<Boolean_value>,
"manufacturedate":<String_value>,
"gateway_deployment":<Boolean_value>,
"std_bw_config":<Integer_value>,
"ns_ip_address":<String_value>,
"gateway_ipv6":<String_value>,
"instance_available":<Integer_value>,
"instance_state":<String_value>,
"device_finger_print":<String_value>,
"name":<String_value>,
"diskavail":<Integer_value>,
"mastools_version":<String_value>,
"virtualization":<String_value>,
"ent_bw_total":<Integer_value>,
"termination_protection":<Boolean_value>,
"ssh_port":<Integer_value>,
"vcpu_config":<Integer_value>,
"clip":<String_value>,
"netmask":<String_value>,
"device_uuid":<String_value>,
"ent_bw_config":<Integer_value>,
"version":<String_value>,
"datacenter_id":<String_value>,
"instance_config":<Integer_value>,
"instance_mode":<String_value>,
"discovery_time":<Double_value>,
"health":<String_value>,
"public_dns":<String_value>,
"number_of_ssl_cores_up":<Integer_value>,
"instance_type":<String_value>,
"std_bw_available":<Integer_value>,
"disksize":<Integer_value>,
"sysid":<String_value>,
"nodeid":<Integer_value>,
"tenancy":<String_value>,
"instance_name":<String_value>,
"vm_state":<String_value>,
"uuid":<String_value>,
"encoded_serialnumber":<String_value>,
"ssl_virtual_functions":<String_value>,
"plt_bw_total":<Integer_value>,
"host_ip_address":<String_value>,
"id":<String_value>,
"ipv6_address":<String_value>,
"mgmt_ip_address":<String_value>,
"plt_bw_available":<Integer_value>,
"cpufrequncy":<Integer_value>,
"is_clip":<Boolean_value>,
"device_family":<String_value>,
"http_req":<Double_value>,
"ha_sync":<String_value>,
"ha_ip_address":<String_value>,
"type":<String_value>,
"throughput":<Double_value>,
"ns_observationdomainid":<String_value>,
"node_state":<String_value>,
"status":<String_value>,
"gateway":<String_value>,
"http_port":<Integer_value>,
"systemname":<String_value>,
"geo_location":<String_value>,
"iscco":<Boolean_value>,
"ns_memory_usage":<Double_value>,
"isolation_policy":<String_value>,
"instance_id":<String_value>,
"provision_request_id":<String_value>,
"lb_role":<String_value>,
"license":<String_value>,
"https_port":<Integer_value>,
"domain_name":<String_value>,
"serialnumber":<String_value>,
"snmp_port":<Integer_value>,
"subnet_id":<String_value>,
"image_name":<String_value>,
"hostname":<String_value>,
"ha_master_state":<String_value>,
"vpc_id":<String_value>,
"vnc_console_url":<String_value>,
"pre_auth_key":<String_value>,
"region":<String_value>,
"reason":<String_value>,
"virtual_functions":<String_value>,
"ns_total_tx":<Double_value>,
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
"model_id":<String_value>,
"sysservices":<Double_value>,
"host_type":<String_value>,
"tenant_id":<String_value>,
"ns_mgmt_cpu_usage":<Double_value>,
"num_pes":<Integer_value>,
"burst_priority":<Integer_value>,
"routable":<Boolean_value>,
"port_range":<String_value>,
"do_config":<Boolean_value>,
"autoprovisioned":<Boolean_value>,
"host_id":<String_value>,
"is_managed":<Boolean_value>,
"system_hardwareversion":<String_value>,
"ns_tx":<Double_value>,
"key_name":<String_value>,
"number_of_cpu":<Integer_value>,
"instance_total":<Integer_value>,
"is_ha_configured":<Boolean_value>,
"trust_id":<String_value>,
"ipv4_address":<String_value>,
"profile_name":<String_value>,
"is_swg":<Boolean_value>,
"seq_no":<Double_value>,
"dns":<String_value>,
"backplane":<String_value>,
"diskused":<Integer_value>,
"servicepackage":<String_value>,
"state":<String_value>,
"task_id":<String_value>,
"last_updated_time":<Double_value>,
"cloud":<String_value>,
"uptime":<String_value>,
"private_ip":<String_value>,
"license_edition":<String_value>,
"partition_id":<String_value>,
"cpu_license_type":<Integer_value>,
"upsince_persisted":<String_value>,
"location":<String_value>,
"customid":<String_value>,
"contactperson":<String_value>,
"public_ip":<String_value>,
"number_of_ssl_cores":<Integer_value>,
"ns_cpu_usage":<Double_value>,
"bmcrevision":<String_value>,
"number_of_ssl_cards":<Integer_value>,
"ns_rx":<Double_value>,
"vm_description":<String_value>,
"user_profile_name":<String_value>,
"max_burst_throughput":<Double_value>,
"config_type":<Integer_value>,
"cmd_policy":<String_value>,
"node_id":<String_value>,
"diskperusage":<Integer_value>,
"ip_address":<String_value>,
"ping_state":<Integer_value>,
"number_of_cores":<Integer_value>,
"display_name":<String_value>,
"std_bw_total":<Integer_value>,
"ami_id":<String_value>,
"root_device_type":<String_value>,
"ebs_optimized":<Boolean_value>,
"ns_total_rx":<Double_value>,
"partition_name":<String_value>,
"plt_bw_config":<Integer_value>,
"sslvpn_total":<Integer_value>,
"agent_id":<String_value>,
"formation_instance_id":<String_value>,
"config_progress_status":<String_value>,
"save_config":<Boolean_value>,
"num_ports":<Integer_value>,
"parent_inventory":<Boolean_value>,
"provision_request_id":<String_value>,
"profile_username":<String_value>,
"profile_password":<String_value>,
"start_port":<Integer_value>,
"EULA":<Boolean_value>,
"file_location_path":<String_value>,
"file_name":<String_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>,
"LS_IP":<String_value>,
"diff_exists":<Boolean_value>,
"entity_tag":[{
"prop_value":<String_value>,
"prop_key":<String_value>}]}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns":[{
"clusterid":<Integer_value>,
"is_grace":<Boolean_value>,
"manufacturedate":<String_value>,
"gateway_deployment":<Boolean_value>,
"std_bw_config":<Integer_value>,
"ns_ip_address":<String_value>,
"gateway_ipv6":<String_value>,
"instance_available":<Integer_value>,
"instance_state":<String_value>,
"device_finger_print":<String_value>,
"name":<String_value>,
"diskavail":<Integer_value>,
"mastools_version":<String_value>,
"virtualization":<String_value>,
"ent_bw_total":<Integer_value>,
"termination_protection":<Boolean_value>,
"ssh_port":<Integer_value>,
"vcpu_config":<Integer_value>,
"clip":<String_value>,
"netmask":<String_value>,
"device_uuid":<String_value>,
"ent_bw_config":<Integer_value>,
"version":<String_value>,
"datacenter_id":<String_value>,
"instance_config":<Integer_value>,
"instance_mode":<String_value>,
"discovery_time":<Double_value>,
"health":<String_value>,
"public_dns":<String_value>,
"number_of_ssl_cores_up":<Integer_value>,
"instance_type":<String_value>,
"std_bw_available":<Integer_value>,
"disksize":<Integer_value>,
"sysid":<String_value>,
"nodeid":<Integer_value>,
"tenancy":<String_value>,
"instance_name":<String_value>,
"vm_state":<String_value>,
"uuid":<String_value>,
"encoded_serialnumber":<String_value>,
"ssl_virtual_functions":<String_value>,
"plt_bw_total":<Integer_value>,
"host_ip_address":<String_value>,
"id":<String_value>,
"ipv6_address":<String_value>,
"mgmt_ip_address":<String_value>,
"plt_bw_available":<Integer_value>,
"cpufrequncy":<Integer_value>,
"is_clip":<Boolean_value>,
"device_family":<String_value>,
"http_req":<Double_value>,
"ha_sync":<String_value>,
"ha_ip_address":<String_value>,
"type":<String_value>,
"throughput":<Double_value>,
"ns_observationdomainid":<String_value>,
"node_state":<String_value>,
"status":<String_value>,
"gateway":<String_value>,
"http_port":<Integer_value>,
"systemname":<String_value>,
"geo_location":<String_value>,
"iscco":<Boolean_value>,
"ns_memory_usage":<Double_value>,
"isolation_policy":<String_value>,
"instance_id":<String_value>,
"provision_request_id":<String_value>,
"lb_role":<String_value>,
"license":<String_value>,
"https_port":<Integer_value>,
"domain_name":<String_value>,
"serialnumber":<String_value>,
"snmp_port":<Integer_value>,
"subnet_id":<String_value>,
"image_name":<String_value>,
"hostname":<String_value>,
"ha_master_state":<String_value>,
"vpc_id":<String_value>,
"vnc_console_url":<String_value>,
"pre_auth_key":<String_value>,
"region":<String_value>,
"reason":<String_value>,
"virtual_functions":<String_value>,
"ns_total_tx":<Double_value>,
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
"model_id":<String_value>,
"sysservices":<Double_value>,
"host_type":<String_value>,
"tenant_id":<String_value>,
"ns_mgmt_cpu_usage":<Double_value>,
"num_pes":<Integer_value>,
"burst_priority":<Integer_value>,
"routable":<Boolean_value>,
"port_range":<String_value>,
"do_config":<Boolean_value>,
"autoprovisioned":<Boolean_value>,
"host_id":<String_value>,
"is_managed":<Boolean_value>,
"system_hardwareversion":<String_value>,
"ns_tx":<Double_value>,
"key_name":<String_value>,
"number_of_cpu":<Integer_value>,
"instance_total":<Integer_value>,
"is_ha_configured":<Boolean_value>,
"trust_id":<String_value>,
"ipv4_address":<String_value>,
"profile_name":<String_value>,
"is_swg":<Boolean_value>,
"seq_no":<Double_value>,
"dns":<String_value>,
"backplane":<String_value>,
"diskused":<Integer_value>,
"servicepackage":<String_value>,
"state":<String_value>,
"task_id":<String_value>,
"last_updated_time":<Double_value>,
"cloud":<String_value>,
"uptime":<String_value>,
"private_ip":<String_value>,
"license_edition":<String_value>,
"partition_id":<String_value>,
"cpu_license_type":<Integer_value>,
"upsince_persisted":<String_value>,
"location":<String_value>,
"customid":<String_value>,
"contactperson":<String_value>,
"public_ip":<String_value>,
"number_of_ssl_cores":<Integer_value>,
"ns_cpu_usage":<Double_value>,
"bmcrevision":<String_value>,
"number_of_ssl_cards":<Integer_value>,
"ns_rx":<Double_value>,
"vm_description":<String_value>,
"user_profile_name":<String_value>,
"max_burst_throughput":<Double_value>,
"config_type":<Integer_value>,
"cmd_policy":<String_value>,
"node_id":<String_value>,
"diskperusage":<Integer_value>,
"ip_address":<String_value>,
"ping_state":<Integer_value>,
"number_of_cores":<Integer_value>,
"display_name":<String_value>,
"std_bw_total":<Integer_value>,
"ami_id":<String_value>,
"root_device_type":<String_value>,
"ebs_optimized":<Boolean_value>,
"ns_total_rx":<Double_value>,
"partition_name":<String_value>,
"plt_bw_config":<Integer_value>,
"sslvpn_total":<Integer_value>,
"agent_id":<String_value>,
"formation_instance_id":<String_value>,
"config_progress_status":<String_value>,
"save_config":<Boolean_value>,
"num_ports":<Integer_value>,
"parent_inventory":<Boolean_value>,
"provision_request_id":<String_value>,
"profile_username":<String_value>,
"profile_password":<String_value>,
"start_port":<Integer_value>,
"EULA":<Boolean_value>,
"file_location_path":<String_value>,
"file_name":<String_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>,
"LS_IP":<String_value>,
"diff_exists":<Boolean_value>,
"entity_tag":[{
"prop_value":<String_value>,
"prop_key":<String_value>}]}]}
```







###manage







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns/id_value&lt;String&gt;?action=manage;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{"ns": { }}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>}
```







