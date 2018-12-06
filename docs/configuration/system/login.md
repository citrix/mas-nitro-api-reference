#login



Configuration for Login/Logout resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ID</td><td>&lt;String></td><td>Read-write</td><td>ID of the User that wants to login in cloud.<br>Maximum length = 128</td></tr><tr><td>permission</td><td>&lt;String></td><td>Read-write</td><td>Actions that this user is authorized to perform.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>session_timeout</td><td>&lt;Integer></td><td>Read-write</td><td>Session Timeout in seconds, if no activity is performed for specified time then session will be expired.</td></tr><tr><td>auth_with_remote_pubkey</td><td>&lt;Integer></td><td>Read-write</td><td>Login request to specify if SSH authentication took place with remote public keys for this user, 1 for remotely managed pubkey else 0.</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>User Name that wants to login.<br>Maximum length = 128</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Password.<br>Maximum length = 128</td></tr><tr><td>challenge</td><td>&lt;String></td><td>Read-write</td><td>Challenge request for authentication.</td></tr><tr><td>challenge_response</td><td>&lt;String></td><td>Read-write</td><td>Challenge response for authentication.</td></tr><tr><td>client_ip</td><td>&lt;String></td><td>Read-write</td><td>Login client IP.</td></tr><tr><td>client_port</td><td>&lt;Integer></td><td>Read-write</td><td>Login Client port.<br>Maximum value =</td></tr><tr><td>sessionid</td><td>&lt;String></td><td>Read-write</td><td>Session ID would only be set if login was performed successfully.</td></tr><tr><td>token</td><td>&lt;String></td><td>Read-write</td><td>Random token to identify session during logout.</td></tr><tr><td>Secret</td><td>&lt;String></td><td>Read-write</td><td>Secret.<br>Maximum length = 128</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/login?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{login: {
<b>"client_port":<Integer_value></b>,
"ID":<String_value>,
"session_timeout":<Integer_value>,
"auth_with_remote_pubkey":<Integer_value>,
"password":<String_value>,
"challenge_response":<String_value>,
"challenge":<String_value>,
"token":<String_value>,
"permission":<String_value>,
"username":<String_value>,
"client_ip":<String_value>,
"sessionid":<String_value>,
"Secret":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "login":[{
"ID":<String_value>,
"tenant_name":<String_value>,
"permission":<String_value>,
"session_timeout":<Integer_value>,
"challenge_token":<String_value>,
"auth_with_remote_pubkey":<Integer_value>,
"username":<String_value>,
"login_type":<String_value>,
"password":<String_value>,
"challenge":<String_value>,
"challenge_response":<String_value>,
"client_ip":<String_value>,
"client_port":<Integer_value>,
"cert_verified":<Boolean_value>,
"sessionid":<String_value>,
"token":<String_value>,
"Secret":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/login/

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







