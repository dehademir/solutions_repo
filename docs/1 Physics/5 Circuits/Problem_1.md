# Problem 1
#  Equivalent Resistance Using Graph Theory with NetworkX

##  Why Use Graph Theory?

In electrical engineering, calculating **equivalent resistance** is essential for analyzing circuits. Traditionally, we simplify circuits by:
- Combining **resistors in series** (add them)
- Combining **resistors in parallel** (use the reciprocal formula)

However, for **complex circuits**, especially those with mixed configurations or multiple loops, manual simplification becomes inefficient or error-prone.

**Graph theory** provides a structured, programmable approach by modeling circuits as **graphs**.

---

##  Core Idea: Model the Circuit as a Graph

A **circuit** can be seen as a **graph**:
- **Nodes** represent junction points in the circuit
- **Edges** represent resistors between nodes, with resistance as a **weight** or **attribute**

This makes it possible to simplify the circuit algorithmically.

---

##  NetworkX Graph Types

| Graph Type     | Description                              | Use Case                          |
|----------------|------------------------------------------|-----------------------------------|
| `Graph`        | Undirected, no parallel edges            | Simple resistor networks          |
| `DiGraph`      | Directed graph                           | Circuits with diodes or flow      |
| `MultiGraph`   | Allows multiple (parallel) edges         | Circuits with parallel resistors  |
| `MultiDiGraph` | Directed with multiple edges             | Advanced cases with flow + parallel|

For circuits, we often use **`MultiGraph`** to model parallel resistors.

---
[collab][https://colab.research.google.com/drive/1fsUJpDVypQU71mnMMy1hdp6iO0DhJJAF)

![alt text](image-1.png)

#  Visualization of Equivalent Resistance Using Graph Theory

##  Objective

Use **graph theory and NetworkX** to simplify a nested resistor circuit into a single equivalent resistance step-by-step, and **visualize each transformation**.

---

##  Step 0: Original Nested Circuit

The circuit consists of:
- A resistor between `A-B` of 2Ω
- Two paths from `B → D`:
  - Via `C`: `B-C` (2Ω) and `C-D` (4Ω)
  - Direct: `B-D` (4Ω)
- Final segment: `D-E` (1Ω)

![alt text](image.png)

![alt text](image-3.png)

