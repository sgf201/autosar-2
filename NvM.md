# NvM
* Modules to be configured
    1. Fee
    1. NvM
* JonFinished
***

## Fee Module
### Block Configuration
1. Add FeeBlock with desired value and short name

## NvM module
### Block Descriptor tab
1. add nvMBlockDescriptor
1. Set the below items
    * Continer Details
        * Block Use Crc
        * Calc Ram Block Crc
        * Max Num Of Read Retries
        * Max Num Of Write Retries
        * Select Block For Read All
        * Select Block For Write All
    * To Be Configured
        * Block Crc Type
        * Block Management Type
        * Nv Block Base Number
        * Nv Block Length
        * Nv Block Num
        * Nvram Block Identifier
        * Ram Block Data Address
        * Rom Block Data Address
        * Rom Block Num
        * Single Block Callback
        * Write Verification Data Size
1. right click on block descriptor, and then click NvMTargetBlockReference
    * jump to NvMTargetBlockReference (automatically)
    * Choose Ea or Fee (Normally Fee Ref)
        * jump to NvMFeeRef (automatically)
        * click Browse and select appropriate FeeBlock

## JobFinished configuration
Go to SWC_NvM

### SWC_NvM

### Ports
1. Add provided port with **NvMNotifyJobFinished Interface**!!!
1. Enable Provided Com Specs
1. Type in Queue Length (typ: 10???)

### Runnables
1. Add Runnable named NvMJobFinished_[BLOCKNAME]
1. RTE Event > Add > **Operation Invoked Event**

### EcucValueCollection
1. Go To *Service and I/O* tab
1. Connect added port with PNJF_NvMBlock_XXX of Svc_NvM


### OS & RTE
1. Go to OS
1. Add Events for extended tasks *OsEvent_NvMCallback__*
1. Add Task *OsTask_ASW_FG2_NvMCallback* (prioritry between ASW_FG1 ~ ASW_FG3)
1. Register events for *Event Ref*
1. 
### OS

### 
---

### Runnables
1. Add Runnable named NvMJobFinished_[BLOCKNAME]
---

### All Contents
1. Right click on Events
1. Add **Operation Invoked Event**
1. Rename shortname to **OIE_NvMJobFinished_[BLOCKNAME]**
1. Designate **Start On Event**
### (Optional) Os
1. Make Task will be containing NvM Events
1. Make tasks with number of Operation Invoked Events
1. Register Evenets for NvM Task
### Rte > Task Mapping
1. 
---


## Caution!
* NvMNvBlockBaseNumber should be equal to right shifted FeeBlockNumber
* There should be **no unmapped FeeBlock**
* FeeBlockLength should be greater than NvMBlockLength (normally, +2)

***

### Concept
Block: 
1. Nv Block:
    * Base Number:
    * Length:
    * Num:
1. Nvram Block:
    * Identifier:
    * Device Id:
1. Rom Block:
    * Data Address:
    * Num:
1. Ram Block:
    * Data Address:
***

## SWC_NvM
### Ports tab
1. add Port with desired interface (server-client)
1. rename
1. In Communication Spec, select desired operation then enable Com Specs

### Runnables tab
1. Click *Operation / Mode / Trigger Access*
1. Add enabled operations to **Synchronous Server Call Points**

## EcucVallueCollection
### Service and I/O tab
1. Select Svc and desired ports
1. Click add
1. Uncheck *Respecting Naming Rules*
1. Mapping with proper service name
***
