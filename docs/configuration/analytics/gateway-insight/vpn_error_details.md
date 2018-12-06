#vpn_error_details



Configuration for Af report for VPN Error details resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>error_count</td><td>&lt;Double></td><td>Read-write</td><td>Error Code.</td></tr><tr><td>policy_name</td><td>&lt;String></td><td>Read-write</td><td>EPA Policy Name.<br>Maximum length = 1024</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>cs_vserver_name</td><td>&lt;String></td><td>Read-write</td><td>CS Server Name..<br>Maximum length = 128</td></tr><tr><td>error_description</td><td>&lt;String></td><td>Read-write</td><td>STA Validation Failure Counts..<br>Maximum length = 1024</td></tr><tr><td>sso_method_type</td><td>&lt;String></td><td>Read-write</td><td>SSO Method Type.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>flag</td><td>&lt;Double></td><td>Read-write</td><td>Flag.</td></tr><tr><td>ad_server_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Active Directory Server IP Address.<br>Maximum length = 32</td></tr><tr><td>ica_device_ip_address</td><td>&lt;String></td><td>Read-write</td><td>ICA Device IP Address..<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>next_factor_policy_label</td><td>&lt;String></td><td>Read-write</td><td>next factor policy label.<br>Maximum length = 255</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is not dicided yet.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>vpn_server_name</td><td>&lt;String></td><td>Read-write</td><td>VPN Server Name..<br>Maximum length = 128</td></tr><tr><td>authentication_state</td><td>&lt;String></td><td>Read-write</td><td>Authentication State.<br>Maximum length = 128</td></tr><tr><td>auth_type</td><td>&lt;String></td><td>Read-write</td><td>Authentication Type.<br>Maximum length = 128</td></tr><tr><td>server_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Server IP Address..<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>sta_ip</td><td>&lt;String></td><td>Read-write</td><td>STA Server IP..<br>Maximum length = 128</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>User Name.<br>Maximum length = 128</td></tr><tr><td>error_code</td><td>&lt;Double></td><td>Read-write</td><td>Error Code.</td></tr><tr><td>error_time</td><td>&lt;Double></td><td>Read-write</td><td>Flag.</td></tr><tr><td>vpn_fqdn</td><td>&lt;String></td><td>Read-write</td><td>VPN FQDN.<br>Maximum length = 128</td></tr><tr><td>resource_name</td><td>&lt;String></td><td>Read-write</td><td>Resource Name.<br>Maximum length = 128</td></tr><tr><td>req_url</td><td>&lt;String></td><td>Read-write</td><td>req_url.<br>Maximum length = 255</td></tr><tr><td>current_factor_policy_label</td><td>&lt;String></td><td>Read-write</td><td>current factor policy label.<br>Maximum length = 255</td></tr><tr><td>epa_expression</td><td>&lt;String></td><td>Read-write</td><td>EPA Expression.<br>Maximum length = 255</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/vpn_error_details

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "vpn_error_details":[{
"error_count":<Double_value>,
"policy_name":<String_value>,
"__count":<Double_value>,
"cs_vserver_name":<String_value>,
"error_description":<String_value>,
"sso_method_type":<String_value>,
"flag":<Double_value>,
"ad_server_ip_address":<String_value>,
"ica_device_ip_address":<String_value>,
"next_factor_policy_label":<String_value>,
"id":<String_value>,
"vpn_server_name":<String_value>,
"authentication_state":<String_value>,
"auth_type":<String_value>,
"server_ip_address":<String_value>,
"epa_method_type":<String_value>,
"sta_ip":<String_value>,
"username":<String_value>,
"error_code":<Double_value>,
"error_time":<Double_value>,
"client_ip_address":<String_value>,
"vpn_fqdn":<String_value>,
"resource_name":<String_value>,
"req_url":<String_value>,
"current_factor_policy_label":<String_value>,
"epa_expression":<String_value>}]}
```







