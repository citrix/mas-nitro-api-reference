#config_advice



Configuration for Config Advice resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>is_xendesktop</td><td>&lt;Boolean></td><td>Read-write</td><td>Enables search for Xen Desktop properties .</td></tr><tr><td>output_file</td><td>&lt;String></td><td>Read-write</td><td>File Path.</td></tr><tr><td>is_pci</td><td>&lt;Boolean></td><td>Read-write</td><td>Enables search for PCI properties.</td></tr><tr><td>config_advice_results</td><td>&lt;config_advice_result[]></td><td>Read-write</td><td>config advice result.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>command</td><td>&lt;String></td><td>Read-write</td><td>Commands.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[CUSTOM](#c)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###custom







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/config_advice?action=custom;onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{config_advice: {
"is_pci":<Boolean_value>,
"id":<String_value>,
"is_xendesktop":<Boolean_value>,
"ip_address":<String_value>,
"command":<String_value>,
"config_advice_results":[{
"modification_status_message":<String_value>,
"parent_id":<String_value>,
"issue":<String_value>,
"category":<String_value>,
"id":<String_value>,
"parent_name":<String_value>,
"corrective_command":<String_value>,
"advice":<String_value>,
"severity":<String_value>,
"modification_status":<Boolean_value>}],
"output_file":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "config_advice":[{
"is_xendesktop":<Boolean_value>,
"output_file":<String_value>,
"is_pci":<Boolean_value>,
"config_advice_results":[{
"parent_name":<String_value>,
"modification_status_message":<String_value>,
"issue":<String_value>,
"parent_id":<String_value>,
"modification_status":<Boolean_value>,
"corrective_command":<String_value>,
"id":<String_value>,
"category":<String_value>,
"severity":<String_value>,
"advice":<String_value>}],
"ip_address":<String_value>,
"id":<String_value>,
"command":<String_value>}]}
```







