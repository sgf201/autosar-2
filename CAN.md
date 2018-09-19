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
1. Check **E2E & Category**(Normal, Diag, Xcp, Etc.) for each message(=SignalGroup)
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
1. Check enable Com Specs
1. Configure proper InitVal
### SWC_X > Runnables
1. Click Runnable which will use the port data
1. Select specific Access Type and Click add button
1. Add proper message from candidate
### Variable Access
***

## Data Mapping
### EcuExtract > Data Mapping
### Com > Signal Group
Check Notification & Timeout Notification column for **Required Messages** are empty
If empty, fill it with bulk change (patterned change)
***

## E2E
***

## Caution!
Port can be created by imported CAN message, but DataType is not updated automatically
So it could be possible that mismatch between data and port occur
Should check Interface, Port, DataType
***
