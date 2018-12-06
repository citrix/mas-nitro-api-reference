#provision_setting



Configuration for Provision settings can be used to configure global settings such as management network, the image that can be used to provision new NS devices, profiles and licenses. resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>images</td><td>&lt;images[]></td><td>Read-write</td><td>Image that will be used for provisioning new devices..</td></tr><tr><td>server_boundaries</td><td>&lt;server_boundaries[]></td><td>Read-write</td><td>Server boundaries present in provision settings..</td></tr><tr><td>management_networks</td><td>&lt;management_networks[]></td><td>Read-write</td><td>Management Networks of OpenStack that has to be registered with Control Centre..</td></tr><tr><td>licenses</td><td>&lt;profiles[]></td><td>Read-write</td><td>Licenses that will be used for newly provisioned devices..</td></tr><tr><td>profiles</td><td>&lt;profiles[]></td><td>Read-write</td><td>Profile that will be used for newly provisioned devices..</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/provision_setting

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "provision_setting":[{
"images":[{
"ref":<String_value>,
"type":<String_value>}],
"server_boundaries":[{
"topology":<String_value>,
"l3config":<String_value>}],
"management_networks":[{
"ref":<String_value>}],
"licenses":[{
"name":<String_value>,
"type":<String_value>}],
"profiles":[{
"name":<String_value>,
"type":<String_value>}]}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/provision_setting/

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{provision_setting:{
"images":[{
<b>"ref":<String_value></b>,
<b>"type":<String_value></b>}],
"server_boundaries":[{
"topology":<String_value>,
"l3config":<String_value>}],
"licenses":[{
<b>"name":<String_value></b>,
<b>"type":<String_value></b>}],
"management_networks":[{
<b>"ref":<String_value></b>}],
"profiles":[{
<b>"name":<String_value></b>,
<b>"type":<String_value></b>}]}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "provision_setting":[{
"images":[{
"ref":<String_value>,
"type":<String_value>}],
"server_boundaries":[{
"topology":<String_value>,
"l3config":<String_value>}],
"management_networks":[{
"ref":<String_value>}],
"licenses":[{
"name":<String_value>,
"type":<String_value>}],
"profiles":[{
"name":<String_value>,
"type":<String_value>}]}]}
```







