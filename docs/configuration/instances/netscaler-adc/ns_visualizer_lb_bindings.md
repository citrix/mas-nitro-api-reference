#ns_visualizer_lb_bindings



Configuration for visualizer lbv server binding resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>lbvserver_auditsyslogpolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Audit syslog policy binding of Lbvserver.</td></tr><tr><td>lbvserver_appfwpolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>App Flow policy binding of Lbvserver.</td></tr><tr><td>lbvserver_rewritepolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Rewrite policy binding of Lbvserver.</td></tr><tr><td>policy_type</td><td>&lt;String></td><td>Read-write</td><td>Policy Type.</td></tr><tr><td>lbvserver_spilloverpolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Spill Over policy binding of Lbvserver.</td></tr><tr><td>lbvserver_auditnslogpolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Audit ns policy binding of Lbvserver.</td></tr><tr><td>lbvserver_transformpolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Transform policy binding of Lbvserver.</td></tr><tr><td>lbvserver_appqoepolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>app qo policy binding of Lbvserver.</td></tr><tr><td>lbvserver_filterpolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Filter policy binding of Lbvserver.</td></tr><tr><td>lbvserver_csvserver_binding</td><td>&lt;String[]></td><td>Read-write</td><td>CSV Server binding of Lbvserver.</td></tr><tr><td>lbvserver_feopolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Feo policy binding of Lbvserver.</td></tr><tr><td>lbvserver_appflowpolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>App Flow policy binding of Lbvserver.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>lbvserver_authorizationpolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Authorization policy binding of Lbvserver.</td></tr><tr><td>lbvserver_capolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>CA policy binding of Lbvserver.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of lbvserver.</td></tr><tr><td>lbvserver_servicegroup_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Service group binding of Lbvserver.</td></tr><tr><td>lbvserver_cachepolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Cache policy binding of Lbvserver.</td></tr><tr><td>port</td><td>&lt;String></td><td>Read-write</td><td>Port number for the virtual server.</td></tr><tr><td>lbvserver_service_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Service binding of Lbvserver.</td></tr><tr><td>lbvserver_responderpolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Responder policy binding of Lbvserver.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>type.</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>IP Address of virtual server.</td></tr><tr><td>lbvserver_tmtrafficpolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>TM Traffic policy binding of Lbvserver.</td></tr><tr><td>lbvserver_cmppolicy_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Compression policy binding of Lbvserver.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_visualizer_lb_bindings

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_visualizer_lb_bindings":[{
"lbvserver_auditsyslogpolicy_binding":<String_value>,
"lbvserver_appfwpolicy_binding":<String_value>,
"lbvserver_rewritepolicy_binding":<String_value>,
"policy_type":<String_value>,
"lbvserver_spilloverpolicy_binding":<String_value>,
"lbvserver_auditnslogpolicy_binding":<String_value>,
"lbvserver_transformpolicy_binding":<String_value>,
"lbvserver_appqoepolicy_binding":<String_value>,
"lbvserver_filterpolicy_binding":<String_value>,
"lbvserver_csvserver_binding":<String_value>,
"lbvserver_feopolicy_binding":<String_value>,
"lbvserver_appflowpolicy_binding":<String_value>,
"ip_address":<String_value>,
"lbvserver_authorizationpolicy_binding":<String_value>,
"lbvserver_capolicy_binding":<String_value>,
"name":<String_value>,
"lbvserver_servicegroup_binding":<String_value>,
"lbvserver_cachepolicy_binding":<String_value>,
"port":<String_value>,
"lbvserver_service_binding":<String_value>,
"lbvserver_responderpolicy_binding":<String_value>,
"type":<String_value>,
"ipaddress":<String_value>,
"lbvserver_tmtrafficpolicy_binding":<String_value>,
"lbvserver_cmppolicy_binding":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_visualizer_lb_bindings/name_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_visualizer_lb_bindings":[{
"lbvserver_auditsyslogpolicy_binding":<String_value>,
"lbvserver_appfwpolicy_binding":<String_value>,
"lbvserver_rewritepolicy_binding":<String_value>,
"policy_type":<String_value>,
"lbvserver_spilloverpolicy_binding":<String_value>,
"lbvserver_auditnslogpolicy_binding":<String_value>,
"lbvserver_transformpolicy_binding":<String_value>,
"lbvserver_appqoepolicy_binding":<String_value>,
"lbvserver_filterpolicy_binding":<String_value>,
"lbvserver_csvserver_binding":<String_value>,
"lbvserver_feopolicy_binding":<String_value>,
"lbvserver_appflowpolicy_binding":<String_value>,
"ip_address":<String_value>,
"lbvserver_authorizationpolicy_binding":<String_value>,
"lbvserver_capolicy_binding":<String_value>,
"name":<String_value>,
"lbvserver_servicegroup_binding":<String_value>,
"lbvserver_cachepolicy_binding":<String_value>,
"port":<String_value>,
"lbvserver_service_binding":<String_value>,
"lbvserver_responderpolicy_binding":<String_value>,
"type":<String_value>,
"ipaddress":<String_value>,
"lbvserver_tmtrafficpolicy_binding":<String_value>,
"lbvserver_cmppolicy_binding":<String_value>}]}
```







