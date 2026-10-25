# EvoSolve — Genetic Algorithm Optimization Studio

<p align="center">
  <strong>An interactive, browser-based lab for exploring Genetic Algorithms (GAs).</strong><br/>
  Adjust evolutionary parameters, watch populations evolve, compare against random search, and export experiment data — no installation or backend required.
</p>

<p align="center">
  <img alt="Static site" src="https://img.shields.io/badge/site-static-2563eb">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-vanilla-f7df1e?logo=javascript&logoColor=111">
  <img alt="License MIT" src="https://img.shields.io/badge/license-MIT-22c55e">
  <img alt="No dependencies" src="https://img.shields.io/badge/dependencies-none-14b8a6">
</p>

> **Live demo:** After enabling GitHub Pages, replace this line with your published URL: `https://rathoreniranjan18-beep.github.io/evosolve/`

## What is EvoSolve?

EvoSolve demonstrates how a Genetic Algorithm searches for better solutions by borrowing ideas from biological evolution. It is designed for students, instructors, and curious developers who want to see optimization concepts in action rather than only read about them.

### Features

- **Interactive optimization:** run, pause, step through, or reset an experiment.
- **Multiple objectives:** Target Match, Sphere, and Rastrigin.
- **Evolution controls:** configure population size, mutation rate, crossover rate, and generation count.
- **Live feedback:** inspect chromosomes and follow best/average fitness trends.
- **Baseline comparison:** compare a GA run with random search.
- **Experiment export:** download results as CSV for further analysis.
- **Zero setup:** single-page static app; no server, API key, build step, or external package is required.

## Quick start

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Choose an objective, adjust the parameters, and select **Run**.
4. Use **Step** to observe evolution one generation at a time.
5. Export the experiment CSV if you want to inspect the data in a spreadsheet.

To run a local web server (optional):

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## How the Genetic Algorithm works

1. **Initialize:** create a population of candidate chromosomes.
2. **Evaluate:** calculate a fitness score for each candidate.
3. **Select:** prefer higher-ranked candidates as parents.
4. **Crossover:** combine parent chromosomes to create offspring.
5. **Mutate:** randomly flip bits to maintain diversity.
6. **Elitism:** carry the current best candidate into the next generation.
7. **Repeat:** evaluate the next generation until the run ends.

The Target Match objective uses a 12-bit target chromosome (`101101001110`). Its fitness is the number of bit positions that match the target, so a perfect candidate scores 12. The Sphere and Rastrigin objectives provide additional optimization landscapes.

## Project structure

```text
evosolve/
├── index.html                  # Complete app (HTML, CSS, JavaScript)
├── README.md                   # Overview, setup, and usage
├── LICENSE                     # MIT License
├── CONTRIBUTING.md             # Contribution workflow
├── CODE_OF_CONDUCT.md          # Community expectations
├── SECURITY.md                 # Security reporting guidance
├── CHANGELOG.md                # Release history
├── CITATION.cff                # Citation metadata
├── .gitignore
├── .nojekyll                   # Tell GitHub Pages not to run Jekyll
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   └── feature_request.md
│   └── workflows/
│       └── pages-check.yml     # Basic HTML sanity check
└── docs/
    ├── ALGORITHM.md            # Algorithm notes and assumptions
    ├── EXPERIMENTS.md           # Suggested repeatable experiments
    └── DEPLOYMENT.md            # GitHub Pages instructions
```

## Suggested experiments

- **Mutation rate:** compare a low, medium, and high mutation rate while keeping other settings constant.
- **Population size:** test whether a larger population changes convergence speed or consistency.
- **Crossover rate:** compare low and high crossover rates over several runs.
- **GA vs random search:** repeat the comparison across multiple runs. A single run is illustrative, not proof that one method is always better.
- **Objective landscape:** compare the behavior of Target Match, Sphere, and Rastrigin.

For a fair comparison, keep the evaluation budget similar, repeat each configuration several times, and report the average and variability. Evolutionary algorithms are stochastic: results can differ between runs.

## Technology

- HTML5
- CSS
- Vanilla JavaScript
- Browser APIs for interaction and CSV download

## Limitations

- This is an educational visualization, not a production optimization service.
- Runs are stochastic, and one experiment is not enough to establish general performance.
- The GA and random-search comparison should be treated as an illustrative baseline unless you run repeated, budget-matched trials.
- The app runs locally in your browser; no data is sent to a server by the static page.

## Roadmap ideas

- [ ] Add seeded runs for reproducibility.
- [ ] Add repeated-trial statistics (mean, median, standard deviation).
- [ ] Add an experiment configuration JSON export.
- [ ] Add unit tests for fitness and genetic operators.
- [ ] Separate JavaScript and CSS into dedicated files.
- [ ] Add accessibility and mobile-browser regression checks.

## Deploy on GitHub Pages

Follow [`docs/DEPLOYMENT.md`](docs/DEPLOYMENT.md). Once published, add the live URL above and optionally add a screenshot/GIF to this README.

## Contributing

Bug reports, suggestions, documentation improvements, and pull requests are welcome. Read [`CONTRIBUTING.md`](CONTRIBUTING.md) first.

## License

Released under the MIT License. See [`LICENSE`](LICENSE).
