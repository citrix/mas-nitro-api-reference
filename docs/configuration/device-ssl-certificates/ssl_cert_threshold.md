#ssl_cert_threshold



Configuration for SSL certificate Threshold configuration resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>name.</td></tr><tr><td>region</td><td>&lt;String></td><td>Read-write</td><td>Region Code.<br>Maximum length = 256</td></tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>Rule.</td></tr><tr><td>stylebook_flag</td><td>&lt;Boolean></td><td>Read-write</td><td>Stylebook threshold configuration true or false.</td></tr><tr><td>country</td><td>&lt;String></td><td>Read-write</td><td>Country Code.<br>Maximum length = 256</td></tr><tr><td>sms_profile</td><td>&lt;String></td><td>Read-write</td><td>SMS Profile.</td></tr><tr><td>feature</td><td>&lt;String></td><td>Read-write</td><td>feature.</td></tr><tr><td>ctnsappname</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr><tr><td>hide_default_certs</td><td>&lt;Boolean></td><td>Read-write</td><td>Set the value to true if default certs in device need not be managed.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the Thresholds configuration .<br>Maximum length = 256</td></tr><tr><td>resource_type</td><td>&lt;String></td><td>Read-write</td><td>Resource Type.</td></tr><tr><td>mail_profile</td><td>&lt;String></td><td>Read-write</td><td>Mail Profile.</td></tr><tr><td>is_enabled</td><td>&lt;String></td><td>Read-write</td><td>true or false.</td></tr><tr><td>duration</td><td>&lt;String></td><td>Read-write</td><td>duration of metric to be checked against threshold.</td></tr><tr><td>days_to_expiry</td><td>&lt;Integer></td><td>Read-write</td><td>Days remaining for expiry.<br>Maximum value =</td></tr><tr><td>city</td><td>&lt;String></td><td>Read-write</td><td>City.<br>Maximum length = 256</td></tr><tr><td>tenant_name</td><td>&lt;String></td><td>Read-write</td><td>Tenant Name.</td></tr><tr><td>group_name</td><td>&lt;String></td><td>Read-write</td><td>Group Name.</td></tr><tr><td>reference_key</td><td>&lt;String></td><td>Read-write</td><td>Reference Key.</td></tr><tr><td>exporter_id</td><td>&lt;Double></td><td>Read-write</td><td>Exporter Id.</td></tr><tr><td>approved_ssl_protocol_list</td><td>&lt;String[]></td><td>Read-write</td><td>SSL Protocols List.</td></tr><tr><td>approved_key_strength_list</td><td>&lt;String[]></td><td>Read-write</td><td>Key Strength List.</td></tr><tr><td>approved_issuers_list</td><td>&lt;String[]></td><td>Read-write</td><td>Issuers List.</td></tr><tr><td>approved_signature_algo_list</td><td>&lt;String[]></td><td>Read-write</td><td>Signature Algorithm List.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ssl_cert_threshold

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ssl_cert_threshold":[{
"name":<String_value>,
"region":<String_value>,
"rule":<String_value>,
"stylebook_flag":<Boolean_value>,
"country":<String_value>,
"issuers_list":<String_value>,
"sms_profile":<String_value>,
"signature_algo_list":<String_value>,
"feature":<String_value>,
"ctnsappname":<String_value>,
"hide_default_certs":<Boolean_value>,
"id":<String_value>,
"resource_type":<String_value>,
"mail_profile":<String_value>,
"is_enabled":<String_value>,
"duration":<String_value>,
"days_to_expiry":<Integer_value>,
"city":<String_value>,
"key_strength_list":<String_value>,
"ssl_protocol_list":<String_value>,
"tenant_name":<String_value>,
"group_name":<String_value>,
"reference_key":<String_value>,
"exporter_id":<Double_value>,
"approved_ssl_protocol_list":<String_value>,
"approved_key_strength_list":<String_value>,
"approved_issuers_list":<String_value>,
"approved_signature_algo_list":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ssl_cert_threshold/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ssl_cert_threshold":[{
"name":<String_value>,
"region":<String_value>,
"rule":<String_value>,
"stylebook_flag":<Boolean_value>,
"country":<String_value>,
"issuers_list":<String_value>,
"sms_profile":<String_value>,
"signature_algo_list":<String_value>,
"feature":<String_value>,
"ctnsappname":<String_value>,
"hide_default_certs":<Boolean_value>,
"id":<String_value>,
"resource_type":<String_value>,
"mail_profile":<String_value>,
"is_enabled":<String_value>,
"duration":<String_value>,
"days_to_expiry":<Integer_value>,
"city":<String_value>,
"key_strength_list":<String_value>,
"ssl_protocol_list":<String_value>,
"tenant_name":<String_value>,
"group_name":<String_value>,
"reference_key":<String_value>,
"exporter_id":<Double_value>,
"approved_ssl_protocol_list":<String_value>,
"approved_key_strength_list":<String_value>,
"approved_issuers_list":<String_value>,
"approved_signature_algo_list":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ssl_cert_threshold/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ssl_cert_threshold:{
<b>"id":<String_value></b>,
"sms_profile":<String_value>,
"feature":<String_value>,
"hide_default_certs":<Boolean_value>,
"ctnsappname":<String_value>,
"mail_profile":<String_value>,
"resource_type":<String_value>,
"is_enabled":<String_value>,
"region":<String_value>,
"name":<String_value>,
"days_to_expiry":<Integer_value>,
"duration":<String_value>,
"approved_issuers_list":<String_value[]>,
"stylebook_flag":<Boolean_value>,
"rule":<String_value>,
"city":<String_value>,
"tenant_name":<String_value>,
"country":<String_value>,
"group_name":<String_value>,
"approved_ssl_protocol_list":<String_value[]>,
"reference_key":<String_value>,
"approved_key_strength_list":<String_value[]>,
"exporter_id":<Double_value>,
"approved_signature_algo_list":<String_value[]>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ssl_cert_threshold":[{
"name":<String_value>,
"region":<String_value>,
"rule":<String_value>,
"stylebook_flag":<Boolean_value>,
"country":<String_value>,
"issuers_list":<String_value>,
"sms_profile":<String_value>,
"signature_algo_list":<String_value>,
"feature":<String_value>,
"ctnsappname":<String_value>,
"hide_default_certs":<Boolean_value>,
"id":<String_value>,
"resource_type":<String_value>,
"mail_profile":<String_value>,
"is_enabled":<String_value>,
"duration":<String_value>,
"days_to_expiry":<Integer_value>,
"city":<String_value>,
"key_strength_list":<String_value>,
"ssl_protocol_list":<String_value>,
"tenant_name":<String_value>,
"group_name":<String_value>,
"reference_key":<String_value>,
"exporter_id":<Double_value>,
"approved_ssl_protocol_list":<String_value>,
"approved_key_strength_list":<String_value>,
"approved_issuers_list":<String_value>,
"approved_signature_algo_list":<String_value>}]}
```







