# Rastrigin-Function-Genetic-Algorithm
A mono objective genetic algorithm to solve the Rastrigin function. Coded in Python on Jupyter Notebook.

## Rastrigin Function
The Rastrigin function is a non-convex function used to evaluate the performance of optimization algorithms. It was initially proposed by Rastrigin as a two-dimensional function and later generalized by Muhlenbein et al.

The goal is to implement a GA and apply it to minimize the Rastrigin function with n = 10 variables.

<img src="https://raw.githubusercontent.com/CelsoMeireles/Rastrigin-Function-Genetic-Algorithm/main/Rastrigin.PNG" width=450>

with x<sub>i</sub> &#8714; [5:12; 5:12]. The global minima is x* = 0, where f(x*) = 0.

The GA must have the following characteristics:
> Representation of the variables using binary codification;
> Selection operator of individuals by means of:
> 
> - Roulette wheel with 50% of probability;
> 
> - Tournament with 50% of probability.
> 
> Crossover: 1 cutoff point per variable;
> 
> Mutation: bit flip.
> 
> Others operators are free to use.

Define the values of the hyper-parameters p<sub>c</sub> and p<sub>m</sub> or make a dynamic adjustment of them. The computational budget is 10,000 fitness function evaluations.

Important note:
The input and output parameters must be according to the following statements:
> [x*, f*] = firstname lastname[nvar, ncal], being:
> 
> x*: vector which contains the variables of the best individual;
> 
> f*: fitness function evaluated over x*
> 
> ncal: total number of calls (or evaluations) of the fitness function;
> 
> nvar: number of decision variables.

## 🔨 The Genetic Algorithm

The algorithm is an implementation of a mono objective genetic algorithm and is explained through the comments I put along the code. 

The algorithm seeks to minimize the function until it consumes the entire computational budget defined (there is a margin to prevent it from exceeding consumption). To avoid unnecessary budget consumption, I implemented a cache that stores the calculated results for each individual and does not evaluate the Rastrigin function when the result is already known. I noticed that it was necessary to reduce the mutation percentage parameters and crossover cutoff points as the budget was consumed, since, although useful at first, they were causing too much disturbance in the model and, after implementation, the result arrived closer to the minimum. 

The algorithm tries to find values of x* where f* are close to 2 and 3 most of the time, but it fails to reach the global minimum of f* = 0. I believe that, to reach the global minimum, the genetic algorithm should be allied with a local search engine.

## How to run the code

This is a Python implantation. In order to keep it easy, I did it using Jupyter Notebook. Just download the “Rastrigin Function Genetic Algorithm.ipynb” file, and run it on Jupyter Notebook.

Feel free to ask questions and contribute.

## Autor

| [<img src="https://avatars.githubusercontent.com/u/33962854?v=4" width=115><br><sub>Celso Meireles</sub>](https://github.com/CelsoMeireles) 
| :---: | 
