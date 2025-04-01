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

Table C: Experimental comparisons on the ImageNet-1k benchmark.
| Method | iNaturalist | SUN | Places | Texture | Average |
| :---: | ----- | ----- | ----- | ----- | ----- |
|  | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC |
| LoCoOpGL | 16.05/96.86 | 23.44/95.07 | 32.87/91.98 | 42.28/90.19 | 28.66/93.52 |
| LoCoOpMCM | 23.06/95.45 | 32.70/93.35 | 39.92/90.64 | 40.23/91.32 | 33.98/92.69 |
| DualCnst(ours) | 1.29/99.65 | 17.60/95.89 | 31.91/92.13 | 42.15/90.51 | **23.24/94.55** |

Table D: Experimental comparisons on the ImageNet-1k task, with near and far datasets evaluated as OOD data.
| Method | ssb-hard | NINOC | iNaturalist | Texture | Average |
| :---: | ----- | ----- | ----- | ----- | ----- |
|  | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC |
| NegLabel | 87.57/68.60 | 73.36/73.79 | 1.91/99.49 | 43.56/90.22 | 51.60/83.03 |
| LSA | 69.13/79.57 | 72.00/76.88 | 28.53/93.90 | 65.21/79.41 | 58.72/82.44 |
| DualCnst(ours) | 85.94/68.81 | 70.76/76.26 | 1.29/99.65 | 42.15/90.51 | **50.03/83.80** |

Table E: Time comparison for accelerated SD models.
| SD model | Time to generate ID images | Time to generate both ID and OOD images |
| :---: | :---: | :---: |
| SD1. 5 | 55m42s | 10h22m |
| SDXL-Turbo | **4m10s** | **55m52s** |

Table F: Performance comparison between SD models in the DualCnst method.
| SD model | iNaturalist | SUN | Places | Texture | Average |
| :---: | ----- | ----- | ----- | ----- | ----- |
|  | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC |
| SD1. 5 | 1.29/99.65 | 17.60/95.89 | 31.91/92.13 | 42.15/90.51 | 23.24/94.55 |
| SDXL-Turbo | 1.29/99.67 | 17.46/95.82 | 31.51/92.01 | 41.52/90.74 | **22.95/94.56** |

Table G: Experimental comparisons on the ImageNet-1k task, with iNaturalist, SUN, Places, and Texture used as out-of-distribution (OOD) data for evaluation.
| Method | iNaturalist | SUN | Places | Texture | Average |
| :---: | ----- | ----- | ----- | ----- | ----- |
|  | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC |
| DualCnst(ours) | 1.29/99.65 | 17.60/95.89 | 31.91/92.13 | 42.15/90.51 | **23.24**/94.55 |
| LAPt | 1.16/99.63 | 19.12/96.01 | 33.01/92.01 | 91.06/40.32 | 23.40/**94.68** |

Table H: Performance comparison of integrating DualCnst with MCM for OOD detection on ImageNet-1k (ID dataset) .
| SD model | ssb-hard | NINOC | iNaturalist | Texture | Average |
| :---: | ----- | ----- | ----- | ----- | ----- |
|  | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC |
| MCM | 89.43/64.15 | 82.70/69.85 | 30.91/94.61 | 57.77/86.11 | 65.20/78.68 |
| MCM+DualCnst | 88.69/63.66 | 78.96/74.05 | 28.56/94.77 | 58.72/85.82 | **63.73/79.58** |

Table I: Experimental comparison between real OOD samples and synthetic OOD samples, with ImageNet-1k as the ID dataset.
| Source of OOD images | iNaturalist | SUN | Places | Texture | Average |
| :---: | ----- | ----- | ----- | ----- | ----- |
|  | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC |
| Synthetic OOD samples | 1.29/99.65 | 17.60/95.89 | 31.91/92.13 | 42.15/90.51 | 23.24/94.55 |
| Real OOD samples | 1.73/99.28 | 6.55/98.67 | 18.51/95.69 | 22.64/95.35 | **12.36/97.25** |

Table J: Performance comparison between SD model and DiT models in the DualCnst method.
| SD model | iNaturalist | SUN | Places | Texture | Average |
| :---: | :---: | :---: | :---: | :---: | :---: |
|  | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC |
| SD1. 5 | 1.29/99.65 | 17.60/95.89 | 31.91/92.13 | 42.15/90.51 | 23.24/**94.55** |
| Hunyuan-DiT | 1.51 & 99.62 | 17.55 & 95.95 | 31.24 & 92.18 | 42.46 & 90.37 | **23.19 &** 94.53 |

Table K: Experimental comparison under generated image style shifts. ID dataset: ImageNet-1k.
| Image Style (Method) | iNaturalist | SUN | Places | Texture | Average |
| :---: | ----- | ----- | ----- | ----- | ----- |
|  | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC | FPR95/AUROC |
| Natural Images (DualCnst) | 1.29/99.65 | 17.60/95.89 | 31.91/92.13 | 42.15/90.51 | **23.24/94.55** |
| Oil Painting Images (DualCnst) ） | 1.31/99.65 | 17.73/95.79 | 32.18/92.00 | 44.10/90.04 | 23.83/94.37 |
| NegLabel | 1.91/99.49 | 20.53/95.49 | 35.59/91.64 | 43.56/90.22 | 25.40/94.21 |

Table L: OOD Detection Experiments on Remote Sensing Data.
| Method | AID |
| :---: | :---: |
|  | FPR95/AUROC |
| NegLabel | 97.98/62.46 |
| DualCnst(ours) | **97.19/66.11** |

