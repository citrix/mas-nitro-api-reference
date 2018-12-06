#ns_appflow_param_config



Configuration for Appflow param configuration on NetScaler resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>observationDomainName</td><td>&lt;String></td><td>Read-write</td><td>NetScaler observationDomainName.<br>Minimum length = 1<br>Maximum length = 256</td></tr><tr><td>is_clip</td><td>&lt;Boolean></td><td>Read-write</td><td>Is Clip.</td></tr><tr><td>template_interval</td><td>&lt;Integer></td><td>Read-write</td><td>Template refresh interval.</td></tr><tr><td>httpxforwardedfor</td><td>&lt;String></td><td>Read-write</td><td>.<br>Minimum length = 1<br>Maximum length = 10</td></tr><tr><td>observationDomainID</td><td>&lt;Double></td><td>Read-write</td><td>observationDomainID.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NetScaler IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [MODIFY](#m)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_appflow_param_config

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_appflow_param_config":[{
"observationDomainName":<String_value>,
"is_clip":<Boolean_value>,
"template_interval":<Integer_value>,
"httpxforwardedfor":<String_value>,
"observationDomainID":<Double_value>,
"ns_ip_address":<String_value>}]}
```







###modify







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_appflow_param_config/

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_appflow_param_config:{
"observationDomainName":<String_value>,
"ns_ip_address":<String_value>,
"is_clip":<Boolean_value>,
"httpxforwardedfor":<String_value>,
"template_interval":<Integer_value>,
"observationDomainID":<Double_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_appflow_param_config":[{
"observationDomainName":<String_value>,
"is_clip":<Boolean_value>,
"template_interval":<Integer_value>,
"httpxforwardedfor":<String_value>,
"observationDomainID":<Double_value>,
"ns_ip_address":<String_value>}]}
```







