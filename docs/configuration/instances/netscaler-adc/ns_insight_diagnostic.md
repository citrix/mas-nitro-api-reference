#ns_insight_diagnostic



Configuration for Insight Diagnostic resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>httpreferer</td><td>&lt;String></td><td>Read-write</td><td>HTTP referer logging..</td></tr><tr><td>templaterefresh</td><td>&lt;Integer></td><td>Read-write</td><td>IPFIX template refresh interval..</td></tr><tr><td>securityinsightrecordinterval</td><td>&lt;Integer></td><td>Read-write</td><td>SecurityInsight record export interval..</td></tr><tr><td>hostname</td><td>&lt;String></td><td>Read-write</td><td>Hostname of NetScaler..</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NS IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>httpsetcookie</td><td>&lt;String></td><td>Read-write</td><td>HTTP Setcookie header logging..</td></tr><tr><td>httpvia</td><td>&lt;String></td><td>Read-write</td><td>HTTP Via header logging..</td></tr><tr><td>lbvserver</td><td>&lt;ns_lbvserver_diagnostic[]></td><td>Read-write</td><td>load balancing vserver Diagnostic.</td></tr><tr><td>httpdomain</td><td>&lt;String></td><td>Read-write</td><td>HTTP Domain Name logging..</td></tr><tr><td>httpsetcookie2</td><td>&lt;String></td><td>Read-write</td><td>HTTP Setcookie2 header logging..</td></tr><tr><td>vpnvserver</td><td>&lt;ns_nonlbvserver_diagnostic[]></td><td>Read-write</td><td>VPN Vserver Diagnostic.</td></tr><tr><td>flowrecordinterval</td><td>&lt;Integer></td><td>Read-write</td><td>IPFIX flow record export interval..</td></tr><tr><td>httpauthorization</td><td>&lt;String></td><td>Read-write</td><td>HTTP Authorization header logging..</td></tr><tr><td>skipcacheredirectionhttptransaction</td><td>&lt;String></td><td>Read-write</td><td>Skip Cache Redirection HTTP Transaction..</td></tr><tr><td>aaausername</td><td>&lt;String></td><td>Read-write</td><td>AAA username logging..</td></tr><tr><td>udppmtu</td><td>&lt;Integer></td><td>Read-write</td><td>IPFIX UDP Path MTU..</td></tr><tr><td>clienttrafficonly</td><td>&lt;String></td><td>Read-write</td><td>Log only client-side traffic..</td></tr><tr><td>securityinsighttraffic</td><td>&lt;String></td><td>Read-write</td><td>Stream Identifier Session Name logging..</td></tr><tr><td>httpcontenttype</td><td>&lt;String></td><td>Read-write</td><td>HTTP Content-Type header logging..</td></tr><tr><td>crvserver</td><td>&lt;ns_nonlbvserver_diagnostic[]></td><td>Read-write</td><td>Cache Redirection Vserver Diagnostic.</td></tr><tr><td>csvserver</td><td>&lt;ns_nonlbvserver_diagnostic[]></td><td>Read-write</td><td>Content switching vserver Diagnostic.</td></tr><tr><td>httpmethod</td><td>&lt;String></td><td>Read-write</td><td>HTTP Method logging..</td></tr><tr><td>httplocation</td><td>&lt;String></td><td>Read-write</td><td>HTTP Location header logging..</td></tr><tr><td>is_appflow_enabled</td><td>&lt;Boolean></td><td>Read-write</td><td>true if appflow is enabled at NetScaler.</td></tr><tr><td>identifiersessionname</td><td>&lt;String></td><td>Read-write</td><td>Stream Identifier Session Name logging..</td></tr><tr><td>connectionchaining</td><td>&lt;String></td><td>Read-write</td><td>Connection Chaining..</td></tr><tr><td>httpxforwardedfor</td><td>&lt;String></td><td>Read-write</td><td>HTTP X-Forwarded-For header logging..</td></tr><tr><td>appnamerefresh</td><td>&lt;Integer></td><td>Read-write</td><td>Appname refresh interval..</td></tr><tr><td>observationdomainname</td><td>&lt;String></td><td>Read-write</td><td>IPFIX Observation Domain Name..</td></tr><tr><td>identifiername</td><td>&lt;String></td><td>Read-write</td><td>Stream Identifier Name logging..</td></tr><tr><td>httpcookie</td><td>&lt;String></td><td>Read-write</td><td>HTTP COOKIE LOGGING..</td></tr><tr><td>httpurl</td><td>&lt;String></td><td>Read-write</td><td>HTTP URL logging..</td></tr><tr><td>httpuseragent</td><td>&lt;String></td><td>Read-write</td><td>HTTP User Agent Logging..</td></tr><tr><td>httphost</td><td>&lt;String></td><td>Read-write</td><td>HTTP Host logging..</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_insight_diagnostic

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_insight_diagnostic":[{
"httpreferer":<String_value>,
"templaterefresh":<Integer_value>,
"securityinsightrecordinterval":<Integer_value>,
"hostname":<String_value>,
"ns_ip_address":<String_value>,
"httpsetcookie":<String_value>,
"httpvia":<String_value>,
"lbvserver":[{
"appflowlog":<String_value>,
"name":<String_value>,
"servicegroup":[{
"appflowlog":<String_value>,
"name":<String_value>}],
"service":[{
"appflowlog":<String_value>,
"name":<String_value>}],
"appflow_policies":[{
"hits":<Double_value>,
"name":<String_value>,
"rule":<String_value>,
"traffic_flow":<Boolean_value>}],
"state":<String_value>}],
"httpdomain":<String_value>,
"httpsetcookie2":<String_value>,
"vpnvserver":[{
"appflowlog":<String_value>,
"name":<String_value>,
"appflow_policies":[{
"hits":<Double_value>,
"name":<String_value>,
"rule":<String_value>,
"traffic_flow":<Boolean_value>}],
"state":<String_value>}],
"flowrecordinterval":<Integer_value>,
"httpauthorization":<String_value>,
"skipcacheredirectionhttptransaction":<String_value>,
"aaausername":<String_value>,
"udppmtu":<Integer_value>,
"clienttrafficonly":<String_value>,
"securityinsighttraffic":<String_value>,
"httpcontenttype":<String_value>,
"crvserver":[{
"appflowlog":<String_value>,
"name":<String_value>,
"appflow_policies":[{
"hits":<Double_value>,
"name":<String_value>,
"rule":<String_value>,
"traffic_flow":<Boolean_value>}],
"state":<String_value>}],
"csvserver":[{
"appflowlog":<String_value>,
"name":<String_value>,
"appflow_policies":[{
"hits":<Double_value>,
"name":<String_value>,
"rule":<String_value>,
"traffic_flow":<Boolean_value>}],
"state":<String_value>}],
"httpmethod":<String_value>,
"httplocation":<String_value>,
"is_appflow_enabled":<Boolean_value>,
"identifiersessionname":<String_value>,
"connectionchaining":<String_value>,
"httpxforwardedfor":<String_value>,
"appnamerefresh":<Integer_value>,
"observationdomainname":<String_value>,
"identifiername":<String_value>,
"httpcookie":<String_value>,
"httpurl":<String_value>,
"httpuseragent":<String_value>,
"httphost":<String_value>}]}
```







