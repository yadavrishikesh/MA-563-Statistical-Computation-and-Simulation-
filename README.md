# MA 563 — Statistical Computation and Simulation

**Credits:** 3-0-2-4  
**Semester:** Even Semester 2026  
**School:** School of Mathematics and Statistical Sciences (SMSS), IIT Mandi

> “All models are wrong, but simulation lets us find out just how wrong – and what to do about it.”

## Welcome

Suppose you cannot solve an integral by hand, do not know the exact distribution of your estimator, or have a dataset that is too small to trust classical formulas.

**What do you do?**

**You simulate.**

This course develops the computational ideas needed to simulate, estimate, resample, and perform statistical inference when closed-form solutions are unavailable or difficult to obtain.

---

## 1. Course Information

### Instructor

**Dr. Rishikesh Yadav (Rishi)**  
Assistant Professor  
School of Mathematics and Statistical Sciences (SMSS), IIT Mandi

**Office:** F17, 2nd floor, A13, North Campus  
**Email:** rishikesh@iitmandi.ac.in

### Teaching Assistant

**Vedant Vibhor**  
**Email:** D24028@students.iitmandi.ac.in

### Prerequisites

- Probability & Statistics (MA 524)
- and/or IC 252

### Intended Audience

- B.Tech. 3rd/4th year
- MS
- MSc
- PhD

### Credit Structure

**3-0-2-4**

- 3 Lecture hours/week
- 0 Tutorial hours/week
- 2 Laboratory hours/week

---

## 2. Course Schedule

| Day | Time | Type |
|---|---|---|
| Tuesday | 2:00–2:50 | Lecture |
| Wednesday | 10:00–10:50 AM | Lecture |
| Friday | 11:00–11:50 AM | Lecture |
| Tuesday | 3:00–5:00 PM | Lab |

---

## 3. Why Does This Course Matter?

Simulation and computational statistics appear across many areas:

| Area | Example Application |
|---|---|
| Finance | Monte Carlo pricing of options and portfolio risk (Value-at-Risk) |
| Genomics | EM algorithm to recover missing genotype data |
| AI / ML / Data Science | MCMC and Bayesian inference behind uncertainty-aware models |
| Medicine | Bootstrap confidence intervals from small clinical trials |
| Climate Science | Stochastic weather and climate simulators |
| Graphics / Gaming | Random number generators, procedural worlds, and ray tracing |
| Engineering | Monte Carlo tolerance and reliability analysis |
| Astrophysics | MCMC to infer exoplanet orbits from noisy telescope data |

### The Common Thread

Every one of these fields can encounter the same wall:

> **No clean formula exists.**

Simulation provides a computational bridge from:

> “We don't know”

to

> “Here is our best estimate, and here is how uncertain it is.”

---

## 4. From a Random Seed to Real Insight

A large part of computational statistics begins with a random seed.

```text
Seed
  ↓
Pseudo-Random Generator
  ↓
U(0,1) random stream
  ↓
Transformation
  ↓
Normal / Exponential / Poisson / ...
```

Common transformations include:

- Inverse CDF / inverse transform
- Box–Muller transformation
- Other simulation algorithms

Everything from a simulated stock-price path to a simulated epidemic ultimately starts with a deterministic algorithm that produces a sequence that behaves like random numbers.

---

## 5. Overall Course Objectives

By the end of the course, students should be able to:

1. Generate pseudo-random numbers and simulate arbitrary random variables from scratch.
2. Use Monte Carlo methods to estimate quantities that have no closed form, including integrals, expectations, and tail probabilities.
3. Quantify uncertainty using resampling methods such as bootstrap, cross-validation, and permutation tests.
4. Fit models with missing or latent structure using the Expectation-Maximization (EM) algorithm.
5. Perform Bayesian computation and sample from posterior distributions using MCMC methods, including Metropolis–Hastings and Gibbs sampling.
6. Translate statistical ideas into working code and apply them to real and simulated datasets.

---

## 6. Semester Roadmap

The course is organized into **5 modules**, covering **42 lectures** together with weekly hands-on laboratory sessions.

| Module | Topic | Lectures |
|---|---|---:|
| Module 1 | Random Number Generation & Simulation Foundations | 8 |
| Module 2 | Monte Carlo Methods | 8 |
| Module 3 | Resampling & Simulation-Based Statistical Inference | 10 |
| Module 4 | Iterative Computational Algorithms (EM) | 6 |
| Module 5 | Bayesian Computation & MCMC | 10 |
| **Total** | | **42** |

