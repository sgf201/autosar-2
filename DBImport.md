# DBImport
Update and configure CAN related modules with **new dbc**   
If there are many changes in CANDB, should look into [data mapping](#related-configuration).
***

## Replace DB
EcuExtract > Communication and Topology

    Select and remove existing DB

EcuExtract > Overview

    Import DBC
    Select whether to use E2E per message
    Set Prefix & Signal Groups for ALL

## Import New DB
If you aren't gonna set E2E option, you can [**SKIP**](#harmonize) the below

## Harmonize
EcucValueCollection > Harmonize
    
    Harmonize the relevant modules (check the below)

    - Can Stack
    - Com Stack
    - Ecuc
    - Miscellaneous
        - ComXf
        - E2EXf

## E2E Configuration
E2E


***
## Related configuration
[Port](Port.md)  
[Data mapping](DataMapping.md)
