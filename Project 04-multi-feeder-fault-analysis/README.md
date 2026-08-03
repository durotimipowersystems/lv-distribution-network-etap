PROJECT 3: Fault Analysis & Protection Coordination in a Multi-Feeder LV Network

1. PROBLEM STATEMENT

Design and analyze a protection scheme for a low-voltage distribution system with multiple feeders, ensuring:

Proper fault detection
Correct breaker operation sequence
Selective isolation of faults
Reliable backup protection

2. SYSTEM DESCRIPTION
Source: Utility Grid (33 kV, 500 MVAsc)
Transformer: 1 MVA, 33/0.415 kV, 5% impedance
Main Bus: 0.415 kV distribution bus
Feeders:
Feeder 1 → Load 1 (0.75 MVA)
Feeder 2 → Load 2 (0.5 MVA)

3. PROTECTION ARCHITECTURE
Device	Location	Function
CB1	Feeder 1	Protects Load 1
CB3	Feeder 2	Protects Load 2

CB2	Upstream (Main)	Transformer & system backup
4. LOAD CALCULATIONS
Load 1 Current:
I=
3
	​

×415
0.75×10
6
	​

=1043A
Load 2 Current:
I=
3
	​

×415
0.5×10
6
	​

=695A

5. PROTECTION SETTINGS
CB1 (Feeder 1)
Pickup = 1200 A
Time Delay = 0.3 s
Instantaneous = ~8300 A

CB3 (Feeder 2)
Pickup = 1000 A
Time Delay = 0.3 s
Instantaneous = ~7200 A

CB2 (Upstream Backup)
Pickup = 1200 A
Time Delay = 0.5 s
Instantaneous = ~10000 A

6. PROTECTION PHILOSOPHY
The system is designed using selective coordination principles:

Downstream breakers (CB1, CB3) clear faults first
Upstream breaker (CB2) operates only as backup
Time delays are graded to ensure proper fault isolation hierarchy

7. SHORT CIRCUIT ANALYSIS RESULTS
Case 1: Fault at Load 1 Bus
Fault Current ≈ 3.8 – 4 kA
CB1 carries full fault current → Trips
CB2 acts as backup if CB1 fails

Case 2: Fault at Load 2 Bus
Fault Current ≈ 2.5 – 3 kA
CB3 carries full fault current → Trips
CB2 acts as backup
Case 3: Fault at Main Bus
Fault Current ≈ 28.9 kA
CB2 sees highest fault current → Instant trip
CB1 & CB3 remain stable (not in primary fault path)

8. COORDINATION LOGIC
Time Grading:
CB1 = 0.3 s
CB3 = 0.3 s
CB2 = 0.5 s
Instantaneous Grading:
CB2 > CB1 & CB3 

9. ENGINEERING INTERPRETATION
Fault current flows toward the fault from the source
The nearest breaker to the fault carries the highest current
Proper coordination ensures:
Only the faulted section is isolated
The rest of the system remains operational

10. KEY INSIGHTS
Fault current distribution depends on network impedance paths
Misreading branch currents can lead to wrong conclusions
Selectivity is achieved through:
Current grading
Time delay coordination
Backup protection is essential for system reliability

11. LIMITATIONS
ETAP relay curve library was unavailable
Analysis focused on:
Logical coordination
Current distribution understanding
Full TCC curve validation not performed

12. CONCLUSION
The protection system successfully achieves:

Selective fault isolation
Reliable backup protection
Fast clearing of high-magnitude faults

This project demonstrates practical understanding of:

 Fault analysis
 Protection coordination
 Multi-feeder system behavior

13. FILES INCLUDED
ETAP Project File
Single Line Diagram (SLD)
Fault Analysis Screenshots
Protection Settings Documentation