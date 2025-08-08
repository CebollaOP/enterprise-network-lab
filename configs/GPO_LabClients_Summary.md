# LabClients Default Policy — Summary

**Scope (Link):** `mydomain.local/LabClients`  
**Security Filtering:** Authenticated Users  
**GPO Status:** Enabled  
**Who owns it:** Domain Admins / Enterprise Admins

## Key User Policies
- **Prohibit access to Control Panel and PC settings**  
  Path: `User Configuration → Administrative Templates → Control Panel`  
  State: **Enabled**  
  Effect: Blocks `Control.exe` and `SystemSettings.exe` (no Control Panel or Settings for standard users).

## Computer Policies
- None defined in this GPO (user-side lockdown only).

## Why this exists
- Prevents casual tampering with network/DHCP/DNS configs, uninstalling software, or changing security posture on lab client machines.

## Proof / Full Export
- See the exported HTML report here: [`GPO_LabClients_DefaultPolicy.html`](./GPO_LabClients_DefaultPolicy.html)

## Planned Hardening (next iterations)
- USB storage: block/allow by policy (SRP/AppLocker or device install restrictions)
- Task Manager / CMD / PowerShell limitations for standard users
- AppLocker allow-list for approved software
- Browser restrictions (downloads, SmartScreen, extensions)
