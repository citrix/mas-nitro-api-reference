#mas_license



Configuration for MAS License Information resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>vcpu_lic</td><td>&lt;Integer></td><td>Read-write</td><td>vCPU Licenses, 0=Unlicensed/Disabled, 1=Unlicensed/Enabled, 2=Licensed/Disabled, 3=Licensed/Enabled.</td></tr><tr><td>lic_type</td><td>&lt;Integer></td><td>Read-write</td><td>0 = Trial Period, 1 = Licensed, 2 = Grace period, 3 = unlicensed.</td></tr><tr><td>cpx_lic</td><td>&lt;Integer></td><td>Read-write</td><td>CPX Licenses, 0=Unlicensed/Disabled, 1=Unlicensed/Enabled, 2=Licensed/Disabled, 3=Licensed/Enabled.</td></tr><tr><td>analytics</td><td>&lt;Integer></td><td>Read-write</td><td>Analytics, 0=Unlicensed/Disabled, 1=Unlicensed/Enabled, 2=Licensed/Disabled, 3=Licensed/Enabled.</td></tr><tr><td>adv_analytics</td><td>&lt;Integer></td><td>Read-write</td><td>Advanced Analytics, 0=Unlicensed/Disabled, 1=Unlicensed/Enabled, 2=Licensed/Disabled, 3=Licensed/Enabled.</td></tr><tr><td>perf</td><td>&lt;Integer></td><td>Read-write</td><td>Perf, 0=Unlicensed/Disabled, 1=Unlicensed/Enabled, 2=Licensed/Disabled, 3=Licensed/Enabled.</td></tr><tr><td>vpx_lic</td><td>&lt;Integer></td><td>Read-write</td><td>VPX Licenses, 0=Unlicensed/Disabled, 1=Unlicensed/Enabled, 2=Licensed/Disabled, 3=Licensed/Enabled.</td></tr><tr><td>syslog</td><td>&lt;Integer></td><td>Read-write</td><td>Syslog, 0=Unlicensed/Disabled, 1=Unlicensed/Enabled, 2=Licensed/Disabled, 3=Licensed/Enabled.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key.</td></tr><tr><td>pooled_lic</td><td>&lt;Integer></td><td>Read-write</td><td>Pooled Licenses, 0=Unlicensed/Disabled, 1=Unlicensed/Enabled, 2=Licensed/Disabled, 3=Licensed/Enabled.</td></tr><tr><td>snmp_traps</td><td>&lt;Integer></td><td>Read-write</td><td>SNMP Traps, 0=Unlicensed/Disabled, 1=Unlicensed/Enabled, 2=Licensed/Disabled, 3=Licensed/Enabled.</td></tr><tr><td>get_consumed_db</td><td>&lt;Boolean></td><td>Read-write</td><td>Get Consumed DB.</td></tr><tr><td>max_vips</td><td>&lt;String></td><td>Read-only</td><td>Maximum VIPs.</td></tr><tr><td>max_storage</td><td>&lt;String></td><td>Read-only</td><td>Max Storage.</td></tr><tr><td>node_id</td><td>&lt;String></td><td>Read-only</td><td>Node ID.</td></tr><tr><td>max_tp_vservers</td><td>&lt;String></td><td>Read-only</td><td>Maximum Third Party Vservers.</td></tr><tr><td>rpt_sampletime</td><td>&lt;Double></td><td>Read-only</td><td>Time Stamp.</td></tr><tr><td>total_managed_vips</td><td>&lt;Integer></td><td>Read-only</td><td>Total managed VIPs.</td></tr><tr><td>total_managed_tp_vservers</td><td>&lt;Integer></td><td>Read-only</td><td>Total managed Third Party Vservers.</td></tr><tr><td>total_allowed_tp_vservers</td><td>&lt;Integer></td><td>Read-only</td><td>Total Allowed Third Party Vservres.</td></tr><tr><td>total_discovered_vips</td><td>&lt;Integer></td><td>Read-only</td><td>Total discovered VIPs.</td></tr><tr><td>consumed_db_storage</td><td>&lt;String></td><td>Read-only</td><td>Consumed DB storage.</td></tr><tr><td>total_allowed_vips</td><td>&lt;Integer></td><td>Read-only</td><td>Total Allowed VIPs.</td></tr><tr><td>entitled_db_storage</td><td>&lt;Integer></td><td>Read-only</td><td>Entitled DB storage in GB.</td></tr><tr><td>total_discovered_tp_vservers</td><td>&lt;Integer></td><td>Read-only</td><td>Total discovered Third Party Vservres.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mas_license

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mas_license":[{
"vcpu_lic":<Integer_value>,
"lic_type":<Integer_value>,
"cpx_lic":<Integer_value>,
"max_vips":<String_value>,
"max_storage":<String_value>,
"analytics":<Integer_value>,
"adv_analytics":<Integer_value>,
"perf":<Integer_value>,
"node_id":<String_value>,
"vpx_lic":<Integer_value>,
"max_tp_vservers":<String_value>,
"syslog":<Integer_value>,
"id":<String_value>,
"rpt_sampletime":<Double_value>,
"pooled_lic":<Integer_value>,
"snmp_traps":<Integer_value>,
"total_managed_vips":<Integer_value>,
"total_managed_tp_vservers":<Integer_value>,
"total_allowed_tp_vservers":<Integer_value>,
"total_discovered_vips":<Integer_value>,
"get_consumed_db":<Boolean_value>,
"consumed_db_storage":<String_value>,
"total_allowed_vips":<Integer_value>,
"entitled_db_storage":<Integer_value>,
"total_discovered_tp_vservers":<Integer_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mas_license/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{mas_license:{
"vcpu_lic":<Integer_value>,
"cpx_lic":<Integer_value>,
"lic_type":<Integer_value>,
"analytics":<Integer_value>,
"adv_analytics":<Integer_value>,
"perf":<Integer_value>,
"get_consumed_db":<Boolean_value>,
"syslog":<Integer_value>,
"vpx_lic":<Integer_value>,
"id":<String_value>,
"pooled_lic":<Integer_value>,
"snmp_traps":<Integer_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mas_license":[{
"vcpu_lic":<Integer_value>,
"lic_type":<Integer_value>,
"cpx_lic":<Integer_value>,
"max_vips":<String_value>,
"max_storage":<String_value>,
"analytics":<Integer_value>,
"adv_analytics":<Integer_value>,
"perf":<Integer_value>,
"node_id":<String_value>,
"vpx_lic":<Integer_value>,
"max_tp_vservers":<String_value>,
"syslog":<Integer_value>,
"id":<String_value>,
"rpt_sampletime":<Double_value>,
"pooled_lic":<Integer_value>,
"snmp_traps":<Integer_value>,
"total_managed_vips":<Integer_value>,
"total_managed_tp_vservers":<Integer_value>,
"total_allowed_tp_vservers":<Integer_value>,
"total_discovered_vips":<Integer_value>,
"get_consumed_db":<Boolean_value>,
"consumed_db_storage":<String_value>,
"total_allowed_vips":<Integer_value>,
"entitled_db_storage":<Integer_value>,
"total_discovered_tp_vservers":<Integer_value>}]}
```







