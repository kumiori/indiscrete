# Indiscrete
How do elementary systems evolve under irreversibility constraints?
How do complex systems _fail_ to be stable? What is the relation between
observability, scientific theory, and real processes?

We play a game, and this is our toy.

## Discrete Toy Model of Damageable Springs

## Overview
This repository contains code for a discrete toy model of damageable springs, designed to demonstrate the application of an evolution law in simulating the behavior of complex structures (or systems).

## Description of the Theory
The discrete toy model represents a simplified system of interconnected springs, where each spring can undergo damage over time. The model aims to capture the evolution of damage and softening within the material and its effects on the overall structural mechanical behavior.
More fundamentally, we are testing an evolution law based on a unilateral notion of stability which can be put under the following form

Given a state $y$ and its associated energy $E$, given admissible variations $z\in \mathcal K$, then $y$ is (statically) Stable _only if_

$$
E(y)\leq E(y+z), \quad \forall z \in \mathcal K
$$

Remark that _the elephant in the room_ can be hidden in the definition of $\mathcal K$.

More practically, 
We show how to fully exploit a variational stability criterion to study a 1d nontrivial discrete (fully nonlinear) model of $N$ elements,  
providing full closed form solutions for the evolution problem. Furthermore, we explore three models which are commonplace in
the applications of fracture mechanics, providing interactive notebooks reproduce the conceptual experiments.
To expand on the topic, we provide a comparison with a numerically computed solution via finite elements (cf. [irrevolutions](https://github.com/kumiori/irrevolutions))
showing one fundamental difference between the 1d and the general case. 
Finally, to further investigate the connection between discrete and continuum models, we sketch the asymptotic process of $\lim N \to \infty$ which leads to a well-posed 1d evolutionary continuum model.

[tbd]

## Features
- Implementation of a discrete model representing interconnected springs.
- Incorporation of an evolution law governing the progression of damage within the material.
- Visualisation tools to observe the evolution of damage and mechanical response over time.

## Usage
1. Clone the repository to your local machine.
2. Install the necessary dependencies (list them if applicable).
3. Run the main simulation script to execute the model.
4. Adjust parameters and settings as needed to explore different scenarios.
5. Analyse the output data and visualisation to understand the behavior of the system.

## Dependencies
List any external libraries or dependencies required to run the code.

## File Structure
Files within the repository, including key scripts, modules, and data files are structured as follows:
[tbd]

## Contributing
We welcome contributions to enhance the functionality and usability of the model. Feel free to fork the repository, make changes, and submit pull requests.
Do you have ideas of application of such theory to _otherwise irreversible discrete systems?_

## License
The code is distributed as Free Software with GPLv3 license. Please remark that, here, the term 'free' has all to do
with freedom and nothing to do with price. 



## Contact
For questions, feedback, or suggestions, please contact [author/contact information].
