#eventrule_config_command

Configuration for Configuration Commands for use in configuration template resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol used by Configuration Command: SSH|SCP|SFTP|NITRO.<br>Minimum length = 1<br>Maximum length = 32</td></tr><tr><td>index</td><td>&lt;Integer></td><td>Read-write</td><td>Index that stores the position of the command in a command array.</td></tr><tr><td>parent_name</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>timeout</td><td>&lt;Integer></td><td>Read-write</td><td>Command Timeout in secs.<br>Maximum value =</td></tr><tr><td>nitro_payload</td><td>&lt;String></td><td>Read-write</td><td>NITRO Request Payload.</td></tr><tr><td>nitro_resource</td><td>&lt;String></td><td>Read-write</td><td>NITRO Resource Name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>nitro_method</td><td>&lt;String></td><td>Read-write</td><td>NITRO Request Method: POST|PUT|DELETE.<br>Minimum length = 1<br>Maximum length = 32</td></tr><tr><td>command</td><td>&lt;String></td><td>Read-write</td><td>Command String for Protocols SSH|SCP|SFTP.</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

