# Forensics & Recon

> This part of the guide is more technical, but I assume if you're taking control of your own incident you're capable of this.

Now that you've gotten the initial response out of the way, you've taken the affected device(s) offline, and you've lowered the risk by changing credentials, we can inspect the affected device(s).

A lot of this is OS specific, so you can scroll to where your OS is, or click the shiny buttons here -> [Windows](#windows) - [macOS](#macos) - [Linux](#linux)

## Generalised Advice
- Especially if this is a personal matter, don't spend all your time collecting information on the threat, ensure your accounts are secured and you haven't suffered from a data breach first, once the device is offline, no other data can be exfiltrated (To a point, if you're dealing with a physical compromise, glhf lock your doors and stand guard :P)
- If you'd like, you can create a physical backup of the machine for evidence (Booting a Live Linux USB, using DD to create an image, etc.)
  - As always, take caution when inspecting the image and any drive contents.
  - If you're using a FDE (Full Disk Encryption) solution (Bitlocker, FileVault, LUKS), ensure you have required recovery keys/decryption keys on hand for later analysis.

## Windows
The first thing to do on Windows is collecting data about what might have been added to startup processes & services, there are a couple of different mechanisms for this, but for now we can stick to the following few.
> TODO: Powershell script to create easy to inspect logs, etc.
### Scheduled Tasks
```
schtasks /query /fo LIST /v
```

### Services
```
sc query type= service state= all
```

### Startup Items
```
wmic startup get caption,command
```

### Run a Windows Defender offline scan (This is the easiest and most complete offering from Defender)
> You can alternatively access this by opening Run (Win+R) and typing `windowsdefender://wdoscan/`
- Open the Windows Security app
- Select "Virus & threat protection"
- Select "Scan options"
- Find "Microsoft Defender Antivirus (offline scan) and run it.

## macOS
> TODO

## Linux
> TODO