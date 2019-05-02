# Dcm

## Add Variant Coding
* Go to All Contents > DcmConfigSet > DcmDsp
* Data Info
    1. Create Data Info **Typically, use existing one**
* Data
    1. Add Data
    1. Set *Name, Size(in bit), Type* and
    1. Choose proper **Info ref** from Data Info
* Did Info
    1. Add Did Info and go to Did Access
    1. Add *Did Read / Did Write*
    1. Select *Security Level Ref and Session Ref* (**Security Level is only set in Did Write**)
* Did
    1. Add Did
    1. Type in ID and Set *Used* to true
    1. Choose **Info Ref** from Did Info
    1. Click on **Signal** and select Data reference
        * Set *Data Pos and Endianness*

* Generate

* App_Dcm > SWC_DiagnosticService
    1. Go to **Ports**
        1. Create Server Port made
        1. Select *Operations* (ReadData / WriteData)
        1. Enable Com Specs
        1. Set Queue Length to 1
    1. Go to **Runnables**
        1.

* EcucValueCollection
    1. Go to **Service and I/O** 
    1. Expand Dcm
    1. Connect DataService port to SWC_DiagnosticService
---

## Resolve error when Diag messages are changed
* Go to Dcm module > All Contents > DcmConfigSet > DcmDsl > Dcm_DiagCom_Protocol > Row > UDS_ON_CAN > MainConnection
    1. Mapping    (**DcmIPdu not NPdu**)

* Go to Xcp module > 

* Go to EcuValueCollection
    1. Click Regenerate Handle IDs
    1. Check as below
        * Can Stack
        * Com Stack
        * Diagnostic
        * Ecuc
    1. Click Finish

* Go to PduR module > Routing Tables > ... > Routing Path
    1. Find Pdu Hande Id of 65535
    1. Fix Id to Non zero value
* Go to CanTp module > 