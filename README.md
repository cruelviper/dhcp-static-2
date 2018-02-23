Statische IPv4-Vergabe im FFSH-DHCP

!!!IPv6 bitte bevorzugt verwenden!!!

Statische IPs muessen im Netz 10.144.1.0/21 sein!

Bitte Pull-Requests schicken!

Wenn ihr auch statische IPs an eure MAC gebunden haben wollt, macht einen fork, fuegt euch in die static.conf hinzu (nach IP sortiert!) und macht einen pull-request.




Anleitung fürs Gateway:

useradd -m -s /bin/bash dhcpstatic

cd /home/dhcpstatic

su dhcpstatic

git clone https://github.com/ffsh/dhcp-static.git

chmod +x dhcp-static/updateStatics.sh

exit

/home/dhcpstatic/dhcp-static/updateStatics.sh

*/5 * * * * root /home/dhcpstatic/dhcp-static/updateStatics.sh > /dev/null 2>&1
