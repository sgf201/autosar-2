# CAN
Contains belows
1. [DB Update](#db-update)
1. [Data Mapping](#data-mapping)
1. [E2E](#e2e)
***

## DB Update
### Import new DB
#### EcuExtract > Communication and Topology
    Select and remove existing DB

#### EcuExtract > Overview
    Import DBC
    Select whether to use E2E per message(=SignalGroup)
    Set Prefix & Signal Groups for ALL

### Harmonize
#### EcuValueCollection > Generate ECU Configuration
    Harmonize a relevant modules (check the below)
    - Can Stack
    - Com Stack
    - EcuC
    - Miscellaneous
        - ComXf
        - E2EXf

## Data Mapping

### Check Com module
#### Com > Signal Group
    Check Notification & Timeout Notification column for **Required Messages** are empty
    If empty, fill it with bulk change (patterned change)

## E2E
