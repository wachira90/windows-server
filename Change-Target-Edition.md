You can convert Windows Server 2022 Evaluation to Standard edition using DISM commands. Here's the process:

## Step 1: Check Current Edition
First, verify your current edition:
```cmd
dism /online /get-currentedition
```

## Step 2: List Available Target Editions
Check which editions you can upgrade to:
```cmd
dism /online /get-targeteditions
```

## Step 3: Convert to Standard Edition
Use this command to convert from Evaluation to Standard:
```cmd
dism /online /set-edition:ServerStandard /productkey:VDYBN-27WPP-V4HQT-9VMD4-VMK7H /accepteula
```

**Important notes:**

- The product key shown above (`VDYBN-27WPP-V4HQT-9VMD4-VMK7H`) is a generic KMS client key for Windows Server 2022 Standard
- After conversion, you'll need to activate with a valid license key using: `slmgr /ipk YOUR-ACTUAL-LICENSE-KEY`
- The conversion process will require a reboot
- Run these commands in an elevated Command Prompt (Run as Administrator)
- This conversion retains all your installed programs, settings, and data

## Alternative Method
You can also use PowerShell:
```powershell
Get-WindowsEdition -Online
Set-WindowsEdition -Online -TargetEdition ServerStandard -ProductKey VDYBN-27WPP-V4HQT-9VMD4-VMK7H -AcceptLicense
```

The system will automatically reboot during the conversion process. Make sure you have a valid Windows Server 2022 Standard license for activation after the conversion completes.
