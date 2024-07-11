To forward all ports from the external IP address 111.223.52.180 to the internal IP address 192.168.10.10 on Windows Server 2022, you'll need to use a slightly different approach than the single port forwarding example you provided. Here's how you can do it:

1. Open an elevated Command Prompt or PowerShell as an administrator.

2. Use the following command to enable IPv4 forwarding:

```
netsh interface ipv4 set global forwarding=enabled
```

3. Use the Windows Firewall with Advanced Security to create a rule that allows all incoming traffic to the external IP. You can do this with the following PowerShell command:

```
New-NetFirewallRule -DisplayName "Allow All Inbound Traffic" -Direction Inbound -LocalAddress 111.223.52.180 -Action Allow
```

4. Set up NAT (Network Address Translation) using the following PowerShell commands:

```
Add-NetNatStaticMapping -ExternalIPAddress "111.223.52.180" -ExternalPort 0 -Protocol ALL -InternalIPAddress "192.168.10.10" -InternalPort 0 -NatName "AllPortForward"
```

This command will forward all protocols and ports from the external IP to the internal IP.

5. Enable NAT on the external interface (replace 'EXTERNAL_INTERFACE_NAME' with your actual interface name):

```
Add-NetNat -Name "NAT" -InternalIPInterfaceAddressPrefix "192.168.10.0/24"
```

Please note that forwarding all ports can be a security risk. It's generally recommended to only forward the specific ports you need. Also, make sure you have proper security measures in place on the internal server (192.168.10.10) as it will be exposed to all incoming traffic.

Would you like me to explain any part of this process in more detail?
