#mps_network_config



Configuration for MPS Network Configuration resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>alternate_dns_v6</td><td>&lt;String></td><td>Read-write</td><td>Alternate DNS Server IPv6 Address.</td></tr><tr><td>dns</td><td>&lt;String></td><td>Read-write</td><td>DNS Server.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>gateway</td><td>&lt;String></td><td>Read-write</td><td>Gateway .<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>alternate_dns</td><td>&lt;String></td><td>Read-write</td><td>Alternate DNS Server.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>config_type</td><td>&lt;Integer></td><td>Read-write</td><td>Configuration Type. Values: 0: IPv4, 1: IPv6, 2: Both.<br>Maximum value =</td></tr><tr><td>dns_v6</td><td>&lt;String></td><td>Read-write</td><td>DNS Server IPv6 Address.</td></tr><tr><td>gateway_ipv6</td><td>&lt;String></td><td>Read-write</td><td>Gateway IPv6 Address.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>Netmask.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>ipv6_address</td><td>&lt;String></td><td>Read-write</td><td>Management Service IPv6 Address.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps_network_config

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mps_network_config":[{
"alternate_dns_v6":<String_value>,
"dns":<String_value>,
"gateway":<String_value>,
"alternate_dns":<String_value>,
"config_type":<Integer_value>,
"dns_v6":<String_value>,
"gateway_ipv6":<String_value>,
"ip_address":<String_value>,
"netmask":<String_value>,
"ipv6_address":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps_network_config/

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{mps_network_config:{
<b>"config_type":<Integer_value></b>,
<b>"netmask":<String_value></b>,
"dns":<String_value>,
"gateway_ipv6":<String_value>,
"ipv6_address":<String_value>,
"gateway":<String_value>,
"alternate_dns":<String_value>,
"ip_address":<String_value>,
"alternate_dns_v6":<String_value>,
"dns_v6":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mps_network_config":[{
"alternate_dns_v6":<String_value>,
"dns":<String_value>,
"gateway":<String_value>,
"alternate_dns":<String_value>,
"config_type":<Integer_value>,
"dns_v6":<String_value>,
"gateway_ipv6":<String_value>,
"ip_address":<String_value>,
"netmask":<String_value>,
"ipv6_address":<String_value>}]}
```







