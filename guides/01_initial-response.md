# Initial Response

First things first, you've experienced a cyber incident.
So far we're unsure on if this is malware, unauthorized physical access, etc.

### Note: If you're an employee of a company with processes in place
- Stop reading/using this guide.
- Immediately contact your IT Helpdesk/Security Team and follow their instructions
- Disconnect the affected device(s) from any networks/external devices.

> Checklist available! - If you'd like to follow along a checklist, they're in the `checklists` directory [here](../checklists/)

### 1. Contain any threat(s)
- Disconnect the affected device ASAP from any networks (Ethernet/WiFi/Other) - Enabling Aeroplane mode isn't a bad idea at this time too.
- If you feel safe to do so, don't turn the device off at this point (This may be beneficial for collecting logs)
- If multiple devices are suspected, at all for any reason, disconnect them as well.
- If you have external media attached to the affected device (External SSDs/HDDs/Flash Drives), disconnect them at this time and ***DO NOT*** attach them to another device yet.
- If you're unable to access data on the device, or it is encrypted and you are being asked to pay, this is [Ransomware](./ransomware/README.md).
  - It's still important to collect information and change credentials, so you can keep reading, however check the Ransomware page on what you can do.

### 2. Collect basic information
- Take note of the following
  - Date/Time of the potential incident
  - Activity prior to the incident (Software Installs/Upgrades, Downloads, etc.)
  - What did you observe (Suspicious error messages, unknown software, unauthorized behaviour on accounts, etc.)

### 3. Change Credentials
- Firstly, ensure you are doing this from a known-clean/safe device (Whether this be another machine not connected to the same network at the time, or even a fresh install of an OS on a separate machine)
- If you don't already, consider this as a time to look into a password manager.
  - If you are using a Password Manager, ensure you revoke the session for the affected device(s), change passwords, and enable 2FA if it isn't already active.
- Ensure you change all potentially affected credentials, not just accounts used on the affected device, but also consider ones that may have been exposed
  - This can include any accounts in a password manager on the affected device, saved logins in the browser, etc.

### [Next - Forensics & Recon](02_forensics-recon.md)