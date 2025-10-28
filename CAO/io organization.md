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
Error dection is another ciritical function of the i/o module. it is responsible for detecting mechanical and electrical malfunctions reported by the device such as paper jams or bad ink tracks. the module also identifies unintentional chnages to the bit pattern and transmission errors. technique like parity bits , ehekcsums or crc calculations are used to verify data integrity and detect errors during transfer.

### An i/o interface
an i/o interface  also known as an i/o controller or i/o module, is a hardware component that allows a computer system to communicate with external devices and exchange data. it serves as a bridge between the computers internal components and the outside world.
![[Pasted image 20251028171525.png]]
peripheral devices are connected to the cpu through a bus that contains thee data bus, address bus and control bus ,however the processor is not directly connected to these devices and requires an interface.
CPUs are significantly faster than peripheral devices such as keyboards,  
printers, and magnetic disks. To synchronize their speeds, an interface is  
necessary to match the data transfer rates.  
different devices generate signals of varying nature, such as electrical,  
electro-mechanical, or electromagnetic. The interface assists in converting  
these signals to ensure compatibility.  
CPUs have specific data word sizes (e.g., 32-bit or 64-bit), whereas  
peripheral devices like keyboards, printers, and magnetic disks may have  
different formats and word sizes. The interface helps align the data  
formats and word sizes between the CPU and the peripherals.  
peripheral devices have different functions and require different logics or  
programs for data transfer. Instead of creating separate logics for each  
device, an interface provides a standardized way to handle the data  
transfer process.  
using interfaces helps avoid unnecessary complexity in handling different  
devices and allows for easier system upgrades or changes without altering  
the underlying logic

| isolated i/o                                                                                        | memory mapped i/o                                                                                                |
| --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| they have a separate i/o read/write control lines<br>in addition to memory read/write control lines | they have a single set of read/write control line                                                                |
| separate memory and i/o address spaces                                                              | memory and i/0 addresses share the common address space which reduces memory address range available             |
| distinct input and output instrcutions                                                              | no specific input or output instructionn so the same memory reference instructions can be used for i/o transfers |
|                                                                                                     |                                                                                                                  |
#### Reason behind the requirement of i/o interfaces
Device Connectivity: I/O interfaces enable computers to connect and  
communicate with a wide range of external devices. These devices can include  
peripherals such as keyboards, mice, printers, scanners, and storage devices  
like hard drives and USB flash drives.  
Data Transfer and Communication: I/O interfaces play a crucial role in  
facilitating data transfer and communication between the computer and  
external systems. For example, network interface cards (NICs) provide the  
necessary interface for connecting a computer to a local area network (LAN)  
or the internet.  
Standardization and Compatibility: I/O interfaces help establish standards  
and ensure compatibility between different devices and systems. By providing  
a standardized interface, I/O interfaces enable devices from different manufacturers to connect and communicate with each other seamlessly. For  
instance, USB (Universal Serial Bus) has become a widely adopted standard for  
connecting various peripherals to computers, regardless of the specific  
manufacturer or device type. Standardized I/O interfaces reduce complexity,  
promote interoperability, and simplify the integration of different hardware  
components and devices within a computer system.

### Programmed i/o

![[Pasted image 20251028172730.png]]

the i/o device pputs the data on the i/o bus and activates the data valid signal. the interface receives the data in the data register , sets the status register's F bit indicating data availability and activates the data accepted signal.
the i/o device disables the data valid line
The CPU continuously monitors the interface by checking the F bit of the  
status register.  
 If the F bit is set (1), the CPU reads the data from the data register and  
sets the F bit to zero.  
 If the F bit is reset (0), the CPU continues monitoring the interface.  

The interface disables the data accepted signal, and the system returns to an  
initial state, waiting for the next item of data to be placed on the data bus.

#### features
- Countinous cpu involvement 
- cpu slowed down to i/o speed
- simple
- least hardware
#### applications
- useful in small