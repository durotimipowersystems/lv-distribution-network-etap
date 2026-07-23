# Coordinated Overcurrent Protection Design for a Low Voltage Distribution System

## 1. Objective

Design a coordinated overcurrent protection scheme for a 0.75 MVA low-voltage load supplied through a 1 MVA transformer.  
The goal is to achieve **selectivity, reliability, and effective fault isolation** using time-current coordination principles.

## 2. System Description

- **Source:** Utility Grid (33 kV, 500 MVAsc)  
- **Transformer:** 1 MVA, 33/0.415 kV, 5% impedance  
- **Load:** 0.75 MVA lumped load  
- **Protection Devices:**  
  - **CB1:** Downstream breaker (load protection)  
  - **CB2:** Upstream breaker (transformer backup protection)  
- **Measurement:** Current Transformer (1500/5 ratio)  

## 3. Engineering Calculations

### Full Load Current

\[
I = \frac{0.75 \times 10^6}{\sqrt{3} \times 415} = 1043 \, A
\]

---

### Relay Pickup Current

\[
I_{pickup} = 1.15 \times I_{FLC} \approx 1200 \, A
\]

> Pickup is set above full load current to prevent nuisance tripping while maintaining sensitivity to overload conditions.

---

### Instantaneous Trip Range

\[
I_{inst} = 8 \times I_{FLC} \rightarrow 12 \times I_{FLC}
\]

\[
= 8000 \, A \rightarrow 12000 \, A
\]

> Instantaneous protection ensures rapid clearing of high-magnitude fault currents.

---

## 4. Protection Design

### 🔹 CB1 (Downstream — Load Protection)

- Pickup Current: **1200 A**  
- Time Delay: **0.3 s**  
- Instantaneous Trip: **8000 A**  

---

### 🔹 CB2 (Upstream — Transformer Backup Protection)

- Pickup Current: **1300 A**  
- Time Delay: **0.7 s**  
- Instantaneous Trip: **12000 A**  

---

## 5. Protection Philosophy

The protection scheme is designed to ensure **selective coordination** between protective devices.

- The downstream breaker (CB1) is configured to clear faults at the load level.
- The upstream breaker (CB2) operates with a **time delay margin** to provide backup protection.
- Instantaneous settings are graded to prevent unnecessary upstream tripping during downstream faults.

This approach ensures that:

> Only the faulted section is isolated while the rest of the system remains energized.

---

## 6. Coordination Strategy

- **Time Grading Margin:** 0.4 s  
- **Selectivity Condition:**  
  - CB2 delay > CB1 delay ✔  
  - CB2 instantaneous > CB1 instantaneous ✔  

---

## 7. Expected System Behavior

| Fault Location        | Protective Response              |
|----------------------|---------------------------------|
| Load (Downstream)    | CB1 trips                       |
| CB1 fails            | CB2 trips after delay (backup)  |
| Near Transformer     | CB2 trips instantaneously       |

---

## 8. Challenges & Limitations

- ETAP relay curve library was unavailable in this setup  
- Time-Current Coordination (TCC) curves could not be fully visualized  
- Protection design validated using engineering calculations and logic  

---

## 9. Key Takeaways

- Effective protection design requires coordination of both **current magnitude** and **time delay**  
- Selectivity ensures minimal system disruption during faults  
- Backup protection is essential for system reliability  

---

## 10. Tools Used

- ETAP (Electrical Power System Analysis Software)  
- Manual Engineering Calculations  

---
