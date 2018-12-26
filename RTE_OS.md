# RTE, OS

## Adding SWC instance
### Configuration > System > Swcd_App
1. ARXML file(App_NAME.arxml) with ARRoot
1. Add *Application Sw Component Type*

### Build > generate.py
1. Add App_NAME to GenerateRte
1. (Optional) If SWC use IOC(Inter Os Communication) port, register App_NAME at GenerateOs_Common

### SWC_XXX > Runnable
1. Add Runnable
1. Uncheck **Can Be Invoked Concurrently** (to false)
1. Change short name and symbol
1. Add Timing Event w/ period

### CSWC_RootComposition > Components and Ports
1. Add SWC_XXX

### EcuExtract > Overview
1. Click on *ECU Software Components Mapping* at bottom right
1. Click OK and check changes

### EcuC module
Go to All Contents and
* EcuC
    * EcucPartitionCollection
        * *EcucPartition*

**Assign to desired Core**
***

## SWC registration (Assigning Core, Task, Alarm)
### EcuC module > All Contents
1. EcuC -> EcucPartitionCollection > Ecuc Partition
1. Add to *Software Component Instance Ref*

### Os module
**Sequence: Event or Alarm > Task > Application**
* Go to *Task tab*, create task  
* Go to *Alarm tab*, configure alarm  
* Application tab  
    1. Double click on OsApplication_X
    1. Click Browse of *App Alarm Ref*
    1. Add OsAlarm
    1. Click Browse of *App Task Ref*
    1. Add Task

### Rte module
Sw Component Instance tab
1. Add SwcInstance reference
1. **Path to reference** should start with ECU_EXTRACT, not AUTOSAR/CSWC_RootComposition**
1. Right click, then click *RteEventToTaskMapping*
1. Go to added Event To Task Mapping
1. Set **Event Ref**, **Mapped To Task Ref** and **Used Os Alarm Ref** with pre-configured references

Task Mapping tab (not essential)
1. Check position of added event in the task
    1. Go to **OsTask Mapping Table**
    1. Select Task
    1. Check Position in the left category
1. Go back to Sw Component Instance tab
1. Enter the checked position in **Position In Task**

### SWC_XXX > Overview
Generate Code
***

## Extended Task
### Os module
Event tab
1. Add OsEvent as amount of handler
1. Rename and set bit mask for extended task

Task tab
1. Add task for handling
1. Rename, set Priority and set Stack size
1. Click *Event Ref*
1. Select and Click add button with added OsEvents

Application tab
1. Double click on desired OsApplication on the left
1. Click browse at the *App Task Ref*
1. Select the task and click add button

### Rte > Task Mapping
Event Table
1. Select the desired Instance (SWC or BSW)
1. Check unshaded events to map

OsTask Mapping Table
1. Check proper option
1. Verify the mapped Tasks (could be empty)

Mapping
1. Select desired events
1. Click **Add**

#### Caution
* Application contain Tasks
* Task contain Events
* OsEvents are mapped to RteEvent
***

## Changing stack size
### OS > Application
1. Change stack size
***
