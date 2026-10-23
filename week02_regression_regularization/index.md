# Week 2: Regression, regularization, and the bias–variance trade-off

**This week in one sentence.** Flexible models overfit; regularization keeps
the flexibility and tames the overfitting, and Lasso tells you which inputs
matter.

## Goals

- Explain, with the degree of a polynomial as the example, why training error and test error diverge as a model becomes more flexible. (LO 5.)
- Define bias and variance and say what more data does to each. (LO 5.)
- Fit Ridge and Lasso regressions, standardize correctly, and choose the penalty on a validation set. (LO 3.)
- Use Lasso's selected attributes as a hypothesis about the physics, and check it against domain knowledge. (LO 6.)

## Before you start

From Week 1 you need: the train/test split, the RMSE, the baseline, and the
scikit-learn `fit`/`predict` pattern (Week 1 core 2, sections "Step 3, the
scikit-learn way" and "Step 4"). The Week 2 lab and homework download the
same CAMELS files as Week 1; if `data/` from Week 1
is still on your machine, copying it into this week's folder saves the
download.

## Order of work and time

| Step | Item | Time |
|---|---|---|
| 1 | Watch the lecture | 20–30 min |
| 2 | `W02_core1_bias_variance.ipynb` | 45–75 min |
| 3 | `W02_core2_ridge_lasso.ipynb` | 45–75 min |
| 4 | Concept-check quiz on Canvas (four questions need the core exercises done) | 15 min |
| 5 | `W02_labA_camels_lasso.ipynb` — which catchment attributes matter? | 2–3 h |
| 6 | `W02_hw_camels_baseflow.ipynb` — what controls baseflow? | 3–5 h |

Due Monday of Week 3, 11:59 pm Central: lab completion and homework.

## Where this goes next

Week 3 fixes the remaining dishonesty in our evaluation: test catchments that
are neighbors of training catchments. It introduces cross-validation,
spatial and temporal leakage, metrics beyond RMSE, and the course's first
classifier.

## References

- James, Witten, Hastie and Tibshirani, *An Introduction to Statistical Learning* (2nd ed.), section 2.2 (bias–variance) and section 6.2 (shrinkage methods: ridge and lasso). Free PDF.
- scikit-learn user guide: *Linear models* (Ridge, Lasso) and *Preprocessing data* (StandardScaler).
- Addor, N., Newman, A. J., Mizukami, N., and Clark, M. P. (2017). The CAMELS data set: catchment attributes and meteorology for large-sample studies. *Hydrology and Earth System Sciences* 21, 5293–5313.
- Kratzert, F., Klotz, D., Shalev, G., Klambauer, G., Hochreiter, S., and Nearing, G. (2019). Towards learning universal, regional, and local hydrological behaviors via machine learning applied to large-sample datasets. *Hydrology and Earth System Sciences* 23, 5089–5110.
