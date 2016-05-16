Writing Fast Code 1 by Andrei Alexandrescu
=========================================

1. Prefer 32 bits to any other size types.
2. Prefer unsigned to signed.
3. Double precision as fast as single precision.

Strength reduction
Don't waste time replacing a /= 2 with a >>= 1
add mult all take 1 cycle
FP division, remainder - quite expensive

int division, remainder - worst of all
Cannot afford for division

fewer indirect writes
regular access aptterns

optimize code judiciously for today's dynamics
good baselines

The Forgotten Parallelism
The ALU in the processor
