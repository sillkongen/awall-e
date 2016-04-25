# awall-e
Firewall update scripts for PF.

There are 4 scripts.

1 fwadd / Add an item to be on the permanent blocked list.

2 fwdel / Delete an item on the permanent blocked list.

3 fwprep / It scans /var/log/authlog and blocks all items that meet the following conditions which are the following:
  "Did not receive identification".
  "Bad protocol version identification"
  
4 fwlist / List all IP's that are blocked currently.

I copy all scripts to /usr/local/bin/fwlist and make the executable via chmod +x

*Add this your crontab entry to.
# Update FW blocking rules every 5 minutes
*/5 * * * * /usr/local/bin/fwprep

 
