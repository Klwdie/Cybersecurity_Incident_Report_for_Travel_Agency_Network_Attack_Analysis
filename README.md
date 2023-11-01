# Cybersecurity Incident Report for Travel Agency: Network Attack Analysis

---

While working as a security analyst for a (*fictional*) travel agency that advertises sales and promotions on the company’s website, I received an automated alert from my monitoring system indicating a problem with the web server. Employees of the company regularly access the company’s sales webpage to search for vacation packages their customers might like, so any issues could have a financial impact. I attempted to visit the company’s website but received a connection timeout error message in my browser.

I launched a packet sniffer, **Wireshark**, to capture data packets in transit to and from the web server. The resulting logs revealed a large number of TCP SYN requests incoming from an unfamiliar IP address. Additionally, the web server appeared to be overwhelmed by the volume of incoming traffic and was losing its ability to respond to the abnormally large number of SYN requests. The server was suspected to be under attack by a malicious actor. 

*The Wireshark TCP/HTTP logs can be found in this repository.*

After reviewing the logs, I took the server offline temporarily so that the machine could recover and return to a normal operating status. Additionally, I configured the company’s firewall to block the malicious actor's IP address that was sending the abnormal number of SYN requests. *This IP blocking solution was temporary, as the attacker could spoof other IP addresses to get around this block.* During this period, I quickly alerted my manager about this problem and discussed the next steps to stop this attacker and prevent this problem from reoccurring. This included information regarding the type of attack discovered and how it was affecting the web server and employees. I have also written a follow-up report regarding this incident, including all related information. *This follow-up report can be found in this repository.*

---
