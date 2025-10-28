peripherals are external devices that are connected to a computer system to enhance its functionality and provide additional features. they serve specific purposes and interact with the computer system to input or output data.
## i/o module
an io module or controller or interface is a device or componnent in a computer system that facilitates communication between the CPU and external devices. It manages the exchnage of data and control signlas between the compuer and various input and output devices.
![[Pasted image 20251028132626.png]]

## i/o module functions
the i/0 module is a special hardware component interface between the cpu and peripherals to supervise and synchronize all i/o transformation.
the detailed functions of i/o modules are :
### control and timing:
i/o module includes control and timing to coordinate the flow of traffic between internal resources and external devices. the control of the transfer of data from external devices to processor consists following steps:
- the processor interrogates the i/o module to check status of the attached device.
- the i/o module returns the device status.
- if the device is operational and ready to transmit, the processor requests the transfer of data by means of a command to i/o module.
- the i/o module obtains the unit of data from the external device
- then the data are transferred from the i/o module to the processor.
### Processor communication
i/o module communicates with the processor
- command decoding
- data exchange between processor and itself
- status reporting as peripherals are too slow and it is important to know the status of i/o module.
- address recognition i/o module must recognize one unique address for each peripheral it controls
### Device communication
in the context of an i/o module device communication refers to the exchange of commands, status information and data between the module and the connected external devices.
commands are instructions sent from the processor to the io module, specifying the desired actions to be performed by the device. Status information is provided by the i/o module to the processor indicating the current state or condition of the device. data refers to the actual information being transferred between between device and processor

### Data Buffering 
data buffering is essential when the i/o device operates at a different speed than the memory. if the device is faster there is a risk of losin data. to prevent this an i/o module buffers the data. this intermediate step allows the memory to catch up with the devices speed and ensures that no data is lost. Buffering means temporaliry storing the data in a dedicated area called a buffer or a cache. conversely, if the device is slower the i/o module buffers the incoming data from the slower device and holds it in the buffer until the memory is ready.

### error detection