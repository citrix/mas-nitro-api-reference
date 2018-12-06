#lb_export_report



Configuration for Export or Schedule NS Entities report resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>is_enabled</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable Scheduled Report (default is enabled).</td></tr><tr><td>enable_cr</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable CR Report.</td></tr><tr><td>enable_lb</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable LB Report.</td></tr><tr><td>enable_gslb</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable GSLB Report.</td></tr><tr><td>recurrence_type</td><td>&lt;String></td><td>Read-write</td><td>Tenant.<br>Maximum length = 255</td></tr><tr><td>enable_sslvpn</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable SSLVPN Report.</td></tr><tr><td>tz_offset</td><td>&lt;Integer></td><td>Read-write</td><td>Time zone offset..</td></tr><tr><td>recurrence_options</td><td>&lt;String></td><td>Read-write</td><td>Comma Seperated recurrence options of job that is scheduled.</td></tr><tr><td>enable_auth</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable Auth Report.</td></tr><tr><td>file_name</td><td>&lt;String></td><td>Read-write</td><td>Report File name..</td></tr><tr><td>recurrence_times_epoch</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch (string representation of 11 digit numbers)..</td></tr><tr><td>export_now</td><td>&lt;Boolean></td><td>Read-write</td><td>Export now.</td></tr><tr><td>enable_cs</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable CS Report.</td></tr><tr><td>mail_profile</td><td>&lt;String></td><td>Read-write</td><td>Mail Profile.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [GET (ALL)](#get-all)| [UPDATE](#update)| [DOWNLOAD](#dow)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/lb_export_report?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{lb_export_report: {
"enable_auth":<Boolean_value>,
"recurrence_times_epoch":<String_value>,
"file_name":<String_value>,
"mail_profile":<String_value>,
"is_enabled":<Boolean_value>,
"enable_cr":<Boolean_value>,
"enable_lb":<Boolean_value>,
"enable_gslb":<Boolean_value>,
"recurrence_type":<String_value>,
"recurrence_options":<String_value>,
"tz_offset":<Integer_value>,
"enable_sslvpn":<Boolean_value>,
"export_now":<Boolean_value>,
"enable_cs":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "lb_export_report":[{
"is_enabled":<Boolean_value>,
"enable_cr":<Boolean_value>,
"enable_lb":<Boolean_value>,
"enable_gslb":<Boolean_value>,
"recurrence_type":<String_value>,
"enable_sslvpn":<Boolean_value>,
"tz_offset":<Integer_value>,
"recurrence_options":<String_value>,
"enable_auth":<Boolean_value>,
"file_name":<String_value>,
"recurrence_times_epoch":<String_value>,
"export_now":<Boolean_value>,
"enable_cs":<Boolean_value>,
"mail_profile":<String_value>}]}
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/lb_export_report

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "lb_export_report":[{
"is_enabled":<Boolean_value>,
"enable_cr":<Boolean_value>,
"enable_lb":<Boolean_value>,
"enable_gslb":<Boolean_value>,
"recurrence_type":<String_value>,
"enable_sslvpn":<Boolean_value>,
"tz_offset":<Integer_value>,
"recurrence_options":<String_value>,
"enable_auth":<Boolean_value>,
"file_name":<String_value>,
"recurrence_times_epoch":<String_value>,
"export_now":<Boolean_value>,
"enable_cs":<Boolean_value>,
"mail_profile":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/lb_export_report/

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{lb_export_report:{
"enable_auth":<Boolean_value>,
"recurrence_times_epoch":<String_value>,
"file_name":<String_value>,
"mail_profile":<String_value>,
"is_enabled":<Boolean_value>,
"enable_cr":<Boolean_value>,
"enable_lb":<Boolean_value>,
"enable_gslb":<Boolean_value>,
"recurrence_type":<String_value>,
"recurrence_options":<String_value>,
"tz_offset":<Integer_value>,
"enable_sslvpn":<Boolean_value>,
"export_now":<Boolean_value>,
"enable_cs":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "lb_export_report":[{
"is_enabled":<Boolean_value>,
"enable_cr":<Boolean_value>,
"enable_lb":<Boolean_value>,
"enable_gslb":<Boolean_value>,
"recurrence_type":<String_value>,
"enable_sslvpn":<Boolean_value>,
"tz_offset":<Integer_value>,
"recurrence_options":<String_value>,
"enable_auth":<Boolean_value>,
"file_name":<String_value>,
"recurrence_times_epoch":<String_value>,
"export_now":<Boolean_value>,
"enable_cs":<Boolean_value>,
"mail_profile":<String_value>}]}
```







###download







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/download/lb_export_report/_value&lt;&gt;

<b>HTTP Method:</b>null







