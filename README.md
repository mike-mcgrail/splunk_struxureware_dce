# splunk_struxureware_dce
Splunk Add-On to Ingest Data from APC StruxureWare Data Center Expert

The add-on was built using the Splunk Add-On Builder.  The add-on makes calls to the DCE web services API.  The API returns SOAP envelopes; the Python scripts in the add-on manually parse the tags and return key-value pairs for writing to the Splunk index (the add-on is not necessary on the indexers or search head cluster).  At the time of this writing, alerts and devices are being retrieved.

Instructions:
1. Install add-on to heavy forwarder or Splunk Enterprise instance
2. Navigate to Configuration -> Account and enter API credentials
3. If a proxy is required, enter the details on the Proxy tab
4. On the Add-on Settings tab, enter the server and index the data will be written to
5. Navigate to inputs and click Create New Input to add alerts and/or devices
Note: device custom properties added in StruxureWare are not exposed to the API; only core device information is available.