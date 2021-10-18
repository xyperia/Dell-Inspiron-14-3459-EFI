# DPCIManager
Fork of [MuntashirAkonsource code](https://github.com/MuntashirAkon/DPCIManager)


Simple OS X app for viewing PCI hardware info

The [original source code](https://sourceforge.net/projects/dpcimanager) was from @phpdev32 

### Release
Download ➣ [Release DPCIManager](https://github.com/chris1111/DPCIManager/releases/tag/V1.8)

Old binaries can be found here: https://sourceforge.net/projects/dpcimanager/files

**NOTE:** The old binary files contain `DirectHW.kext` which might lead your antivirus program to believe that this application contains a virus. This has been completely removed from this version (V 1.8)

### Usage (for `dspci`)
If you're running version `1.6`, see usage [here](https://github.com/MuntashirAkon/DPCIManager/blob/e302cd9ce6f62d90d5da627cccc14cb088696444/README.md#usage-for-dspci).

As of version `1.7`, you can see usage by running:
```sh
dspci --help
```

#### JSON Schema for default JSON output
For `1.6`, see [old schema](https://github.com/MuntashirAkon/DPCIManager/blob/e302cd9ce6f62d90d5da627cccc14cb088696444/README.md#json-schema).

An output contains an array of objects which have the following attributes. 
For understanding JSON schema easily, I've used . (dot) for objects and [] (square brackets) for arrays:

* `BDF`: (String) Bus number, Device number, Function number (Format `B:D.F`)
* `Class`: (Object) Device's class
    - `Class.ClassName`: (String) Device's class name
    - `Class.SubclassName`: (String) Device's subclass name
    - `Class.ID`: (Hex String) Device's class code
* `Info`: (Object) Device info
    - `Info.Name`: (String) Device's name
    - `Info.Vendor`: (String) Device's vendor
* `ID`: (Object) Device's full ID
    - `ID.VendorID`: (Hex String) Device's vendor ID
    - `ID.DeviceID`: (Hex String) Device's ID
* `SubsysID`: (Object) Device's subsystem ID
    - `SubsysID.VendorID`: (Hex String) Subsystem's vendor ID
    - `SubsysID.DeviceID`: (Hex String) Subsystem's ID
* `Rev`:  (Hex String)  Revision

#### Example Output
```json
[
  {
    "Info" : {
      "Name" : "Wireless 3165",
      "Vendor" : "Intel Corporation"
    },
    "ID" : {
      "VendorID" : "8086",
      "DeviceID" : "3165"
    },
    "SubsysID" : {
      "VendorID" : "8086",
      "DeviceID" : "4410"
    },
    "Rev" : "79",
    "BDF" : "01:00.0",
    "Class" : {
      "ID" : "0280",
      "ClassName" : "Network controller",
      "SubclassName" : "Network controller"
    }
  },
  {
    "Info" : {
      "Name" : "RTL810xE PCI Express Fast Ethernet controller",
      "Vendor" : "Realtek Semiconductor Co., Ltd."
    },
    "ID" : {
      "VendorID" : "10ec",
      "DeviceID" : "8136"
    },
    "SubsysID" : {
      "VendorID" : "1028",
      "DeviceID" : "0767"
    },
    "Rev" : "07",
    "BDF" : "02:00.0",
    "Class" : {
      "ID" : "0200",
       "ClassName" : "Network controller",
       "SubclassName" : "Ethernet controller"
    }
  }
]
```

### License
- GPLv2
