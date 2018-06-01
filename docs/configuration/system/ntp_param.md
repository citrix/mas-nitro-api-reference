#ntp_param

Configuration for NTP Parameters resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>trusted_key_list</td><td>&lt;Integer[]></td><td>Read-write</td><td>List of Trusted Key Identifiers for Symmetric Key Cryptography.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>automax_logsec</td><td>&lt;Integer></td><td>Read-write</td><td>Automax Interval (as power of 2 in seconds).</td></tr><tr><td>revoke_logsec</td><td>&lt;Integer></td><td>Read-write</td><td>Revoke Interval (as power of 2 in seconds).</td></tr><tr><td>authentication</td><td>&lt;Boolean></td><td>Read-write</td><td>Authentication Enabled.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [UPDATE](#u)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ntp_param
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ntp_param":[{"trusted_key_list":<Integer_value>,"automax_logsec":<Integer_value>,"revoke_logsec":<Integer_value>,"authentication":<Boolean_value>}]}```



###update



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ntp_param/
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{ntp_param:{"trusted_key_list":<Integer_value[]>,"automax_logsec":<Integer_value>,"revoke_logsec":<Integer_value>,"authentication":<Boolean_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ntp_param":[{"trusted_key_list":<Integer_value>,"automax_logsec":<Integer_value>,"revoke_logsec":<Integer_value>,"authentication":<Boolean_value>}]}```



