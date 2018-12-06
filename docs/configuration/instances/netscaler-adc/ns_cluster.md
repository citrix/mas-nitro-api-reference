#ns_cluster



Configuration for ns_cluster resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>add_nodegroup</td><td>&lt;Boolean></td><td>Read-write</td><td>Add Node group in cluster instance if this property is true.</td></tr><tr><td>backplane</td><td>&lt;String></td><td>Read-write</td><td>Backplane Interface.</td></tr><tr><td>clusterid</td><td>&lt;Integer></td><td>Read-write</td><td>Cluster Id.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>nodeid</td><td>&lt;Integer></td><td>Read-write</td><td>Node Id.<br>Maximum value =</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Node State.<br>Minimum length = 1<br>Maximum length = 32</td></tr><tr><td>channel_interface_list</td><td>&lt;ns_clag_node[]></td><td>Read-write</td><td>Array of CLAG nodes that are part of this channel (10/1, 10/4).</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Password of the Configuration Coordinator node(Cluster IP).<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>clag_intf_list</td><td>&lt;String[]></td><td>Read-write</td><td>CLAG Interface List containing interfaces which aren't shared across nodes and aren't backplanes.</td></tr><tr><td>process_local</td><td>&lt;Boolean></td><td>Read-write</td><td>Process Local.</td></tr><tr><td>clviewleader</td><td>&lt;String></td><td>Read-write</td><td>Cluster CCO NSIP.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>inc_mode</td><td>&lt;Boolean></td><td>Read-write</td><td>Inc Mode.</td></tr><tr><td>clnumnodes</td><td>&lt;Integer></td><td>Read-write</td><td>Cluster ID.<br>Maximum value =</td></tr><tr><td>scheduleId</td><td>&lt;String></td><td>Read-write</td><td>scheduleId is used to refer maintenaince schedule task.</td></tr><tr><td>clnodes</td><td>&lt;String></td><td>Read-write</td><td>List of Nodes part of Cluster.</td></tr><tr><td>preemption</td><td>&lt;Boolean></td><td>Read-write</td><td>Preemption.</td></tr><tr><td>iscco</td><td>&lt;Boolean></td><td>Read-write</td><td>Is CCO.</td></tr><tr><td>clip</td><td>&lt;String></td><td>Read-write</td><td>Cluster IPAddress.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>node_group</td><td>&lt;String></td><td>Read-write</td><td>Node group.</td></tr><tr><td>nodegroup_list</td><td>&lt;String[]></td><td>Read-write</td><td>Available Node group list on this cluster.</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>NS ipaddress.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>profile_name</td><td>&lt;String></td><td>Read-write</td><td>Profile Name.<br>Maximum length = 128</td></tr><tr><td>mgmt_cpu_usage</td><td>&lt;Double></td><td>Read-only</td><td>Management CPU Usage (%) of Cluster Instance.</td></tr><tr><td>totpropagationtimeout</td><td>&lt;Double></td><td>Read-only</td><td>Number of times the update to the client timed-out.</td></tr><tr><td>totsteeredpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of packets steered on the cluster backplane.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr><tr><td>numdfddroppkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of packets steered on the cluster backplane.</td></tr><tr><td>http_req</td><td>&lt;Double></td><td>Read-only</td><td>HTTP Requests/second on Cluster Instance.</td></tr><tr><td>cpu_usage</td><td>&lt;Double></td><td>Read-only</td><td>CPU Usage (%) of Cluster Instance.</td></tr><tr><td>clbkplanerx</td><td>&lt;Double></td><td>Read-only</td><td>Traffic received on backplane (in mbits).</td></tr><tr><td>clbkplanetx</td><td>&lt;Double></td><td>Read-only</td><td>Traffic transmitted from backplane (in mbits).</td></tr><tr><td>operationalstate</td><td>&lt;String></td><td>Read-only</td><td>Cluster Operational State.</td></tr><tr><td>tx</td><td>&lt;Double></td><td>Read-only</td><td>Out Throughput of Cluster Instance in Mbps.</td></tr><tr><td>clcurstatus</td><td>&lt;String></td><td>Read-only</td><td>State of the cluster.</td></tr><tr><td>rx</td><td>&lt;Double></td><td>Read-only</td><td>In Throughput of Cluster Instance in Mbps.</td></tr><tr><td>memory_usage</td><td>&lt;Double></td><td>Read-only</td><td>Memory Usage (%) of Cluster Instance.</td></tr><tr><td>clbkplanetxrate</td><td>&lt;Double></td><td>Read-only</td><td>Traffic rate transmitted from backplane (in mbits).</td></tr><tr><td>health</td><td>&lt;String></td><td>Read-only</td><td>Node Health State.</td></tr><tr><td>clbkplanerxrate</td><td>&lt;Double></td><td>Read-only</td><td>Traffic rate received on backplane (in mbits).</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[REMOVE](#r)| [GET (ALL)](#get-all)| [MODIFY_PASSWORD](#modify_pas)| [FORM_CLUSTER](#form_cl)| [JOIN]()





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###remove







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_cluster?action=remove;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_cluster: {
<b>"ipaddress":<String_value></b>,
"add_nodegroup":<Boolean_value>,
"clusterid":<Integer_value>,
"backplane":<String_value>,
"nodeid":<Integer_value>,
"clnodes":<String_value>,
"state":<String_value>,
"channel_interface_list":[{
"nodeid":<Integer_value>,
"parent_id":<String_value>,
"id":<String_value>,
"interface_name":<String_value>,
"local_node":<Boolean_value>,
"parent_name":<String_value>}],
"preemption":<Boolean_value>,
"password":<String_value>,
"clip":<String_value>,
"iscco":<Boolean_value>,
"process_local":<Boolean_value>,
"clag_intf_list":<String_value[]>,
"clviewleader":<String_value>,
"inc_mode":<Boolean_value>,
"clnumnodes":<Integer_value>,
"node_group":<String_value>,
"scheduleId":<String_value>,
"nodegroup_list":<String_value[]>,
"profile_name":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_cluster":[{
"add_nodegroup":<Boolean_value>,
"mgmt_cpu_usage":<Double_value>,
"backplane":<String_value>,
"clusterid":<Integer_value>,
"nodeid":<Integer_value>,
"state":<String_value>,
"channel_interface_list":[{
"local_node":<Boolean_value>,
"interface_name":<String_value>,
"parent_name":<String_value>,
"nodeid":<Integer_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"totpropagationtimeout":<Double_value>,
"totsteeredpkts":<Double_value>,
"password":<String_value>,
"clag_intf_list":<String_value>,
"process_local":<Boolean_value>,
"act_id":<String_value>,
"numdfddroppkts":<Double_value>,
"clviewleader":<String_value>,
"inc_mode":<Boolean_value>,
"clnumnodes":<Integer_value>,
"http_req":<Double_value>,
"scheduleId":<String_value>,
"sync_operation":<Boolean_value>,
"cpu_usage":<Double_value>,
"clbkplanerx":<Double_value>,
"clnodes":<String_value>,
"clbkplanetx":<Double_value>,
"preemption":<Boolean_value>,
"iscco":<Boolean_value>,
"clip":<String_value>,
"operationalstate":<String_value>,
"tx":<Double_value>,
"clcurstatus":<String_value>,
"rx":<Double_value>,
"memory_usage":<Double_value>,
"node_group":<String_value>,
"clbkplanetxrate":<Double_value>,
"health":<String_value>,
"clbkplanerxrate":<Double_value>,
"nodegroup_list":<String_value>,
"ipaddress":<String_value>,
"profile_name":<String_value>}]}
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_cluster

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_cluster":[{
"add_nodegroup":<Boolean_value>,
"mgmt_cpu_usage":<Double_value>,
"backplane":<String_value>,
"clusterid":<Integer_value>,
"nodeid":<Integer_value>,
"state":<String_value>,
"channel_interface_list":[{
"local_node":<Boolean_value>,
"interface_name":<String_value>,
"parent_name":<String_value>,
"nodeid":<Integer_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"totpropagationtimeout":<Double_value>,
"totsteeredpkts":<Double_value>,
"password":<String_value>,
"clag_intf_list":<String_value>,
"process_local":<Boolean_value>,
"act_id":<String_value>,
"numdfddroppkts":<Double_value>,
"clviewleader":<String_value>,
"inc_mode":<Boolean_value>,
"clnumnodes":<Integer_value>,
"http_req":<Double_value>,
"scheduleId":<String_value>,
"sync_operation":<Boolean_value>,
"cpu_usage":<Double_value>,
"clbkplanerx":<Double_value>,
"clnodes":<String_value>,
"clbkplanetx":<Double_value>,
"preemption":<Boolean_value>,
"iscco":<Boolean_value>,
"clip":<String_value>,
"operationalstate":<String_value>,
"tx":<Double_value>,
"clcurstatus":<String_value>,
"rx":<Double_value>,
"memory_usage":<Double_value>,
"node_group":<String_value>,
"clbkplanetxrate":<Double_value>,
"health":<String_value>,
"clbkplanerxrate":<Double_value>,
"nodegroup_list":<String_value>,
"ipaddress":<String_value>,
"profile_name":<String_value>}]}
```







###modify_password







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_cluster?action=modify_password;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_cluster: {
<b>"ipaddress":<String_value></b>,
"add_nodegroup":<Boolean_value>,
"clusterid":<Integer_value>,
"backplane":<String_value>,
"nodeid":<Integer_value>,
"clnodes":<String_value>,
"state":<String_value>,
"channel_interface_list":[{
"nodeid":<Integer_value>,
"parent_id":<String_value>,
"id":<String_value>,
"interface_name":<String_value>,
"local_node":<Boolean_value>,
"parent_name":<String_value>}],
"preemption":<Boolean_value>,
"password":<String_value>,
"clip":<String_value>,
"iscco":<Boolean_value>,
"process_local":<Boolean_value>,
"clag_intf_list":<String_value[]>,
"clviewleader":<String_value>,
"inc_mode":<Boolean_value>,
"clnumnodes":<Integer_value>,
"node_group":<String_value>,
"scheduleId":<String_value>,
"nodegroup_list":<String_value[]>,
"profile_name":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_cluster":[{
"add_nodegroup":<Boolean_value>,
"mgmt_cpu_usage":<Double_value>,
"backplane":<String_value>,
"clusterid":<Integer_value>,
"nodeid":<Integer_value>,
"state":<String_value>,
"channel_interface_list":[{
"local_node":<Boolean_value>,
"interface_name":<String_value>,
"parent_name":<String_value>,
"nodeid":<Integer_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"totpropagationtimeout":<Double_value>,
"totsteeredpkts":<Double_value>,
"password":<String_value>,
"clag_intf_list":<String_value>,
"process_local":<Boolean_value>,
"act_id":<String_value>,
"numdfddroppkts":<Double_value>,
"clviewleader":<String_value>,
"inc_mode":<Boolean_value>,
"clnumnodes":<Integer_value>,
"http_req":<Double_value>,
"scheduleId":<String_value>,
"sync_operation":<Boolean_value>,
"cpu_usage":<Double_value>,
"clbkplanerx":<Double_value>,
"clnodes":<String_value>,
"clbkplanetx":<Double_value>,
"preemption":<Boolean_value>,
"iscco":<Boolean_value>,
"clip":<String_value>,
"operationalstate":<String_value>,
"tx":<Double_value>,
"clcurstatus":<String_value>,
"rx":<Double_value>,
"memory_usage":<Double_value>,
"node_group":<String_value>,
"clbkplanetxrate":<Double_value>,
"health":<String_value>,
"clbkplanerxrate":<Double_value>,
"nodegroup_list":<String_value>,
"ipaddress":<String_value>,
"profile_name":<String_value>}]}
```







