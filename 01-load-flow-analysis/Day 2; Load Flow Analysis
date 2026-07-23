🟦 Day 2: Load Flow Analysis — First Functional Model
🎯 Objective:
Build a simple power system and successfully run Load Flow Analysis in ETAP.

🟦 Day 2

What I did:
Built a complete system: Grid → Transformer → Bus → Load in ETAP
Configured grid (33 kV, 500 MVAsc)
Added transformer (33 / 0.415 kV, 1 MVA)
Ran Load Flow Analysis with different load values

What I learned:
How to run Load Flow Analysis in ETAP
Importance of setting a Swing Bus for system stability
Transformer impedance and X/R ratio affect system behavior
Grid strength (MVAsc) impacts voltage stability
Voltage must stay within 95%–105% for acceptable operation

Problems faced:
Bus voltage mismatch errors
System not converging
Transformer and cable impedance initially set to 0
Some buses were not energized due to connection issues
Grid strength was too low
Load values were unrealistic

How I solved it:
Set the Grid as Swing Bus
Increased grid strength to 500 MVAsc
Defined transformer impedance (5%) and X/R ratio (10)
Corrected all system connections (topology)
Ensured all components had proper electrical data
Reduced load to realistic values

Key observation:
As load increases, voltage drops across the system
At 0.8 MVA load, voltage remained stable (~97.82%)
At 2 MVA load, voltage dropped below acceptable limit (~94.18%)
Transformer became overloaded (~200%) at high load
A system can run in ETAP but still be physically unrealistic if ratings are exceeded.
