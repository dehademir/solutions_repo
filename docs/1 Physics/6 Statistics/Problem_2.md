# Problem 2

#  Problem 2: Estimating π Using Monte Carlo Methods

---

##  Motivation

Monte Carlo methods are a class of algorithms that solve numerical and probabilistic problems by using **random sampling**. One of the most elegant applications is the estimation of the constant π, where randomness and geometry intersect beautifully.

By simulating the outcomes of randomly generated events and observing their relation to geometric boundaries, we can approximate π in a way that is **intuitive, visual, and computationally insightful**.

This exercise connects key ideas from:
- Probability theory
- Geometric reasoning
- Numerical convergence
- Simulation-based computation

---

##  Part 1: Estimating π Using a Circle (Geometric Probability)

###  Theoretical Foundation

Imagine a **unit circle** (radius = 1) perfectly inscribed in a square of side length 2. The area of the square is:

$$
A_{\text{square}} = 2 \times 2 = 4
$$

The area of the unit circle is:

$$
A_{\text{circle}} = \pi r^2 = \pi
$$

The ratio of the areas is:

$$
\frac{A_{\text{circle}}}{A_{\text{square}}} = \frac{\pi}{4}
$$

This implies that if we throw random points into the square, the proportion of points that fall **inside the circle** is approximately $\pi/4$. Thus, we can estimate π using:

$$
\pi \approx 4 \cdot \left( \frac{\text{points inside the circle}}{\text{total points}} \right)
$$

###  Simulation Process

1. Generate $n$ random points in the square $[-1, 1] \times [-1, 1]$.
2. Determine which points fall inside the unit circle using $x^2 + y^2 \leq 1$.
3. Count the points inside and outside.
4. Use the ratio to estimate π.

###  Visualization

A scatter plot can be created:
- **Blue points** represent those inside the circle.
- **Red points** are outside the circle but within the square.
- A black outline indicates the exact circle.

This allows us to **see the estimation process geometrically**.

###  Analysis

- The **accuracy improves** as the number of random points increases.
- For small samples, fluctuations are common.
- The convergence rate follows the **law of large numbers**:
  
  $$
  \text{Error} \propto \frac{1}{\sqrt{n}}
  $$

- The method is **simple and visual**, but **converges slowly**, requiring many samples for high precision.

---

##  Part 2: Estimating π Using Buffon’s Needle (Probabilistic Geometry)

###  Theoretical Foundation

Buffon’s Needle is a classic problem in **geometric probability**. Imagine dropping a needle of length $L$ onto a surface with **parallel horizontal lines** spaced distance $d$ apart ($L \leq d$). The probability that the needle **crosses** a line is:

$$
P = \frac{2L}{d\pi}
$$

Rearranging for π, we estimate it as:

$$
\pi \approx \frac{2L \cdot n}{d \cdot h}
$$

Where:
- $n$ is the total number of needle drops
- $h$ is the number of times the needle crosses a line

###  Simulation Process

1. Define $L$ (needle length) and $d$ (distance between lines).
2. Simulate $n$ needle drops:
   - Random center position on the vertical axis.
   - Random angle $\theta$ between $0$ and $\pi$.
3. Determine if the needle crosses a line using trigonometric conditions.
4. Estimate π using the observed proportion of crossings.

###  Visualization

- The parallel lines are shown as equally spaced horizontal lines.
- Each needle is drawn:
  - **Red** if it crosses a line.
  - **Blue** if it does not.
- This creates an engaging geometric probability visualization.

###  Analysis

- Like the circle-based method, the **accuracy improves** with more trials.
- However, this method **converges slower** and is more **sensitive to geometric constraints**.
- It is particularly useful in demonstrating how **experimental probability** relates to mathematical constants.

---

##  Deliverables

| Component            | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
|  Markdown Document | Full explanation of both simulation approaches                              |
|  Visual Outputs     | Plots of point distribution (circle) and needle crossing (Buffon)          |
|  Convergence Charts | Graphs showing estimated π vs number of samples for each method             |
|  Analysis           | Comparison of convergence rate and accuracy between both simulation types |

---

##  Summary

