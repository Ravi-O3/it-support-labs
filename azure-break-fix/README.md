# Azure Break/Fix Lab

A small Windows Server environment in Azure, built to practise real technical support work and security monitoring.

## Environment

| Item | Value |
|---|---|
| Server | SUPPORT-SRV01, Windows Server 2022 Datacenter: Azure Edition |
| Web | IIS with a test site on DefaultAppPool |
| Database | SQL Server Express (instance SQLEXPRESS) with a SupportLab database |
| Access | RDP allowed from my own IP only through a network security group rule |
| Monitoring | Log Analytics workspace with Microsoft Sentinel, Windows Security Events through the Azure Monitor Agent |
| Cost controls | Budget alerts at 50% and 90%, VM auto-shutdown |

## Tickets

| # | Ticket | Root cause |
|---|---|---|
| 1 | [Website returns HTTP 503](tickets/Ticket01-iis-503.md) | IIS application pool stopped |
| 2 | [External users cannot reach the web server on port 80](tickets/Ticket02-firewall-port-80.md) | Windows Defender Firewall block rule |
| 3 | [SQL Server refuses TCP connections](tickets/Ticket03-sql-tcp-1433.md) | TCP/IP protocol disabled in SQL Server Express |

## Detection

[kql/4625-failed-logons.kql](kql/4625-failed-logons.kql) hunts for repeated failed logons (Event ID 4625, MITRE ATT&CK T1110) in Microsoft Sentinel.
