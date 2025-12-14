# AdaBoost (Adaptive Boosting)

Adaptive Boosting (AdaBoost) is an ensemble classification method that trains many individual "weak learners" sequentially, updating their sample weights based on previous misclassification and assigning a weight to each learner's contribution to the final prediction based on its effectiveness.

In this project, we implement the AdaBoost algorithm from scratch using `numpy` and compare our results to the `AdaBoostClassifier` from `scikit-learn`. Our implementation relies on the most common weak learner used with AdaBoost, a Decision Tree with a depth of 1 (also known as a Decision "Stump"), which we implement separately as the `Stump` class.

We test this implementation against sklearn's `AdaBoostClassifier` on the [WI Breast Cancer Diagnostic](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic) dataset and confirm that we can reproduce sklearn's results with the same decision boundary and test score of `0.9736842...`

## Prerequisites

To ensure all dependencies are met, create a new conda environment with the specifications from `ada-boost.yml`:
```bash
conda env create -n adaboost -f ada-boost.yml
conda activate adaboost
```
The model classes and subsequent sklearn tests are all defined in `model.ipynb` as sections:

* **Overview** contains more detailed information on the algorithm
* **Model** contains definitions for the `Stump` and `AdaBoost` classes
* **Check Model** contains unit tests for the classes
* **Main** contains code for training a binary classifier on the [WI Breast Cancer Diagnostic](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic) dataset, comparing our implementation to sklearn's

Run the cells using a kernel from the conda environment defined above.

## Reports

A final report generated from the `model.ipynb` notebook as a pdf as well slides used during the presentation of our findings can be found in `/reports`. This project was completed for the Fall 2025 section of `DATA2060: Machine Learning`.

## References

1. Freund, Y. & Schapire, R.E., 1997. A Decision‑Theoretic Generalization of On‑Line Learning and an Application to Boosting. Journal of Computer and System Sciences, 55(1), pp.119–139. https://doi.org/10.1006/jcss.1997.1504

2. GeeksforGeeks, 2025. AdaBoost in Machine Learning. [online] Available at: https://www.sciencedirect.com/science/article/pii/S002200009791504X [Accessed 5 December 2025].  

3. Schapire, R.E., 2013. Explaining AdaBoost. In: B. Schölkopf, Z. Luo and V. Vovk, eds. Empirical Inference: Festschrift in Honour of Vladimir N. Vapnik. Berlin: Springer, pp.37–52. DOI: 10.1007/978‑3‑642‑41136‑6_5.  

4. de Giorgio, A., 2023. Systematic review of class imbalance problems in machine learning and deep learning solutions in manufacturing. Expert Systems with Applications, 229, p.120193. Available at: https://www.sciencedirect.com/science/article/pii/S0278612523002157 [Accessed 5 December 2025].

## Contributors

* Kate Gilbert, kate_gilbert@brown.edu
* Pranav Gundrala, pranav_gundrala@brown.edu