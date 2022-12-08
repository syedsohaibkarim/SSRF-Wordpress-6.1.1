# SSRF-Wordpress-6.1.1
#### Description (Authenticated SSRF)
A Server-Side Request Forgery (SSRF) attack involves an attacker abusing server functionality to access or modify resources. The attacker targets an application that supports data imports from URLs or allows them to read data from URLs. URLs can be manipulated, either by replacing them with new ones or by tampering with URL path traversal. Here in this case, after successful authentication, attacker can able to retrieve the True-IP of the hosting server, abuse the hosting server inducing the server in a way that it is requesting external server for HTTP & DNS requests. 
##### WordPress Version Affected. 6.1.1
##### Path. Dashboard --> Pages --> Add Media from the URL

### Security Risk
1.	The attacker can send forged request to the webserver that is vulnerable to SSRF and resides on either on same internal network or external network as the target server.
2.	The vulnerable webserver sends the attacker-controlled request to the victim’s server, bypassing the firewall.
3.	It can also be used to sent back the data to the attacker and can used to exfiltrate or infer this information.
