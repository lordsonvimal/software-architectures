# Memory Access Latency

Sources of latency
- Finite heap memory
- Large heap memory
  - Heap memory is large than RAM
  - OS will use Hard disk and does swapping memory 
  - Even when RAM is big, large heap should be garbage collected
- GC Algorithm
  - Different runtimes use different algorithms
  - Each algorithm specializes in specific cases
- Finite buffer memory
  - Every read / write operation
  - To write a data to DB, it need to read data from harddisk and then update it and save, then returns
  - So, buffer memory is critical for throughput

Approaches to overcome
- Avoid memory bloat
  - Reduce number of instruction
  - Heap size should be as small as possible
  - Reduce allocations of objects
- Weak / Soft references
  - When allocating large objects, we can use weak references
  - In JAVA, we can mark a reference as weak reference
- Multiple smaller processes
  - Instead of one large process, split into multiple processes for efficiency
- Garbage collection algorithm
  - One that pauses when doing garbage collection. Suitable for batch processing
  - One that runs along with the process. Suitable for server requests

- DB Normalization
  - Avoid duplicate data
  - Sometimes, we do denormalization when improving performance of query time
- Compute over storage
  - Anything that can be derived, derive the data instead of storing
