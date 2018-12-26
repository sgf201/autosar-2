# NvM
Modules to be configured
1. Fee
1. NvM

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
