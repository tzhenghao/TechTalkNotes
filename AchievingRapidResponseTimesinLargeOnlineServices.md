## Speaker: Jeff Dean

##Basic Latency Reduction Techniques


	1. Differentiated service classes
	2. Reduce head-of-line blocking
		a. Defer opportunities till at night or something


##Fault tolerance
- make a reliable whole out of unreliable parts
- Worried about hard drive crashing, machine power supply screws up

##Tolerable variability - Happens thousands of times a second in large scale

##Latency Tolerating Techniques

	1. Cross request adaptation
		a. Examine recent behavior
		b. Time scale: 10s of seconds to minutes
	2. Within request adaptation
		a. Cope with slow subsystems in context of higher level request

Solution - fine-grained dynamic partitioning

More than 1 partition per machine
BigTable, query serving system, GFS.

More than one piece per machine. - example: GFS - break down files to 64MB chunks
Good for load balancing

##Speeding Failure Recovery
If machine dies, we need to reassign to other machines.

##Selective Replication
	- Make more replicas of it.
	- Both static + dynamic
	- More replicas of Chinese documents as Chinese documents increase.

##Latency-Induced Probation
Servers can be slow to respond
Could be data dependent - due to interference effects
Return service to machine if machine somehow "works better".

##Within Request Variability

Data Independent Failures - Concurrent request becomes shitty.
Takes a long time to recover.
Solution: Canary Requests.

##Canary Requests
Send to just one machine first, then check if the request returns.

##Backup Requests
With Cross-Server Cancellation
