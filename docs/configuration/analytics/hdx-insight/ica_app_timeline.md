#ica_app_timeline



Configuration for Af report for ICA App timeline resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>usage_time</td><td>&lt;Double></td><td>Read-write</td><td>ica app usages time..</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>app_start_time</td><td>&lt;Double></td><td>Read-write</td><td>Application start time..</td></tr><tr><td>active_launches</td><td>&lt;Double></td><td>Read-write</td><td>ica active_launches.</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>App state..</td></tr><tr><td>app_launch_count</td><td>&lt;Double></td><td>Read-write</td><td>ica app_launch_count.</td></tr><tr><td>launch_duration</td><td>&lt;Double></td><td>Read-write</td><td>ICA App launch duration..</td></tr><tr><td>app_count</td><td>&lt;Double></td><td>Read-write</td><td>ica app_count..</td></tr><tr><td>app_enumeration_duration</td><td>&lt;Double></td><td>Read-write</td><td>ica app enumeration duration..</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is ICA App Name.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>up_time</td><td>&lt;Double></td><td>Read-write</td><td>ica app up time..</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of ICA Device.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>total_bytes</td><td>&lt;Double></td><td>Read-write</td><td>Total bytes accounted by this URL in sampled timeframe..</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>app_terminate_time</td><td>&lt;Double></td><td>Read-write</td><td>Application terminate time..</td></tr><tr><td>is_active</td><td>&lt;Double></td><td>Read-write</td><td>Is Active..</td></tr><tr><td>timeline_user_count</td><td>&lt;Double></td><td>Read-write</td><td>timeline_user_count..</td></tr><tr><td>user_count</td><td>&lt;Double></td><td>Read-write</td><td>user_count..</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ica_app_timeline

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ica_app_timeline":[{
"ica_user_name":<String_value>,
"usage_time":<Double_value>,
"__count":<Double_value>,
"app_start_time":<Double_value>,
"active_launches":<Double_value>,
"state":<String_value>,
"ica_device_ip_address":<String_value>,
"app_launch_count":<Double_value>,
"launch_duration":<Double_value>,
"ica_session_id":<String_value>,
"app_count":<Double_value>,
"app_enumeration_duration":<Double_value>,
"id":<String_value>,
"up_time":<Double_value>,
"name":<String_value>,
"total_bytes":<Double_value>,
"rpt_sample_time":<Double_value>,
"app_terminate_time":<Double_value>,
"is_active":<Double_value>,
"timeline_user_count":<Double_value>,
"user_count":<Double_value>}]}
```







