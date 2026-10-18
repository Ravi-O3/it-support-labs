# IT Support Labs

Hands-on labs where I build Windows Server environments in Microsoft Azure, break them on purpose, and fix them the way a service desk or technical support analyst would. Every ticket is written up with the reported problem, what I checked, the root cause, the fix and how I verified it.

## Labs

| Lab | What it covers | Status |
|---|---|---|
| [azure-break-fix](azure-break-fix/) | IIS, Windows Defender Firewall, SQL Server Express, Microsoft Sentinel and KQL | Tickets 1 to 3 published |
| [active-directory](active-directory/) | Active Directory Domain Services, DNS, Group Policy, share and NTFS permissions, PowerShell | In progress |

## Tickets

| # | Ticket | Area |
|---|---|---|
| 1 | [Website returns HTTP 503](azure-break-fix/tickets/Ticket01-iis-503.md) | IIS application pools |
| 2 | [External users cannot reach the web server on port 80](azure-break-fix/tickets/Ticket02-firewall-port-80.md) | Windows Defender Firewall, Azure NSG |
| 3 | [SQL Server refuses TCP connections](azure-break-fix/tickets/Ticket03-sql-tcp-1433.md) | SQL Server network configuration |

New tickets are added here as each one is finished.

## Tools

Azure Virtual Machines, Windows Server 2022, PowerShell, IIS Manager, SQL Server Configuration Manager, Log Analytics, Microsoft Sentinel, KQL, Windows App (RDP from macOS).

## Note on evidence

Screenshots are from my own lab. Public IP addresses, account names and subscription details are removed before anything is published.
