# War Room Network Design

Request: DEPO-2026-001

## Proposed Networks
VLAN 10: Staff - 192.168.10.0/24
VLAN 20: Guest - 192.168.20.0/24
VLAN 30: AV - 192.168.30.0/24

## Security Requirements
- Guest traffic isolated from staff and AV networks
- Staff-to-AV access limited to required services
- Strong Wi-Fi authentication
- Firewall enabled
- No inbound internet access unless explicitly required

## Planned Validation
- DHCP address assignment
- DNS resolution
- Internet connectivity
- Video conferencing connectivity
- Packet loss and latency checks
- Print and scan functionality
- Guest isolation verification

## Incident Scenario
At 9:40 AM, a remote attorney cannot join the
10:00 AM deposition.

The technician must identify the failure,
restore connectivity, and document the incident.

All network configuration is proposed or simulated
until explicitly deployed and tested.