Each module is paired with hands-on computational work applying the week's ideas to real and simulated data.

---

# Module 1 — Random Number Generation & Simulation Foundations

**8 lectures**

### Topics

- Pseudo-random generators
- Simulation foundations
- Inverse transform sampling
- Acceptance–rejection sampling
- Box–Muller transformation
- Ratio-of-uniforms method
- Diagnosing randomness

### Where You Will See This

**Casinos & gaming:** understanding and checking random number generation.

**Cryptography:** cryptographically secure randomness for keys.

**Procedural game worlds:** generating terrain, loot, and NPC behaviour.

**Engineering noise models:** injecting realistic sensor/measurement noise into simulations.

---

# Module 2 — Monte Carlo Methods

**8 lectures**

### Topics

- Monte Carlo estimation
- Monte Carlo integration
- Law of Large Numbers
- Crude Monte Carlo
- Importance sampling
- Variance reduction
- Diagnostics

### Where You Will See This

**Estimating π:** randomly generating points and estimating the area ratio.

**Quantitative finance:** pricing path-dependent options when no closed-form solution exists.

**Physics and engineering:** evaluating high-dimensional integrals and structural reliability.

**Computer graphics:** Monte Carlo ray tracing for photorealistic rendering.

---

# Module 3 — Resampling & Simulation-Based Statistical Inference

**10 lectures**

### Topics

- Bootstrap
- Parametric bootstrap
- Nonparametric bootstrap
- Jackknife
- Cross-validation
- Permutation tests
- Monte Carlo hypothesis testing

### Where You Will See This

**Clinical trials:** bootstrap confidence intervals when patient samples are small and expensive.

**Machine learning:** cross-validation for choosing model complexity.

**Genomics:** permutation tests for assessing observed gene-expression differences.

**A/B testing:** simulation and resampling for comparing product variants.

---

# Module 4 — Iterative Computational Algorithms (EM)

**6 lectures**

### Topics

- Stochastic approximation ideas
- Likelihood-based computation
- Gaussian mixture models
- Expectation-Maximization (EM) algorithm
- Simulation-based interpretation of EM

### Where You Will See This

**Customer segmentation:** identifying hidden customer types using Gaussian mixture models.

**Speech recognition:** estimating hidden acoustic states from noisy audio.

**Image segmentation:** separating regions when pixel labels are unobserved.

**Population genetics:** inferring allele frequencies from incomplete genotype data.

---

# Module 5 — Bayesian Computation & MCMC

**10 lectures**

### Topics

- Basics of Bayesian inference
- Markov chains
- Stationary distributions
- Metropolis–Hastings
- Gibbs sampling
- Posterior diagnostics

### Where You Will See This

**Astrophysics:** posterior sampling for exoplanet orbital parameters.

**Spam filtering:** Bayesian updating of beliefs about spam and non-spam messages.

**Modern AI:** Bayesian neural networks and sampling ideas related to uncertainty.

**Bayesian A/B testing:** continuously updating beliefs as new observations arrive.

---

## 7. Laboratory Component

The laboratory component is designed to reinforce lecture concepts through practical implementation.

### Python Programming is Essential

The laboratory sessions require students to write **Python code independently**.

The emphasis is on:

1. Correct implementation
2. Clear understanding of the underlying statistical concepts

### Laboratory Tests

Approximately **five laboratory tests** will be conducted during the semester, with one lab test for each unit/module.

The laboratory component consists of:

- Lab tests
- Viva

The laboratory component contributes **30% of the overall course grade**.

### Practice Exercises

Before each lab test:

- Practice exercises will be shared in advance.
- These exercises are intended to help students prepare.
- Lab-test problems will be similar in nature to the practice exercises.
- A short viva will follow the programming component.

---

## 8. Preparing for Laboratory Sessions

### Python Programming is Essential

If you are not yet comfortable with Python:

- Start learning Python as early as possible.
- Work through the practice exercises provided before each lab test.
- Build familiarity with programming, numerical computation, arrays, functions, loops, simulations, and plotting.

Students with little or no prior programming experience are strongly encouraged to complete an introductory Python course before the first lab test.

### Recommended Course

