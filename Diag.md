# Diagnostic Configuration
1. Dem
1. Dcm

## Memory & DTCClass configuration
### Dem Module
1. Go to *DTCClass* tab
1. List up the DTC classes by adding
1. Go to *Event Parameter* tab
1. **Add common DemEventClass and Copy and Paste in All contents**
1. Add Event parameter and double click then set the belows
    * Event Kind
    * Aging Allowed
    * Event OBD Readiness Goup
    * DTC Class Ref
    * Operation Cycle Ref

## SWC configuration
### Swcd_App > App_Dem
1. Go to Ports tab
1. add client ports(DTCClass) with DiagnosticMonitor interface
1. Go to Runnables tab
1. Go to DIagnosticMonitor runnable > Operation / Mode / Trigger Acces
1. Add *.SetEventStatus to Synchronous Server Call Points

### EcucValueCollection > Service and I/O
1. Click Dem
1. Select Event_DEM_E_UDS_DTC_ 
1. Click **add** at top right
1. Check and Connect

## Extended Data
1. Set extended data in Dem module
1. Generate Swc


## Dcm
