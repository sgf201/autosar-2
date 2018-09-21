# CAN
### Contents
1. [DB Update](#db-update)
1. [Port Configuration](#port-configuration)
1. [Data Mapping](#data-mapping)
1. [E2E](#e2e)
***

## DB Update
### EcuExtract > Communication and Topology
1. Select and remove existing DB

### EcuExtract > Overview
1. Click **Import DBC**
1. Set Prefix & Signal Groups for ALL  
1. Check **E2E & Type**(Normal, Diag, Xcp, Etc.) for each message(=SignalGroup)
1. Finish

### EcuValueCollection > Generate ECU Configuration(=Harmonize)
1. Harmonize a relevant modules (check the below items)
    - Can Stack
    - Com Stack
    - EcuC
    - Miscellaneous *(When there are messages using E2E)*
        - ComXf
        - E2EXf
1. Click **Finish**
***

## Port Configuration
### SWC_X > Ports
1. Add port by choosing proper interface
1. Check enable Com Specs **AND**
    1. Set Alive Timeout
    1. Handle Never Received **false**
    1. Enable Update **false**
1. Configure proper InitVal
### SWC_X > Runnables
1. Click Runnable which will use the port data
1. Select specific Access Type and Click add button
1. Add proper message from candidate
### Variable Access
### When signal and properties changed(=ARXML doesn't match to DB)
1. Copy DataTypes from DB
1. Amend reference DataTypes of interface in ARXML
1. Compare and modify InitVal in ARXML
***

## Data Mapping
### EcuExtract > Data Mapping
### Com > Signal Group
Check Notification & Timeout Notification column for **Required Messages** are empty.  
If empty, fill it with bulk change (patterned change)
***

## E2E
***

## Caution!
Port can be created by imported CAN message, but DataType is not updated automatically.  
It could be possible that mismatch between data and port occur.  
Should check Interface, Port, DataType  
Port -> Interface -> DataTypes  
**InitVal only reside in composition so should modify InitVal manually in constant**  
InitVal doesn't refer to NAME, it convert list to array

Interface and DataTypes are **COMMON**  
Port is **INDIVIDUAL** for SWC
***
