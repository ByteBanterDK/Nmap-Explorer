<h1>Nmap Demonstration</h1>
<h2>Description:</h2>
Nmap (Network Mapper) is a powerful open-source network scanning tool used for discovering hosts and services on a computer network, thus creating a "map" of the network's topology. It offers a wide range of features for network reconnaissance, security auditing, and vulnerability assessment.

<h2>Key Objectives:</h2>
Perform network scans to identify active hosts and open ports.
Conduct OS detection to determine the operating systems of target hosts.
Explore various scanning techniques and Nmap options to gather comprehensive network information.
Utilize Nmap's scripting engine for vulnerability detection and service enumeration.
Understand the importance of root access in executing certain Nmap commands effectively.
<h2>Utilities Used:</h2>
Nmap: The primary tool for network scanning and reconnaissance.
Kali Linux Terminal: Provides an environment for executing Nmap commands.
Windows OS: Target machine for network scans.
<h2>Environments Used:</h2>
Operating Systems: Kali Linux, Windows
Hardware: Virtual Machines
Tools: Nmap, Terminal
<h2>Program Walk-through:</h2>
Login as Root:
<img src="https://i.imgur.com/1DsWp0p.png">
Root access is essential when using Nmap or the Kali Linux terminal because many Nmap commands require elevated privileges to access and manipulate network resources effectively, and seen in the screenshot we're using a windows OS on a virtual box to scan the computer ip address. 
Finding Windows Machine IP Address:
<img src="https://i.imgur.com/6BMCsJA.png">
Use the ipconfig command on the Windows machine to determine its IP address.
Executing Nmap Commands:
<img src="https://i.imgur.com/tWlGZc7.png"> <img src="https://i.imgur.com/O7xLSlt.png">
nmap -O -d -v 192.168.0.92: Performs aggressive OS detection with debugging and verbose output on the target IP address 192.168.0.92.
nmap -Sp 192.168.0.92/24: Conducts a ping scan on the specified subnet to identify responsive hosts.
<img src="https://i.imgur.com/LmI9vK0.png"> <img src="https://i.imgur.com/gOxgAUH.png">
nmap -sS 192.168.0.92: Initiates a SYN scan to determine open ports on the target system.
<img src="https://i.imgur.com/6HJPJJM.png">
nmap -p 80 192.168.0.92: Scans port 80 on the target machine to check for HTTP service availability, however you could input any ports but for this demonstration it's "80".
<img src="https://i.imgur.com/6HJPJJM.png">
nmap --script vuln 192.168.0.92: Utilizes Nmap's scripting engine to perform vulnerability detection on the target.
<img src="https://i.imgur.com/r9MSaxx.png">
Basic Nmap Commands:
nmap -sP <target>: Ping scan to check which hosts are up.
nmap -sV <target>: Version detection scan to determine service versions.
nmap -A <target>: Aggressive scan with OS detection, version detection, script scanning, and traceroute.
