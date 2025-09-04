# MOD-59 Digital Clock (Skip 56)

## 📌 Project Overview
This project implements a **digital clock** using **T flip-flops, logic gates, and counters** in Logisim.  
The clock is designed to **skip pulse 56** in seconds and minutes, ensuring proper synchronization.  
It displays time using **seven-segment displays** and counts up to **24 hours**.

---

## 🎯 Objectives
- Understand the mechanism of a digital clock.
- Design a clock that skips the 56th pulse in seconds and minutes.
- Explore asynchronous counters and flip-flops.
- Derive equations for T flip-flops and implement them.
- Use seven-segment displays for visual output.
- Build and simulate the digital clock in **Logisim**.

---

## 🛠 Required Components
- **Logic Gates:**  
  - NOT (6)  
  - AND (19)  
  - OR (9)  
  - NOR (3)  
  - XOR (1)  
  - XNOR (2)  
- **T Flip-Flop (7)**  
- **Clock Pulse Generator**  
- **7-Segment Display (6)**  

---

## 🔢 Counter Design

### 0–9 Counter
Implemented using **4 T flip-flops** to hold 4 bits.

**Functions:**

T0 = T1T2T3 + T0T3<br/>
T1 = T2T3<br/>
T2 = T0’T3<br/>
T3 = 1<br/>

### 0–5 Counter
Implemented using **3 T flip-flops**.

**Functions:**

T0 = T0T2 + T1T2<br/>
T1 = T0’T2<br/>
T2 = 1<br/>

---

## 🔡 BCD to 7-Segment Decoder
Binary numbers are converted into decimal and displayed on **7-segment displays**.  

**Expressions:**

X = b’d’ + c + bd + a<br/>
Y = b’d’ + c + bd + a<br/>
Z = c’ + d + b<br/>
U = b’d’ + b’c + cd’ + bc’d + a<br/>
V = bd’ + cd’<br/>
W = c’d’ + bc’ + bd’ + a<br/>
S = b’c + bc’ + bd’ + a<br/>

---

## ⏱ Skip 56 in Seconds & Minutes
To skip **56**, the circuit checks when:
- Units counter = 6  
- Tens counter = 5  

If both match, the preset input of the last flip-flop is triggered, skipping pulse 56.

---

## 🕒 Hour Counter
- Counts **1 to 24** using the same 0–9 and 0–5 counters.  
- When the counter reaches **24**, it resets to **01** using preset pins.

---

## 🔗 Circuit Integration
1. Built an **IC for Seconds Counter** (also used for Minutes).  
2. Designed a separate **Hour Counter Circuit**.  
3. Combined all modules for full clock functionality.

---

## 📷 Preview
<img width="602" height="290" alt="image" src="https://github.com/user-attachments/assets/71f4f360-f3f0-4b48-8667-13a05edbdd86" />


## ✅ Conclusion
This project demonstrates:
- Practical application of **digital electronics concepts**.  
- Design and implementation of **counters, flip-flops, and decoders**.  
- Building a **skip functionality** in a digital clock.  

---

## 👤 Author
**Name:** Sree Shuvo Kumar Joy  
**Roll:** 2107116  
**Group:** B2  
**Course:** Digital Logic Design Laboratory  
**Institution:** KUET  
