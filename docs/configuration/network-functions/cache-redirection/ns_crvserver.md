#ns_crvserver

Configuration for NS CRvserver Information resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>user_managed</td><td>&lt;Boolean></td><td>Read-write</td><td>User Managed Idenfication.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NS IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key.</td></tr><tr><td>vsvr_port</td><td>&lt;Integer></td><td>Read-write</td><td>Vserver Port.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Vserver Name.<br>Minimum length = 1<br>Maximum length = 100</td></tr><tr><td>managed</td><td>&lt;Boolean></td><td>Read-write</td><td>Managed.</td></tr><tr><td>vsvr_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Vserver IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>throughput</td><td>&lt;Double></td><td>Read-write</td><td>throughput value.</td></tr><tr><td>save_config</td><td>&lt;Boolean></td><td>Read-write</td><td>Save configuration after enable/disable.</td></tr><tr><td>is_throughput_req</td><td>&lt;Boolean></td><td>Read-write</td><td>Throghput required.</td></tr><tr><td>hostname</td><td>&lt;String></td><td>Read-only</td><td>Hostname of the managed device.</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>Vserver State.</td></tr><tr><td>cachetype</td><td>&lt;String></td><td>Read-only</td><td>Cache Type.</td></tr><tr><td>hits</td><td>&lt;String></td><td>Read-only</td><td>Vserver Health.</td></tr><tr><td>vsvr_type</td><td>&lt;String></td><td>Read-only</td><td>Vserver Type.</td></tr><tr><td>poll_time</td><td>&lt;Integer></td><td>Read-only</td><td>Last Polling Time.</td></tr><tr><td>display_name</td><td>&lt;String></td><td>Read-only</td><td>Display Name.</td></tr><tr><td>partition_name</td><td>&lt;String></td><td>Read-only</td><td>Partition Name.</td></tr><tr><td>targetlbvserver</td><td>&lt;String></td><td>Read-only</td><td>Default Target LBVserver.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ENABLE](#e)| [POLL]()| [GET]()| [DISABLE](#di)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###enable



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_crvserver?action=enable;onerror=&lt;String_value&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{ns_crvserver: {<b>"id":<String_value></b>,"user_managed":<Boolean_value>,"is_throughput_req":<Boolean_value>,"ns_ip_address":<String_value>,"save_config":<Boolean_value>,"vsvr_port":<Integer_value>,"name":<String_value>,"managed":<Boolean_value>,"vsvr_ip_address":<String_value>,"throughput":<Double_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_crvserver":[{"user_managed":<Boolean_value>,"hostname":<String_value>,"state":<String_value>,"ns_ip_address":<String_value>,"cachetype":<String_value>,"hits":<String_value>,"vsvr_type":<String_value>,"id":<String_value>,"vsvr_port":<Integer_value>,"name":<String_value>,"poll_time":<Integer_value>,"display_name":<String_value>,"managed":<Boolean_value>,"partition_name":<String_value>,"targetlbvserver":<String_value>,"vsvr_ip_address":<String_value>,"throughput":<Double_value>,"save_config":<Boolean_value>,"is_throughput_req":<Boolean_value>}]}```



###poll



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_crvserver?action=poll;onerror=&lt;String_value&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{ns_crvserver: {<b>"id":<String_value></b>,"user_managed":<Boolean_value>,"is_throughput_req":<Boolean_value>,"ns_ip_address":<String_value>,"save_config":<Boolean_value>,"vsvr_port":<Integer_value>,"name":<String_value>,"managed":<Boolean_value>,"vsvr_ip_address":<String_value>,"throughput":<Double_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_crvserver":[{"user_managed":<Boolean_value>,"hostname":<String_value>,"state":<String_value>,"ns_ip_address":<String_value>,"cachetype":<String_value>,"hits":<String_value>,"vsvr_type":<String_value>,"id":<String_value>,"vsvr_port":<Integer_value>,"name":<String_value>,"poll_time":<Integer_value>,"display_name":<String_value>,"managed":<Boolean_value>,"partition_name":<String_value>,"targetlbvserver":<String_value>,"vsvr_ip_address":<String_value>,"throughput":<Double_value>,"save_config":<Boolean_value>,"is_throughput_req":<Boolean_value>}]}```



###get



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_crvserver
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_crvserver":[{"user_managed":<Boolean_value>,"hostname":<String_value>,"state":<String_value>,"ns_ip_address":<String_value>,"cachetype":<String_value>,"hits":<String_value>,"vsvr_type":<String_value>,"id":<String_value>,"vsvr_port":<Integer_value>,"name":<String_value>,"poll_time":<Integer_value>,"display_name":<String_value>,"managed":<Boolean_value>,"partition_name":<String_value>,"targetlbvserver":<String_value>,"vsvr_ip_address":<String_value>,"throughput":<Double_value>,"save_config":<Boolean_value>,"is_throughput_req":<Boolean_value>}]}```



###disable



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_crvserver?action=disable;onerror=&lt;String_value&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{ns_crvserver: {<b>"id":<String_value></b>,"user_managed":<Boolean_value>,"is_throughput_req":<Boolean_value>,"ns_ip_address":<String_value>,"save_config":<Boolean_value>,"vsvr_port":<Integer_value>,"name":<String_value>,"managed":<Boolean_value>,"vsvr_ip_address":<String_value>,"throughput":<Double_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_crvserver":[{"user_managed":<Boolean_value>,"hostname":<String_value>,"state":<String_value>,"ns_ip_address":<String_value>,"cachetype":<String_value>,"hits":<String_value>,"vsvr_type":<String_value>,"id":<String_value>,"vsvr_port":<Integer_value>,"name":<String_value>,"poll_time":<Integer_value>,"display_name":<String_value>,"managed":<Boolean_value>,"partition_name":<String_value>,"targetlbvserver":<String_value>,"vsvr_ip_address":<String_value>,"throughput":<Double_value>,"save_config":<Boolean_value>,"is_throughput_req":<Boolean_value>}]}```



