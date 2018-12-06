#backup_component



Configuration for backup components resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>component_message</td><td>&lt;String></td><td>Read-write</td><td>Information about the componenet.</td></tr><tr><td>component_versions</td><td>&lt;String></td><td>Read-write</td><td>Backup component version.</td></tr><tr><td>component_minimum_version</td><td>&lt;String></td><td>Read-write</td><td>Minimum version supported by the NetScaler.</td></tr><tr><td>backup_file_name</td><td>&lt;String></td><td>Read-write</td><td>Backup file name.<br>Maximum length = 64</td></tr><tr><td>component</td><td>&lt;String></td><td>Read-write</td><td>Backup component.</td></tr><tr><td>component_name</td><td>&lt;String></td><td>Read-write</td><td>Backup component Name.</td></tr><tr><td>component_ip</td><td>&lt;String></td><td>Read-write</td><td>Backup component IPaddress.</td></tr><tr><td>component_version_bit</td><td>&lt;String></td><td>Read-write</td><td>(32/64 bit) information for backup component version.</td></tr><tr><td>component_hostname</td><td>&lt;String></td><td>Read-write</td><td>Backup component VM Name.</td></tr><tr><td>component_error_severity</td><td>&lt;Integer></td><td>Read-write</td><td>Severity of error for the component.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



