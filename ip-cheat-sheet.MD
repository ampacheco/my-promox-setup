# 🧠 Linux `ip` Command Cheat Sheet

## 🔗 Interface Management
| Command | Description |
|--------|-------------|
| `ip link show` | Show all interfaces |
| `ip link show eth0` | Show specific interface |
| `ip link set eth0 up` | Bring interface up |
| `ip link set eth0 down` | Bring interface down |
| `ip link set eth0 mtu 1400` | Set MTU |
| `ip link set eth0 promisc on` | Enable promiscuous mode |

---

## 🌐 IP Address Management
| Command | Description |
|--------|-------------|
| `ip addr show` or `ip a` | Show all IP addresses |
| `ip addr add 192.168.1.100/24 dev eth0` | Add IP address |
| `ip addr del 192.168.1.100/24 dev eth0` | Delete IP address |

---

## 🚦 Routing
| Command | Description |
|--------|-------------|
| `ip route show` or `ip r` | Show routing table |
| `ip route add default via 192.168.1.1` | Add default gateway |
| `ip route del default` | Remove default gateway |
| `ip route add 10.10.0.0/16 via 192.168.1.1` | Add route to subnet |

---

## 📡 ARP (Neighbor Table)
| Command | Description |
|--------|-------------|
| `ip neigh` | Show ARP table |
| `ip neigh add 192.168.1.10 lladdr AA:BB:CC:DD:EE:FF dev eth0` | Add static ARP entry |
| `ip neigh del 192.168.1.10 dev eth0` | Remove ARP entry |

---

## 🧪 VLAN / Virtual Interfaces
| Command | Description |
|--------|-------------|
| `ip link add link eth0 name eth0.10 type vlan id 10` | Create VLAN interface |
| `ip link delete eth0.10` | Delete VLAN interface |

---

## 🧱 Bridge Management
| Command | Description |
|--------|-------------|
| `ip link add name br0 type bridge` | Create a bridge |
| `ip link set eth0 master br0` | Add interface to bridge |
| `ip link set br0 up` | Bring bridge up |
| `ip addr add 192.168.1.1/24 dev br0` | Assign IP to bridge |

---

## 🧰 Testing & Debugging
| Command | Description |
|--------|-------------|
| `ip -s link` | Show interface statistics |
| `ip monitor` | Monitor link/IP/route changes live |
| `ip route get 8.8.8.8` | Trace route decision for an IP |
