# Demo: Ops Challenge - Automated Endpoint Configuration

```powershell
# Allow ICMP reply in Powershell

netsh advfirewall firewall add rule name="ICMP Allow incoming V4 echo request" protocol=icmpv4:8,any dir=in action=allow
```
