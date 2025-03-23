# 🧰 PowerShell Network Troubleshooting Cheat Sheet

## 🌐 Basic Network Info
| Command | Description |
|--------|-------------|
| `Get-NetIPAddress` | View all IP addresses |
| `Get-NetIPConfiguration` | IP, DNS, Gateway info (like ipconfig) |
| `Get-NetAdapter` | List all network adapters |
| `Get-NetAdapterStatistics` | View adapter stats (packets, errors) |
| `Get-DnsClientServerAddress` | Show DNS servers |

---

## 📡 Test Connectivity
| Command | Description |
|--------|-------------|
| `Test-Connection google.com` | Basic ping test (like `ping`) |
| `Test-Connection -ComputerName 8.8.8.8 -Count 4` | Ping with specific options |
| `Test-NetConnection google.com` | Ping + DNS + port test |
| `Test-NetConnection -ComputerName google.com -Port 443` | Test HTTPS port |

---

## 🧭 Routing & ARP
| Command | Description |
|--------|-------------|
| `Get-NetRoute` | Show route table |
| `Get-NetNeighbor` | View ARP cache |
| `Clear-NetNeighbor` | Clear ARP cache |
| `tracert example.com` | Trace route to host (classic command-line) |

---

## 🛠 DNS Troubleshooting
| Command | Description |
|--------|-------------|
| `Resolve-DnsName google.com` | DNS lookup (like `nslookup`) |
| `Clear-DnsClientCache` | Clear DNS cache |
| `Get-DnsClientCache` | View DNS cache |

---

## 🔗 Network Adapter Actions
| Command | Description |
|--------|-------------|
| `Enable-NetAdapter -Name "Ethernet0"` | Enable adapter |
| `Disable-NetAdapter -Name "Ethernet0"` | Disable adapter |
| `Restart-NetAdapter -Name "Ethernet0"` | Restart adapter |

---

## 🌐 Firewall & Port Checks
| Command | Description |
|--------|-------------|
| `Get-NetFirewallProfile` | Get firewall status |
| `Get-NetFirewallRule` | List all firewall rules |
| `New-NetFirewallRule -DisplayName "Allow80" -Direction Inbound -LocalPort 80 -Protocol TCP -Action Allow` | Add allow rule |

---

## 🧪 Advanced Network Testing
| Command | Description |
|--------|-------------|
| `netstat -an` | Show active ports and connections |
| `Get-NetTCPConnection` | PowerShell version of `netstat` |
| `ipconfig /flushdns` | Flush DNS cache (classic) |
| `arp -a` | View ARP table (classic) |

---

## 🧹 Network Reset Commands (Use with Caution)
| Command | Description |
|--------|-------------|
| `netsh winsock reset` | Reset Winsock Catalog |
| `netsh int ip reset` | Reset TCP/IP stack |
| `Restart-Computer` | Reboot (for full reset effect) |
