#device_license_info



Configuration for Device License Info resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>last_updated_time</td><td>&lt;Double></td><td>Read-write</td><td>Last Updated Time.</td></tr><tr><td>configured_on_vm</td><td>&lt;Integer></td><td>Read-only</td><td>Configured license capacity of VM.</td></tr><tr><td>current_throughput</td><td>&lt;String></td><td>Read-only</td><td>Current Througput of device.</td></tr><tr><td>license_pool</td><td>&lt;String></td><td>Read-only</td><td>License Pool.</td></tr><tr><td>allocated_on_vm</td><td>&lt;Integer></td><td>Read-only</td><td>Running license capacity of VM.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>Name of managed device.</td></tr><tr><td>days_to_expiry</td><td>&lt;Integer></td><td>Read-only</td><td>No of days after which grace license expires.</td></tr><tr><td>grace</td><td>&lt;Boolean></td><td>Read-only</td><td>True if this device is managed by NMX.</td></tr><tr><td>managed_device_id</td><td>&lt;String></td><td>Read-only</td><td>Device id managaed device.</td></tr><tr><td>license_state</td><td>&lt;String></td><td>Read-only</td><td>State of device, UP only if device accessible.</td></tr><tr><td>allocated</td><td>&lt;Integer></td><td>Read-only</td><td>Allocate license on License server.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-only</td><td>IP Address for this managed device.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Type of device, (Xen | NS).</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_license_info

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_license_info":[{
"configured_on_vm":<Integer_value>,
"current_throughput":<String_value>,
"license_pool":<String_value>,
"allocated_on_vm":<Integer_value>,
"name":<String_value>,
"days_to_expiry":<Integer_value>,
"grace":<Boolean_value>,
"managed_device_id":<String_value>,
"license_state":<String_value>,
"last_updated_time":<Double_value>,
"allocated":<Integer_value>,
"ip_address":<String_value>,
"type":<String_value>}]}
```







