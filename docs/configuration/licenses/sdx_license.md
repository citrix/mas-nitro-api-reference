#sdx_license



Configuration for License Information resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>std_bw_available</td><td>&lt;String></td><td>Read-only</td><td>Available standard Bandwidth in Mbps.</td></tr><tr><td>max_number_of_ns_instances</td><td>&lt;Integer></td><td>Read-only</td><td>Maximum NetScaler Instances.</td></tr><tr><td>std_bw_config</td><td>&lt;String></td><td>Read-only</td><td>Configured Standard Bandwidth in Mbps.</td></tr><tr><td>ent_bw_total</td><td>&lt;String></td><td>Read-only</td><td>Total enterprise Bandwidth in Mbps.</td></tr><tr><td>provisioned_swg_instances</td><td>&lt;Integer></td><td>Read-only</td><td>Provisioned number of SWG Instances.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr><tr><td>available_throughput</td><td>&lt;String></td><td>Read-only</td><td>Available Throughput in Mbps.</td></tr><tr><td>instances_config</td><td>&lt;Integer></td><td>Read-only</td><td>Instances Configured .</td></tr><tr><td>plt_bw_total</td><td>&lt;String></td><td>Read-only</td><td>Maximum platinum Bandwidth in Mbps.</td></tr><tr><td>platform</td><td>&lt;String></td><td>Read-only</td><td>Platform.</td></tr><tr><td>max_number_of_instances</td><td>&lt;Integer></td><td>Read-only</td><td>Maximum Instances.</td></tr><tr><td>max_number_of_br_instances</td><td>&lt;Integer></td><td>Read-only</td><td>Maximum NetScaler SD-WAN Instances.</td></tr><tr><td>plt_bw_available</td><td>&lt;String></td><td>Read-only</td><td>Available platinum Bandwidth in Mbps.</td></tr><tr><td>provisioned_nonswg_instances</td><td>&lt;Integer></td><td>Read-only</td><td>Provisioned number of NS/ADC/Third-party VM Instances.</td></tr><tr><td>ent_bw_config</td><td>&lt;String></td><td>Read-only</td><td>Configured Enterpise Bandwidth in Mbps.</td></tr><tr><td>cluster</td><td>&lt;Boolean></td><td>Read-only</td><td>Cluster License.</td></tr><tr><td>available_number_of_ns_instances</td><td>&lt;Integer></td><td>Read-only</td><td>Available NetScaler Instances (Shared).</td></tr><tr><td>max_throughput</td><td>&lt;String></td><td>Read-only</td><td>Maximum Throughput in Mbps.</td></tr><tr><td>available_nonswg_instances</td><td>&lt;Integer></td><td>Read-only</td><td>Available number of NS/ADC/Third-party VM Instances.</td></tr><tr><td>std_bw_total</td><td>&lt;String></td><td>Read-only</td><td>Total standard Bandwidth in Mbps.</td></tr><tr><td>ent_bw_available</td><td>&lt;String></td><td>Read-only</td><td>Available enterprise Bandwidth in Mbps.</td></tr><tr><td>plt_bw_config</td><td>&lt;String></td><td>Read-only</td><td>Configured platinum Bandwidth in Mbps.</td></tr><tr><td>available_swg_instances</td><td>&lt;Integer></td><td>Read-only</td><td>Available number of SWG Instances.</td></tr><tr><td>is_pooled_license</td><td>&lt;Boolean></td><td>Read-only</td><td>Platform license for Triscaler feature.</td></tr><tr><td>swg_license_present</td><td>&lt;Boolean></td><td>Read-only</td><td>Indication for SWG License.</td></tr><tr><td>available_number_of_instances</td><td>&lt;Integer></td><td>Read-only</td><td>Available Instances.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[APPLY](#)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###apply







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sdx_license?action=apply;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{"sdx_license": { }}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sdx_license

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "sdx_license":[{
"std_bw_available":<String_value>,
"max_number_of_ns_instances":<Integer_value>,
"std_bw_config":<String_value>,
"ent_bw_total":<String_value>,
"provisioned_swg_instances":<Integer_value>,
"act_id":<String_value>,
"available_throughput":<String_value>,
"instances_config":<Integer_value>,
"plt_bw_total":<String_value>,
"platform":<String_value>,
"max_number_of_instances":<Integer_value>,
"max_number_of_br_instances":<Integer_value>,
"plt_bw_available":<String_value>,
"provisioned_nonswg_instances":<Integer_value>,
"ent_bw_config":<String_value>,
"cluster":<Boolean_value>,
"available_number_of_ns_instances":<Integer_value>,
"max_throughput":<String_value>,
"available_nonswg_instances":<Integer_value>,
"std_bw_total":<String_value>,
"ent_bw_available":<String_value>,
"sync_operation":<Boolean_value>,
"plt_bw_config":<String_value>,
"available_swg_instances":<Integer_value>,
"is_pooled_license":<Boolean_value>,
"swg_license_present":<Boolean_value>,
"available_number_of_instances":<Integer_value>}]}
```







