#ns_vserver_appflow_config

Configuration for Virtual server appflow config on NetScaler resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NetScaler IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>TenantID.</td></tr><tr><td>agent_list</td><td>&lt;String[]></td><td>Read-write</td><td>Agent List, on which traffic will flow.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>Virtual server IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>icalog</td><td>&lt;String></td><td>Read-write</td><td>ICA log.</td></tr><tr><td>servicetype</td><td>&lt;String></td><td>Read-write</td><td>servicetype.</td></tr><tr><td>export_option</td><td>&lt;String[]></td><td>Read-write</td><td>Export Options: TCP, ICA.</td></tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Appflow log.</td></tr><tr><td>appflow_policy_rule</td><td>&lt;String></td><td>Read-write</td><td>Appflow policy rule.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Virtual server name.<br>Maximum length = 255</td></tr><tr><td>es4nslog</td><td>&lt;String></td><td>Read-write</td><td>ESNS enable.</td></tr><tr><td>export_list</td><td>&lt;String[]></td><td>Read-write</td><td>Export List: WebInsight, SecurityInsight.</td></tr><tr><td>transport_mode</td><td>&lt;String></td><td>Read-write</td><td>Transport Mode [ Logstream/Appflow ].</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Tells whether virtual server type.<br>Minimum length = 2<br>Maximum length = 64</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>Tells whether virtual server up/down.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [GET (ALL)](#get-)| [MODIFY](#m)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_vserver_appflow_config?onerror=&lt;String_value&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{ns_vserver_appflow_config: {"ns_ip_address":<String_value>,"agent_list":<String_value[]>,"tenant_id":<String_value>,"ip_address":<String_value>,"servicetype":<String_value>,"icalog":<String_value>,"export_option":<String_value[]>,"appflow_policy_rule":<String_value>,"appflowlog":<String_value>,"es4nslog":<String_value>,"name":<String_value>,"export_list":<String_value[]>,"transport_mode":<String_value>,"type":<String_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_vserver_appflow_config":[{"state":<String_value>,"ns_ip_address":<String_value>,"tenant_id":<String_value>,"agent_list":<String_value>,"ip_address":<String_value>,"icalog":<String_value>,"servicetype":<String_value>,"export_option":<String_value>,"primary_appflowlog":<String_value>,"appflowlog":<String_value>,"appflow_policy_rule":<String_value>,"name":<String_value>,"es4nslog":<String_value>,"export_list":<String_value>,"is_vsever_to_query":<Boolean_value>,"transport_mode":<String_value>,"type":<String_value>}]}```



###delete



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_vserver_appflow_config/
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }```



###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_vserver_appflow_config
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_vserver_appflow_config":[{"state":<String_value>,"ns_ip_address":<String_value>,"tenant_id":<String_value>,"agent_list":<String_value>,"ip_address":<String_value>,"icalog":<String_value>,"servicetype":<String_value>,"export_option":<String_value>,"primary_appflowlog":<String_value>,"appflowlog":<String_value>,"appflow_policy_rule":<String_value>,"name":<String_value>,"es4nslog":<String_value>,"export_list":<String_value>,"is_vsever_to_query":<Boolean_value>,"transport_mode":<String_value>,"type":<String_value>}]}```



###modify



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_vserver_appflow_config/
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{ns_vserver_appflow_config:{"ns_ip_address":<String_value>,"agent_list":<String_value[]>,"tenant_id":<String_value>,"ip_address":<String_value>,"servicetype":<String_value>,"icalog":<String_value>,"export_option":<String_value[]>,"appflow_policy_rule":<String_value>,"appflowlog":<String_value>,"es4nslog":<String_value>,"name":<String_value>,"export_list":<String_value[]>,"transport_mode":<String_value>,"type":<String_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_vserver_appflow_config":[{"state":<String_value>,"ns_ip_address":<String_value>,"tenant_id":<String_value>,"agent_list":<String_value>,"ip_address":<String_value>,"icalog":<String_value>,"servicetype":<String_value>,"export_option":<String_value>,"primary_appflowlog":<String_value>,"appflowlog":<String_value>,"appflow_policy_rule":<String_value>,"name":<String_value>,"es4nslog":<String_value>,"export_list":<String_value>,"is_vsever_to_query":<Boolean_value>,"transport_mode":<String_value>,"type":<String_value>}]}```



