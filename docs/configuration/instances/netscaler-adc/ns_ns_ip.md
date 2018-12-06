#ns_ns_ip



Configuration for NS IP on NetScaler resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>save_config</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if save config is required.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of IP Address, Possible Values: SNIP.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>netmask.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>NS ipaddress that needs to be created.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NetScaler IP Address where NSIP needs to be created.<br>Minimum length = 1<br>Maximum length = 64</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ns_ip?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_ns_ip: {
<b>"type":<String_value></b>,
<b>"netmask":<String_value></b>,
<b>"ipaddress":<String_value></b>,
<b>"ns_ip_address":<String_value></b>,
"save_config":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_ns_ip":[{
"save_config":<Boolean_value>,
"type":<String_value>,
"netmask":<String_value>,
"ipaddress":<String_value>,
"ns_ip_address":<String_value>}]}
```







