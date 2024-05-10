<h1>Wireshark- Packet Capture </h1>

<h2>Description</h2>
Project consists of downloading current operating system version of Wireshark. Learn to execute packet capture on an wireless port and save it to file. Use a display filter to detect HTTPS packets. Visit a web page and detect its IP address using a display filter. End with locating all HTTPS packets from a capture not containing a certain IP address:



<br />


<h2>Operating System Used<h2>

- <b>MacOS Monterey Version 12.7.4</b>

<h2>Downloads<h2>
 
- <b>[Wireshark 4.2.4 Intel](https://www.wireshark.org/)</b>

<h2>Project walk-through:</h2>

<p align="center">
Download Wireshark: <br/>
<img src="https://i.imgur.com/tJvjb7u.png" height="80%" width="80%" />
<br />
<br />
Select source of capture: Wireless, Ethernet etc: <br/>
<img src="https://i.imgur.com/aW7aT8R.png" height="80%" width="80%" />
<br />
<br />
Upper left click -green- "sharkfin" to begin your capture: <br/>
<img src="https://i.imgur.com/L84dc7r.png" height="80%" width="80%" />
<br />
<br />
Stop your capture with -red- box and save to your file of choosing:  <br/>
<img src="https://i.imgur.com/iSeAtMG.png" height="80%" width="80%" />
<br />
<br />
Use a display filter to detect HTTPS packets:  <br/>
 ●To display certain packets in an existing packet capture, use a display filter <br/>
 ●To display only HTTPS traffic, use a filter on TCP port 443: tcp.port == 443 <br/>
<img src="https://i.imgur.com/oMqtdb8.png" height=80%" width="80%" />
<br />
<br />
Use a display filter to detect DNS (Domain Name System)if websites and subsites visited:  <br/>
<img src="https://i.imgur.com/c290sSx.png" height="80%" width="80%" />
<br />
 - <b>https://wiki.wireshark.org/DisplayFilters
<br />
<br />
Once message “Elastic Agent has been successfully installed.” It will automatically start collecting and forwarding logs to your Elastic SIEM  <br/>
<img src="https://i.imgur.com/AW19rNt.png" height="80%" width="80%" />
<br />
<br />
Verify that the agent has been installed correctly by running this command: sudo systemctl status elastic-agent.service  <br/>
<img src="https://i.imgur.com/BSbRH5o.png" height="80%" width="80%" />
<br />
<br />
Create Security Events by using "Nmap" (“nmap -sS <ip address>”, “nmap -sT <ip address>”, “nmap -p- <ip address>”etc..) <br/>
<img src="https://i.imgur.com/zCVJzfU.png" height="80%" width="80%" />
<br />
<br />
Navigate to "Logs" in Elastic to view logs fron Kali VM  <br/>
<img src="https://i.imgur.com/aj1TnOD.png" height="80%" width="80%" />
<br />
<br />
Filter the results by using "Search"  <br/>
<img src="https://i.imgur.com/byjLPJn.png" height="80%" width="80%" />
<br />
<br />
Click on the menu icon on the top-left, then under “Analytics,” click on “Dashboards.” -> Create a Dashboard to Visualize the Events  <br/>
<img src="https://i.imgur.com/BPXi94a.png" height="80%" width="80%" />
<br />
<br />
Click on the “Create Visualization” button to add a new visualization to the dashboard <br/>
Select “Area” or “Line” as the visualization type. This will create a chart that shows the count of events over time. <br/>
In the “Metrics” section, select “Count” as the vertical field type and “Timestamp” for the horizontal field. This will show the count of events over time. <br/>
<br />
<br /> 
Click on the “Save” button to save the visualization and then complete the rest of the settings. <br/>
<img src="https://i.imgur.com/3CYbLef.png" height="80%" width="80%" />
<br />
<br /> 
Set an "ALERT" -> Click on the menu icon on the top-left, then under “Security,” click on “Alerts.” <br>
<img src="https://i.imgur.com/FC6LSnF.png" height="80%" width="80%" />" 
<br />
<br /> 
Click on the “Create new rule” button at the top right <br>
Under the “Define rule” section, select the “Custom query” option from the dropdown menu <br>
Under “Custom query,” set the conditions for the rule <br>
Set the severity level for the alert. Keep all the other default settings under “Schedule rule” and click “Continue.” <br>
<br />
<br /> 
Finally, click the “Create and enable rule” button to create the alert. Once you’ve created the alert, it will monitor your logs for Nmap scan events <br>
<img src="https://i.imgur.com/YaLzbD3.png" height="80%" width="80%" />" 






