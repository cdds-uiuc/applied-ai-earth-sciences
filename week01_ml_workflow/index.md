# Week 1: Your toolkit and the machine-learning workflow

**This week in one sentence.** Get your tools working, and walk the five-step
workflow once with the simplest model there is, a straight line, on real river
catchments.

Week 1 is a setup week on purpose. Setting up the environment, learning how a
notebook runs, and learning how to use an AI assistant responsibly are part of
the content of an applied AI course. If something does not install, continue
on Google Colab (upload the notebook there; the [setup page](W01_core0_setup.md)
shows how) and sort it out in Week 2; the Week 1 discussion thread is for
exactly that.

## Goals

- Run a notebook top to bottom from a clean kernel, and know why that is the test of correct work. (Learning outcome 3, 7.)
- Describe the five steps of the ML workflow and what each produces. (LO 1.)
- Explain what a loss function measures and how gradient descent lowers it. (LO 3.)
- Fit, evaluate against a baseline, and interpret a linear regression on real catchment data. (LO 1, 3, 6.)
- State what the course's AI-assistant policy allows. (LO 7.)

## Before you start

From 517 you need: reading a CSV with pandas, NumPy arrays and their shapes,
and a matplotlib scatter plot. Nothing about scikit-learn is assumed; the
notebooks introduce it. Before the first notebook, work through
[`W01_core0_setup.md`](W01_core0_setup.md) (step 0 below): it gets the notebooks onto your
machine, or into Google Colab, and a kernel running.

## Order of work and time

| Step | Item | Time |
|---|---|---|
| 0 | `W01_core0_setup.md` — get the notebooks, create the `geol522` environment or open Colab | 15 min (Colab) to 1–2 h (local install) |
| 1 | Watch the lecture | 20–30 min |
| 2 | `W01_core1_toolkit.ipynb` — your toolkit | 45–60 min |
| 3 | `W01_core2_ml_workflow.ipynb` — the workflow with linear regression | 60–75 min |
| 4 | Concept-check quiz on Canvas (two questions need the core exercises done) | 15 min |
| 5 | `W01_labA_camels_regression.ipynb` — mean flow from catchment attributes | 2–3 h |
| 6 | `W01_hw_camels_regression.ipynb` — short this week | 1.5–2 h |

Due Monday of Week 2, 11:59 pm Central: lab completion and homework.

## Where this goes next

Week 2 takes the same CAMELS data and asks what happens when the model is
allowed to bend: polynomial features, overfitting, and the two regularization
methods (Ridge, Lasso) that keep flexibility honest. The train/test split and
the baseline from this week are used in every week that follows.

## References

- James, Witten, Hastie and Tibshirani, *An Introduction to Statistical Learning* (2nd ed.), chapter 2 (statistical learning) and section 3.1 (simple linear regression). Free PDF.
- scikit-learn user guide: *Linear models*, and the *Getting started* page for the `fit`/`predict` pattern.
- Addor, N., Newman, A. J., Mizukami, N., and Clark, M. P. (2017). The CAMELS data set: catchment attributes and meteorology for large-sample studies. *Hydrology and Earth System Sciences* 21, 5293–5313.
- Kratzert, F., Klotz, D., Shalev, G., Klambauer, G., Hochreiter, S., and Nearing, G. (2019). Towards learning universal, regional, and local hydrological behaviors via machine learning applied to large-sample datasets. *Hydrology and Earth System Sciences* 23, 5089–5110. (The source of the 27 attributes used as features.)
