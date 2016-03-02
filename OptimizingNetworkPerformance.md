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

##Simple Cache on Android
Need to do a number of context switches - a check on the filesystem.

Avoid context switches and going back to disk.

Blue line is the original, with latency

Speculative optimizations: Preresolve, prerender, prefetch improvements

allowing multiple simultaneous prerender tasks.

More aggressive optimzation on mobile

Detachable prefetch


##Protocols and optimization as a service

SPDY - target 50% reduction in PLT latency.

Minimize deployment complexity.

Enable more secure browsing.

Enable multiplexing, prioritization.

SPDY as an experimental step for HTTP/2.

20-40-50% latency as compared to HTTPS.

High RTT such as mobile.

##Quick UDP Internet Connections(QUIC)

Tunneling protocol, running atop UDP, which can multiplex a large number of streams between two endpoints.

Makes headway on its own and delivers performance improvements/

TCP and TLS leverage techniques.

##Chrome Data Compression

Convert images to WebP
Text: applies gzip

Runs over SPDY
DNS late-binding, secure browsing

Secure traffic goes direct
proxy is not used for HTTPS

Not rendering it on Google servers, everything done on the phone.

WebSocket Compression
