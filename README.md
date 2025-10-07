# Home-Lab Virtualization Host — Oracle Linux 8 / KVM + Cockpit

## Summary
Configured an Oracle Linux 8 hypervisor (db01) with KVM/libvirt and Cockpit for browser-based VM management.  
Created and verified a full virtualization stack, including VNC-accessible guest consoles via Cockpit and direct QEMU VNC ports.

## Environment
| Component | Details |
|------------|----------|
| Host | Oracle Linux 8 (db01.lab.local) |
| Hypervisor | KVM/QEMU via libvirt |
| Management | Cockpit 310 + cockpit-machines |
| Networking | Bridge NAT on 192.168.88.0/24 |
| Example VM | ubuntusrv01 — Ubuntu Server 22.04 |
| Console Access | Cockpit web console (HTTPS :9090) and QEMU VNC (TCP :5900) |
| Remote CLI | SSH from macOS Terminal |

## Skills Demonstrated
- Linux service management (systemd, firewall-cmd)  
- Virtualization stack configuration (libvirt domains, bridges)  
- VNC and remote-desktop troubleshooting  
- Secure remote access over SSH  
- Host/guest network isolation  
- Cockpit administration and plugin management  

## Screenshots
1. Cockpit dashboard showing host resources  
2. Virtual Machines panel listing `ubuntusrv01`  
3. VM console tab with guest terminal or GUI  
4. `virsh list --all` output  
5. `ss -tlnp | grep 5900` confirming QEMU listener  

## Notes
This project demonstrates a clean, maintainable home-lab hypervisor setup suitable for database and backend dev workloads.