| Method               | Type           | Convergence Speed | Visualization Strength | Educational Value |
|----------------------|----------------|-------------------|------------------------|-------------------|
| Circle-Based         | Geometric Area |  Moderate        |  Excellent         |  Excellent    |
| Buffon’s Needle      | Probabilistic  |  Slower         |  Good               |  Strong       |

- Both methods highlight the power of **Monte Carlo simulations**.
- Circle-based approach is more **efficient and visual**.
- Buffon’s method offers a **historic and probabilistic twist**.

---

##  Hints & Tips

- Start with **small samples** to ensure your implementation works.
- Gradually **scale up** the number of trials to observe convergence.
- Use libraries like **NumPy** for efficient sampling and **Matplotlib** for visual feedback.
- Ensure **uniform random distribution** in all simulations for accuracy.

---

##  Final Note

These experiments not only teach us about $\pi$, but also about the **core ideas of randomness, simulation, convergence, and reproducibility** — foundational principles across mathematics, science, and engineering.



---

[colab](https://colab.research.google.com/drive/10CvKTTT-QjSl0bnWkZGDVUa7A6SbA-2Q)

![alt text](image-4.png)

##  Monte Carlo Estimation of $\pi$ – Geometric Visualization

![Monte Carlo π Estimation](/mnt/data/0f5e7bbc-fb1f-4ec0-94f4-88dd30982d7d.png)

###  Description

This plot demonstrates the **Monte Carlo method** to estimate the value of $\pi$ by simulating random points inside a square that bounds a **unit circle**.

- The square spans from $x = -1$ to $1$ and $y = -1$ to $1$.
- A **unit circle** is inscribed in the square (radius = 1).
- **10,000 points** were randomly generated within the square.

###  Color Legend

- **Blue points**: Lie **inside the circle** ($x^2 + y^2 \leq 1$)
- **Red points**: Lie **outside the circle** but still inside the square

###  π Estimation Formula

The value of $\pi$ is estimated using:

$$
\pi \approx 4 \cdot \left( \frac{\text{points inside circle}}{\text{total points}} \right)
$$

In this plot, the estimate is:

$$
\hat{\pi} \approx 3.13480 \quad \text{(from 10,000 points)}
$$

###  Insights

- The **ratio of blue to total points** approximates the **area of the circle** relative to the square.
- With **more points**, the estimate gets **closer to the true value of π**.
- The plot provides a **visual intuition** for convergence via geometric probability.

---

This is a foundational example of how randomness and geometry can be used together to estimate fundamental constants like π.


![alt text](image-5.png)

## 📈 Convergence of Monte Carlo Estimation of $\pi$

![Monte Carlo Convergence Plot](/mnt/data/d11b941e-3a92-40a9-8a37-ea7ea75a3f11.png)

###  What This Plot Shows

This graph demonstrates how the Monte Carlo estimate of $\pi$ evolves as the number of randomly sampled points increases.

- The **blue line** represents the **cumulative estimate of $\pi$** after each additional point.
- The **red dashed line** indicates the **true value of $\pi$** (approximately 3.14159).

---

###  Explanation

At each simulation step:
- A point is randomly placed inside the square $[-1, 1] \times [-1, 1]$
- We check whether it lies inside the unit circle: $x^2 + y^2 \leq 1$
- We update the estimate of $\pi$ using:
  $$
  \pi \approx 4 \cdot \left( \frac{\text{points inside circle}}{\text{total points}} \right)
  $$

---

###  Observations

| Range         | Behavior                        |
|---------------|---------------------------------|
| First 100 pts | High variability and oscillation|
| 500+ pts      | Gradual convergence toward $\pi$|
| 5000–10000    | Estimate stabilizes near 3.14   |

- The **fluctuations** early in the process are due to small sample size.
- Over time, the **law of large numbers** ensures convergence to the true value.

---

###  Key Takeaway

The Monte Carlo method:
- Converges **slowly but steadily** to an accurate value of $\pi$
- Becomes more reliable with a **larger number of trials**
- Demonstrates how **probabilistic techniques** can approximate deterministic values

This plot is a perfect example of a **stochastic simulation** stabilizing around a theoretical constant.

---


![alt text](image-6.png)
