Coordinated Overcurrent Protection Design for a Low Voltage Distribution System

1. PROBLEM STATEMENT 
Design a protection scheme for a 0.75 MVA low-voltage load supplied through a 1 MVA transformer, ensuring proper coordination between downstream and upstream circuit breakers to achieve selectivity, reliability, and equipment protection.

2. SYSTEM DESCRIPTION
Source: Utility Grid (33 kV)
Transformer: 1 MVA, 33/0.415 kV, 5% impedance
Load: 0.75 MVA
Protection Devices:
CB1 (Load protection)
CB2 (Transformer backup protection)
Measurement: Current Transformer (1500/5)

3. CALCULATIONS
Full Load Current
I= (0.75x10^6)/(√3x415) = 1043A

Relay Pickup
I pickup =1.15×1043≈1200A

Instantaneous Range
I inst =8×I FLC →12×I FLC
	​=8000A→12000A

4. PROTECTION DESIGN
 CB1 (Downstream)
Pickup = 1200 A
Time delay = 0.3 s
Instantaneous = 8000 A

CB2 (Upstream)
Pickup = 1300 A
Time delay = 0.7 s
Instantaneous = 12000 A
5. PROTECTION PHILOSOPHY (THIS IS CRITICAL)

The protection scheme is designed to ensure selectivity by allowing the downstream breaker (CB1) to clear load-side faults first, while the upstream breaker (CB2) operates with a time delay to provide backup protection. Instantaneous settings are graded to prevent upstream tripping during downstream faults while ensuring rapid fault clearance for high-magnitude faults near the source.

6. COORDINATION LOGIC
Time grading margin = 0.4 s
CB2 delay > CB1 delay ✔
CB2 instantaneous > CB1 instantaneous ✔

7. RESULTS / EXPECTED BEHAVIOR
Fault Location	Expected Operation
Load	CB1 trips
CB1 fails	CB2 trips (backup)
Near transformer	CB2 trips instantly

8. CHALLENGES & LIMITATIONS
ETAP relay curve library unavailable
Used logical design instead of full TCC visualization
Focused on engineering reasoning over software output

9. KEY TAKEAWAYS

Effective protection design requires coordination of both time and current to ensure selective fault clearing while minimizing system disruption.