# Reproduction Instructions

## 1. Requirements

Install the packages listed in `requirements.txt`.

```bash
pip install -r requirements.txt
```

## 2. Inspect saved results

Open `UAV_Robust_Optimisation.ipynb` in Jupyter or Google
Colab and execute its cells.

## 3. Optimisation rerun

The notebook currently provides inspection of the saved
results. To rerun the original optimisation, include the
complete source implementation used to construct the graph,
generate scenarios, formulate the MILP, solve the model,
extract recourse paths and perform collision validation.

The saved CSV files alone are not sufficient to reconstruct
every solver decision.

## 4. Expected outputs

The repository includes the saved scenario results,
optimisation summary, collision-validation records,
route data and figures.

## 5. Interpretation

The experiments use a synthetic static environment and
finite sampled uncertainty scenarios. They are not real
flight tests or a statistical estimate of real-world
collision probability.
