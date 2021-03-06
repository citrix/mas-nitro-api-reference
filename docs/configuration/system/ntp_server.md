#ntp_server



Configuration for NTP Server resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>preferred_server</td><td>&lt;Boolean></td><td>Read-write</td><td>NTP Server Preferred.</td></tr><tr><td>maxpoll</td><td>&lt;Integer></td><td>Read-write</td><td>Maximum Poll Interval.<br>Maximum value =</td></tr><tr><td>minpoll</td><td>&lt;Integer></td><td>Read-write</td><td>Minimum Poll Interval.<br>Maximum value =</td></tr><tr><td>autokey</td><td>&lt;Boolean></td><td>Read-write</td><td>Autokey Public Key Authentication.</td></tr><tr><td>key_id</td><td>&lt;Integer></td><td>Read-write</td><td>Key Identifier for Symmetric Key Authentication.<br>Maximum value =</td></tr><tr><td>server</td><td>&lt;String></td><td>Read-write</td><td>NTP Time Server Address.</td></tr><tr><td>client</td><td>&lt;String></td><td>Read-write</td><td>Sender of request, whether from Setup Wizard or direct NTP configuration.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ntp_server?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ntp_server: {
<b>"server":<String_value></b>,
"client":<String_value>,
"minpoll":<Integer_value>,
"maxpoll":<Integer_value>,
"preferred_server":<Boolean_value>,
"autokey":<Boolean_value>,
"key_id":<Integer_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ntp_server":[{
"preferred_server":<Boolean_value>,
"maxpoll":<Integer_value>,
"minpoll":<Integer_value>,
"autokey":<Boolean_value>,
"key_id":<Integer_value>,
"server":<String_value>,
"client":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ntp_server/server_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ntp_server

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ntp_server":[{
"preferred_server":<Boolean_value>,
"maxpoll":<Integer_value>,
"minpoll":<Integer_value>,
"autokey":<Boolean_value>,
"key_id":<Integer_value>,
"server":<String_value>,
"client":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ntp_server/server_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ntp_server":[{
"preferred_server":<Boolean_value>,
"maxpoll":<Integer_value>,
"minpoll":<Integer_value>,
"autokey":<Boolean_value>,
"key_id":<Integer_value>,
"server":<String_value>,
"client":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ntp_server/server_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ntp_server:{
"client":<String_value>,
"minpoll":<Integer_value>,
"maxpoll":<Integer_value>,
"preferred_server":<Boolean_value>,
"autokey":<Boolean_value>,
"key_id":<Integer_value>,
"server":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ntp_server":[{
"preferred_server":<Boolean_value>,
"maxpoll":<Integer_value>,
"minpoll":<Integer_value>,
"autokey":<Boolean_value>,
"key_id":<Integer_value>,
"server":<String_value>,
"client":<String_value>}]}
```







