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
- Destination Port: 5357
- HTTP POST request observed
- Application data transmitted as SOAP/XML
- Clear-text data visible after reconstructing traffic using Follow TCP Stream

## Security Impact
Unencrypted HTTP traffic exposes sensitive information to attackers through packet sniffing and man-in-the-middle attacks.

## Evidence
- TCP stream screenshot: screenshots/http-stream.png

## Conclusion
HTTPS should be enforced to protect data confidentiality and prevent information disclosure.
