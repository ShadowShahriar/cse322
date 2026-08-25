# Final Term Examination

## Topic List

1. **Lecture 1**
    - [**Uncertainty**](#uncertainty)
    - [**Causes of Uncertainty**](#causes-of-uncertainty)
    - [**Rational Decisions**](#11-how-rational-decisions-are-made-using-decision-theory)
    - [**Decision Tree**](#decision-tree)
    - [**Principle of MEU**](#principle-of-meu)
    - [**Probability**](#13-why-probability-is-needed)
    - [**Types of Probability**](#14-types-of-probability)
    - [**Random Variable**](#random-variable)
    - [**Probabilty Model**](#15-probabilty-model)
    - Joint Probability Distribution
    - Conditional Probability
    - Inference by Enumeration
    - Normalization
    - Conditional Independence
    - Bayes' Rule
    - Combining Evidence

2. **Lecture 2**
    - Bayesian Networks
    - Naive Bayes
    - Classification vs Regression
    - Bayesian Classification
    - Naive Bayes Models
    - NBC Advantages and Disadvantages
    - Bayes' Theorem
    - NBC Training Dataset

3. **Lecture 3**
    - Genetic Algorithm
    - GA Keywords and Terminology
    - GA Flowchart
    - Traveling Salesman Problem (TSP)
    - 0/1 Knapsack Problem

4. **Lecture 4**
    - Confusion Matrix
    - Types of Confusion
    - Support Vector Machines (SVM)
    - Regression Types

5. **Lecture 5**
    - Game Theory
    - Mini-Max
    - Alpha-Beta Pruning

6. **Lecture 6**
    - Single Layer Perceptron
    - Terminology
    - Artificial vs Biological Neuron

## Definitions

### Uncertainty

**Uncertainty** is the lack of complete, precise, or crystal-clear information when a system tries to make a prediction or decision.

- **Aleatoric Uncertainty:** Randomness that is built into the real world (like _rolling dice_ or _sudden weather changes_).

- **Epistemic Uncertainty:** A lack of knowledge or gaps in the training data that **can be fixed** by giving the AI more information.

[**↪ Topic List**](#topic-list)

### Causes of Uncertainty

- **Incomplete Data:** Missing sensor readings or hidden variables.
- **Noisy Inputs:** Blurry images or static in audio.
- **Dynamic Environments:** Surroundings that shift unpredictably over time.

[**↪ Topic List**](#topic-list)

### Decision Tree

A **decision tree** is a flowchart-like model that uses a hierarchy of questions and conditions to sort data, solve problems, or make predictions. It mimics human reasoning by breaking a complex choice into simple, step-by-step paths.

- <ins><b>Root node:</b></ins> The top starting point that looks at the whole dataset.
- <ins><b>Internal/Decision nodes:</b></ins> Points where the data is split based on a specific question or test.
- <ins><b>Branches:</b></ins> The lines that connect nodes, showing the outcome of a test or choice.
- <ins><b>Leaf/End nodes:</b></ins> The final predictions or categories at the end of the branches.

[**↪ 1.2. Rational Decision-Making Process**](#12-rational-decision-making-process)

### Principle of MEU

The Principle of MEU (**Maximum Expected Utility**) states that,

> "a rational agent should always choose the action that yields **the highest expected utility**, calculated by weighting the utility of **each possible outcome** by its probability."

[**↪ Topic List**](#topic-list)

### Random Variable

A **random variable** is a mathematical rule that assigns a specific numerical value to each possible outcome of a random event.

- A random variable has a domain of possible values,
- Each value has an assigned probability between 0 and 1,
- The values are mutually exclusive and complete

**Mutually Exclusive?** Disjoint. Only one of them are true.<br>
**Complete?** There is always one that is true.

A random variable: _Weather_

```
P(Weather=Sunny)  = 0.7
P(Weather=Rainy)  = 0.2
P(Weather=Cloudy) = 0.08
P(Weather=Snowy)  = 0.02
```

**The domain?**

```
<Sunny, Rainy, Cloudly, Snowy>
```

**Probability Distribution?**

```
P(Weather) = [0.7 0.2 0.08 0.02]
```

[**↪ Topic List**](#topic-list)

---

## Theoretical Questions

### 1.1. How Rational Decisions are made using Decision Theory?

Rational decisions are made using decision theory by,

- systematically identifying options,
- weighing probabilities and risks, and
- selecting the choice that maximizes personal value or expected utility.

```
Decision Theory = Probability Theory + Utility Theory
```

[**↪ Topic List**](#topic-list)

---

### 1.2. Rational Decision-Making Process

- **Define the problem:** Clearly state the goal or issue that requires a choice.
- **Identify criteria:** Determine which factors matter most (such as cost, time, or risk).
- **Weigh the criteria:** Assign relative importance or numerical values to each factor.
- **Generate alternatives:** List all possible courses of action.
- **Evaluate outcomes:** Use tools like a [**↪ Decision Tree**](#decision-tree) to map out options, potential consequences, and their likelihoods.
- **Maximize utility:** Select the alternative with the highest calculated payoff or satisfaction score.

[**↪ Topic List**](#topic-list)

---

### 1.3. Why Probability is needed?

Probability is a mathematical tool that measures the likelihood of an event or outcome so systems can reason and make decisions despite missing or noisy data.

Notation for unconditional probability for a proposition **A**:

```
P(A)
```

Axioms for probabilities:

```
[1]. 0 <= P(A) <= 1
[2]. P(True) = 1, P(False) = 0
[3]. P(A ∨ B) = P(A) + P(B) - P(A ^ B)
```

Probability is needed to-

- <ins><b>Handle uncertainty:</b></ins> Real-world data is often incomplete or unclear. Probability lets AI score multiple options rather than guessing a single hard answer.
- <ins><b>Make predictions:</b></ins> Models use past patterns to forecast future results, such as the _next word in a sentence_ or _weather trends_.
- <ins><b>Update beliefs:</b></ins> Using **Bayes' Theorem**, AI adjusts its conclusions as new evidence arrives.

[**↪ Topic List**](#topic-list)

---

### 1.4. Types of Probability

**Prior Probability:** The initial chance of an event happening before seeing any new evidence or data. For example, the general chance that an email is spam before reading its contents.

```
Prior = Before any evidence is obtained
```

Properties:

- ✅ Independent
- ✅ Unconditional

**Posterior Probability:** The updated chance of an event happening after new evidence or data is observed. For example, the chance an email is spam after seeing the word "winner" inside it.

```
Posterior = After the evidence is obtained
```

Properties:

- ⛔ Dependent
- ⛔ Conditional

[**↪ Topic List**](#topic-list)

---

### 1.5. Probabilty Model

A **probability model** is a mathematical description of a random situation that lists all possible outcomes and assigns a probability to each one.

**Sample Space (Ω):** The complete set of all possible results or outcomes (like _getting heads or tails when flipping a coin_).

**Events (ω):** Specific outcomes or combinations of outcomes you want to study. Also known as an _atomic event_.

```
ω ∈ Ω
```

**Probabilities:** Numbers from 0 to 1 assigned to each outcome, showing how likely they are to happen. The sum of all probabilities in the model must always equal 1.

```
[1]. 0 <= P(ω) <= 1
[2]. ∑(ω) P(ω) = 1
```

[**↪ Topic List**](#topic-list)
