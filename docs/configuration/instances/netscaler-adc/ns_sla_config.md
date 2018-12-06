#ns_sla_config



Configuration for SLA Virtual server config on NetScaler resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Appflow log.</td></tr><tr><td>acceptancethreshold</td><td>&lt;String></td><td>Read-write</td><td>Tells whether bind type virtual server type.<br>Minimum length = 1<br>Maximum length = 10</td></tr><tr><td>is_active_policy</td><td>&lt;Integer></td><td>Read-write</td><td>Policy is Active or Not.</td></tr><tr><td>rule</td><td>&lt;String></td><td>Read-write</td><td>Responder policy rule.</td></tr><tr><td>appflowaction</td><td>&lt;String></td><td>Read-write</td><td>appflowaction.</td></tr><tr><td>is_response_time_set</td><td>&lt;Integer></td><td>Read-write</td><td>is_response_time_set.</td></tr><tr><td>policy_action</td><td>&lt;String></td><td>Read-write</td><td>policy_action NOOP.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NS IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>hits</td><td>&lt;String></td><td>Read-write</td><td>Hits of Responder Policy.</td></tr><tr><td>maxtransactionthreshold</td><td>&lt;String></td><td>Read-write</td><td>rt_max_threshold .</td></tr><tr><td>DOI</td><td>&lt;String></td><td>Read-write</td><td>DOI name.<br>Maximum length = 255</td></tr><tr><td>vserver_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NetScaler IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>bind_priority</td><td>&lt;String></td><td>Read-write</td><td>bind_priority 1 to 2147483647.</td></tr><tr><td>bind_type</td><td>&lt;String></td><td>Read-write</td><td>Tells whether bind type virtual server type.<br>Minimum length = 2<br>Maximum length = 64</td></tr><tr><td>mintransactionthreshold</td><td>&lt;String></td><td>Read-write</td><td>rt_min_threshold .</td></tr><tr><td>time_window_interval</td><td>&lt;String></td><td>Read-write</td><td>time_window_interval 1 min to 1440 mins .</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [MODIFY](#modify)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_sla_config?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_sla_config: {
"rule":<String_value>,
"is_active_policy":<Integer_value>,
"appflowaction":<String_value>,
"ns_ip_address":<String_value>,
"hits":<String_value>,
"bind_type":<String_value>,
"acceptancethreshold":<String_value>,
"appflowlog":<String_value>,
"policy_action":<String_value>,
"is_response_time_set":<Integer_value>,
"maxtransactionthreshold":<String_value>,
"DOI":<String_value>,
"vserver_ip_address":<String_value>,
"bind_priority":<String_value>,
"mintransactionthreshold":<String_value>,
"time_window_interval":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_sla_config":[{
"appflowlog":<String_value>,
"acceptancethreshold":<String_value>,
"is_active_policy":<Integer_value>,
"rule":<String_value>,
"appflowaction":<String_value>,
"is_response_time_set":<Integer_value>,
"policy_action":<String_value>,
"ns_ip_address":<String_value>,
"hits":<String_value>,
"maxtransactionthreshold":<String_value>,
"DOI":<String_value>,
"vserver_ip_address":<String_value>,
"bind_priority":<String_value>,
"bind_type":<String_value>,
"mintransactionthreshold":<String_value>,
"time_window_interval":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_sla_config/

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_sla_config

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_sla_config":[{
"appflowlog":<String_value>,
"acceptancethreshold":<String_value>,
"is_active_policy":<Integer_value>,
"rule":<String_value>,
"appflowaction":<String_value>,
"is_response_time_set":<Integer_value>,
"policy_action":<String_value>,
"ns_ip_address":<String_value>,
"hits":<String_value>,
"maxtransactionthreshold":<String_value>,
"DOI":<String_value>,
"vserver_ip_address":<String_value>,
"bind_priority":<String_value>,
"bind_type":<String_value>,
"mintransactionthreshold":<String_value>,
"time_window_interval":<String_value>}]}
```







###modify







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_sla_config/

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_sla_config:{
"rule":<String_value>,
"is_active_policy":<Integer_value>,
"appflowaction":<String_value>,
"ns_ip_address":<String_value>,
"hits":<String_value>,
"bind_type":<String_value>,
"acceptancethreshold":<String_value>,
"appflowlog":<String_value>,
"policy_action":<String_value>,
"is_response_time_set":<Integer_value>,
"maxtransactionthreshold":<String_value>,
"DOI":<String_value>,
"vserver_ip_address":<String_value>,
"bind_priority":<String_value>,
"mintransactionthreshold":<String_value>,
"time_window_interval":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_sla_config":[{
"appflowlog":<String_value>,
"acceptancethreshold":<String_value>,
"is_active_policy":<Integer_value>,
"rule":<String_value>,
"appflowaction":<String_value>,
"is_response_time_set":<Integer_value>,
"policy_action":<String_value>,
"ns_ip_address":<String_value>,
"hits":<String_value>,
"maxtransactionthreshold":<String_value>,
"DOI":<String_value>,
"vserver_ip_address":<String_value>,
"bind_priority":<String_value>,
"bind_type":<String_value>,
"mintransactionthreshold":<String_value>,
"time_window_interval":<String_value>}]}
```







