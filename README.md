# Data Overview

Data was collected on our Cowrie honeypot from April 15th 2025 until July 7, 2025. IP's and hashes were checked mainly using virustotal.com with backup information and checks coming from useipdb.com, ipinfo.io, and ipqualityscore.com.

#### Session ID:
Unique Identifier for that users session within the honeypot.
#### Src IP (anonymized):	
The users IP which was anonymized using Crypto-PAn techniques.
#### Src Port:	
The users source port
#### Dst IP:		
The ip of the honeypot the user is accessing
#### Dst Port:		
The port of the honeypot the user is accessing
#### Protocol:	
Which protocol the user used to connect to the honeypot
#### Timestamp Start:		
When the session started
#### Timestamp End:		
When the session ended
#### Event Count:		
How many messages were sent during the session
#### Username(s):		
If the user tried to input any user names
#### Password(s):		
If the user tried to input any passwords
#### Commands:
If the user tried to input any commands
#### Uploaded Files:		
If the user tried to upload any files
#### File Hashes (anonymized):		
Any possible file hashes from uploaded files
#### Messages (anonymized):		
All of the messages that were sent in the session
#### Threat Labels:		
Any threat labels that come from the sources listed above
* Sometimes a threat label may appear although the reputation score is 0 this is because threat labels comes from over 90+ vendors and the reputation comes from community reports * 
#### Reputation Score:		
Reputation score coming from community reports across sources listed above
#### Geo Location:	
Location of the user's IP
#### ISP:		
Internet Service Provider of the user
#### SSH Version:		
Which SSH version the user used
#### SSH Fingerprint:		
The fingerprint of the user's SSH
#### Malicious:	
A score of 1 represents malicious which is given to those who try to insert a username of 'root' or have a reputation score of greater than 50 while a score of 0 represents benign.
