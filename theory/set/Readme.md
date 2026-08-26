# Problem Sets

Curated by **Ifat Metu**.<br>
Solved by **Shayan Shahriar**.

## Set A

<p align="center"><img src="img01.jpg" width="70%"/></p>

[**↪ Solution 1**](#ans-to-the-ques-no-1)<br>
[**↪ Solution 2**](#ans-to-the-ques-no-2)<br>
[**↪ Solution 3**](#ans-to-the-ques-no-3)<br>

### <ins>Ans to the Ques no. 1</ins>

Given here,<br>
Maximum truck capacity = **10 kg**<br>
5 items: **`A, B, C, D, E`**

#### 1. Initialize 5 chromosomes then apply single point crossover at point 3.

<ins><strong>Ans.:</strong></ins> Since there are 5 items, each chromosome has **5 binary genes**:

```
[A B C D E]
```

where:

- 1 = item is selected
- 0 = item is **NOT** selected

We initialize 5 chromosomes:

| Chromosome |   A |   B |   C |   D |   E |  Weight | Value/Fitness |
| ---------- | --: | --: | --: | --: | --: | ------: | ------------: |
| **C1**     |   1 |   1 |   0 |   0 |   1 |    7 kg |            58 |
| **C2**     |   1 |   0 |   1 |   1 |   0 | _11 kg_ |            95 |
| **C3**     |   0 |   1 |   1 |   0 |   1 |    9 kg |            72 |
| **C4**     |   1 |   0 |   0 |   1 |   1 |    9 kg |            78 |
| **C5**     |   0 |   1 |   0 |   1 |   0 |    8 kg |            70 |

Here, **C2** has a weight of **11 kg**, which exceeds the **10 kg** capacity. So, we assign it a fitness score of 0. (penalty for an infeasible solution)

| Chromosome                 | Weight | Fitness |
| -------------------------- | -----: | ------: |
| **C1**&nbsp;=&nbsp;`11001` |      7 |      58 |
| **C2**&nbsp;=&nbsp;`10110` |     11 |   **0** |
| **C3**&nbsp;=&nbsp;`01101` |      9 |      72 |
| **C4**&nbsp;=&nbsp;`10011` |      9 |      78 |
| **C5**&nbsp;=&nbsp;`01010` |      8 |      70 |

Now, a crossover at point 3 means we cut after the third gene.

```
A B C | D E
```

We consider two parents:

```
C1 = 110 | 01
C4 = 100 ∣ 11
```

and exchange the portions after point 3:

```
O1 = 110 | 01 → 11001
O2 = 100 | 01 → 10001
```

**Calculating fitness values:**

```
O1 = 11011
```

This selects:

- **A = 2 kg**, value 18
- **B = 3 kg**, value 25
- **D = 5 kg**, value 45
- **E = 2 kg**, value 15

Total weight:

```
2 + 3 + 5 + 2 = 12 kg
```

Since: `12 > 10`, it is invalid.

Its fitness can therefore be assigned **0**.

```
O2 = 10001
```

This selects **A** and **E**.

Total weight:

```
2 + 2 = 4 kg
```

Fitness value:

```
18 + 15 = 33
```

[**↪ Problem Set**](#set-a)

#### 2. Apply mutation after crossover.

<ins><strong>Ans.:</strong></ins> Mutation means randomly changing one or more bits. Suppose, the mutation occurs at **gene 4** of **O2**:

```
1 0 0 0 1
      ↑

1 0 0 1 1
```

```
10001 → 10011
```

Now the selected items are **A**, **D**, **E**.

Total weight:

```
2 + 5 + 2 = 9 kg
```

New fitness value:

```
18 + 45 + 15 = 78
```

[**↪ Problem Set**](#set-a)

### <ins>Ans to the Ques no. 2</ins>

#### 1. Construct the Confusion Matrix.

<ins><strong>Ans.:</strong></ins> Given there are **500 loan applicants**.

- **220 eligible** applicants were correctly predicted as eligible.
- **30 eligible** applicants were incorrectly predicted as not eligible.
- **40 ineligible** applicants were incorrectly predicted as eligible.
- The remaining ineligible applicants were correctly predicted as not eligible.

Identifying the four parts of the confusion matrix:

- **TP (True Positive)** = eligible predicted as eligible = **220**
- **FN (False Negative)** = eligible predicted as not eligible = **30**
- **FP (False Positive)** = ineligible predicted as eligible = **40**
- **TN (True Negative)** = ineligible predicted as not eligible = ?

Total applicants = 500.

$$
TP+FN+FP+TN=500
$$

$$
220+30+40+TN=500
$$

$$
TN=500-290=\boxed{210}
$$

So the confusion matrix is:

$$
\boxed{
\begin{array}{c|cc}
 & \text{Predicted Eligible} & \text{Predicted Not Eligible}\\
\hline
\text{Actually Eligible} & 220 & 30\\
\text{Actually Not Eligible} & 40 & 210
\end{array}}
$$

[**↪ Problem Set**](#set-a)

#### 2. Calculate Accuracy, Precision, Recall and F1-Score.

<ins><strong>Ans.:</strong></ins> We know, accuracy tells us the proportion of **all predictions that were correct**.

$$
Accuracy=\frac{TP+TN}{TP+TN+FP+FN}
$$

$$
Accuracy=\frac{220+210}{500}
$$

$$
=\frac{430}{500}
$$

$$
=\boxed{0.86}
$$

Then Precision:

$$
Precision=\frac{TP}{TP+FP}
$$

$$
Precision=\frac{220}{220+40}
$$

$$
=\frac{220}{260}
$$

$$
=\boxed{0.8462}
$$

Recall:

$$
Recall=\frac{TP}{TP+FN}
$$

$$
Recall=\frac{220}{220+30}
$$

$$
=\frac{220}{250}
$$

$$
=\boxed{0.88}
$$

Now, F1-score is the harmonic mean of **Precision** and **Recall**.

$$
F1=2\times\frac{Precision\times Recall}{Precision+Recall}
$$

Using:

$$
Precision=0.8462,\qquad Recall=0.88
$$

We get,

$$
F1=2\times\frac{0.8462\times0.88}{0.8462+0.88}
$$

$$
\approx\boxed{0.8627}
$$

| Metric        |     Answer |
| ------------- | ---------: |
| **Accuracy**  |    **86%** |
| **Precision** | **84.62%** |
| **Recall**    |    **88%** |
| **F1-score**  | **86.27%** |

Formulas:

$$
\boxed{Accuracy=\frac{TP+TN}{Total}}
$$

$$
\boxed{Precision=\frac{TP}{TP+FP}}
$$

$$
\boxed{Recall=\frac{TP}{TP+FN}}
$$

$$
\boxed{F1=2\times\frac{Precision\times Recall}{Precision+Recall}}
$$

[**↪ Problem Set**](#set-a)

### <ins>Ans to the Ques no. 3</ins>

<ins><strong>Ans.:</strong></ins> Given here,

$$
w_1=0.7,\qquad w_2=0.6
$$

$$
Learning\,rate,\,\eta=0.2,\qquad \theta=0.6
$$

OR-gate training data:

| Pattern |  x1 |  x2 | Target \(t\) |
| ------- | --: | --: | -----------: |
| 1       |   0 |   0 |            0 |
| 2       |   0 |   1 |            1 |
| 3       |   1 |   0 |            1 |
| 4       |   1 |   1 |            1 |

We know,

**Net input:**

$$
net=x_1w_1+x_2w_2
$$

**Activation function:**

$$
y=
\begin{cases}
1,&net\geq\theta\\
0,&net<\theta
\end{cases}
$$

**Error:**

$$
e=t-y
$$

**Weight update:**

$$
w_i^{new}=w_i+\eta e x_i
$$

#### Epoch 1

Initial weights:

$$
\boxed{w_1=0.7,\quad w_2=0.6}
$$

| Pattern |  x1 |  x2 |   t |  w1 |  w2 | net&nbsp;=&nbsp;x1w1&nbsp;+&nbsp;x2w2 |   y | e=t-y | Delta&nbsp;w1=ηex1 | Delta&nbsp;w2=ηex2 | New&nbsp;w1 | New&nbsp;w2 |
| ------- | --: | --: | --: | --: | --: | ------------------------------------: | --: | ----: | -----------------: | -----------------: | ----------: | ----------: |
| 1       |   0 |   0 |   0 | 0.7 | 0.6 |                       0(0.7)+0(0.6)=0 |   0 | 0-0=0 |        0.2(0)(0)=0 |        0.2(0)(0)=0 |     **0.7** |     **0.6** |
| 2       |   0 |   1 |   1 | 0.7 | 0.6 |                     0(0.7)+1(0.6)=0.6 |   1 | 1-1=0 |        0.2(0)(0)=0 |        0.2(0)(1)=0 |     **0.7** |     **0.6** |
| 3       |   1 |   0 |   1 | 0.7 | 0.6 |                     1(0.7)+0(0.6)=0.7 |   1 | 1-1=0 |        0.2(0)(1)=0 |        0.2(0)(0)=0 |     **0.7** |     **0.6** |
| 4       |   1 |   1 |   1 | 0.7 | 0.6 |                     1(0.7)+1(0.6)=1.3 |   1 | 1-1=0 |        0.2(0)(1)=0 |        0.2(0)(1)=0 |     **0.7** |     **0.6** |

| Epoch | Initial w1 | Initial w2 | Errors | Final w1 | Final w2 | Status        |
| ----- | ---------: | ---------: | -----: | -------: | -------: | ------------- |
| 1     |        0.7 |        0.6 |      0 |      0.7 |      0.6 | **Converged** |

The perceptron converges in the first epoch because all four OR-gate training patterns are correctly classified using the initial weights `w1=0.7`, `w2=0.6`, and threshold `0.6`. Therefore, no weight adjustment is required.

[**↪ Problem Set**](#set-a)

---

## Set B

<p align="center"><img src="img02.jpg" width="70%"/></p>

---

## Set C

<p align="center"><img src="img03.jpg" width="70%"/></p>

---

## Set D

<p align="center"><img src="img04.jpg" width="70%"/></p>

---

<p align="center"><strong>The End.</strong></p>
