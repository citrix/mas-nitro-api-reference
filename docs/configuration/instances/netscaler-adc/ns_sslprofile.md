#ns_sslprofile



Configuration for NS SSL Profile resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>tls11</td><td>&lt;Boolean></td><td>Read-write</td><td>tls11.</td></tr><tr><td>ersa</td><td>&lt;Boolean></td><td>Read-write</td><td>ersa.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name.<br>Minimum length = 1<br>Maximum length = 100</td></tr><tr><td>dh</td><td>&lt;Boolean></td><td>Read-write</td><td>dh.</td></tr><tr><td>tls12</td><td>&lt;Boolean></td><td>Read-write</td><td>tls12.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NS IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>ssl2</td><td>&lt;Boolean></td><td>Read-write</td><td>ssl2.</td></tr><tr><td>ssl3</td><td>&lt;Boolean></td><td>Read-write</td><td>ssl3.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key.</td></tr><tr><td>tls10</td><td>&lt;Boolean></td><td>Read-write</td><td>tls1.</td></tr><tr><td>poll_time</td><td>&lt;Integer></td><td>Read-only</td><td>Last Polling Time.</td></tr><tr><td>display_name</td><td>&lt;String></td><td>Read-only</td><td>Display Name.</td></tr><tr><td>partition_name</td><td>&lt;String></td><td>Read-only</td><td>Partition Name.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_sslprofile

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_sslprofile":[{
"tls11":<Boolean_value>,
"ersa":<Boolean_value>,
"name":<String_value>,
"dh":<Boolean_value>,
"poll_time":<Integer_value>,
"tls12":<Boolean_value>,
"display_name":<String_value>,
"ns_ip_address":<String_value>,
"ssl2":<Boolean_value>,
"ssl3":<Boolean_value>,
"partition_name":<String_value>,
"id":<String_value>,
"tls10":<Boolean_value>}]}
```







