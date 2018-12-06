#snmp_user



Configuration for SNMP User resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>security_level</td><td>&lt;Integer></td><td>Read-write</td><td>Security Level of SNMP User. Values: 0: noAuthNoPriv, 1: authNoPriv, 2: authPriv.<br>Maximum value =</td></tr><tr><td>auth_password</td><td>&lt;String></td><td>Read-write</td><td>Authentication Password of SNMP User.<br>Minimum length = 8<br>Maximum length = 32</td></tr><tr><td>privacy_protocol</td><td>&lt;Integer></td><td>Read-write</td><td>Privacy Protocol of SNMP User. Values: 0:noValue, 1: DES, 2: AES.<br>Maximum value =</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of SNMP User.<br>Minimum length = 1<br>Maximum length = 32</td></tr><tr><td>privacy_password</td><td>&lt;String></td><td>Read-write</td><td>Privacy Password of SNMP User.<br>Minimum length = 8<br>Maximum length = 32</td></tr><tr><td>view_name</td><td>&lt;String></td><td>Read-write</td><td>SNMP View Name attached to the SNMP User.<br>Maximum length = 32</td></tr><tr><td>auth_protocol</td><td>&lt;Integer></td><td>Read-write</td><td>Authentication Protocol of SNMP User. Values: 0:noValue, 1: MD5, 2: SHA1.<br>Maximum value =</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/snmp_user?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{snmp_user: {
<b>"security_level":<Integer_value></b>,
<b>"name":<String_value></b>,
"privacy_password":<String_value>,
"auth_protocol":<Integer_value>,
"view_name":<String_value>,
"auth_password":<String_value>,
"privacy_protocol":<Integer_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "snmp_user":[{
"security_level":<Integer_value>,
"auth_password":<String_value>,
"privacy_protocol":<Integer_value>,
"name":<String_value>,
"privacy_password":<String_value>,
"view_name":<String_value>,
"auth_protocol":<Integer_value>,
"security_level_str":<String_value>,
"privacy_protocol_str":<String_value>,
"auth_protocol_str":<String_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/snmp_user/name_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/snmp_user

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "snmp_user":[{
"security_level":<Integer_value>,
"auth_password":<String_value>,
"privacy_protocol":<Integer_value>,
"name":<String_value>,
"privacy_password":<String_value>,
"view_name":<String_value>,
"auth_protocol":<Integer_value>,
"security_level_str":<String_value>,
"privacy_protocol_str":<String_value>,
"auth_protocol_str":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/snmp_user/name_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "snmp_user":[{
"security_level":<Integer_value>,
"auth_password":<String_value>,
"privacy_protocol":<Integer_value>,
"name":<String_value>,
"privacy_password":<String_value>,
"view_name":<String_value>,
"auth_protocol":<Integer_value>,
"security_level_str":<String_value>,
"privacy_protocol_str":<String_value>,
"auth_protocol_str":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/snmp_user/name_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{snmp_user:{
<b>"security_level":<Integer_value></b>,
<b>"name":<String_value></b>,
"privacy_password":<String_value>,
"auth_protocol":<Integer_value>,
"view_name":<String_value>,
"auth_password":<String_value>,
"privacy_protocol":<Integer_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "snmp_user":[{
"security_level":<Integer_value>,
"auth_password":<String_value>,
"privacy_protocol":<Integer_value>,
"name":<String_value>,
"privacy_password":<String_value>,
"view_name":<String_value>,
"auth_protocol":<Integer_value>,
"security_level_str":<String_value>,
"privacy_protocol_str":<String_value>,
"auth_protocol_str":<String_value>}]}
```







