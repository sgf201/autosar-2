# E2E
## DB import
### 
### Harmonize

## Modify a script
### Build > Generate.py
1. E2EXf
    * Append newly imported DB ARXML
1. ComXf
    * Append newly imported DB ARXML and App using E2E Signal group

## Rte Settings
### Com > Signal Group
1. Select the all Rx E2E signal groups
1. Click **Bulk change** at the top right
1. Patterned Conversion
    * Change mode: Naming with Prefix and/or Postfix
    * Parameter to change: ComNotification & ComTimeoutNotification
    * Check **Ignore Common String**

!! When want to remap the existing E2E data mapping to another
1. disconnect the all related ports
1. harmonize
1. do 

## Rx Signal Group

## AppTransformer
### Ports tab
1. Add receiver ports
1. Add sender ports

### Runnables
1. Go to *Data / Parameter Access*
1. Add data access for both Sender and Receiver ports

## EcuExtract
1. Data Mapping

## SWC_XX
1. Create Receiver port
1. Add data access

### CSWC_RootComposition
1. 

### EcuExtract
* ECU Software Components Mapping

***

## Tx Signal Group
***

## ~~ComXf & E2EXf~~
Should check Signal Group using E2E is mapped to Data prototype

### E2EXf, ComXf > Implementation Mapping
Check each signal group has a **Variable Data Prototype Instance Ref**

## Cautions
* Data types MUST be implemented with Send/Receive access
* Not Read/Write access
