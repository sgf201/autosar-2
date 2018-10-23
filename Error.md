# Error

## Generate Error
### ERR001122
    <'/DBCImport/ImplementationDataTypes_CCANFD/MsgGr_CCANFD_MgsGroupLogger01_10ms'>
    configured for IocDataTypeRef parameter in container is not valid. It
    should be present in software component description

In order to use IOC interface, ARXML including Implementation data type should be in Os_Common
#### Build > Generate.py
1. Register coreesponding ARXML in Os_Common

---

## Compile Error
### E219
    ctc E219: ["Static_Code\Modules\b_autosar_com_ComXf_R43\delivery\ComXf.h" 38/1] cannot open #include file "ComXf_APIs.h" 
    ctc E219: ["Static_Code\Modules\b_autosar_com_ComXf_R43\delivery\ComXf.c" 33/1] cannot open #include file "ComXf_Cfg.h" 
    ctc E201: ["Static_Code\Modules\b_autosar_com_ComXf_R43\delivery\ComXf.c" 65/3] #error "ComXf.c : Mismatch in AUTOSAR Release Major Version" 
    ctc E201: ["Static_Code\Modules\b_autosar_com_ComXf_R43\delivery\ComXf.c" 68/3] #error "ComXf.c : Mismatch in AUTOSAR Release Minor Version" 
    ctc E201: ["Static_Code\Modules\b_autosar_com_ComXf_R43\delivery\ComXf.c" 75/3] #error "ComXf.c: Mismatch in Software Major Version" 
    5 errors, 0 warnings
    scons: * [Debug\Static_Code\Modules\b_autosar_com_ComXf_R43\delivery\ComXf.o] Error 1
    ctc E219: ["Static_Code\Modules\b_autosar_com_ComXf_R43\delivery\ComXf.h" 38/1] cannot open #include file "ComXf_APIs.h" 
    1 errors, 0 warnings
    scons: [Debug\Static_Code\Modules\b_autosar_com_ComXf_R43\delivery\ComXf_GlobalDataDefinition.o] Error 1
    ctc E219: ["Static_Code\Modules\b_autosar_com_ComXf_R43\delivery\ComXf.h" 38/1] cannot open #include file "ComXf_APIs.h" 
    1 errors, 0 warnings
    scons: ** [Debug\Generated\Bsw_Output\src\Rte_Partition_EcucPartition_Main.o] Error 1
    scons: building terminated because of errors.

#### Build > Generate.py
1. E2EXf
    * Append newly imported DB ARXML
1. ComXf
    * Append newly imported DB ARXML and App using E2E Signal group