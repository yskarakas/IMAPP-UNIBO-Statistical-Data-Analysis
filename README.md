# Statistical Data Analysis for Nuclear and Subnuclear Physics — Solutions

My solutions to the hands-on exercises of the IMAPP course, based on the original material by Gabriele Sirri:
**[gabriele-sirri/statistical-data-analysis](https://github.com/gabriele-sirri/statistical-data-analysis)**.

## Lab 1 · RooFit basics and likelihood fits

| Notebook | Topic | Key result |
|---|---|---|
| [`lab1_A_gaussian_exponential_ML_fits.ipynb`](lab1_A_gaussian_exponential_ML_fits.ipynb) | Unbinned & binned ML fits on toy data | σ = 3.002 ± 0.022 (truth 3), τ = 4.96 ± 0.30 (truth 4.5) |
| [`lab1_C_B0_ppbar_signal_background_fit.ipynb`](lab1_C_B0_ppbar_signal_background_fit.ipynb) | Extended signal + background fit, B⁰ → pp̄ | N_s = 34.0 ± 7.9 (≈ 4σ) |

*Note:* in the B⁰ → pp̄ notebook (exercise C) the mass range was extended to [5080, 5560] MeV, because one event at 5540.88 MeV lies outside the original range and recent ROOT versions reject it.

## Lab 2 · Likelihood, MINUIT and nuisance parameters

| Notebook | Topic | Key result |
|---|---|---|
| [`lab2_A_B0_ppbar_migrad_hesse_minos_profile.ipynb`](lab2_A_B0_ppbar_migrad_hesse_minos_profile.ipynb) | MIGRAD, HESSE and MINOS by hand with `RooMinimizer`; correlations, NLL slice vs profile, contours | N_s = 34.0 +8.3 −7.5 (MINOS), ± 7.9 (HESSE) |
| [`lab2_B_on_off_problem_profile_likelihood.ipynb`](lab2_B_on_off_problem_profile_likelihood.ipynb) | On/off counting experiment, profile likelihood vs MINOS vs slice | s = 13.2 +4.5 −3.9, b = 3.80 ± 0.60; poorer control region → profile interval 11 % wider |

*Notes:*
- Exercise A uses the same extended mass range [5080, 5560] MeV as Lab 1 C (`RooDataSet.read` silently drops the event at 5540.88 MeV otherwise).
- Exercise B: in ROOT 6.40 `RooProfileLL::getVal()` is already relative to the minimum, so the profile scan uses `prof.getVal()` without subtracting `nll_min`.

Run with ROOT 6.40 (Lab 1 on [CERN SWAN](https://swan.cern.ch)). Place the notebooks in `course/lab1/` or `course/lab2/` of the original repository (they read the data from `../../examples/`).

## License

EUPL-1.2, same as the original course material.
