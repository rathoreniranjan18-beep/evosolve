# Algorithm notes

## Chromosome representation

For the Target Match objective, a candidate is a 12-bit binary chromosome. Each bit represents one decision position. The target is `101101001110`.

## Fitness

Fitness is the number of positions that match the target. Scores range from 0 to 12; higher is better. For example, `101001001110` has one mismatching position and therefore scores 11/12.

## Evolution cycle

1. Generate the initial population.
2. Evaluate fitness for each candidate.
3. Rank candidates and select parents from the higher-ranked portion of the population.
4. Apply one-point crossover according to the crossover rate.
5. Apply bit-flip mutation according to the mutation rate.
6. Preserve the best candidate through elitism.
7. Continue until the generation limit or a stopping condition is reached.

## Important concepts

- **Selection pressure:** stronger preference for high-fitness candidates can speed up progress but may reduce diversity.
- **Crossover:** combines parts of two parent chromosomes.
- **Mutation:** randomly changes genes and can help maintain diversity.
- **Elitism:** protects the current best candidate from being lost in the next generation.
- **Stochasticity:** initialization and genetic operators introduce randomness, so repeated runs may differ.

## Interpreting results

A rising best-fitness curve suggests that the algorithm is finding better candidates. Average fitness gives a broader view of the population. A plateau can indicate convergence, insufficient diversity, or simply that the remaining search is difficult.

Do not claim that a genetic algorithm always beats random search. Compare methods using the same evaluation budget and multiple independent runs.
