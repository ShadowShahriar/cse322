# Mid Term Examination

## Topic List

1. **Lecture 1**
    - Artificial Intelligence ✔️
    - Significance of Studying AI ✔️
    - Applications of AI ✔️
    - Relevant Fields of AI ✔️
    - Goals of AI
    - Turing Test
    - Building an Intelligent Agent
    - Strong AI vs Weak AI
    - Importance of AI
    - Alan Turing

2. **Lecture 2**
    - Knowledge and Data
    - Intelligent Agent
    - Task Environment
    - Types of Agent
    - Learning
    - Classification (_Partial_)

3. **Lecture 3**
    - Problem Types
    - State Space
    - 8 Puzzle Game
    - Searching
        - Tree Searching
        - Searching Strategies
        - Evaluating Search Methods
    - Uninformed Searching Methods
        - Breadth-First Search (BFS)
        - Depth-First Search (DFS)
        - BFS vs DFS
        - Depth Limited Search (DLS)
        - Iterative Deepening Search (IDS)
        - Uniform-Cost Search (UCS)
        - Bidirectional Search

4. **Lecture 4**
    - Informed (Heuristic) Searching Methods
        - Simple Hill Climbing
        - A\* Algorithm

## Definitions

### Artificial Intelligence

Artificial intelligence (**AI**) is a branch of computer science focused on building systems capable of performing tasks that typically require human intelligence.

- AI is a way of **making machines think** and **behave intelligently**. These machines are controlled by intelligent softwares.
- AI is a science of **finding theories** and **methodologies**.
- AI helps machines **understand the world** and **react to situations** accordingly.
- AI is closely related to the study of human brain. By mimicking the way the human brain learns, thinks, and takes action, we can build a machine that can do the same.

## Theoretical Questions

### 1.1. Why do we need to study AI?

AI has the ability to impact every aspect of our lives.

> Studying Artificial Intelligence is essential because it equips us to **navigate the rapidly evolving future**, **unlock highly lucrative career opportunities** across all industries, and **solve complex global challenges** by automating tasks and generating data-driven insights.

Studying AI offers several practical and long-term benefits:

1. <ins><b>Future-Proofing One's Career:</b></ins> AI skills are in high demand across nearly every sector. So, understanding AI prevents career obsolescence.

2. <ins><b>Solving Real-World Problems:</b></ins> AI enables us to tackle massive global challenges, such as climate change, disease detection, and scientific research, by identifying patterns in massive datasets.

3. <ins><b>Boost Efficiency and Automation:</b></ins> AI helps us automate tedious, repetitive tasks, freeing up our precious time for higher-level strategic and creative works.

4. <ins><b>Drive Ethical Innovation:</b></ins> As AI slowly becomes pervasive, there is a critical need for professionals who understand how to develop and manage these technologies responsibly, addressing issues of privacy, bias, and fairness.

---

### 1.2. How AI works?

The progression from raw facts to actionable insight is typically explained using the **DIKW model** (Data, Information, Knowledge, Wisdom).

<p align="center"><img src="img01.png"/><br><i><u>figure 1.2.: DIKW model.</u></i></p>

1. <ins><b>Data:</b></ins> Unprocessed, unorganized facts.

    > 1010110, 98.6

2. <ins><b>Information:</b></ins> The data is **processed** using ingestion pipelines and ML. It adds meaning by **structuring it** into tables, trend lines, or vectors.

    > "98.6 is a patient's temperature."

3. <ins><b>Knowledge:</b></ins> AI utilizes pattern recognition and neural networks to establish relationships between datasets. It answers _why_ things happen based on historical correlations.

    > "98.6°F is a normal human temperature; anything above 100°F indicates a fever and usually correlates with an infection."

4. <ins><b>Wisdom:</b></ins> **True wisdom requires foresight, ethics, and human conscience.** The AI provides the **Knowledge**, but the human applies the **Wisdom** to make the final ethical, strategic, or long-term decision.

---

### 1.3. Applications of AI

1. <ins><b>Computer Vision (CV)</b></ins>
    - Deals with visual data, (images and videos)
    - Understand content and extract insights.

    > **Example:** Automated Food Delivery Robot.

2. <ins><b>Natural Language Processing (NLP)</b></ins>
    - Deals with text content,
    - Interacts with natural language.
    - Includes **STT** (Speech to Text) and **TTS** (Text to Speech)

    > **Examples:**
    >
    > - Deliver accurate search results.
    > - Detect malicious/harmful/hate speech.

