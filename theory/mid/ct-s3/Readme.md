## Section 3

<p align="center"><img src="3.jpg"/></p>

### 1(a). Scenario-based

#### i. Identify the type of intelligent agent used in this system.

<ins><b>Ans.:</b></ins> Model-Based Reflex Agent.

#### ii. Justify the answer by explaining how the characteristics and features of the system support the identified agent type.

<ins><b>Ans.:</b></ins> The **ICU patient monitoring system** is a Model-Based Reflex Agent because:

1. <ins><b>Uses sensors to perceive the environment</b></ins>
    - The system continuously collects data from sensors such as heart rate, blood pressure, oxygen level, and body temperature.
2. <ins><b>Maintains an internal state (model)</b></ins>
    - It stores each patient's previous health records and current condition.
    - This internal model helps the system understand the patient's health status over time.
3. <ins><b>Makes decisions based on current and past information</b></ins>
    - The system does not rely only on the current sensor reading.
    - It compares current data with stored patient history to detect abnormal conditions.
4. <ins><b>Performs automatic actions according to predefined rules</b></ins>
    - When oxygen level falls below a safe threshold or other abnormalities are detected, the system automatically alerts doctors and recommends appropriate actions.

<p align="center"><img src="../img09.png"/><br><i><u>figure 1(a).: Working diagram of a Model-Based Reflex Agent.</u></i></p>

Since the system observes the environment, maintains patient history (_internal state_), and takes actions based on both current and stored information, it is best classified as a **Model-Based Reflex Agent**.

---

<p align="center"><img src="4.jpg"/></p>

### 1(b). Uninformed Search Math

<ins><b>Ans.:</b></ins> Assuming successors are expanded from left to right.

We know, DFS explores the deepest node first.

<ins><b>Search Process</b></ins>

- Start at $S$
- Go to $A$
- From $A$, visit $B$
- From $B$, visit $C$
- From $C$, visit $G$ (**Goal found**)

---

[**↪ CT Archive**](https://shadowshahriar.github.io/cse322/theory/mid/#ct-archive)
