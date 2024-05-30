# MultiBody

Main objectives:
1. Implement a parallel multi-body dynamics simulator.
   Remark: parallelism is achieved with MPI and it is on the particles

a. Define an underlying structured grid common to all cores.
b. Detect neighbours from the structured grid.
c. Implement attractive force
d. Implement repulsive force

Caveat:
  - too many particles in a cell could kill the performance

# Physics
Use Verlet integration to solve the equations of motion.
  $$x_{n+1} = 2x_n - x_{n-1} + a_n \Delta t^2$$

## Gravity
$$F = G \frac{m_1 m_2}{r^2}$$ 

## Container
The container is a box with periodic boundary conditions.
