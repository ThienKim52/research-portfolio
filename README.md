# Research Portfolio

A personal portfolio focused on mathematical foundations, machine learning, and computer vision. This repository documents the learning process through explanations, algorithm implementations, reproducible experiments, and analysis.

## Learning Goals

- Strengthen the linear algebra, calculus, probability, and optimization foundations needed for machine learning.
- Understand algorithms by implementing them before relying on high-level libraries.
- Use PyTorch to build, train, and evaluate computer vision models.
- Design controlled benchmarks and experiments with clearly documented data, metrics, and limitations.
- Study the trade-off between image segmentation quality and model storage and computation costs.

## Research Goals

Build small, verifiable, and reproducible studies: define a question, establish a baseline, select suitable metrics, compare methods under consistent conditions, and report limitations. The planned application areas are edge detection on cultural object images and flood image segmentation with model compression methods.

Numerical results, conclusions, and completion status will only be reported after experiments have been run. Large, copyrighted, or sensitive datasets will not be added to this repository unless their usage rights are clear.

## Checkpoint Roadmap

The checkpoints below are a planned roadmap based on the current project structure. Each checkpoint should include relevant notes or source code; experimental results should include configuration details and reproduction instructions.

### CP0 — Portfolio Setup

- [x] **CP0.1 — Repository foundation:** create a public repository; complete the README, changelog, and project structure; list all checkpoints; create and push the `cp-0.1` tag.
- [ ] **CP0.2 — Math for ML (due November 27, 2026):** complete two Jupyter notebooks: derivatives and numerical gradients, then gradient descent for one- and two-variable functions. Compare analytical and numerical gradients; visualize convergence for small, medium, and large learning rates.
- [ ] **CP0.3 — Machine learning fundamentals:** explain datasets, features, labels, train/validation/test splits, supervised and unsupervised learning, classification and regression, loss, overfitting/underfitting, cross-validation, data leakage, and accuracy/precision/recall/F1.
- [ ] **CP0.4 — Algorithms from scratch:** implement k-nearest neighbors (kNN), a decision tree, and K-means; test them on small datasets and use evaluation methods appropriate to supervised classification versus unsupervised clustering.
- [ ] **CP0.5 — Reproducible workflow:** define the Python environment, dependency and naming conventions, quality checks, and experiment organization.
- [ ] **CP0.6 — Application experiment plans:** finalize the research questions, data scope, baselines, metrics, and completion criteria for both application projects.

### CP1 — Mathematical Foundations for ML (`math-for-ml/`)

- [ ] **CP1.1 — Linear algebra:** vectors, matrices, linear transformations, eigenvalues, and geometric intuition.
- [ ] **CP1.2 — Calculus and probability:** derivatives/gradients, the chain rule, probability distributions, and expectation.
- [ ] **CP1.3 — Optimization:** loss functions, gradient descent, learning rates, and their connection to model training.

### CP2 — Machine Learning from Scratch (`ml-methods-from-scratch/`)

- [ ] **CP2.1 — Data and baselines:** data pipelines, dataset splits, preprocessing, and appropriate metrics.
- [ ] **CP2.2 — Core algorithms:** implement selected fundamental ML algorithms, state their assumptions, and test them on small examples.
- [ ] **CP2.3 — Evaluation and analysis:** compare against reference libraries, analyze errors, and document implementation limitations.

### CP3 — Computer Vision with PyTorch (`pytorch-cv-fundamentals/`)

- [ ] **CP3.1 — PyTorch fundamentals:** tensors, autograd, `Dataset`/`DataLoader`, and training loops.
- [ ] **CP3.2 — Models and training:** build a CNN, monitor training, and save/load checkpoints.
- [ ] **CP3.3 — Computer vision evaluation:** establish a computer vision baseline, define metrics, analyze errors, and document a reproducible workflow.

### CP4 — Cultural Object Edge Benchmark (`cultural-object-edge-benchmark/`)

- [ ] **CP4.1 — Benchmark scope:** define the question, permitted data sources, annotation criteria, and data-splitting procedure.
- [ ] **CP4.2 — Methods and metrics:** select edge-detection baselines, standardize inputs/outputs, and define evaluation metrics.
- [ ] **CP4.3 — Experiments:** compare methods under consistent conditions, analyze results, and report limitations and reproducibility details.

### CP5 — Flood Segmentation and Model Compression (`flood-segmentation-compression/`)

