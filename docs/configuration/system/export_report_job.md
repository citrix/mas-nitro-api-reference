#export_report_job



Configuration for Scheduled export report job resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>recurrence_option</td><td>&lt;String></td><td>Read-write</td><td>Recurrence option (Weekly -&gt; mon - sun, Monthly -&gt; date in DD format)..</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-write</td><td>Schedule Status.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>export_format</td><td>&lt;String></td><td>Read-write</td><td>Report Export format (PDF/JPEG/PNG).<br>Minimum length = 3<br>Maximum length = 4</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Report Description..<br>Maximum length = 512</td></tr><tr><td>mail_profile_name</td><td>&lt;String></td><td>Read-write</td><td>Mail profile name to send notification mail..<br>Minimum length = 1<br>Maximum length = 255</td></tr><tr><td>recurrence</td><td>&lt;String></td><td>Read-write</td><td>Recurrence (Daily, Weekly, Monthly)..<br>Maximum length = 16</td></tr><tr><td>tz_offset</td><td>&lt;Integer></td><td>Read-write</td><td>Time zone offset..</td></tr><tr><td>next_scheduletime</td><td>&lt;Integer></td><td>Read-write</td><td>Next Schedule Time.</td></tr><tr><td>export_time</td><td>&lt;String></td><td>Read-write</td><td>Report Export time GMT epoch (string representation of 10 digit numbers)..<br>Minimum length = 5<br>Maximum length = 16</td></tr><tr><td>job_name</td><td>&lt;String></td><td>Read-write</td><td>job name is ExportJob..<br>Maximum length = 16</td></tr><tr><td>trigger_start</td><td>&lt;String></td><td>Read-write</td><td>Time at which the trigger should start.Format:YY:MM:DD:HH:MM.</td></tr><tr><td>report_name</td><td>&lt;String></td><td>Read-write</td><td>report name.<br>Maximum length = 255</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is job_schedule id for all the export_report_job details.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[DELETE](#delete)| [GET (ALL)](#get-all)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/export_report_job/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/export_report_job

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "export_report_job":[{
"recurrence_option":<String_value>,
"status":<String_value>,
"export_format":<String_value>,
"description":<String_value>,
"mail_profile_name":<String_value>,
"recurrence":<String_value>,
"tz_offset":<Integer_value>,
"next_scheduletime":<Integer_value>,
"export_time":<String_value>,
"job_name":<String_value>,
"trigger_start":<String_value>,
"report_name":<String_value>,
"id":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/export_report_job/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{export_report_job:{
<b>"id":<String_value></b>,
"export_format":<String_value>,
"description":<String_value>,
"tz_offset":<Integer_value>,
"recurrence":<String_value>,
"recurrence_option":<String_value>,
"status":<String_value>,
"mail_profile_name":<String_value>,
"trigger_start":<String_value>,
"job_name":<String_value>,
"report_name":<String_value>,
"next_scheduletime":<Integer_value>,
"export_time":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "export_report_job":[{
"recurrence_option":<String_value>,
"status":<String_value>,
"export_format":<String_value>,
"description":<String_value>,
"mail_profile_name":<String_value>,
"recurrence":<String_value>,
"tz_offset":<Integer_value>,
"next_scheduletime":<Integer_value>,
"export_time":<String_value>,
"job_name":<String_value>,
"trigger_start":<String_value>,
"report_name":<String_value>,
"id":<String_value>}]}
```







