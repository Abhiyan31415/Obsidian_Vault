memory is an essential component 
we can divide various memory system based on various fields or stuffs right so lets take one of them ie the access method we have 4 types of method to access anything alright lets start with the sequentia one 
1. sequential access
   In this access it must start with beginning and read through a speicifc linear sequence. this means access time of data unit depends on positon of records and previous location.
   A classic example of sequential access is a magnetic tape. To access data in the middle of the tape, you have to rewind or fast-forward through all the preceding data. The further the desired data is from the current position, the longer it takes to access.
2. Direct access
   in this method individual blocks of records have unique address based on location. **Direct (or random) access** means that each data element (or block of records) can be reached directly by using its unique address or index, without having to read any other data first. Because the location is known in advance, the access time is essentially constant (‑ O(1) ‑) regardless of where the element resides in memory.
3. Random Access
   the time to access a given location 