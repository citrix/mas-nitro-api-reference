#export_report



Configuration for Export report resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>page_name</td><td>&lt;String></td><td>Read-write</td><td>Page name..<br>Minimum length = 1<br>Maximum length = 255</td></tr><tr><td>recurrence_option</td><td>&lt;String></td><td>Read-write</td><td>Recurrence option (Weekly -&gt; mon - sun, Monthly -&gt; date in DD format)..<br>Maximum length = 128</td></tr><tr><td>report_context</td><td>&lt;String></td><td>Read-write</td><td>Report context..</td></tr><tr><td>export_format</td><td>&lt;String></td><td>Read-write</td><td>Report Export format (PDF/JPEG/PNG).<br>Minimum length = 3<br>Maximum length = 4</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Report Description..<br>Maximum length = 512</td></tr><tr><td>report_title</td><td>&lt;String></td><td>Read-write</td><td>Report Title.</td></tr><tr><td>mail_profile_name</td><td>&lt;String></td><td>Read-write</td><td>Mail profile name to send notification mail..<br>Maximum length = 255</td></tr><tr><td>recurrence</td><td>&lt;String></td><td>Read-write</td><td>Recurrence (Daily, Weekly, Monthly)..<br>Maximum length = 16</td></tr><tr><td>tz_offset</td><td>&lt;Integer></td><td>Read-write</td><td>Time zone offset..</td></tr><tr><td>file_name</td><td>&lt;String></td><td>Read-write</td><td>Report File name..</td></tr><tr><td>csv_export_arr</td><td>&lt;csv_export[]></td><td>Read-write</td><td>CSV Export Array.</td></tr><tr><td>export_time</td><td>&lt;String></td><td>Read-write</td><td>Report Export time epoch (string representation of 11 digit numbers)..<br>Minimum length = 10<br>Maximum length = 16</td></tr><tr><td>export_now</td><td>&lt;Boolean></td><td>Read-write</td><td>Export now.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DOWNLOAD](#download)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/export_report?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{export_report: {
"export_format":<String_value>,
"file_name":<String_value>,
"page_name":<String_value>,
"description":<String_value>,
"tz_offset":<Integer_value>,
"recurrence":<String_value>,
"report_title":<String_value>,
"export_now":<Boolean_value>,
"recurrence_option":<String_value>,
"mail_profile_name":<String_value>,
"report_context":<String_value>,
"export_time":<String_value>,
"csv_export_arr":[{
"report_end_time":<Double_value>,
"args":<String_value>,
"order_by":<String_value>,
"resource_id":<String_value>,
"report_start_time":<Double_value>,
"asc":<String_value>,
"duration_summary":<String_value>,
"id":<String_value>,
"section_title":<String_value>,
"is_count":<String_value>,
"attrs":<String_value>,
"filter":<String_value>,
"detailview":<String_value>,
"duration":<String_value>,
"cr_enabled":<String_value>,
"sla_enabled":<String_value>,
"resource_name":<String_value>,
"type":<String_value>,
"csv_mapping_id":<String_value>}]}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "export_report":[{
"page_name":<String_value>,
"recurrence_option":<String_value>,
"report_context":<String_value>,
"export_format":<String_value>,
"description":<String_value>,
"report_title":<String_value>,
"mail_profile_name":<String_value>,
"recurrence":<String_value>,
"tz_offset":<Integer_value>,
"file_name":<String_value>,
"csv_export_arr":[{
"report_end_time":<Double_value>,
"order_by":<String_value>,
"args":<String_value>,
"report_start_time":<Double_value>,
"resource_id":<String_value>,
"asc":<String_value>,
"duration_summary":<String_value>,
"id":<String_value>,
"section_title":<String_value>,
"attrs":<String_value>,
"is_count":<String_value>,
"filter":<String_value>,
"detailview":<String_value>,
"duration":<String_value>,
"cr_enabled":<String_value>,
"sla_enabled":<String_value>,
"type":<String_value>,
"resource_name":<String_value>,
"csv_mapping_id":<String_value>}],
"export_time":<String_value>,
"export_now":<Boolean_value>}]}
```







###download







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/download/export_report/_value&lt;&gt;

<b>HTTP Method: </b>null







