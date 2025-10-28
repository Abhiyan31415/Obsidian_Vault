memory is an essential component 
we can divide various memory system based on various fields or stuffs right so lets take one of them ie the access method we have 4 types of method to access anything alright lets start with the sequential one 
1. sequential access
   In this access it must start with beginning and read through a speicifc linear sequence. this means access time of data unit depends on positon of records and previous location.
   A classic example of sequential access is a magnetic tape. To access data in the middle of the tape, you have to rewind or fast-forward through all the preceding data. The further the desired data is from the current position, the longer it takes to access.
2. Direct access
   in this method individual blocks of records have unique address based on location. **Direct (or random) access** means that each data element (or block of records) can be reached directly by using its unique address or index, without having to read any other data first. Because the location is known in advance, the access time is essentially constant (‑ O(1) ‑) regardless of where the element resides in memory.
3. Random Access
   the time to access a given location is independent of the sequemce of priror accesses and is constant. thus any location can be selected out randomly and directly addressed and accessed. 
4. Associative access
   this is random access type of memory that enables one to make a comparison of desired bit locations within a word for a specified match and to do this for all words simultaneously.
so okay what we gotta know is that their will always be a tradeoff between the capcaity access time and cost per bit so  we must obtain highest possible access speed while minimizing the total cost of the memory system.
cpu doesnt need all the accumulated information at the same time.
therefore it is more economical to use low-cost storage devices to serve as a backup for storing the information that is not currently used by cpu
the memory unit that directly communicate with cpu is called the main memory.
devices that provide backup storage is called auxillary memory.
as we go down in the hierarchy 
cost per bit decreases
capcaity of memory increased and access time increases
frequency of access of memory by processor also decreases.
the memory systems diagram is shown in [[heirarchy]]
the various type of memeory are discussed below:
a. Registers
fastest smallest storage locations in a computer system, used to hold data that is currently being processed by the CPU
b. L1 cache
this is a small amount of memeory that is integrated into the CPU chip and used to store data that is frequntly accessed by the CPU.
c. L2 cache
this is a larger amount of memory that is located on the cpu chip or on a seperate chip and used to store data that is frequently accessed but not as frequently as data soted in l1 cache
d. main memory
this is the primary system memory that holds data and instructions that the cpu accesses freqquntly. It is slower than cache memory but faster than secondary storage.
e. Disk Cache
this is a portion of Ram that is used to temporarily store data that is being read from or written to a hard disk drive in order to improve performance.
f. hard disk drive
this is a non volatile storage device that stores data on spinning magnetic disks. it provides large storage capacity at a relatively low cost but is slower than main memory.
g. optical storage 
this includes cd roms dvds and bluray disks . these are non volatile storage devices that store data using lasers to read and write information on a reflective surface. 
h. tape storage 
this is a non volatile storage medium that uses magnetic tape to store data. it is used for long term storage and archiving but is very slow and has limited random access capabilities.
