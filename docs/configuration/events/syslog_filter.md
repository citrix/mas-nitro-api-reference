#syslog_filter



Configuration for Syslog Suppress Filters resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>is_enabled</td><td>&lt;Boolean></td><td>Read-write</td><td>Filter is enabled or disabled.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Filter Name.<br>Maximum length = 255</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key.</td></tr><tr><td>severity</td><td>&lt;String></td><td>Read-write</td><td>Comma separated string of severities to be suppressed.</td></tr><tr><td>message</td><td>&lt;String></td><td>Read-write</td><td>Wildcard substring for syslog message to be suppressed.</td></tr><tr><td>facilities</td><td>&lt;String></td><td>Read-write</td><td>Comma separated string of facilities to be suppressed.</td></tr><tr><td>devices</td><td>&lt;String></td><td>Read-write</td><td>Comma separated string of devices to be suppressed.</td></tr><tr><td>facilities_array</td><td>&lt;String[]></td><td>Read-write</td><td>Facilities list.</td></tr><tr><td>devices_array</td><td>&lt;String[]></td><td>Read-write</td><td>Devices list.</td></tr><tr><td>severity_array</td><td>&lt;String[]></td><td>Read-write</td><td>Severity list.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_filter?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{syslog_filter: {
"devices_array":<String_value[]>,
"id":<String_value>,
"is_enabled":<Boolean_value>,
"name":<String_value>,
"devices":<String_value>,
"facilities_array":<String_value[]>,
"severity":<String_value>,
"message":<String_value>,
"severity_array":<String_value[]>,
"facilities":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "syslog_filter":[{
"is_enabled":<Boolean_value>,
"name":<String_value>,
"id":<String_value>,
"severity":<String_value>,
"message":<String_value>,
"facilities":<String_value>,
"devices":<String_value>,
"facilities_array":<String_value>,
"devices_array":<String_value>,
"severity_array":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_filter/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_filter

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "syslog_filter":[{
"is_enabled":<Boolean_value>,
"name":<String_value>,
"id":<String_value>,
"severity":<String_value>,
"message":<String_value>,
"facilities":<String_value>,
"devices":<String_value>,
"facilities_array":<String_value>,
"devices_array":<String_value>,
"severity_array":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_filter/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "syslog_filter":[{
"is_enabled":<Boolean_value>,
"name":<String_value>,
"id":<String_value>,
"severity":<String_value>,
"message":<String_value>,
"facilities":<String_value>,
"devices":<String_value>,
"facilities_array":<String_value>,
"devices_array":<String_value>,
"severity_array":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_filter/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{syslog_filter:{
<b>"id":<String_value></b>,
"devices_array":<String_value[]>,
"is_enabled":<Boolean_value>,
"name":<String_value>,
"devices":<String_value>,
"facilities_array":<String_value[]>,
"severity":<String_value>,
"message":<String_value>,
"severity_array":<String_value[]>,
"facilities":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "syslog_filter":[{
"is_enabled":<Boolean_value>,
"name":<String_value>,
"id":<String_value>,
"severity":<String_value>,
"message":<String_value>,
"facilities":<String_value>,
"devices":<String_value>,
"facilities_array":<String_value>,
"devices_array":<String_value>,
"severity_array":<String_value>}]}
```







