# Housing model results | Portfolio edition

Jesse Coggins | WGU D600 | November 2026

I evaluated three approaches on 7,000 properties: price regression using size and school rating, classification of luxury status using bedrooms and bathrooms, and regression on principal components. The price fits report training R²; luxury accuracy describes a separate held-out classification outcome.

## Final price model and its comparison

The submitted final model retains **SquareFootage and SchoolRating**, both statistically significant in the fitted OLS summary. Its training R² is **0.354** (adjusted R² **0.353**). The SquareFootage-only model is a comparison with R² **0.295**, not the submitted final model. The residual and Q-Q figures use the two-predictor model.

| Final price-model metric | Verified notebook value |
|---|---:|
| Training MSE ($ squared) | 14,797,731,172.37 |
| Test MSE ($ squared) | 13,350,444,375.96 |

The original report’s E5 prose gives 1,479,773,117.37 and 1,335,044,375.96, roughly tenfold transcription errors. This edition uses the notebook outputs, reproduced in a fresh run. Model coefficients and fitted predictions were not changed to repair the prose. The original submitted files remain unchanged.

Size and school rating support a pricing comparison within this dataset, but the model leaves substantial price variation unexplained. Associations do not establish that a renovation or a change in school rating will cause an equivalent price increase. The residual diagnostics should be inspected before relying on an individual estimate.

## Luxury classification

Bedrooms and bathrooms predict IsLuxury with **68.70% training** and **67.21% test accuracy**. Both predictors remain in the fitted model. AIC is **6688.13** and BIC **6708.02**; the report’s 6690 and 6710 are coarse rounding. This task classifies a label rather than estimating a dollar price.

## Principal component regression

Four components retain approximately **50.72% of predictor variance**. PC4 is then removed from regression; PC1–PC3 give training R² **0.629** (adjusted R² **0.628**). Predictor variance and variance in Price explained by regression are different quantities.

| Principal component regression metric | Verified notebook value |
|---|---:|
| Training MSE ($ squared) | 8,503,731,548.34 |
| Test MSE ($ squared) | 8,440,870,587.90 |

The submitted report prose gives 850,373,154.34 and 844,087,058.79. These are roughly tenfold transcription errors; the notebook values above were reproduced. The coursework fits the scaler and PCA before the split, so the test predictor distribution informs preprocessing. The reported test error is exploratory: a stricter deployment evaluation must fit those transforms on training data only. No new model fit was substituted for the coursework result.

## Evidence and scope

[Linear model](../notebooks/linear_regression.ipynb) · [Luxury model](../notebooks/logistic_regression.ipynb) · [PCA model](../notebooks/pca_analysis.ipynb) · [Original figures](../assets/housing/README.md)

The verified rerun reproduced the saved numerical fits. It did not measure investment returns, marketing lift or causal effects. These models support exploratory valuation and classification questions; actual financial benefits require a separate evaluation.

Verified environment: Python 3.13.1, numpy 2.2.2, pandas 2.2.3, scipy 1.15.2, scikit-learn 1.6.1, statsmodels 0.14.4, matplotlib 3.10.0, seaborn 0.13.2.
