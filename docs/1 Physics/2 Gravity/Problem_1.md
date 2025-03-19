# Problem 1

# **Gravity: Problem 1**
## <span style="font-size: 1.2em; font-weight: bold;">Orbital Period and Orbital Radius</span>

## **1. Motivation**
Kepler’s Third Law states that the square of a planet’s orbital period ($T^2$) is proportional to the cube of its orbital radius ($r^3$). This law plays a crucial role in astronomy, as it allows scientists to determine planetary masses, orbital distances, and even exoplanet properties.

This relationship is fundamental to **celestial mechanics**, helping explain:
- The motion of planets around the Sun.
- The orbit of satellites around Earth.
- The gravitational influence of massive bodies in space.

## **2. Derivation of Kepler’s Third Law**
For a **circular orbit**, a planet of mass $m$ orbits a star of mass $M$ under the influence of gravitational force:

$F = \frac{GMm}{r^2}$

According to Newton’s Second Law:

$F = m a$

For circular motion, the acceleration is the **centripetal acceleration**:

$a = \frac{v^2}{r}$

Equating both forces:

$\frac{GMm}{r^2} = m \frac{v^2}{r}$

Canceling $m$:

$\frac{GM}{r^2} = \frac{v^2}{r}$

Rewriting velocity using $v = \frac{2\pi r}{T}$:

$\frac{GM}{r^2} = \frac{(2\pi r / T)^2}{r}$

Expanding:

$\frac{GM}{r^2} = \frac{4\pi^2 r^2}{T^2 r}$

Simplifying:

$T^2 = \frac{4\pi^2 r^3}{GM}$

### **Kepler’s Third Law**
$T^2 \propto r^3$

This equation shows that the square of the orbital period is proportional to the cube of the orbital radius.

## **3. Applications in Astronomy**
- **Determining Planetary Masses**: By observing the orbit of a moon around a planet, we can calculate the planet’s mass.
- **Exoplanet Discovery**: Astronomers use Kepler’s law to estimate distances of exoplanets from their stars.
- **Satellite Orbits**: The relationship helps determine the orbital altitude needed for geostationary satellites.

## **4. Python Simulation of Circular Orbits**
The following Python script simulates circular orbits and verifies **Kepler’s Third Law**.

![alt text](image-1.png)

![alt text](image-2.png)