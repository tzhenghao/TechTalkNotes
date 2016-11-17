CPU Caches and Why You Care
===========================
by Scott Meyers

Thread memory matters

Differences between row/col major comes down to CPU caches.

CPU Caches
small amounts of unusually fast memory.

Data (D-cache)
Instruction (I-cache)
Translation lookaside buffer (TLB) - Caches result from virtual pages to physical page.

Changing algorithm to take advantage of instruction caches.

Locality counts.
Read/Write on A, hardware will speculatively prefetch things around A.

Multiple copies in different caches.

Cache Coherency
Assume both cores are running threads.

False sharing
Suppose Core 0 accesses A and Core 1 accesses A+1.

A and A+1 probably map to the same cache line.

Where practical, employ linear array traversals.

Be alert for false sharing in multithreaded systems.

Take advantage of PGO and WPO.
