#ns_application



Configuration for Applications Managed by Management System resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>curclntconnections</td><td>&lt;Double></td><td>Read-write</td><td>curclntconnections Value across all vips of the app.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Application Name.<br>Maximum length = 1024</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key..</td></tr><tr><td>app_criteria</td><td>&lt;criteria[]></td><td>Read-write</td><td>Application criteria.</td></tr><tr><td>cursrvrconnections</td><td>&lt;Double></td><td>Read-write</td><td>cursrvrconnections Value across all vips of the app.</td></tr><tr><td>configpack_id</td><td>&lt;String></td><td>Read-write</td><td>Config pack Id..</td></tr><tr><td>application_managed</td><td>&lt;Boolean></td><td>Read-write</td><td>Managed field.</td></tr><tr><td>family</td><td>&lt;String></td><td>Read-write</td><td>Application Family.<br>Minimum length = 1<br>Maximum length = 255</td></tr><tr><td>app_category</td><td>&lt;String></td><td>Read-write</td><td>Application Category.<br>Minimum length = 1<br>Maximum length = 255</td></tr><tr><td>throughput_avg</td><td>&lt;Double></td><td>Read-write</td><td>Sum of throughput across all vips of the app.</td></tr><tr><td>app_components</td><td>&lt;authorized_scope_app[]></td><td>Read-write</td><td>Application components.</td></tr><tr><td>no_of_auth</td><td>&lt;String></td><td>Read-write</td><td>Number of AUTH VIPs.</td></tr><tr><td>no_of_gslb</td><td>&lt;String></td><td>Read-write</td><td>Number of GSLB VIPs.</td></tr><tr><td>no_of_cr</td><td>&lt;String></td><td>Read-write</td><td>Number of CR VIPs.</td></tr><tr><td>no_of_gslbsvc</td><td>&lt;String></td><td>Read-write</td><td>Number of LB VIPs.</td></tr><tr><td>no_of_cs</td><td>&lt;String></td><td>Read-write</td><td>Number of CS VIPs.</td></tr><tr><td>no_of_svc</td><td>&lt;String></td><td>Read-write</td><td>Number of Services.</td></tr><tr><td>no_of_svcgrp</td><td>&lt;String></td><td>Read-write</td><td>Number of Service Groups.</td></tr><tr><td>no_of_haproxy_be</td><td>&lt;String></td><td>Read-write</td><td>Number of Banckends.</td></tr><tr><td>force_delete</td><td>&lt;Boolean></td><td>Read-write</td><td>force delete.</td></tr><tr><td>stylebook_params</td><td>&lt;String></td><td>Read-write</td><td>Stylebook Parameter.</td></tr><tr><td>no_of_svr</td><td>&lt;String></td><td>Read-write</td><td>Number of Servers.</td></tr><tr><td>no_of_vpn</td><td>&lt;String></td><td>Read-write</td><td>Number of VPN VIPs.</td></tr><tr><td>no_of_lb</td><td>&lt;String></td><td>Read-write</td><td>Number of LB VIPs.</td></tr><tr><td>application_ids</td><td>&lt;String[]></td><td>Read-write</td><td>Application IDs that are part of this application.</td></tr><tr><td>no_of_haproxy_fe</td><td>&lt;String></td><td>Read-write</td><td>Number of Frontends.</td></tr><tr><td>application_class</td><td>&lt;String></td><td>Read-only</td><td>Application class.</td></tr><tr><td>tenant_name</td><td>&lt;String></td><td>Read-only</td><td>Tenant Name.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant Id.</td></tr><tr><td>user_name</td><td>&lt;String></td><td>Read-only</td><td>User Name.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_application?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_application: {
"app_category":<String_value>,
"curclntconnections":<Double_value>,
"no_of_gslb":<String_value>,
"no_of_auth":<String_value>,
"no_of_gslbsvc":<String_value>,
"no_of_cr":<String_value>,
"no_of_cs":<String_value>,
"application_managed":<Boolean_value>,
"id":<String_value>,
"no_of_svc":<String_value>,
"app_criteria":[{
"criteria_condn":<String_value>,
"parent_id":<String_value>,
"id":<String_value>,
"criteria_value":<String_value>,
"parent_name":<String_value>,
"criteria_type":<String_value>}],
"no_of_svcgrp":<String_value>,
"throughput_avg":<Double_value>,
"name":<String_value>,
"cursrvrconnections":<Double_value>,
"no_of_haproxy_be":<String_value>,
"force_delete":<Boolean_value>,
"no_of_svr":<String_value>,
"stylebook_params":<String_value>,
"no_of_lb":<String_value>,
"no_of_vpn":<String_value>,
"no_of_haproxy_fe":<String_value>,
"application_ids":<String_value[]>,
"app_components":[{
"parent_id":<String_value>,
"appname":<String_value>,
"id":<String_value>,
"config_path":<String_value>,
"parent_name":<String_value>,
"app_state":<String_value>,
"app_protocol":<String_value>,
"device_ip_address":<String_value>,
"app_ip_address":<String_value>,
"app_type":<String_value>,
"entity_id":<String_value>}],
"family":<String_value>,
"configpack_id":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_application":[{
"curclntconnections":<Double_value>,
"name":<String_value>,
"application_class":<String_value>,
"id":<String_value>,
"app_criteria":[{
"parent_name":<String_value>,
"criteria_type":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"criteria_value":<String_value>,
"criteria_condn":<String_value>}],
"tenant_name":<String_value>,
"cursrvrconnections":<Double_value>,
"configpack_id":<String_value>,
"application_managed":<Boolean_value>,
"family":<String_value>,
"tenant_id":<String_value>,
"app_category":<String_value>,
"throughput_avg":<Double_value>,
"user_name":<String_value>,
"app_components":[{
"parent_name":<String_value>,
"app_state":<String_value>,
"parent_id":<String_value>,
"device_ip_address":<String_value>,
"app_protocol":<String_value>,
"appname":<String_value>,
"app_ip_address":<String_value>,
"entity_id":<String_value>,
"app_type":<String_value>,
"id":<String_value>,
"config_path":<String_value>}],
"no_of_auth":<String_value>,
"no_of_gslb":<String_value>,
"no_of_cr":<String_value>,
"no_of_gslbsvc":<String_value>,
"act_id":<String_value>,
"no_of_cs":<String_value>,
"no_of_svc":<String_value>,
"no_of_svcgrp":<String_value>,
"no_of_haproxy_be":<String_value>,
"force_delete":<Boolean_value>,
"stylebook_params":<String_value>,
"no_of_svr":<String_value>,
"no_of_vpn":<String_value>,
"no_of_lb":<String_value>,
"application_ids":<String_value>,
"no_of_haproxy_fe":<String_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_application/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_application

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_application":[{
"curclntconnections":<Double_value>,
"name":<String_value>,
"application_class":<String_value>,
"id":<String_value>,
"app_criteria":[{
"parent_name":<String_value>,
"criteria_type":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"criteria_value":<String_value>,
"criteria_condn":<String_value>}],
"tenant_name":<String_value>,
"cursrvrconnections":<Double_value>,
"configpack_id":<String_value>,
"application_managed":<Boolean_value>,
"family":<String_value>,
"tenant_id":<String_value>,
"app_category":<String_value>,
"throughput_avg":<Double_value>,
"user_name":<String_value>,
"app_components":[{
"parent_name":<String_value>,
"app_state":<String_value>,
"parent_id":<String_value>,
"device_ip_address":<String_value>,
"app_protocol":<String_value>,
"appname":<String_value>,
"app_ip_address":<String_value>,
"entity_id":<String_value>,
"app_type":<String_value>,
"id":<String_value>,
"config_path":<String_value>}],
"no_of_auth":<String_value>,
"no_of_gslb":<String_value>,
"no_of_cr":<String_value>,
"no_of_gslbsvc":<String_value>,
"act_id":<String_value>,
"no_of_cs":<String_value>,
"no_of_svc":<String_value>,
"no_of_svcgrp":<String_value>,
"no_of_haproxy_be":<String_value>,
"force_delete":<Boolean_value>,
"stylebook_params":<String_value>,
"no_of_svr":<String_value>,
"no_of_vpn":<String_value>,
"no_of_lb":<String_value>,
"application_ids":<String_value>,
"no_of_haproxy_fe":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_application/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_application":[{
"curclntconnections":<Double_value>,
"name":<String_value>,
"application_class":<String_value>,
"id":<String_value>,
"app_criteria":[{
"parent_name":<String_value>,
"criteria_type":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"criteria_value":<String_value>,
"criteria_condn":<String_value>}],
"tenant_name":<String_value>,
"cursrvrconnections":<Double_value>,
"configpack_id":<String_value>,
"application_managed":<Boolean_value>,
"family":<String_value>,
"tenant_id":<String_value>,
"app_category":<String_value>,
"throughput_avg":<Double_value>,
"user_name":<String_value>,
"app_components":[{
"parent_name":<String_value>,
"app_state":<String_value>,
"parent_id":<String_value>,
"device_ip_address":<String_value>,
"app_protocol":<String_value>,
"appname":<String_value>,
"app_ip_address":<String_value>,
"entity_id":<String_value>,
"app_type":<String_value>,
"id":<String_value>,
"config_path":<String_value>}],
"no_of_auth":<String_value>,
"no_of_gslb":<String_value>,
"no_of_cr":<String_value>,
"no_of_gslbsvc":<String_value>,
"act_id":<String_value>,
"no_of_cs":<String_value>,
"no_of_svc":<String_value>,
"no_of_svcgrp":<String_value>,
"no_of_haproxy_be":<String_value>,
"force_delete":<Boolean_value>,
"stylebook_params":<String_value>,
"no_of_svr":<String_value>,
"no_of_vpn":<String_value>,
"no_of_lb":<String_value>,
"application_ids":<String_value>,
"no_of_haproxy_fe":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_application/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_application:{
"app_category":<String_value>,
"curclntconnections":<Double_value>,
"no_of_gslb":<String_value>,
"no_of_auth":<String_value>,
"no_of_gslbsvc":<String_value>,
"no_of_cr":<String_value>,
"no_of_cs":<String_value>,
"application_managed":<Boolean_value>,
"id":<String_value>,
"no_of_svc":<String_value>,
"app_criteria":[{
"criteria_condn":<String_value>,
"parent_id":<String_value>,
"id":<String_value>,
"criteria_value":<String_value>,
"parent_name":<String_value>,
"criteria_type":<String_value>}],
"no_of_svcgrp":<String_value>,
"throughput_avg":<Double_value>,
"name":<String_value>,
"cursrvrconnections":<Double_value>,
"no_of_haproxy_be":<String_value>,
"force_delete":<Boolean_value>,
"no_of_svr":<String_value>,
"stylebook_params":<String_value>,
"no_of_lb":<String_value>,
"no_of_vpn":<String_value>,
"no_of_haproxy_fe":<String_value>,
"application_ids":<String_value[]>,
"app_components":[{
"parent_id":<String_value>,
"appname":<String_value>,
"id":<String_value>,
"config_path":<String_value>,
"parent_name":<String_value>,
"app_state":<String_value>,
"app_protocol":<String_value>,
"device_ip_address":<String_value>,
"app_ip_address":<String_value>,
"app_type":<String_value>,
"entity_id":<String_value>}],
"family":<String_value>,
"configpack_id":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_application":[{
"curclntconnections":<Double_value>,
"name":<String_value>,
"application_class":<String_value>,
"id":<String_value>,
"app_criteria":[{
"parent_name":<String_value>,
"criteria_type":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"criteria_value":<String_value>,
"criteria_condn":<String_value>}],
"tenant_name":<String_value>,
"cursrvrconnections":<Double_value>,
"configpack_id":<String_value>,
"application_managed":<Boolean_value>,
"family":<String_value>,
"tenant_id":<String_value>,
"app_category":<String_value>,
"throughput_avg":<Double_value>,
"user_name":<String_value>,
"app_components":[{
"parent_name":<String_value>,
"app_state":<String_value>,
"parent_id":<String_value>,
"device_ip_address":<String_value>,
"app_protocol":<String_value>,
"appname":<String_value>,
"app_ip_address":<String_value>,
"entity_id":<String_value>,
"app_type":<String_value>,
"id":<String_value>,
"config_path":<String_value>}],
"no_of_auth":<String_value>,
"no_of_gslb":<String_value>,
"no_of_cr":<String_value>,
"no_of_gslbsvc":<String_value>,
"act_id":<String_value>,
"no_of_cs":<String_value>,
"no_of_svc":<String_value>,
"no_of_svcgrp":<String_value>,
"no_of_haproxy_be":<String_value>,
"force_delete":<Boolean_value>,
"stylebook_params":<String_value>,
"no_of_svr":<String_value>,
"no_of_vpn":<String_value>,
"no_of_lb":<String_value>,
"application_ids":<String_value>,
"no_of_haproxy_fe":<String_value>}]}
```







