#ns_visualizer_gslb_bindings



Configuration for visualizer gslbvserver binding resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>gslbdomain_lbmonitor_binding</td><td>&lt;String[]></td><td>Read-write</td><td>lb monitor binding of Gslbvserver.</td></tr><tr><td>gslbdomain_gslbvserver_binding</td><td>&lt;String[]></td><td>Read-write</td><td>Service binding of Gslbvserver.</td></tr><tr><td>gslbdomain_gslbservice_binding</td><td>&lt;String[]></td><td>Read-write</td><td>GSLB service binding of Gslbvserver.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of gslbvserver.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_visualizer_gslb_bindings

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_visualizer_gslb_bindings":[{
"gslbdomain_lbmonitor_binding":<String_value>,
"gslbdomain_gslbvserver_binding":<String_value>,
"gslbdomain_gslbservice_binding":<String_value>,
"name":<String_value>,
"ip_address":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_visualizer_gslb_bindings/name_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_visualizer_gslb_bindings":[{
"gslbdomain_lbmonitor_binding":<String_value>,
"gslbdomain_gslbvserver_binding":<String_value>,
"gslbdomain_gslbservice_binding":<String_value>,
"name":<String_value>,
"ip_address":<String_value>}]}
```







