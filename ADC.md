# ADC Configuration

## Port
### PortContainer > PortPin
1. Go to PortPin which will use ADC in Container
1. Set Mode (Usually PORT_PIN_MODE_ALL)

## Adc
### Hw Unit
1. Register ADCx in Hw Unit
1. Add channel on ADCx
    * List up ANx with proper settings
    * Channel > Input Class Selection > AdcGlobInputClass_0
1. Add Group on ADCx
    * AdcGroup > Definition
    * Browse and grouping the ANx
1. Add Kernel Input Class

## IoHwAb