#allocationgroup

Configuration for NetScaler Control Center allocates NetScaler instances according to the SLA that is defined as part this service package. resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>partitionspec</td><td>&lt;groupmember></td><td>Read-write</td><td>ID of a Partition Specification. The partition specification will be used while creating partition.</td></tr><tr><td>devicespec</td><td>&lt;groupmember></td><td>Read-write</td><td>ID of a Device Specification. The device specification will be used while creating device instances.</td></tr><tr><td>device_type</td><td>&lt;String></td><td>Read-write</td><td>The device type that has to be allocated. Possible values - 'NetScaler'.</td></tr><tr><td>placement_scheme</td><td>&lt;String></td><td>Read-write</td><td>The allocation policy scheme which will help allocating a device when allocation policy is 'shared'. Possible values - 'roundrobin', 'leastentity'.</td></tr><tr><td>devicegroup</td><td>&lt;groupmember></td><td>Read-write</td><td>Devicegroup from which devices will be allocated.</td></tr><tr><td>allocationpolicy</td><td>&lt;String></td><td>Read-write</td><td>The allocation policy of the device instance. Possible values - 'shared', 'dedicated'.</td></tr><tr><td>device_allocation_type</td><td>&lt;String></td><td>Read-write</td><td>The device instance that has to be allocated. Possible values - 'netScaler', 'partition'.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/allocationgroup
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "allocationgroup":[{"partitionspec":<groupmember_value>,"devicespec":<groupmember_value>,"device_type":<String_value>,"placement_scheme":<String_value>,"devicegroup":<groupmember_value>,"allocationpolicy":<String_value>,"device_allocation_type":<String_value>}]}```



