#mps_upgrade



Configuration for System Upgrade resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>image_name</td><td>&lt;String></td><td>Read-write</td><td>image_name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>doc_file</td><td>&lt;String></td><td>Read-write</td><td>This property is no longer used;ltbr;gtDocumentation File Name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>do_cleanup</td><td>&lt;Boolean></td><td>Read-write</td><td>True, if user wants to clean the image files once upgrade is completed successfully.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[UPGRADE](#up)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###upgrade







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps_upgrade?action=upgrade;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{mps_upgrade: {
<b>"image_name":<String_value></b>,
"do_cleanup":<Boolean_value>,
"doc_file":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mps_upgrade":[{
"image_name":<String_value>,
"doc_file":<String_value>,
"do_cleanup":<Boolean_value>}]}
```







