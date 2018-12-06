#triton_config



Configuration for Configuration details for Triton module resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>active_framework</td><td>&lt;String></td><td>Read-write</td><td>Currently active container orchestration framework (Kubernetes or Marathon).</td></tr><tr><td>marathon_params</td><td>&lt;marathon_param></td><td>Read-write</td><td>Marathon parameters.</td></tr><tr><td>netmode</td><td>&lt;String></td><td>Read-write</td><td>Network mode of the operation: IP per container or CPX per host.<br>Maximum length = 200</td></tr><tr><td>dns_params</td><td>&lt;dns_param></td><td>Read-write</td><td>DNS Parameters.</td></tr><tr><td>framework_healthcheck</td><td>&lt;Boolean></td><td>Read-write</td><td>This indicates default monitor is enabled on this app or not.</td></tr><tr><td>kube_params</td><td>&lt;kubernetes_param></td><td>Read-write</td><td>Kubernetes parameters.</td></tr><tr><td>loopback_disabled</td><td>&lt;Boolean></td><td>Read-write</td><td>This indicates default monitor is enabled on this app or not.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id.</td></tr><tr><td>networking_params</td><td>&lt;networking_param></td><td>Read-write</td><td>Networking parameters.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [GET (ALL)](#get-all)| [MODIFY](#modify)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/triton_config?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{triton_config: {
"active_framework":<String_value>,
"loopback_disabled":<Boolean_value>,
"id":<String_value>,
"marathon_params":<marathon_param_value>,
"dns_params":<dns_param_value>,
"kube_params":<kubernetes_param_value>,
"netmode":<String_value>,
"framework_healthcheck":<Boolean_value>,
"networking_params":<networking_param_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "triton_config":[{
"active_framework":<String_value>,
"marathon_params":<marathon_param_value>,
"netmode":<String_value>,
"dns_params":<dns_param_value>,
"framework_healthcheck":<Boolean_value>,
"kube_params":<kubernetes_param_value>,
"loopback_disabled":<Boolean_value>,
"id":<String_value>,
"networking_params":<networking_param_value>}]}
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/triton_config

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "triton_config":[{
"active_framework":<String_value>,
"marathon_params":<marathon_param_value>,
"netmode":<String_value>,
"dns_params":<dns_param_value>,
"framework_healthcheck":<Boolean_value>,
"kube_params":<kubernetes_param_value>,
"loopback_disabled":<Boolean_value>,
"id":<String_value>,
"networking_params":<networking_param_value>}]}
```







###modify







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/triton_config/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{triton_config:{
<b>"id":<String_value></b>,
"active_framework":<String_value>,
"loopback_disabled":<Boolean_value>,
"marathon_params":<marathon_param_value>,
"dns_params":<dns_param_value>,
"kube_params":<kubernetes_param_value>,
"netmode":<String_value>,
"framework_healthcheck":<Boolean_value>,
"networking_params":<networking_param_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "triton_config":[{
"active_framework":<String_value>,
"marathon_params":<marathon_param_value>,
"netmode":<String_value>,
"dns_params":<dns_param_value>,
"framework_healthcheck":<Boolean_value>,
"kube_params":<kubernetes_param_value>,
"loopback_disabled":<Boolean_value>,
"id":<String_value>,
"networking_params":<networking_param_value>}]}
```







