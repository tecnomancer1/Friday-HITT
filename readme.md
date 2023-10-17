IP Ranges
Name	CIDR Block	Availability zone	Description
VPC	10.0.0.0/16		Default VPC for stack
PublicSubnet1	10.0.0.0/24	Eu-west-1a	Public subnet for webservers
PublicSubnet2	10.0.1.0/24	Eu-west-1b	Public subnet for webservers and jumpbox
PrivateSubnet1	10.0.2.0/24	Eu-west-1a	Private subnet for database servers
PrivateSubnet1	10.0.3.0/24	Eu-west-1b	Private subnet for database servers


Protocols and Ports
Protocol	Port	Security Group	Notes
HTTP	80	WebSecurityGroup	HTTP access to the web servers from the public internet
TCP	22	JumpboxSecurityGroup	SSH access to/from the jumpbox instance for administration and management
TCP	22	WebSecurityGroup 	SSH access to the web server instances for administration and management
TCP	22	DatabaseSecurityGroup	SSH access to the database server instances for administration and management
TCP	3306	DatabaseSecurityGroup	|MySQL/MariaDB database access from the web server for application data retrieval and storage
ICMP	-1	WebSecurityGroup	Allows all ICMP types and codes for diagnostic and troubleshooting purposes.
ICMP	-1	DatabaseSecurityGroup	Allows all ICMP types and codes for diagnostic and troubleshooting purposes.
ICMP	-1	JumpboxSecurityGroup	Allows all ICMP types and codes for diagnostic and troubleshooting purposes.

