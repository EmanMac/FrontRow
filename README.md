# FrontRow
## Prosody Chat Server

Prosody uses the XMPP protocol. Defined in [RFC 6120](https://tools.ietf.org/html/rfc6120) 

### Host Location

| Provider      | URL                     | IP             |
| ------------- |-------------------------| ---------------|
| DigitalOcean  | sootsplash.csci2461.com | 167.99.232.136 |

# Ports

| Ports            | TCP/UDP                  |         Specific Settings                |
| ---------------  | ------------------------ | ---------------------------------------- | 
| 5222/5223        | TCP                      | XMPP client                              |
| 5269             | TCP                      | XMPP server                              |
| 25565            | TCP                      | Java Server                   

# IPTable rules
1. -A INPUT -p tcp -m state --state NEW --dport 5222 -j ACCEPT
2. -A INPUT -p tcp -m state --state NEW --dport 5223 -j ACCEPT
3. -A INPUT -p tcp -m state --state NEW --dport 5269 -j ACCEPT
4. -A INPUT -p tcp -m state --state NEW --dport 25565 -j ACCEPT
