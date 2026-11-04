# Statistical Data Analysis for Nuclear and Subnuclear Physics — Solutions

My solutions to the hands-on exercises of the IMAPP course, based on the original material by Gabriele Sirri:
**[gabriele-sirri/statistical-data-analysis](https://github.com/gabriele-sirri/statistical-data-analysis)**.

## Lab 1 · RooFit basics and likelihood fits

| Notebook | Topic | Key result |
|---|---|---|
| `ex_A.ipynb` | Unbinned & binned ML fits on toy data | σ = 3.002 ± 0.022 (truth 3), τ = 4.96 ± 0.30 (truth 4.5) |
| `ex_C.ipynb` | Extended signal + background fit, B⁰ → pp̄ | N_s = 34.0 ± 7.9 (≈ 4σ) |

*Note:* in `ex_C` the mass range was extended to [5080, 5560] MeV, because one event at 5540.88 MeV lies outside the original range and recent ROOT versions reject it.

Run on [CERN SWAN](https://swan.cern.ch) (ROOT 6.40). Place the notebooks in `course/lab1/` of the original repository.

## License

EUPL-1.2, same as the original course material.
