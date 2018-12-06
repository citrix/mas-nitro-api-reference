#sms_server



Configuration for SMS server properties resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>optional1_val</td><td>&lt;String></td><td>Read-write</td><td>Optional1 Val for the sms server.<br>Maximum length = 128</td></tr><tr><td>to_seperater</td><td>&lt;String></td><td>Read-write</td><td>To list seperater for the sms server.<br>Maximum length = 128</td></tr><tr><td>username_val</td><td>&lt;String></td><td>Read-write</td><td>Username val for the sms server.<br>Maximum length = 128</td></tr><tr><td>to_key</td><td>&lt;String></td><td>Read-write</td><td>To key for the sms server.<br>Maximum length = 128</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the sms server.</td></tr><tr><td>is_ssl</td><td>&lt;Boolean></td><td>Read-write</td><td>Is SSL support configured..</td></tr><tr><td>base_url</td><td>&lt;String></td><td>Read-write</td><td>Base URL for the sms server, without payload.<br>Maximum length = 2000</td></tr><tr><td>username_key</td><td>&lt;String></td><td>Read-write</td><td>Username key for the sms server.<br>Maximum length = 128</td></tr><tr><td>optional1_key</td><td>&lt;String></td><td>Read-write</td><td>Optional1 key for the sms server.<br>Maximum length = 128</td></tr><tr><td>message_key</td><td>&lt;String></td><td>Read-write</td><td>Message key for the sms server.<br>Maximum length = 128</td></tr><tr><td>message_word_sperater</td><td>&lt;String></td><td>Read-write</td><td>Message Word Seperater for the sms server.<br>Maximum length = 128</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>HTTP type supported for the sms server.<br>Maximum length = 128</td></tr><tr><td>password_val</td><td>&lt;String></td><td>Read-write</td><td>Password Val for the sms server.<br>Maximum length = 128</td></tr><tr><td>password_key</td><td>&lt;String></td><td>Read-write</td><td>Password key for the sms server.<br>Maximum length = 128</td></tr><tr><td>server_name</td><td>&lt;String></td><td>Read-write</td><td>SMS server name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>optional2_val1</td><td>&lt;String></td><td>Read-only</td><td>Optional2 Val for the sms server.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant Id of the Config Jobs.</td></tr><tr><td>optional3_key</td><td>&lt;String></td><td>Read-only</td><td>Optional3 key for the sms server.</td></tr><tr><td>optional3_val</td><td>&lt;String></td><td>Read-only</td><td>Optional3 Val for the sms server.</td></tr><tr><td>optional2_key</td><td>&lt;String></td><td>Read-only</td><td>Optional2 key for the sms server.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sms_server?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{sms_server: {
<b>"username_val":<String_value></b>,
<b>"to_key":<String_value></b>,
<b>"base_url":<String_value></b>,
<b>"username_key":<String_value></b>,
<b>"message_key":<String_value></b>,
<b>"type":<String_value></b>,
<b>"password_val":<String_value></b>,
<b>"password_key":<String_value></b>,
<b>"server_name":<String_value></b>,
"optional1_val":<String_value>,
"to_seperater":<String_value>,
"id":<String_value>,
"message_word_sperater":<String_value>,
"is_ssl":<Boolean_value>,
"optional1_key":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "sms_server":[{
"optional2_val1":<String_value>,
"optional1_val":<String_value>,
"to_seperater":<String_value>,
"username_val":<String_value>,
"to_key":<String_value>,
"tenant_id":<String_value>,
"optional3_key":<String_value>,
"id":<String_value>,
"is_ssl":<Boolean_value>,
"optional3_val":<String_value>,
"base_url":<String_value>,
"username_key":<String_value>,
"optional2_key":<String_value>,
"optional1_key":<String_value>,
"message_key":<String_value>,
"message_word_sperater":<String_value>,
"type":<String_value>,
"password_val":<String_value>,
"password_key":<String_value>,
"server_name":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sms_server/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sms_server

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "sms_server":[{
"optional2_val1":<String_value>,
"optional1_val":<String_value>,
"to_seperater":<String_value>,
"username_val":<String_value>,
"to_key":<String_value>,
"tenant_id":<String_value>,
"optional3_key":<String_value>,
"id":<String_value>,
"is_ssl":<Boolean_value>,
"optional3_val":<String_value>,
"base_url":<String_value>,
"username_key":<String_value>,
"optional2_key":<String_value>,
"optional1_key":<String_value>,
"message_key":<String_value>,
"message_word_sperater":<String_value>,
"type":<String_value>,
"password_val":<String_value>,
"password_key":<String_value>,
"server_name":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sms_server/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "sms_server":[{
"optional2_val1":<String_value>,
"optional1_val":<String_value>,
"to_seperater":<String_value>,
"username_val":<String_value>,
"to_key":<String_value>,
"tenant_id":<String_value>,
"optional3_key":<String_value>,
"id":<String_value>,
"is_ssl":<Boolean_value>,
"optional3_val":<String_value>,
"base_url":<String_value>,
"username_key":<String_value>,
"optional2_key":<String_value>,
"optional1_key":<String_value>,
"message_key":<String_value>,
"message_word_sperater":<String_value>,
"type":<String_value>,
"password_val":<String_value>,
"password_key":<String_value>,
"server_name":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sms_server/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{sms_server:{
<b>"id":<String_value></b>,
"optional1_val":<String_value>,
"to_seperater":<String_value>,
"username_val":<String_value>,
"message_word_sperater":<String_value>,
"type":<String_value>,
"password_val":<String_value>,
"server_name":<String_value>,
"to_key":<String_value>,
"is_ssl":<Boolean_value>,
"base_url":<String_value>,
"username_key":<String_value>,
"message_key":<String_value>,
"optional1_key":<String_value>,
"password_key":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "sms_server":[{
"optional2_val1":<String_value>,
"optional1_val":<String_value>,
"to_seperater":<String_value>,
"username_val":<String_value>,
"to_key":<String_value>,
"tenant_id":<String_value>,
"optional3_key":<String_value>,
"id":<String_value>,
"is_ssl":<Boolean_value>,
"optional3_val":<String_value>,
"base_url":<String_value>,
"username_key":<String_value>,
"optional2_key":<String_value>,
"optional1_key":<String_value>,
"message_key":<String_value>,
"message_word_sperater":<String_value>,
"type":<String_value>,
"password_val":<String_value>,
"password_key":<String_value>,
"server_name":<String_value>}]}
```







