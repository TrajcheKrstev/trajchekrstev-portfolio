+++
title = 'Genetic Programming for Symbolic Regression'
draft = false
featured_image = "/images/cover3.jpg"
summary = "**Genetic Programming for Symbolic Regression** is a group project developed as part of the Intelligent Systems course. This project leverages genetic programming techniques to predict mathematical equations based on given y-values. By simulating the process of natural selection, the algorithm evolves potential solutions over multiple generations to find the best-fitting equation."
+++

**Genetic Programming for Symbolic Regression** is a group project developed as part of the Intelligent Systems course. This project leverages genetic programming techniques to predict mathematical equations based on given y-values. By simulating the process of natural selection, the algorithm evolves potential solutions over multiple generations to find the best-fitting equation.

## Project Overview

### Objective

The primary goal of this project is to predict an equation that best fits a set of provided y-values. This is achieved by using genetic programming, which involves the evolution of mathematical expressions through selection, crossover, and mutation processes.

### Methodology

The project employs a genetic algorithm to evolve populations of potential solutions. Each solution is represented as an encoded expression tree. The fitness of each solution is evaluated based on how well it predicts the y-values for given x-values. The key steps involved in the process are outlined below:

#### Expression tree encoding

We encoded each expression tree using the prefix notation.

For example given tree :

```plaintext
    *
   / \
  +   -
 / \ / \
5  x 8  x

```

in prefix notation is : \*+5x-8x and is interpreted as (5+x)\*(8-x)

In order to work with PyGAD library, which operates with numpy arrays, we must encode operators as numbers. And to differentiate between operators and operands we implemented an additional binary mask where: 1 denotes operator, and 0 operand.

`*+5x-8x` --> 1100100

#### Initial Population Creation

- **create_initial_population(size)**: Generates an initial population of encoded expression trees, each representing a potential mathematical equation.

#### Fitness Evaluation

- **fitness_func(ga_instance, solution, solution_index)**: Calculates the fitness of each solution by comparing the predicted y-values to the actual y-values. The fitness value guides the selection of solutions for the next generation.

#### Expression Evaluation

- **evaluate(expression, x_value)**: Evaluates an encoded expression tree by substituting x-values and performing the corresponding mathematical operations.

#### Genetic Operations

Our approach for performing valid crossovers and mutations was as follows:

- Select only valid subtrees, this was implemented using the recursive function find_subtree(), which returns the ending index of the subtree, and the binary mask.
- For crossover select two parents, valid subtrees are identified. Switch the subtrees. Modify the length of the new individuals, encoding and binary mask accordingly.
- For mutation, if an individual is selected randomly choose whether to mutate only one operator/operand or to replace a subtree with another subtree. When mutating the entire subtree first select a valid subtree using the function find_subtree(). Generate random valid tree using the function create_chromosome. Replace subtree with the new, and modify the length, encoding and binary mask.

#### Execution and Optimization

- **run_genetic_algorithm(n_equation, true_equation, ...)**: Runs the genetic algorithm for a specified number of generations, optimizing the population to find the best-fitting equation.

### Technical Details

The algorithm is implemented using Python and several key libraries, including `pygad` for genetic algorithm operations and `numpy` for numerical computations. The project also utilizes `matplotlib` and `seaborn` for data visualization and analysis.

### Results

The genetic algorithm was tested on a dataset of 98 equations, with x-values and y-values provided for each equation. The algorithm successfully identified the best solutions for over 65% of the equations in the dataset. Notably, even for those it couldn't fully pinpoint, a significant number were very close to being correct, as evidenced by a fitness score under 1000.

The algorithm encounters challenges in finding optimal solutions for more complex equations. For instance, in the case of an equation like **4x^5 - 3x^3 + x^2 + x - 2**, the algorithm often converges to solutions such as **4x^2 - 3x^2 + x^2**, where components like **+ x** or **- 2** may not significantly impact the fitness function.

{{<figure src="/images/acc.jpg" alt="Correct Solutions">}}