[Python for Applied Data Science and AI — Coursera](https://www.coursera.org/learn/python-for-applied-data-science-ai)

---

## 9. Assessment Plan

| Component | Weight |
|---|---:|
| Quizzes (best of planned) | 20% |
| Laboratory Evaluation | 30% |
| Mid-Semester Exam | 20% |
| Final Exam | 30% |
| **Total** | **100%** |

### Attendance

As stated in the course plan:

> Attendance must exceed **80%** to be eligible to appear for the final exam.

---

## 10. Grading Policy

| Grade | Grade Points | Interpretation | Typical Distribution |
|---|---:|---|---:|
| A* / A | 10 | Outstanding / Excellent | 10% |
| A− | 9 | Very Good | 15% |
| B | 8 | Good | 20–25% |
| B− | 7 | Above Average | 20–25% |
| C | 6 | Average | 15–20% |
| C− | 5 | Below Average | 5–10% |
| D | 4 | Marginal | 5% |

---

## 11. Suggested Learning Approach

This course is computational in nature. Students are expected to learn through a combination of:

- Lectures
- Mathematical understanding
- Programming
- Simulation
- Hands-on laboratory exercises
- Practice problems
- Statistical interpretation

A useful learning cycle is:

```text
Understand the statistical idea
        ↓
Understand the algorithm
        ↓
Implement it computationally
        ↓
Run simulations
        ↓
Visualize the results
        ↓
Interpret the statistical output
```

The goal is not simply to use an existing function.

The goal is to understand **how the computation works**.

---

## 12. What You Should Be Able to Do by the End

By the end of the course, students should be comfortable moving from:

> “I don't know the formula.”

to:

> “I can simulate the answer.”

The course provides a general-purpose computational toolkit:

- **Simulate it**
- **Resample it**
- **Estimate it**
- **Sample from its posterior**
- **Check the uncertainty**
- **Interpret the result**

The broader objective is to move beyond simply computing statistics and toward understanding how statistical computation itself can be constructed.

---

## 13. Recommended Books

### Main Textbooks

1. Ross, S. M. *Simulation*, 5th ed., Academic Press (2012).
2. Robert, C. P., & Casella, G. *Monte Carlo Statistical Methods*, Springer (2004).

### Reference Books

3. James, G., Witten, D., Hastie, T., & Tibshirani, R. *An Introduction to Statistical Learning*, Springer (2013).
4. Efron, B., & Tibshirani, R. *An Introduction to the Bootstrap*, CRC Press (1994).

---

## 14. Suggested GitHub Repository Structure

```text
MA563-Statistical-Computation-and-Simulation/
│
├── README.md
│
├── syllabus/
│   └── course-plan.pdf
│
├── module-01-random-number-generation/
│   ├── lectures/
│   ├── examples/
│   ├── practice/
│   └── lab/
│
├── module-02-monte-carlo/
│   ├── lectures/
│   ├── examples/
│   ├── practice/
│   └── lab/
│
├── module-03-resampling/
│   ├── lectures/
│   ├── examples/
│   ├── practice/
│   └── lab/
│
├── module-04-em/
│   ├── lectures/
│   ├── examples/
│   ├── practice/
│   └── lab/
│
├── module-05-bayesian-mcmc/
│   ├── lectures/
│   ├── examples/
│   ├── practice/
│   └── lab/
│
├── assignments/
├── datasets/
└── resources/
```

---

## 15. General Instructions for Students

1. Attend lectures regularly.
2. Work through the computational examples discussed in class.
3. Practice Python programming regularly rather than only before examinations.
4. Complete the practice exercises provided before each laboratory test.
5. Understand the statistical reasoning behind the code.
6. Do not treat simulation as a black box.
7. Check whether simulation results make statistical sense.
8. Learn to visualize and interpret simulation output.
9. Ask questions whenever an algorithm or statistical concept is unclear.
10. Use the recommended books and course material when needed.

---

## 16. Course Philosophy

Statistical computation is not just about writing code.

It is about connecting:

```text
Probability
    +
Statistics
    +
Algorithms
    +
Computation
    +
Simulation
    ↓
Statistical Insight
```

The central idea of this course is:

> When an exact analytical answer is unavailable, computational methods provide a systematic way to approximate the answer and understand its uncertainty.

---

## 17. Final Message

Every field you may work in — finance, biology, engineering, AI, policy, climate science, medicine, or data science — eventually encounters problems for which there is no clean formula.

This course provides a general-purpose toolkit:

> **Simulate it. Resample it. Sample from its posterior.**

By the end of the course, the goal is that you will not just compute statistics — you will understand how to **construct the computation itself**.

## Let's get started.

---

## Course Contact

**Dr. Rishikesh Yadav**  
Assistant Professor  
School of Mathematics and Statistical Sciences  
IIT Mandi

**Email:** rishikesh@iitmandi.ac.in

**Teaching Assistant:** Vedant Vibhor  
**Email:** D24028@students.iitmandi.ac.in
