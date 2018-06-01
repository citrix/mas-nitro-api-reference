#mas_service_license

Configuration for MAS Service License Information resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>entitlement_id</td><td>&lt;String></td><td>Read-write</td><td>Entitlement Id for the license file.</td></tr><tr><td>end_time</td><td>&lt;Double></td><td>Read-write</td><td>License expires at this timestamp.</td></tr><tr><td>customer_id</td><td>&lt;String></td><td>Read-write</td><td>Customer Id for the tenant who has purchased the license.</td></tr><tr><td>serial_numbers</td><td>&lt;String></td><td>Read-write</td><td>SerialNumbers.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key.</td></tr><tr><td>start_date</td><td>&lt;String></td><td>Read-write</td><td>Start date of license subscription.</td></tr><tr><td>entitlement_type</td><td>&lt;String></td><td>Read-write</td><td>Entitlement Type eg. ProductionTrial.</td></tr><tr><td>lic_type</td><td>&lt;Integer></td><td>Read-write</td><td>0 = Trial Period, 1 = Licensed, 2 = Grace period, 3 = Unlicensed, 4 = Canceled.</td></tr><tr><td>quantity</td><td>&lt;String></td><td>Read-write</td><td>Number of Licenses of the type purchased.</td></tr><tr><td>start_time</td><td>&lt;Double></td><td>Read-write</td><td>License validity starts from this timestamp.</td></tr><tr><td>approved</td><td>&lt;Boolean></td><td>Read-write</td><td>Approved.</td></tr><tr><td>product_sku</td><td>&lt;String></td><td>Read-write</td><td>Product SKU of the License which specifies the type of license : VIPs, Storage or ThirdParty VIPS.</td></tr><tr><td>end_date</td><td>&lt;String></td><td>Read-write</td><td>Expiry date of license subscription.</td></tr><tr><td>max_vips</td><td>&lt;String></td><td>Read-only</td><td>Maximum VIPs.</td></tr><tr><td>max_storage</td><td>&lt;String></td><td>Read-only</td><td>Maximum Storage for the license in GB.</td></tr><tr><td>max_tp_vservers</td><td>&lt;String></td><td>Read-only</td><td>Maximum Third Party Vservers.</td></tr><tr><td>days_to_expire</td><td>&lt;Integer></td><td>Read-only</td><td>Days to expire.</td></tr><tr><td>total_allowed_tp_vips</td><td>&lt;Integer></td><td>Read-only</td><td>Total Allowed Third Party Vservres.</td></tr><tr><td>total_allowed_vips</td><td>&lt;Integer></td><td>Read-only</td><td>Total Allowed VIPs.</td></tr><tr><td>entitled_db_storage</td><td>&lt;Integer></td><td>Read-only</td><td>Total entitled DB storage.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [UPDATE](#u)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mas_service_license
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mas_service_license":[{"entitlement_id":<String_value>,"end_time":<Double_value>,"customer_id":<String_value>,"serial_numbers":<String_value>,"id":<String_value>,"start_date":<String_value>,"entitlement_type":<String_value>,"lic_type":<Integer_value>,"max_vips":<String_value>,"quantity":<String_value>,"start_time":<Double_value>,"max_storage":<String_value>,"approved":<Boolean_value>,"product_sku":<String_value>,"end_date":<String_value>,"max_tp_vservers":<String_value>,"days_to_expire":<Integer_value>,"total_allowed_tp_vips":<Integer_value>,"total_allowed_vips":<Integer_value>,"entitled_db_storage":<Integer_value>}]}```



###update



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mas_service_license/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{mas_service_license:{"end_time":<Double_value>,"id":<String_value>,"entitlement_type":<String_value>,"lic_type":<Integer_value>,"start_time":<Double_value>,"end_date":<String_value>,"product_sku":<String_value>,"entitlement_id":<String_value>,"customer_id":<String_value>,"start_date":<String_value>,"serial_numbers":<String_value>,"quantity":<String_value>,"approved":<Boolean_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mas_service_license":[{"entitlement_id":<String_value>,"end_time":<Double_value>,"customer_id":<String_value>,"serial_numbers":<String_value>,"id":<String_value>,"start_date":<String_value>,"entitlement_type":<String_value>,"lic_type":<Integer_value>,"max_vips":<String_value>,"quantity":<String_value>,"start_time":<Double_value>,"max_storage":<String_value>,"approved":<Boolean_value>,"product_sku":<String_value>,"end_date":<String_value>,"max_tp_vservers":<String_value>,"days_to_expire":<Integer_value>,"total_allowed_tp_vips":<Integer_value>,"total_allowed_vips":<Integer_value>,"entitled_db_storage":<Integer_value>}]}```



