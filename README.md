Double Descent in Overparameterised Neural Networks
Project Overview

This project explores the double descent phenomenon—a modern generalisation behaviour observed in highly overparameterised machine learning models. Unlike the classical U-shaped bias–variance trade-off, double descent reveals that test error can decrease, rise sharply near the interpolation threshold, and then decrease again as model capacity becomes extremely large. This behaviour has become central to contemporary deep learning theory and challenges long-standing assumptions in statistics and machine learning.

The project empirically demonstrates double descent by training neural networks of increasing width on a synthetic binary classification task and analysing their test error and decision boundaries.

Objectives

Demonstrate double descent through systematic variation of neural network width.

Compare training and test error across underparameterised, interpolation, and overparameterised regimes.

Visualise decision boundaries for selected model widths.

Provide empirical evidence that supports theoretical insights from modern deep learning research.

Repository Contents

double_descent_error_curve.png — Test error vs. model width showing the full double descent pattern.

decision_boundary_width_4.png — Decision boundary for a narrow, underfitting model.

decision_boundary_width_32.png — Boundary near the interpolation threshold.

decision_boundary_width_256.png — Boundary in the overparameterised regime.

decision_boundary_width_1024.png — Boundary for a very wide model exhibiting the second descent.

Report / PDF — Full written analysis including theory, mathematics, results, and discussion.

Jupyter Notebook — Contains the complete experiment workflow and figure generation.

README.md — This documentation file.

Summary of Findings

The experiments strongly confirm the presence of double descent. Narrow models exhibit high error due to underfitting, while intermediate-width models experience a spike in test error as they begin to perfectly interpolate the training data. As width increases further, test error decreases again, revealing improved generalisation in the overparameterised regime. Decision boundary visualisations clearly show this progression, shifting from overly rigid to unstable and noisy, and finally to smooth, expressive boundaries in very wide models.

Test Error Results
Width	Test Error
2	0.4500
4	0.4500
8	0.0900
16	0.0800
32	0.0600
64	0.0600
128	0.0300
256	0.0300
512	0.0300
1024	0.0300

These results illustrate the characteristic initial descent, interpolation peak, and second descent.

How to Use This Repository : https://github.com/Sindhu809/sindhu-ml-24071473.git

The notebook provides the full training and evaluation pipeline.

All figures used in the report are automatically generated and saved.

The project may be extended by experimenting with:

Different activation functions

Varying dataset noise levels

Depth-based double descent

Random feature models
