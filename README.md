# IOG-O365-AppMailRelay

Application Mail relay through Cisco Cloud solutions
IOG O365 Administration
===================================

# Overview
We now have a brand new Cloud hosted Application mail relay service with Cisco to replace the old on-prem infrastructure to securely support mail relay from applications for both inbound and outbound destinations. The reason for using a separate relay service vs using our O365 environment is that with O365, the security controls are based upon user and shared mailbox interaction. With the extremely high protection filters based upon user email, the generally plain text application mail would be severely filtered. The Cisco appliance has its own security filtering based upon the years of relay through the legacy environment.

The new Cisco solution has been architected to handle up to 1 million emails per day. LexisNexisRisk currently average around 500k emails per day

# Process
In order to relay mail internally and externally, please follow these steps:

Connect source servers to Appmail.risk.regn.net and Appmail-test.risk.regn.net on port 25
Point DEV/Test app to Appmail-test.risk.regn.net
Once confirmed working, point Prod to Appmail.risk.regn.net
If the app is external or not connecting through the appmail VIPs, you should use these hosts mx1.hc5030-60.iphmx.com mx2.hc5030-60.iphmx.com AND contact the messaging team know the NAT IP to allow connection


# Feature Requests
Please enter any feature requests into the issues section of this repository.

# Bugs
Please enter any bugs into the issues section of this repository.

# More Information
More information for the end-to-end process of application packaging can be found here https://reedelsevier.sharepoint.com/sites/OG-CoP-Cloud/SitePages/8wpjrztv.aspx

# Team
Craig Burnett, Operations Manager

Mark Davenport, Systems Engineer

Martin Stemerdink, Systems Engineer

Chris Beaver, Systems Engineer

# Dependancies
Cisco cloud service

https://dh5004-esa1.iphmx.com
https://dh5004-esa2.iphmx.com

Internal F5 (servername required)

DNS for relevant domain names

Appmail.risk.regn.net
Appmail-Test.risk.regn.net
Appmail-BCT.risk.regn.net
 

# Indicators
Availability - The service needs to be available 24 x 7 globally 365 days a year for internal and external mail to be successfully delivered

Response Time - 95% response

Accuracy - The accuracy of the service is important to the Business for large revenue based customer reports

# Objectives
Availability - 99% uptime 24/7 365 days

Response Time - 95%


# Agreements
Availability - 99%

Response Time - 95%
Accuracy - 98%

Indicator	SLA
Availability	99%
Response Time	95%
Accuracy	98%
