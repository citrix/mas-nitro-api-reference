#tacacs_server



Configuration for TACACS Server configuration resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>tacacs_key</td><td>&lt;String></td><td>Read-write</td><td>Key shared between the TACACS+ server and clients.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>auth_timeout</td><td>&lt;Integer></td><td>Read-write</td><td>The maximum number of seconds the system will wait for a response from the TACACS server.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of TACACS server.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>port number of TACACS server.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the TACACS servers.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address of TACACS server.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>accounting</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable accounting in the tacacs server.</td></tr><tr><td>address_type</td><td>&lt;Integer></td><td>Read-only</td><td>Configuration Type. Values: 0: IPv4, 1: IPv6.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tacacs_server?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{tacacs_server: {
<b>"tacacs_key":<String_value></b>,
<b>"name":<String_value></b>,
<b>"ip_address":<String_value></b>,
"auth_timeout":<Integer_value>,
"id":<String_value>,
"port":<Integer_value>,
"accounting":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tacacs_server":[{
"tacacs_key":<String_value>,
"auth_timeout":<Integer_value>,
"name":<String_value>,
"port":<Integer_value>,
"id":<String_value>,
"ip_address":<String_value>,
"accounting":<Boolean_value>,
"address_type":<Integer_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tacacs_server/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tacacs_server

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tacacs_server":[{
"tacacs_key":<String_value>,
"auth_timeout":<Integer_value>,
"name":<String_value>,
"port":<Integer_value>,
"id":<String_value>,
"ip_address":<String_value>,
"accounting":<Boolean_value>,
"address_type":<Integer_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tacacs_server/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tacacs_server":[{
"tacacs_key":<String_value>,
"auth_timeout":<Integer_value>,
"name":<String_value>,
"port":<Integer_value>,
"id":<String_value>,
"ip_address":<String_value>,
"accounting":<Boolean_value>,
"address_type":<Integer_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tacacs_server/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{tacacs_server:{
<b>"name":<String_value></b>,
<b>"id":<String_value></b>,
<b>"ip_address":<String_value></b>,
"auth_timeout":<Integer_value>,
"tacacs_key":<String_value>,
"port":<Integer_value>,
"accounting":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tacacs_server":[{
"tacacs_key":<String_value>,
"auth_timeout":<Integer_value>,
"name":<String_value>,
"port":<Integer_value>,
"id":<String_value>,
"ip_address":<String_value>,
"accounting":<Boolean_value>,
"address_type":<Integer_value>}]}
```







