Table A: Comparison with Other Baselines Using Fixed α=0.1.

| Method | iNaturalist | SUN | Places | Texture | Average |
| :---: | ----- | ----- | ----- | ----- | ----- |
|  | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC |
| MCM | 30.91/94.61 | 37.59/92.57 | 44.69/89.77 | 57.77/86.11 | 42.74/90.77 |
| NegLabel | 1.91/99.49 | 20.53/95.49 | 35.59/91.64 | 43.56/90.22 | 25.40/94.21 |
| ours(Optimal α) | 0.99/99.69 | 17.60/95.89 | 31.63/91.73 | 42.00/90.32 | 23.05/94.41 |
| ours(Fixed α=0. 1\) | 1.29/99.65 | 17.60/95.89 | 31.91/92.13 | 42.15/90.51 | 23.24/94.55 |

Table B: Robustness experiments on ImageNet-1k and ImageNet-R.

| Method | ssb-hard | NINOC | iNaturalist | Texture | Average |
| :---: | :---- | :---- | :---- | :---- | :---- |
|  | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC |
| MCM | 94.00/57.42 | 88.98/63.40 | 75.39/83.18 | 67.94/81.80 | 81.58/71.45 |
| NegLabel | 85.64/66.30 | 70.38/74.74 | 1.56/99.59 | 42.59/89.89 | 50.04/82.63 |
| DualCnst(ours) | 82.33/69.65 | 67.57/76.41 | 1.07/99.68 | 42.55/88.93 | **48.38/83.67** |
