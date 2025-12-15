## Objective
Analyze HTTP traffic from a real-world PCAP to identify unencrypted communication.

## PCAP Used
pcaps/http-sample.pcapng

## Filters Applied
- http
- tcp.port == 80

## Findings
- Client IP: 10.6.13.133
- Server IP: 10.6.13.129
- HTTP POST request observed
- Clear-text data visible in TCP stream

## Security Impact
Unencrypted HTTP traffic exposes sensitive information to attackers.

## Conclusion
HTTPS should be enforced to protect data confidentiality.

