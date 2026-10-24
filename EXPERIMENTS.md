# Experiment plan

Use this plan for a class demonstration or a small report. Record the objective, population size, mutation rate, crossover rate, generation budget, best result, and observations for every run.

## Experiment A — mutation rate

- Keep population size and crossover rate fixed.
- Run low, medium, and high mutation settings.
- Repeat each setting at least five times if time permits.
- Compare final best fitness and consistency.

**Question:** Does increasing mutation help exploration, or does it disrupt good solutions?

## Experiment B — population size

- Compare a small, medium, and large population.
- Keep the generation budget and other settings fixed.
- Note that larger populations use more fitness evaluations per generation.

**Question:** Does a larger population improve solution quality enough to justify the extra evaluations?

## Experiment C — crossover rate

- Compare a low crossover rate with a high crossover rate.
- Keep mutation and population size fixed.

**Question:** How does recombination affect progress in this objective?

## Experiment D — GA and random search

- Use a comparable evaluation budget.
- Repeat independent runs.
- Report average final fitness and spread, not only the single best run.

**Caution:** If the UI's comparison is a quick illustrative comparison, describe it as such. Do not present it as a statistically conclusive benchmark.
