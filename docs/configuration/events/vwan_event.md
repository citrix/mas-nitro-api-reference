#vwan_event



Configuration for VWAN EVENT resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the events.</td></tr><tr><td>source</td><td>&lt;String></td><td>Read-only</td><td>Source.</td></tr><tr><td>wan_link_state</td><td>&lt;String></td><td>Read-only</td><td>Internal Event ID used in the source device..</td></tr><tr><td>virtual_path</td><td>&lt;String></td><td>Read-only</td><td>Operation Type.</td></tr><tr><td>status_message</td><td>&lt;String></td><td>Read-only</td><td>status_message.</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-only</td><td>Event Time.</td></tr><tr><td>virtual_path_state</td><td>&lt;String></td><td>Read-only</td><td>virtual_path_state.</td></tr><tr><td>message</td><td>&lt;String></td><td>Read-only</td><td>VWAN Event_Message.</td></tr><tr><td>host_name</td><td>&lt;String></td><td>Read-only</td><td>Assign hostname to managed device, if this is not provided, name will be set as host name .</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>type.</td></tr><tr><td>category</td><td>&lt;String></td><td>Read-only</td><td>Category of VWAN Event.</td></tr><tr><td>severity</td><td>&lt;String></td><td>Read-only</td><td>Severity of Vwan Event.</td></tr><tr><td>wan_link</td><td>&lt;String></td><td>Read-only</td><td>WAN Link.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/vwan_event

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "vwan_event":[{
"source":<String_value>,
"wan_link_state":<String_value>,
"virtual_path":<String_value>,
"status_message":<String_value>,
"rpt_sample_time":<Double_value>,
"virtual_path_state":<String_value>,
"message":<String_value>,
"host_name":<String_value>,
"type":<String_value>,
"id":<String_value>,
"category":<String_value>,
"severity":<String_value>,
"wan_link":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/vwan_event/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "vwan_event":[{
"source":<String_value>,
"wan_link_state":<String_value>,
"virtual_path":<String_value>,
"status_message":<String_value>,
"rpt_sample_time":<Double_value>,
"virtual_path_state":<String_value>,
"message":<String_value>,
"host_name":<String_value>,
"type":<String_value>,
"id":<String_value>,
"category":<String_value>,
"severity":<String_value>,
"wan_link":<String_value>}]}
```







