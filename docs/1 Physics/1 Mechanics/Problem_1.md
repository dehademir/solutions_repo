# Problem 1

# **Mechanics Problem 1: Investigating the Range as a Function of the Angle of Projection**

## **1. Introduction and Motivation**
Projectile motion is one of the most fundamental topics in mechanics, with applications in sports, ballistics, space exploration, and engineering. Understanding how the **range of a projectile** varies with its **launch angle** is crucial in many real-world scenarios:

- **Sports Science**: Optimizing a soccer player's free-kick or a basketball shot.
- **Military and Ballistics**: Calculating the range of a projectile in different terrains.
- **Space Science**: Predicting the trajectory of spacecraft launched from different planets.
- **Engineering**: Designing water fountains or roller coasters with precise parabolic arcs.

In this study, we investigate how the range of a projectile depends on the launch angle and explore factors that influence projectile motion.

---

## **2. Theoretical Foundation**

### **Newton’s Second Law**
Newton’s second law states that the force acting on an object is equal to the product of its mass and acceleration:

$$
\vec{F} = m \vec{a}
$$

For a projectile in free fall under Earth's gravitational field, the only force acting on it is gravity:

$$
\vec{F} = -mg \hat{j}
$$

Since acceleration is the second derivative of position with respect to time, Newton’s second law can be written as:

$$
m \frac{d^2 \vec{r}}{dt^2} = -mg \hat{j}
$$

Dividing by mass:

$$
\frac{d^2 \vec{r}}{dt^2} = -g \hat{j}
$$

This equation shows that the object experiences **constant downward acceleration** due to gravity while moving freely in space.

---

## **3. Equations of Motion**
Projectile motion consists of **two independent components**:  

- **Horizontal Motion ($x$-direction)**:
  - No force acts in the horizontal direction, so acceleration is zero.

    $$
    \frac{d^2 x}{dt^2} = 0
    $$

  - The horizontal velocity remains constant:

    $$
    v_x = v_0 \cos\theta
    $$

  - The horizontal position as a function of time:

    $$ 
    x(t) = v_0 \cos\theta \cdot t
    $$

- **Vertical Motion ($y$-direction)**:
  - Gravity is the only force acting, so acceleration is:

    $$
    \frac{d^2 y}{dt^2} = -g
    $$

  - The vertical velocity changes over time:

    $$
    v_y = v_0 \sin\theta - gt
    $$

  - The vertical position equation:

    $$ 
    y(t) = h + v_0 \sin\theta \cdot t - \frac{1}{2} g t^2
    $$

---

## **4. Time of Flight**
The total time the projectile spends in the air is obtained by solving for $T$ when the projectile lands ($y(T) = 0$):

$$
h + v_0 \sin\theta \cdot T - \frac{1}{2} g T^2 = 0
$$

Solving for $T$ using the quadratic formula:

$$
T = \frac{v_0 \sin\theta + \sqrt{(v_0 \sin\theta)^2 + 2gh}}{g}
$$

This equation gives the **total duration** the projectile remains airborne.

---

## **5. Range Equation**
The range ($R$) is the total horizontal distance traveled:

$$
R = v_0 \cos\theta \cdot T
$$

Substituting $T$:

$$
R = \frac{v_0 \cos\theta (v_0 \sin\theta + \sqrt{(v_0 \sin\theta)^2 + 2gh})}{g}
$$

For **flat ground** ($h = 0$), the well-known formula simplifies to:

$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$

This equation tells us that **the maximum range occurs at $\theta = 45^\circ$**, assuming no air resistance.

## Python Visualization:

![alt text](image.png)
