# Windows Remote Desktop (RDP)

## Objective

Remotely connect from a Kali Linux virtual machine to a Windows 11 virtual machine using RDP.

---

## Environment

- VMware Workstation
- Windows 11 Pro
- Kali Linux
- xfreerdp

---

## Steps

1. Enabled Remote Desktop on Windows.
2. Verified the user account was allowed to access the computer through Remote Desktop.
3. Found the windows IP address.
4. Troubleshooted firewall issue.
5. Connected from kali using xfreerdp.
6. Verified successful remote administration.

---

## Issue Encountered

The RDP connection failed.

### Cause

Windows Defender Firewall blocked inbound RDP traffic.

### Solution

Enabled the built-in 'Remote Desktop' rule group in Windows Defender Firewall.

---

## Commands Used

```bash
ipconfig
```

```bash
ping -c 4
```

```bash
ip a
```

```bash
xfreerdp /v:<IP> /u:<username> /p:<password> /cert:ignore /size:1920x1080
```

```bash
query user
```

---

## Skills Practiced

- Windows administration
- Remote Desktop Protocol (RDP)
- Windows Firewall
- Troubleshooting
- Remote administration from Linux

## What I Learned

- How to configure Remote Desktop on Windows 11.
- How to remotely administer a Windows machine from Kali Linux using `xfreerdp`.
- How to identify a Windows machine's IP address using `ipconfig`.
- How to verify network connectivity using `ping`.
- How Windows Defender Firewall can block inbound RDP connections and how to resolve the issue.

## Screenshots

The following screenshots show the key stages of configuring and verifying the RDP connection.

![Enable Remote Desktop and find my IP](screenshots/configure-rdp.png)

![Connecting to machine](screenshots/connecting-rdp.png)

![Troubleshooting firewall problem](screenshots/firewall-issue.png)

![Successful RDP connection](screenshots/successful-rdp-session.png)
