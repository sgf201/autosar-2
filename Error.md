# Error

## Generate Error
### ERR001122
    <'/DBCImport/ImplementationDataTypes_CCANFD/MsgGr_CCANFD_MgsGroupLogger01_10ms'>
    configured for IocDataTypeRef parameter in container is not valid. It
    should be present in software component description

In order to use IOC interface, ARXML including Implementation data type should be in Os_Common
#### Build > Generate.py
1. Register coreesponding ARXML in Os_Common


### ERR 0838
    ComNotification<> in
    ComSignal/ComSignalGroup</AUTOSAR/Com/ComConfig/ComISignalGroup_MsgGr_E2E_CCANFD_CLU_01_20ms>
    is empty or invalid.

    [Avoidance Guide]
    ComNotification<> in
    ComSignal/ComSignalGroup</AUTOSAR/Com/ComConfig/ComISignalGroup_MsgGr_E2E_CCANFD_CLU_01_20ms>
    shall be set with valid value.
    Expected ComNotification:
    Rte_COMCbk_ComISignalGroup_MsgGr_E2E_CCANFD_CLU_01_20ms

    [Configuration Info] ComSignal/ComSignalGroup
    Path:
    /AUTOSAR/Com/ComConfig/ComISignalGroup_MsgGr_E2E_CCANFD_CLU_01_20ms
    File: Configuration\Ecu\Ecud_Com.arxml

#### Com > Signal group
1. Bulk change


### ERR0938
    SystemSignalGroupRef</DBCImport/SYSSIGNALGROUPS/MsgGr_CCANFD_CLU_02_100ms>
    in
    SenderReceiverToSignalGroupMapping</ECU_EXTRACT/EcuExtract/DataMappings>
    is empty or invalid.

    SenderReceiverToSignalGroupMapping</ECU_EXTRACT/EcuExtract/DataMappings>
    SystemSignalGroupRef:
    /DBCImport/SYSSIGNALGROUPS/MsgGr_CCANFD_CLU_02_100ms
    ContextComponentRef: /ECU_EXTRACT/EcuComposition/SWC_IDC
    ContextPortRef:
    /ADAS_DRV_Composition/ADAS_DRV_ASWC/SWC_IDC/Gr_MsgGr_CLU_02_100ms
    TargetDataPrototypeRef:
    /ADAS_DRV_Composition/ADAS_DRV_Interface/Network/Main_CAN/Gr_MsgGr_CLU_02_100ms/MsgGr_CLU_02_100ms

    [Avoidance Guide]
    SystemSignalGroupRef</DBCImport/SYSSIGNALGROUPS/MsgGr_CCANFD_CLU_02_100ms>
    in
    SenderReceiverToSignalGroupMapping</ECU_EXTRACT/EcuExtract/DataMappings>
    shall be set with valid SystemSignalGroup path.

    [Configuration Info] SenderReceiverToSignalGroupMapping
    Path: /ECU_EXTRACT/EcuExtract/DataMappings
    File: Configuration\System\Composition\EcuExtract.arxml

#### EcuExtract > Data Mappings
1. Click **Validate Data Mappings** at the top right
1. Remove broken mappings


### ERR 0696
    TargetPPortRef</App_Transformer/SWC_AppTransformer/Gr_MsgGr_CLU_01_20ms_IDS2>
    in
    ProviderIRef</ECU_EXTRACT/EcuComposition/IDS2_Gr_MsgGr_CLU_01_20msOfSWC_AppTransformerToGr_MsgGr_CLU_01_20msOfSWC_IDS2>
    is empty or invalid.

    [Avoidance Guide]
    TargetPPortRef</App_Transformer/SWC_AppTransformer/Gr_MsgGr_CLU_01_20ms_IDS2>
    in
    ProviderIRef</ECU_EXTRACT/EcuComposition/IDS2_Gr_MsgGr_CLU_01_20msOfSWC_AppTransformerToGr_MsgGr_CLU_01_20msOfSWC_IDS2>
    shall be set with valid PPortPrototype path.

    [Configuration Info] ProviderIRef
    Path:
    /ECU_EXTRACT/EcuComposition/IDS2_Gr_MsgGr_CLU_01_20msOfSWC_AppTransformerToGr_MsgGr_CLU_01_20msOfSWC_IDS2
    File: Configuration\System\Composition\EcuExtract.arxml

#### EcuComposition
1. Go to Assembly Connectors
1. Check whether there are broken connections or not
1. Remove broken connections

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