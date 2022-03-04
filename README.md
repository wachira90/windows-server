# windows-server
windows server DISM

## Windows Server LTSC/LTSB versions


# Windows Server 2022

## Windows Server 2022 Standard Evaluation to Full Edition
````
Dism /Online /Get-CurrentEdition
````

## This command will show you the current edition of your Windows Server
````
Dism /Online /Get-TargetEditions
````

## This command will show the edition of the Windows that you can upgrade to
````
Dism /online /Set-Edition:ServerStandard  /ProductKey:VDYBN-27WPP-V4HQT-9VMD4-VMK7H /AcceptEula
````

## This command will upgrade the server to Standard Full Edition
````
Dism /online /Set-Edition:ServerDatacenter  /ProductKey:WX4NM-KYWYW-QJJR4-XV3QB-6VM33 /AcceptEula
````

This command will upgrade the server to DataCenter Full Edition


# Windows Server 2019

## Operating system edition KMS Client Setup Key
````
Windows Server 2019 Datacenter WMDGN-G9PQG-XVVXX-R3X43-63DFG
Windows Server 2019 Standard N69G4-B89J2-4G8F4-WWYCC-J464C
Windows Server 2019 Essentials WVDHN-86M7X-466P6-VHXV7-YY726
````

## CHECK VERSION SUPPORT

````
DISM.exe /Online /Get-TargetEditions
````

#๒ CHANGE VERSION
````
DISM.exe /online /Set-Edition:ServerStandard /ProductKey:N69G4-B89J2-4G8F4-WWYCC-J464C /AcceptEula
````


# LIST KEY
````
WINDOWS SERVER 2022
Operating system edition	KMS Client Product Key
Windows Server 2022 Datacenter	WX4NM-KYWYW-QJJR4-XV3QB-6VM33
Windows Server 2022 Standard	VDYBN-27WPP-V4HQT-9VMD4-VMK7H


WINDOWS SERVER 2019
Operating system edition	KMS Client Product Key
Windows Server 2019 Datacenter	WMDGN-G9PQG-XVVXX-R3X43-63DFG
Windows Server 2019 Standard	N69G4-B89J2-4G8F4-WWYCC-J464C
Windows Server 2019 Essentials	WVDHN-86M7X-466P6-VHXV7-YY726


WINDOWS SERVER 2016
Operating system edition	KMS Client Product Key
Windows Server 2016 Datacenter	CB7KF-BWN84-R7R2Y-793K2-8XDDG
Windows Server 2016 Standard	WC2BQ-8NRM3-FDDYY-2BFGV-KHKQY
Windows Server 2016 Essentials	JCKRF-N37P4-C2D82-9YXRT-4M63B
````

