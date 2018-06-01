#af_geoclient

Configuration for af geoclient API resource resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count of geo location record..</td></tr><tr><td>country_code</td><td>&lt;String></td><td>Read-write</td><td>country_code.</td></tr><tr><td>network_latency_client_side</td><td>&lt;Double></td><td>Read-write</td><td>Network latency client side in selected geo client..</td></tr><tr><td>city</td><td>&lt;String></td><td>Read-write</td><td>city.</td></tr><tr><td>country</td><td>&lt;String></td><td>Read-write</td><td>country.</td></tr><tr><td>total_user</td><td>&lt;Double></td><td>Read-write</td><td>Count of user i.e. various client IP addresses in the selected region..</td></tr><tr><td>region_code</td><td>&lt;String></td><td>Read-write</td><td>region_code.</td></tr><tr><td>region</td><td>&lt;String></td><td>Read-write</td><td>region.</td></tr><tr><td>total_bytes</td><td>&lt;Double></td><td>Read-write</td><td>Total bytes accounted by this in selected geo client..</td></tr><tr><td>bandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Avg Bandwidth..</td></tr><tr><td>network_latency_server_side</td><td>&lt;Double></td><td>Read-write</td><td>Network latency server side in selected geo client..</td></tr><tr><td>client_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Client IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>application_response_time</td><td>&lt;Double></td><td>Read-write</td><td>Application response time..</td></tr><tr><td>total_requests</td><td>&lt;Double></td><td>Read-write</td><td>Count of URL request in selected geo client..</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/af_geoclient
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "af_geoclient":[{"__count":<Double_value>,"country_code":<String_value>,"network_latency_client_side":<Double_value>,"city":<String_value>,"app_unit_name":<String_value>,"country":<String_value>,"total_user":<Double_value>,"region_code":<String_value>,"region":<String_value>,"total_bytes":<Double_value>,"device_ip_address":<String_value>,"domain_name":<String_value>,"bandwidth":<Double_value>,"network_latency_server_side":<Double_value>,"client_ip_address":<String_value>,"application_response_time":<Double_value>,"total_requests":<Double_value>}]}```



