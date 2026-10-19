# Active Directory Lab

An Active Directory domain on Windows Server 2022 in Azure, used to work common help desk tickets: domain join, account lockouts, remote access, file share permissions and Group Policy.

## Environment

| Item | Value |
|---|---|
| Domain | corp.ravilab.internal (NetBIOS RAVILAB) |
| Domain controller | DC01, Windows Server 2022, AD DS and DNS, static private IP 172.16.0.5, no public IP |
| Member server | SUPPORT-SRV01, 172.16.0.4 |
| Access | DC01 is reached only by RDP from SUPPORT-SRV01 over the private network |
| DNS | Virtual network DNS points to DC01, DC01 forwards everything else to Azure DNS (168.63.129.16) |

## Tickets

| # | Ticket | Root cause |
|---|---|---|
| 1 | [SUPPORT-SRV01 cannot join the domain](tickets/Ticket01-domain-join.md) | Virtual network still using Azure-provided DNS instead of the domain controller |

More tickets are added here as each one is finished.
