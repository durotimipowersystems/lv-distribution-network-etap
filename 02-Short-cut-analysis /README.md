# Short-Circuit Analysis for a Low Voltage Distribution System

## 1. Objective
To determine the fault current level at the low-voltage bus and verify protection device adequacy.

## 2. System Description
Source: Utility Grid (33 kV, 500 MVAsc)
Transformer: 1 MVA, 33/0.415 kV, 5% impedance
Load: 0.75 MVA
Protection: Circuit Breaker (60 kA rating) 

## 3. Methodology

A 3-phase fault was simulated at the low-voltage bus using ETAP to determine the maximum fault current.

## 4. Results
Fault Current at LV Bus: 28.5 kA

## 5. Protection Validation
Breaker Rating: 60 kA → Adequate 
Fault Current: 28.5 kA → Within breaking capacity 

## 6. Engineering Interpretation

The high fault current is due to the low impedance of the transformer (5%), which allows a large current to flow during fault conditions.

The circuit breaker rating exceeds the fault current, ensuring safe interruption without equipment damage.

## 7. Key Insight

Fault current magnitude is primarily determined by system impedance. Lower impedance results in higher fault currents, requiring higher-rated protection devices.

## 8. Tools Used
ETAP 19.0
Short Circuit Analysis Module

## 9. Limitations
Simplified system (no motor contribution considered)
Protection coordination not included in this analysis