###form_cluster







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_cluster?action=form_cluster;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_cluster: {
<b>"ipaddress":<String_value></b>,
"add_nodegroup":<Boolean_value>,
"clusterid":<Integer_value>,
"backplane":<String_value>,
"nodeid":<Integer_value>,
"clnodes":<String_value>,
"state":<String_value>,
"channel_interface_list":[{
"nodeid":<Integer_value>,
"parent_id":<String_value>,
"id":<String_value>,
"interface_name":<String_value>,
"local_node":<Boolean_value>,
"parent_name":<String_value>}],
"preemption":<Boolean_value>,
"password":<String_value>,
"clip":<String_value>,
"iscco":<Boolean_value>,
"process_local":<Boolean_value>,
"clag_intf_list":<String_value[]>,
"clviewleader":<String_value>,
"inc_mode":<Boolean_value>,
"clnumnodes":<Integer_value>,
"node_group":<String_value>,
"scheduleId":<String_value>,
"nodegroup_list":<String_value[]>,
"profile_name":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_cluster":[{
"add_nodegroup":<Boolean_value>,
"mgmt_cpu_usage":<Double_value>,
"backplane":<String_value>,
"clusterid":<Integer_value>,
"nodeid":<Integer_value>,
"state":<String_value>,
"channel_interface_list":[{
"local_node":<Boolean_value>,
"interface_name":<String_value>,
"parent_name":<String_value>,
"nodeid":<Integer_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"totpropagationtimeout":<Double_value>,
"totsteeredpkts":<Double_value>,
"password":<String_value>,
"clag_intf_list":<String_value>,
"process_local":<Boolean_value>,
"act_id":<String_value>,
"numdfddroppkts":<Double_value>,
"clviewleader":<String_value>,
"inc_mode":<Boolean_value>,
"clnumnodes":<Integer_value>,
"http_req":<Double_value>,
"scheduleId":<String_value>,
"sync_operation":<Boolean_value>,
"cpu_usage":<Double_value>,
"clbkplanerx":<Double_value>,
"clnodes":<String_value>,
"clbkplanetx":<Double_value>,
"preemption":<Boolean_value>,
"iscco":<Boolean_value>,
"clip":<String_value>,
"operationalstate":<String_value>,
"tx":<Double_value>,
"clcurstatus":<String_value>,
"rx":<Double_value>,
"memory_usage":<Double_value>,
"node_group":<String_value>,
"clbkplanetxrate":<Double_value>,
"health":<String_value>,
"clbkplanerxrate":<Double_value>,
"nodegroup_list":<String_value>,
"ipaddress":<String_value>,
"profile_name":<String_value>}]}
```







###join







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_cluster?action=join;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_cluster: {
<b>"ipaddress":<String_value></b>,
"add_nodegroup":<Boolean_value>,
"clusterid":<Integer_value>,
"backplane":<String_value>,
"nodeid":<Integer_value>,
"clnodes":<String_value>,
"state":<String_value>,
"channel_interface_list":[{
"nodeid":<Integer_value>,
"parent_id":<String_value>,
"id":<String_value>,
"interface_name":<String_value>,
"local_node":<Boolean_value>,
"parent_name":<String_value>}],
"preemption":<Boolean_value>,
"password":<String_value>,
"clip":<String_value>,
"iscco":<Boolean_value>,
"process_local":<Boolean_value>,
"clag_intf_list":<String_value[]>,
"clviewleader":<String_value>,
"inc_mode":<Boolean_value>,
"clnumnodes":<Integer_value>,
"node_group":<String_value>,
"scheduleId":<String_value>,
"nodegroup_list":<String_value[]>,
"profile_name":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_cluster":[{
"add_nodegroup":<Boolean_value>,
"mgmt_cpu_usage":<Double_value>,
"backplane":<String_value>,
"clusterid":<Integer_value>,
"nodeid":<Integer_value>,
"state":<String_value>,
"channel_interface_list":[{
"local_node":<Boolean_value>,
"interface_name":<String_value>,
"parent_name":<String_value>,
"nodeid":<Integer_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"totpropagationtimeout":<Double_value>,
"totsteeredpkts":<Double_value>,
"password":<String_value>,
"clag_intf_list":<String_value>,
"process_local":<Boolean_value>,
"act_id":<String_value>,
"numdfddroppkts":<Double_value>,
"clviewleader":<String_value>,
"inc_mode":<Boolean_value>,
"clnumnodes":<Integer_value>,
"http_req":<Double_value>,
"scheduleId":<String_value>,
"sync_operation":<Boolean_value>,
"cpu_usage":<Double_value>,
"clbkplanerx":<Double_value>,
"clnodes":<String_value>,
"clbkplanetx":<Double_value>,
"preemption":<Boolean_value>,
"iscco":<Boolean_value>,
"clip":<String_value>,
"operationalstate":<String_value>,
"tx":<Double_value>,
"clcurstatus":<String_value>,
"rx":<Double_value>,
"memory_usage":<Double_value>,
"node_group":<String_value>,
"clbkplanetxrate":<Double_value>,
"health":<String_value>,
"clbkplanerxrate":<Double_value>,
"nodegroup_list":<String_value>,
"ipaddress":<String_value>,
"profile_name":<String_value>}]}
```







