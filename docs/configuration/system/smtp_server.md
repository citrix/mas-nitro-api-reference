#smtp_server



Configuration for SMTP server properties resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sender_mail_id</td><td>&lt;String></td><td>Read-write</td><td>Email Address from which email is to be sent.</td></tr><tr><td>is_auth</td><td>&lt;Boolean></td><td>Read-write</td><td>Is authentication enabled for this smtp server.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>SMTP Server port address..<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>Username for the smtp server.<br>Maximum length = 128</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Password for the smtp server.<br>Maximum length = 128</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the smtp server.</td></tr><tr><td>is_ssl</td><td>&lt;Boolean></td><td>Read-write</td><td>Is this smtp server is SSL support configured..</td></tr><tr><td>server_name</td><td>&lt;String></td><td>Read-write</td><td>SMTP server name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant Id of the Config Jobs.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/smtp_server?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{smtp_server: {
<b>"server_name":<String_value></b>,
"sender_mail_id":<String_value>,
"password":<String_value>,
"id":<String_value>,
"port":<Integer_value>,
"username":<String_value>,
"is_ssl":<Boolean_value>,
"is_auth":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "smtp_server":[{
"sender_mail_id":<String_value>,
"is_auth":<Boolean_value>,
"port":<Integer_value>,
"username":<String_value>,
"password":<String_value>,
"tenant_id":<String_value>,
"id":<String_value>,
"is_ssl":<Boolean_value>,
"server_name":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/smtp_server/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/smtp_server

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "smtp_server":[{
"sender_mail_id":<String_value>,
"is_auth":<Boolean_value>,
"port":<Integer_value>,
"username":<String_value>,
"password":<String_value>,
"tenant_id":<String_value>,
"id":<String_value>,
"is_ssl":<Boolean_value>,
"server_name":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/smtp_server/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "smtp_server":[{
"sender_mail_id":<String_value>,
"is_auth":<Boolean_value>,
"port":<Integer_value>,
"username":<String_value>,
"password":<String_value>,
"tenant_id":<String_value>,
"id":<String_value>,
"is_ssl":<Boolean_value>,
"server_name":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/smtp_server/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{smtp_server:{
<b>"id":<String_value></b>,
"sender_mail_id":<String_value>,
"password":<String_value>,
"port":<Integer_value>,
"username":<String_value>,
"server_name":<String_value>,
"is_ssl":<Boolean_value>,
"is_auth":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "smtp_server":[{
"sender_mail_id":<String_value>,
"is_auth":<Boolean_value>,
"port":<Integer_value>,
"username":<String_value>,
"password":<String_value>,
"tenant_id":<String_value>,
"id":<String_value>,
"is_ssl":<Boolean_value>,
"server_name":<String_value>}]}
```







