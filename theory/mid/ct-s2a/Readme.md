## Section 2A

**Question Setter**

```
Fawzia Fairooz
Lecturer
Dept. of CSE
```

### 1. Scenario-based

A company uses an autonomous robot to deliver medicines within a hospital. The robot navigates through corridors, avoids obstacles, identifies patient rooms, and delivers medicines to the correct location.

#### i. Construct the PEAS description for this intelligent agent.

<ins><b>Ans.:</b></ins> PEAS is a foundational framework used to specify, design, and evaluate the task environment of an intelligent agent. Here is the PEAS description for the Autonomous Hospital Medicine Deliver Robot:

<ins><b>PERFORMANCE MONITOR (P):</b></ins>

- Deliver medicines to the correct patient room,
- Minimize delivery time,
- Avoid collisons,
- Ensure safety,
- Conserve battery power,
- Complete tasks successfully.

<ins><b>ENVIRONMENT (E):</b></ins>

- Hospital corridors,
- Patient rooms,
- Nurses, doctors,
- Elevators, walls, doors,
- Moving obstacles.

<ins><b>ACTUATORS (A):</b></ins>

- Wheels/motors for movement,
- Robotic arm or medicine dispenser,
- Door/elevator control interface,
- Speaker or display for communication.

<ins><b>SENSORS (S):</b></ins>

- Cameras,
- LiDAR, ultrasonic sensors,
- GPS/indoor localization sensors,
- RFID/barcode scanners,
- Proximity sensors,
- OMR sensors.

#### ii. Identify the environment type of this agent.

<ins><b>Ans.:</b></ins> The agent operates in a **Partially Observable**, **Dynamic**, and **Stochastic** environment.

1. <ins><b>Partially Observable:</b></ins>
    1. The robot cannot always observe the entire hospital environment.
    2. Obstacles may suddenly appear around corners or behind doors.

2. <ins><b>Dynamic:</b></ins>
    1. The environment changes while the agent is operating.
    2. People, wheelchairs, and equipment move continuously.

3. <ins><b>Stochastic:</b></ins>
    1. Outcomes are uncertain.
    2. Sensors may have errors and human movement might interfere.

---

### 2. Theoretical with example

Why do Goal-based Agents often require search and planning techniques? Explain with an example.

<ins><b>Ans.:</b></ins> A goal-based agent chooses actions that help achieve a specific goal. To reach the goal, it must determine the sequence of actions that is best suitable from the current state to the desired state.

<ins><b>Significance of Searching:</b></ins>

1. There may be many possible actions.
2. The agent searches through possible states, finding a path to the goal.

<ins><b>Significance of Planning:</b></ins>

1. The agent must organize actions in the correct order.
2. Planning helps minimize cost, time, or distance.

<ins><b>Example:</b></ins>

Consider a robot whose goal is to deliver medicine from the pharmacy to room no. 408.

- **Goal:** Reach room no. 408.
- **Search:** Find possible routes.
- **Planning:** Select the shortest and safest route avoiding crowded areas and obstacles.

Thus, goal-based agents use "Search" to find possible solutions and "Planning" to choose and execute the best one.

---

### 3. Scenario-based

A company develops a virtual assistant that can understand spoken commands such as "set an alarm for 7 AM" and answer customer questions in English. Which branch(es) of AI are involved in developing this system?

<ins><b>Ans.:</b></ins> There are several branches of AI involved in developing this intelligent system.

1. <ins><b>Natural Language Processing (NLP):</b></ins>
    1. Allows the system to interpret human language.
    2. Extract the user's intent from spoken commands.

2. <ins><b>Speech Recognition (SR):</b></ins>
    1. Converts spoken words into text.
    2. Allows users to interact using voice commands.

3. <ins><b>Machine Learning (ML):</b></ins>
    1. Improves understanding and response quality through training on large datasets.
    2. Helps recognize different accents and question patterns.

---

[**↪ CT Archive**](https://shadowshahriar.github.io/cse322/theory/mid/#ct-archive)
