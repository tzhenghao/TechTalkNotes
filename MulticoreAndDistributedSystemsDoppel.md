Speaker: Neha Narula - RICON 2014
---------------------------------

Maintaining counters - increment transacations

contend on the same two counters

concurrency control enforce serial execution

3 cores - 2 will have to wait (on locks)

we don't get scalability!

Solution:

per core slices

each core executes on the logically same x

each core stores a copy of x if increment commutes.

db must support general purpose transactions
--------------------------------------------

running on the same key.

run other two transactions separately

Phase Reconciliation
--------------------
detects contention - split, reconciliation, and join

Doppel

Splittable operations, efficient detection and response to contention

operations, detecting contention, implementation, performance evaluation

multiple keys - transform to per core data

are on split AND non-split data

use optimistic concurrent control

core 1, core 3. - concurrency control actively seralize to y.

what happens when someone wants to read x.

reconcile per core writes to data.

reconcile local state to global state. - each core adding their version of x to the global version of x.

once everyone is done, it is in a joined phase - optimistic concurrency data.

use OCC - need to be properly serialized.

transition into split phase again

reorder transactions for better concurrency

properties:

- commutative
- can be efficiently reconciled
- single keys
- have no return value

RESTOCK's merge function

Doppel starts with no split data.
Counts conflicts on records.
Doppel considers moving over to split data.

one worker thread per core
transcations are procedures written in Go

Roadblocks
----------
marking memory for garbage collection slow

at high core counts, Go memory allocation - big problem

need > 48 cores to see this problem! - pushed into 1.3

memory allocation - turn down garbage collection

Go scheduler sleeping / waking.

RPC serialization

marshalling

experimental setup

stashing and execution in parallel

how much stashing? Does Doppel improve throughput for a realistic application.

Doppel executes conflicting workloads in parallel.

Same key on all cores. optimistic concurrent control.

OCC, 2PL losing out significantly to Doppel since those transcations are done serially.

Two phase locking for super high contention

atomic increments stil happen serially - fundamentally slow since everybody is still contending for the same variable.

LIKE Benchmark
--------------
-read a page's like count, read a user's last like.

Doppel splits the page-like counts for popular pages

those counts are also read more often

transactions need to be stashed in the split stage.

batching and doing the parallel reads in the join stage.
