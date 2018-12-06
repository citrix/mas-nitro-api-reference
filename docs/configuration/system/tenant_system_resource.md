#tenant_system_resource



Configuration for System Resources available for a tenant resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>available_scu</td><td>&lt;Integer></td><td>Read-write</td><td>Available number of Symmetric Crypto Units.<br>Maximum value =</td></tr><tr><td>available_disk_size</td><td>&lt;Double></td><td>Read-write</td><td>Available disk size.</td></tr><tr><td>max_plt_bw</td><td>&lt;Integer></td><td>Read-write</td><td>Max Allowed Platinum bandwidth Mbps.</td></tr><tr><td>max_cpu_cores</td><td>&lt;Integer></td><td>Read-write</td><td>Maximum number of CPU Cores.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>max_scu</td><td>&lt;Integer></td><td>Read-write</td><td>Available number of Symmetric Crypto Units.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Id of the parent tenant.</td></tr><tr><td>max_disk_size</td><td>&lt;Double></td><td>Read-write</td><td>Maximum Disk Space.</td></tr><tr><td>max_instances</td><td>&lt;Integer></td><td>Read-write</td><td>Maximum number of Instances.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>available_acu</td><td>&lt;Integer></td><td>Read-write</td><td>Available number of Asymmetric Crypto Units.<br>Maximum value =</td></tr><tr><td>parent_name</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>available_instances</td><td>&lt;Integer></td><td>Read-write</td><td>Available number of instances.<br>Maximum value =</td></tr><tr><td>max_std_bw</td><td>&lt;Integer></td><td>Read-write</td><td>Max Allowed Standard bandwidth Mbps.</td></tr><tr><td>max_memory</td><td>&lt;Double></td><td>Read-write</td><td>Maximum Memory.</td></tr><tr><td>max_ent_bw</td><td>&lt;Integer></td><td>Read-write</td><td>Max Allowed Enterprise bandwidth Mbps.</td></tr><tr><td>available_ssl_cards</td><td>&lt;Integer></td><td>Read-write</td><td>Available number of SSL Cores.<br>Maximum value =</td></tr><tr><td>available_memory</td><td>&lt;Double></td><td>Read-write</td><td>Available memory.</td></tr><tr><td>max_ssl_cards</td><td>&lt;Integer></td><td>Read-write</td><td>Maximum number of SSL cores.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>available_cpu_cores</td><td>&lt;Integer></td><td>Read-write</td><td>Available number of CPU Cores.<br>Maximum value =</td></tr><tr><td>max_acu</td><td>&lt;Integer></td><td>Read-write</td><td>Available number of Asymmetric Crypto Units.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>max_pps</td><td>&lt;String></td><td>Read-only</td><td>Maximum PPS .</td></tr><tr><td>available_std_bw</td><td>&lt;Integer></td><td>Read-only</td><td>Available Standard bandwidth in Mbps.</td></tr><tr><td>available_pps</td><td>&lt;String></td><td>Read-only</td><td>Available PPS.</td></tr><tr><td>available_throughput</td><td>&lt;String></td><td>Read-only</td><td>Available Throughput in Mbps.</td></tr><tr><td>max_throughput</td><td>&lt;String></td><td>Read-only</td><td>Maximum Throughput in Mbps.</td></tr><tr><td>available_ent_bw</td><td>&lt;Integer></td><td>Read-only</td><td>Available Enterprise bandwidth in Mbps.</td></tr><tr><td>available_plt_bw</td><td>&lt;Integer></td><td>Read-only</td><td>Available Platinum bandwidth in Mbps.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



