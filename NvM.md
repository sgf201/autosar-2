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
    * Short Name
    * Block Crc Type
    * Block Use Crc
    * Block Management Type
    * and so on...
1. right click on block descriptor, and then click NvMTargetBlockReference
    * jump to NvMTargetBlockReference (automatically)
    * Choose Ea or Fee (Normally Fee Ref)
        * jump to NvMFeeRef (automatically)
        * click Browse and select appropriate FeeBlock

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
1. add Port with desired interface
1. rename
1. In Communication Spec, select desired operation then enable Com Specs

### Runnables tab
1. Click *Operation / Mode ? Trigger Access*
1. Add enabled operations
***
