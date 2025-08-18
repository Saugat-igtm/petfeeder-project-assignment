# Output Conditions

## Output 1 (O1)
O1 = Dispenser weight changes only when **all four inputs are HIGH**.  

**Formula:**
O1 = A AND B AND C AND D

---

## Output 2 (O2)
O2 = Alert is sent only when **pets do not eat**, **bin is not empty**, and **sensor is not working**.  

**Formula:**
O2 = NOT (A AND C AND D)

---

## Input Definitions
- A = Pet eats  
- B = Bowl empty  
- C = Food bin full  
- D = Sensor OK  

---

## Test Scenarios

| A (pet eats) | B (bowl empty) | C (food bin full) | D (sensor ok) | O1 (disp weight changes) | O2 (alert sent) |
|--------------|----------------|-------------------|---------------|--------------------------|-----------------|
| 0 | 0 | 0 | 0 | 0 | 1 |
| 0 | 0 | 0 | 1 | 0 | 1 |
| 0 | 0 | 0 | 0 | 0 | 1 |
| 0 | 0 | 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 1 |
| 0 | 1 | 1 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 | 0 | 1 |
| 0 | 1 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 0 | 0 | 1 |
| 1 | 0 | 0 | 1 | 0 | 1 |
| 1 | 0 | 0 | 0 | 0 | 1 |
| 1 | 0 | 0 | 1 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 1 | 0 | 1 |
| 1 | 1 | - | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 | 1 | 0 |

---

## Summary
- O1 → Active only when `A=1, B=1, C=1, D=1`  
- O2 → Alert sent unless *pets eat*, *food bin is full*, or *sensor is OK*  
