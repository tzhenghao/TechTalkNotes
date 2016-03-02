Optimizing network performance - Chrome Dev Summit 2013 (Ilya Grigorik)

##Speaker: Ilya Grigorik

Core Chrome improvements

M26 - Async DNS resolver replaces system default.

parallel A/AAAA resolution

adaptive retry timeout (remember which DNS server to use)

adaptive DNS server selection (based on observed performance)

M27 - 5% better speed index score

Replaced the scheduler on perceived performance - speed index over page load time.

Pages were competing on bandwidth. The new scheduler will only load 10 images in parallel.

SPDY - send priorities to server - won't delay on client