3. <ins><b>Speech Recognition (SR)</b></ins>
    - Hear and understand spoken words.

    > **Example:** Google Assistant.

4. <ins><b>Expert Systems (ES)</b></ins>
    - Systems like this provide advice or make decisions.

    > **Working Fields:** Finance, Medicine, Marketing.

5. <ins><b>Games</b></ins>
    - Design intelligent agents that complete with human players.

    > **Example:** GTA-V.

6. <ins><b>Robotics</b></ins>
    - Combines many concepts of AI.
    - Consists of sensors and actuators.
    - Capable of adapting to new environments.

    > **Example:** Roomba.

---

### 1.4. Expert Systems of AI

An Expert System is a branch of Artificial Intelligence designed to simulate the decision-making ability of a human expert.

An expert system consists of three main parts:

1. <ins><b>Knowledge Base:</b></ins> The "library" that stores all facts, data, and rules specific to the domain (e.g., medicine, engineering, finance)

2. <ins><b>Inference Engine:</b></ins> The "brain" of the system. It applies logical reasoning to the knowledge base to analyze user inputs and deduce a solution.

3. <ins><b>User Interface:</b></ins> The communication layer that allows a user to input a problem and receive a recommendation or diagnosis.

<p align="center"><img src="img02.png"/><br><i><u>figure 1.4.: Working of Expert Systems.</u></i></p>

Unlike many modern AI "black boxes," expert systems are highly interpretable. They use a few specific methods to reach conclusions:

1. <ins><b>If-Then Rules:</b></ins> Knowledge is often stored as statements like:

    ```
    IF symptom A AND symptom B, THEN disease C
    ```

2. <ins><b>Forward Chaining:</b></ins> Starts with known facts and applies rules to find a conclusion.

    > "Checking symptoms to determine a diagnosis."

3. <ins><b>Backward Chaining:</b></ins> Starts with a specific goal and works backward to find evidence that supports it.

    > "Verifying if a user has diabetes by looking for supporting symptoms."

---

### 1.5. Sensors vs Actuators

| Sensors                                                                                                  | Actuators                                                                                                                     |
| :------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------- |
| The Inputs                                                                                               | The Outputs                                                                                                                   |
| Sensors detect physical or chemical changes in the environment and convert them into electrical signals. | Actuators receive these processed signals and convert them back into physical actions, such as movement, heat, or fluid flow. |
| Sensors are placed at the input port of a system to monitor and measure properties.                      | Actuators are placed at the output port to manipulate continuous or discrete process parameters.                              |

---

### 1.6. Relevant Fields of AI

1. <ins><b>Machine Learning and Pattern Recognition</b></ins>
    - Design and develop software that learn from data.
    - The learning models make prediction of unknown data.
    - Limited to dataset (`small dataset = less learning`)

    <p align="center"><img src="img03.png"/><br><i><u>figure 1.6.: ML model creation.</u></i></p>

2. <ins><b>Logic-based AI</b></ins>
    - A set of statements in logical form (mathematical logic) that express facts and rules about a particular problem domain.
    - **Domain:** Pattern Matching, Language Parsing, Semantic Analysis.

3. <ins><b>Searching</b></ins>
    - A large number of possibilities are given, pick the most optimal one.
    - **Domain:** Chess, Networking, Resource Allocation, Scheduling.

4. <ins><b>Knowledge Representation</b></ins>
    - Facts represented as mathematical possibilities, tables, and organized datasets.
    - **Domain:** Summarize content (Gemini)

5. <ins><b>Planning</b></ins>
    - Optimal planning gives maximum returns with minimum costs.
    - Starts with a goal statement in a particular situation.
    - Generates the most optimal plan to achieve the goal.

6. <ins><b>Heuristics</b></ins>
    - Heuristics are rules-of-thumb, educated guesses, or "smart shortcuts" used to solve complex problems more efficiently.
    - Instead of calculating every possible solution—which can take an impractical amount of time or computing power-heuristics guide an AI to quickly find a _"good enough"_ answer. **Domain:** Chess, 8-Puzzle.
    - For complex problems, testing every option (called a _"brute-force"_ or exhaustive search) is often impossible. Heuristics allow AI to bypass improbable or inefficient paths and focus only on the most promising ones. **Domain:** Indexing, Search Engine.

7. <ins><b>Genetic Programming (GP)</b></ins>
    - Genetic Programming is a subfield of artificial intelligence where computers automatically write and evolve executable code by mimicking biological evolution.

---

## CT Questions
