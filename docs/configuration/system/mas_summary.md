#mas_summary



Configuration for MAS Summary resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sdwanwo_count</td><td>&lt;Integer></td><td>Read-only</td><td>SDWAN WO count.</td></tr><tr><td>sdx_count</td><td>&lt;Integer></td><td>Read-only</td><td>SDX count.</td></tr><tr><td>partition_count</td><td>&lt;Integer></td><td>Read-only</td><td>Admin Partitions count.</td></tr><tr><td>gateway_count</td><td>&lt;Integer></td><td>Read-only</td><td>Gateway count.</td></tr><tr><td>ns_service_count</td><td>&lt;Integer></td><td>Read-only</td><td>Service count.</td></tr><tr><td>ns_vip_count</td><td>&lt;Integer></td><td>Read-only</td><td>VIP count.</td></tr><tr><td>haproxy_count</td><td>&lt;Integer></td><td>Read-only</td><td>HAProxy count.</td></tr><tr><td>application_count</td><td>&lt;Integer></td><td>Read-only</td><td>Application count.</td></tr><tr><td>ns_count</td><td>&lt;Integer></td><td>Read-only</td><td>NS count.</td></tr><tr><td>ns_ssl_certkey_count</td><td>&lt;Integer></td><td>Read-only</td><td>SSL certificate count.</td></tr><tr><td>ns_servicegroup_count</td><td>&lt;Integer></td><td>Read-only</td><td>Service count.</td></tr><tr><td>tenant_count</td><td>&lt;Integer></td><td>Read-only</td><td>Tenants count.</td></tr><tr><td>sdwanee_count</td><td>&lt;Integer></td><td>Read-only</td><td>SDWAN EE count.</td></tr><tr><td>swg_count</td><td>&lt;Integer></td><td>Read-only</td><td>SWG count.</td></tr><tr><td>dc_count</td><td>&lt;Integer></td><td>Read-only</td><td>DataCenter count.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mas_summary

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mas_summary":[{
"sdwanwo_count":<Integer_value>,
"sdx_count":<Integer_value>,
"partition_count":<Integer_value>,
"gateway_count":<Integer_value>,
"ns_service_count":<Integer_value>,
"ns_vip_count":<Integer_value>,
"haproxy_count":<Integer_value>,
"application_count":<Integer_value>,
"ns_count":<Integer_value>,
"ns_ssl_certkey_count":<Integer_value>,
"ns_servicegroup_count":<Integer_value>,
"tenant_count":<Integer_value>,
"sdwanee_count":<Integer_value>,
"swg_count":<Integer_value>,
"dc_count":<Integer_value>}]}
```







