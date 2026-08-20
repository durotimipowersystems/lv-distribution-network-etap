1. Problem Statement

Design and analyze a low-voltage distribution system to identify and mitigate voltage drop issues affecting downstream loads.

The goal is to:

Maintain acceptable voltage levels (≥ 90%)
Identify root causes of voltage drop
Apply engineering solutions such as cable sizing and load optimization

2. System Description
Source: Utility Grid (33 kV, 500 MVAsc)
Transformer: 1 MVA, 33/0.415 kV, 5% impedance
Main Bus: 0.415 kV distribution bus
Feeders:
Feeder 1 → Load 1
Load: 0.2 MVA
Connected via Cable11
Feeder 2 → Load 2
Load: 0.3 MVA
Connected via Cable12

3. Load Flow Analysis

Load flow analysis was performed in ETAP to evaluate:

Bus voltages
Power flow
System performance under steady-state conditions
4. Initial Results (Problem Identified)
Location	Voltage (%)	Status
Bus24 (Load 1)	~88%	Low
Bus23 (Load 2)	~68%	Critical

5. Root Cause Analysis

The major cause of voltage drop was identified as:

High feeder impedance due to undersized cables and long cable length

6. Engineering Tests Performed
Test 1: Transformer Upgrade
Increased transformer capacity
Result: Minimal improvement

Conclusion: Source strength was NOT the limiting factor

Test 2: Load Reduction
Reduced load demand
Result: Voltage improved significantly

Conclusion: High current contributed to voltage drop

Test 3: Cable Size Optimization (KEY SOLUTION)
Cable size increased from:
16 mm² → 50 mm²
Result:
Location	Voltage (%)	Status
Bus23 (Load 2)	~90%	Acceptable
Bus24 (Load 1)	~88%	Slightly low

7. Engineering Interpretation
Voltage drop is primarily influenced by feeder impedance, not transformer size
Increasing cable size reduces resistance and improves voltage profile
Long cable runs with small conductors significantly degrade system performance

8. Key Equation
V
drop
	​

∝I×(R+jX)

Where:

I = Load current
R = Resistance (dominant factor in LV systems)
X = Reactance

9. Final Solution

Increase feeder cable size
Optimize conductor selection
Maintain voltage ≥ 90%

10. Key Takeaways
Voltage issues are often distribution problems, not generation problems
Cable sizing is critical in LV network design
Engineering decisions must be based on system behavior, not assumptions
Simulation tools like ETAP are essential for validating designs

11. Simulation Results

Add screenshots here

![Load Flow Results](assets/loadflow.png)
![Voltage Profile](assets/voltage_profile.png)

12. Tools Used
ETAP (Load Flow Analysis)
Electrical Engineering Calculations
Power System Design Principles

13. Project Insight

This project demonstrates practical understanding of:

Load flow analysis
Voltage drop mitigation
Feeder design optimization
Real-world power system problem-solving