#radius_server



Configuration for Radius Server configuration resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>auth_timeout</td><td>&lt;Integer></td><td>Read-write</td><td>The maximum number of seconds the system will wait for a response from the Radius server.<br>Maximum value =</td></tr><tr><td>group_separator</td><td>&lt;String></td><td>Read-write</td><td>Group separator string that delimits group names within a RADIUS attribute for RADIUS group extraction.<br>Maximum length = 7</td></tr><tr><td>pass_encoding</td><td>&lt;String></td><td>Read-write</td><td>Enable password encoding in RADIUS packets send to the RADIUS server.</td></tr><tr><td>enable_nas_ip</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable NAS IP extraction.</td></tr><tr><td>radius_key</td><td>&lt;String></td><td>Read-write</td><td>Key of radius server.<br>Minimum length = 4<br>Maximum length = 32</td></tr><tr><td>default_authentication_group</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.<br>Maximum length = 64</td></tr><tr><td>ip_vendor_id</td><td>&lt;Integer></td><td>Read-write</td><td>The vendor ID of the attribute in the RADIUS response which denotes the intranet IP.<br>Maximum value =</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the radius servers.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address of radius server.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>ip_attribute_type</td><td>&lt;Integer></td><td>Read-write</td><td>The attribute type of the remote IP address attribute in a RADIUS response.<br>Maximum value =</td></tr><tr><td>attribute_type</td><td>&lt;Integer></td><td>Read-write</td><td>Attribute type for RADIUS group extraction.<br>Maximum value =</td></tr><tr><td>nas_id</td><td>&lt;String></td><td>Read-write</td><td>NAS ID.<br>Maximum length = 128</td></tr><tr><td>vendor_id</td><td>&lt;Integer></td><td>Read-write</td><td>Vendor ID for RADIUS group extraction.<br>Maximum value =</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of radius server.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Port number of radius server.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>groups_prefix</td><td>&lt;String></td><td>Read-write</td><td>Prefix string that precedes group names within a RADIUS attribute for RADIUS group extraction.<br>Maximum length = 31</td></tr><tr><td>pwd_vendor_id</td><td>&lt;Integer></td><td>Read-write</td><td>Vendor ID of the password in the RADIUS response. Used to extract the user password.<br>Maximum value =</td></tr><tr><td>pwd_attribute_type</td><td>&lt;Integer></td><td>Read-write</td><td>The attribute type of the password attribute in a RADIUS response..<br>Maximum value =</td></tr><tr><td>accounting</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable accounting in the radius server.</td></tr><tr><td>address_type</td><td>&lt;Integer></td><td>Read-only</td><td>Configuration Type. Values: 0: IPv4, 1: IPv6, -1: Hostname.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/radius_server?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{radius_server: {
<b>"radius_key":<String_value></b>,
<b>"ip_address":<String_value></b>,
<b>"name":<String_value></b>,
"auth_timeout":<Integer_value>,
"group_separator":<String_value>,
"pass_encoding":<String_value>,
"enable_nas_ip":<Boolean_value>,
"default_authentication_group":<String_value>,
"id":<String_value>,
"ip_attribute_type":<Integer_value>,
"pwd_vendor_id":<Integer_value>,
"groups_prefix":<String_value>,
"port":<Integer_value>,
"pwd_attribute_type":<Integer_value>,
"accounting":<Boolean_value>,
"ip_vendor_id":<Integer_value>,
"attribute_type":<Integer_value>,
"nas_id":<String_value>,
"vendor_id":<Integer_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "radius_server":[{
"auth_timeout":<Integer_value>,
"group_separator":<String_value>,
"pass_encoding":<String_value>,
"enable_nas_ip":<Boolean_value>,
"radius_key":<String_value>,
"default_authentication_group":<String_value>,
"ip_vendor_id":<Integer_value>,
"id":<String_value>,
"ip_address":<String_value>,
"ip_attribute_type":<Integer_value>,
"attribute_type":<Integer_value>,
"nas_id":<String_value>,
"vendor_id":<Integer_value>,
"name":<String_value>,
"port":<Integer_value>,
"groups_prefix":<String_value>,
"pwd_vendor_id":<Integer_value>,
"pwd_attribute_type":<Integer_value>,
"accounting":<Boolean_value>,
"address_type":<Integer_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/radius_server/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/radius_server

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "radius_server":[{
"auth_timeout":<Integer_value>,
"group_separator":<String_value>,
"pass_encoding":<String_value>,
"enable_nas_ip":<Boolean_value>,
"radius_key":<String_value>,
"default_authentication_group":<String_value>,
"ip_vendor_id":<Integer_value>,
"id":<String_value>,
"ip_address":<String_value>,
"ip_attribute_type":<Integer_value>,
"attribute_type":<Integer_value>,
"nas_id":<String_value>,
"vendor_id":<Integer_value>,
"name":<String_value>,
"port":<Integer_value>,
"groups_prefix":<String_value>,
"pwd_vendor_id":<Integer_value>,
"pwd_attribute_type":<Integer_value>,
"accounting":<Boolean_value>,
"address_type":<Integer_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/radius_server/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "radius_server":[{
"auth_timeout":<Integer_value>,
"group_separator":<String_value>,
"pass_encoding":<String_value>,
"enable_nas_ip":<Boolean_value>,
"radius_key":<String_value>,
"default_authentication_group":<String_value>,
"ip_vendor_id":<Integer_value>,
"id":<String_value>,
"ip_address":<String_value>,
"ip_attribute_type":<Integer_value>,
"attribute_type":<Integer_value>,
"nas_id":<String_value>,
"vendor_id":<Integer_value>,
"name":<String_value>,
"port":<Integer_value>,
"groups_prefix":<String_value>,
"pwd_vendor_id":<Integer_value>,
"pwd_attribute_type":<Integer_value>,
"accounting":<Boolean_value>,
"address_type":<Integer_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/radius_server/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{radius_server:{
<b>"id":<String_value></b>,
<b>"ip_address":<String_value></b>,
<b>"name":<String_value></b>,
"auth_timeout":<Integer_value>,
"group_separator":<String_value>,
"pass_encoding":<String_value>,
"enable_nas_ip":<Boolean_value>,
"default_authentication_group":<String_value>,
"ip_attribute_type":<Integer_value>,
"pwd_vendor_id":<Integer_value>,
"groups_prefix":<String_value>,
"port":<Integer_value>,
"pwd_attribute_type":<Integer_value>,
"accounting":<Boolean_value>,
"radius_key":<String_value>,
"ip_vendor_id":<Integer_value>,
"attribute_type":<Integer_value>,
"nas_id":<String_value>,
"vendor_id":<Integer_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "radius_server":[{
"auth_timeout":<Integer_value>,
"group_separator":<String_value>,
"pass_encoding":<String_value>,
"enable_nas_ip":<Boolean_value>,
"radius_key":<String_value>,
"default_authentication_group":<String_value>,
"ip_vendor_id":<Integer_value>,
"id":<String_value>,
"ip_address":<String_value>,
"ip_attribute_type":<Integer_value>,
"attribute_type":<Integer_value>,
"nas_id":<String_value>,
"vendor_id":<Integer_value>,
"name":<String_value>,
"port":<Integer_value>,
"groups_prefix":<String_value>,
"pwd_vendor_id":<Integer_value>,
"pwd_attribute_type":<Integer_value>,
"accounting":<Boolean_value>,
"address_type":<Integer_value>}]}
```







