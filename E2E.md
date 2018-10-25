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

## ~~ComXf & E2EXf~~
Should check Signal Group using E2E is mapped to Data prototype

### E2EXf, ComXf > Implementation Mapping
Check each signal group has a **Variable Data Prototype Instance Ref**

## Cautions
* Data types MUST be implemented with Send/Receive access
* Not Read/Write access