- [ ] **CP5.1 — Segmentation baseline:** identify the dataset and usage rights, preprocessing pipeline, baseline model, and metrics.
- [ ] **CP5.2 — Model compression:** investigate suitable compression methods and measure quality, model size, and inference cost.
- [ ] **CP5.3 — Comparison and report:** compare the baseline with compressed models, analyze trade-offs, and describe next steps.

## CP0.2 Study Plan

**Deadline:** Friday, November 27, 2026.
**Planning assumption:** 8–10 study hours per week. If your available time differs, keep the same sequence and adjust the number of sessions.

| Dates | Focus | Study tasks | Deliverable |
|---|---|---|---|
| Nov 7–8 | Setup and baseline | Confirm the notebook environment; review derivatives, partial derivatives, and Python functions; run the provided finite-difference example. | Notebook files created with headings, goals, and a working kernel. |
| Nov 9–15 | Notebook 01: derivatives and numerical gradients | Work through one-variable and multivariable derivatives; implement central finite differences; compare numerical and analytical gradients over several inputs and epsilon values. | Notebook 01 with explanations, implementations, comparisons, and a short error analysis. |
| Nov 16–22 | Notebook 02: gradient descent | Implement gradient descent for a one-variable and a two-variable function; try small, medium, and deliberately too-large learning rates; plot objective values and parameter trajectories. | Notebook 02 with runnable experiments and an explanation of convergence and divergence. |
| Nov 23–27 | Review and release | Restart and run both notebooks from top to bottom; check outputs, labels, plots, and markdown; explain the results without reading the code; commit the finished work. | Two reproducible notebooks and a short completion note linked from `math-for-ml/README.md`. |

### Notebook acceptance criteria

**Notebook 01 — Derivatives and Numerical Gradient**

- Explain one-variable derivatives, multivariable derivatives, and partial derivatives using worked examples.
- Implement the supplied example, `f(x) = x**2 + 3*x + 2`, and show that its analytical derivative at `x = 2` agrees with the central finite-difference estimate within a stated tolerance.
- Extend the numerical-gradient implementation to a multivariable function and compare each component with its analytical gradient.
- Briefly explain how the finite-difference step size `eps` affects numerical error.

**Notebook 02 — Gradient Descent**

- Implement gradient descent without using an optimizer library for both one- and two-variable functions.
- Record objective value and parameters at each iteration; plot convergence and, for the two-variable case, the parameter path.
- Compare a small, moderate, and too-large learning rate. Explain divergence using the update rule or observed values, not just the plot.
- State the initial point, stopping criterion, learning rates, and iteration limit so another learner can reproduce the experiment.

Suggested functions with known minima are `f(x) = x**2 + 3*x + 2` and `g(x, y) = (x - 2)**2 + 2*(y + 1)**2`. Choose learning rates based on these functions and verify the behavior rather than assuming a rate is stable.

## CP0.3 and CP0.4 Learning Notes

Before computer vision, be able to explain these machine learning fundamentals in your own words:

1. Dataset, feature, and label.
2. Training, validation, and test sets, and why the test set is held out.
3. Supervised and unsupervised learning.
4. Classification and regression.
5. Loss functions.
6. Overfitting and underfitting.
7. Cross-validation.
8. Data leakage and how to prevent it.
9. Accuracy, precision, recall, and F1-score, including when accuracy can mislead.

For CP0.4, implement kNN and a decision tree as supervised classifiers, and K-means as an unsupervised clustering algorithm. Use stratified 5-fold cross-validation for the supervised classifiers when the dataset and class counts support it; fit preprocessing only on each training fold. Do not apply that same protocol to K-means: use a clustering metric such as Silhouette Score when labels are unavailable, or Adjusted Rand Index when reference labels are available. Explain what each metric measures and its limitations.

## Repository Structure

```text
Research-portfolio/
├── README.md
├── CHANGELOG.md
├── .gitignore
├── math-for-ml/
├── ml-methods-from-scratch/
├── pytorch-cv-fundamentals/
├── cultural-object-edge-benchmark/
└── flood-segmentation-compression/
```

Each project folder has its own README describing its scope and status. Datasets, trained models, and large result files will be managed separately; they should not be committed before checking licensing and file size.

## Status

- **CP0.1:** complete; the public GitHub repository, `main` branch, and `cp-0.1` tag are present on GitHub.
- **CP0.2:** planned; deadline November 27, 2026.
- **Remaining checkpoints:** not started.
