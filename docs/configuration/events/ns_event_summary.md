#ns_event_summary

Configuration for NS event devices summary resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>longitude</td><td>&lt;Double></td><td>Read-write</td><td>longitude.</td></tr><tr><td>is_agent</td><td>&lt;Boolean></td><td>Read-write</td><td>Is this device acting as Gateway..</td></tr><tr><td>latitude</td><td>&lt;Double></td><td>Read-write</td><td>latitude.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>ip_address of the device..</td></tr><tr><td>cityname</td><td>&lt;String></td><td>Read-write</td><td>City Name.<br>Maximum length = 255</td></tr><tr><td>total_critical_events</td><td>&lt;Integer></td><td>Read-only</td><td>Total Critical events city wise..</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant Id.</td></tr><tr><td>total_major_events</td><td>&lt;Integer></td><td>Read-only</td><td>Total major events..</td></tr><tr><td>instance_state</td><td>&lt;String></td><td>Read-only</td><td>State of device, UP only if device accessible.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_event_summary
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_event_summary":[{"total_critical_events":<Integer_value>,"longitude":<Double_value>,"tenant_id":<String_value>,"is_agent":<Boolean_value>,"latitude":<Double_value>,"total_major_events":<Integer_value>,"ip_address":<String_value>,"instance_state":<String_value>,"cityname":<String_value>}]}```



###get



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_event_summary/ip_address_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_event_summary":[{"total_critical_events":<Integer_value>,"longitude":<Double_value>,"tenant_id":<String_value>,"is_agent":<Boolean_value>,"latitude":<Double_value>,"total_major_events":<Integer_value>,"ip_address":<String_value>,"instance_state":<String_value>,"cityname":<String_value>}]}```



