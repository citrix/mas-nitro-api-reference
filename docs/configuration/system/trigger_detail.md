#trigger_detail

Configuration for Trigger Detail resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>expiry</td><td>&lt;String></td><td>Read-write</td><td>Time at which the trigger should end.Format:YY:MM:DD:HH:MM.Applicable for trigger of type fixed.</td></tr><tr><td>parent_name</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>daily_time</td><td>&lt;String></td><td>Read-write</td><td>Time of the day.Format is HH:MM where HH is hours and MM is minutes.Applicable for trigger of type daily.</td></tr><tr><td>trigger_type</td><td>&lt;String></td><td>Read-write</td><td>Trigger type.Possible values: fixed,daily,weekly,monthly.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>recur_hr</td><td>&lt;String></td><td>Read-write</td><td>Recur interval in hours. Applicable for trigger of type fixed.</td></tr><tr><td>duration</td><td>&lt;String></td><td>Read-write</td><td>Duration in days for which the trigger should last. Applicable for trigger of type fixed.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Trigger description.</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>monthday_time</td><td>&lt;String></td><td>Read-write</td><td>Days of the month.Format is DD:HH:MM where DD is either 1-31 or "last" for days of the month,HH is hours and MM is minutes.Applicable for trigger of type monthly..</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>weekday_time</td><td>&lt;String></td><td>Read-write</td><td>Days of the week.Format is Day:HH:MM where Day is 0-6 for sunday-saturday,HH is hours and MM is minutes.Applicable for trigger of type weekly.</td></tr><tr><td>recur_min</td><td>&lt;String></td><td>Read-write</td><td>Recur interval in minutes. Applicable for trigger of type fixed.</td></tr><tr><td>start</td><td>&lt;String></td><td>Read-write</td><td>Time at which the trigger should start.Format:YY:MM:DD:HH:MM.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

