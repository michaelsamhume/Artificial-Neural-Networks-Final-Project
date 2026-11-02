# Predicting the NBA’s Next Great Shooter

**Machine learning for predicting season-over-season changes in NBA three-point shooting percentages.**

This collaborative project compares an artificial neural network (ANN), linear regression, and a no-change baseline using historical NBA shooting data and player features.

## Technical write-up

Read the full [project blog post](docs/ANN-Blog-Post.pdf), covering the dataset, feature engineering, experiments, results, and limitations. The original article references a collaborator's repository; this repository hosts a separate copy of the project.

## Results

| Model | MAE | RMSE |
|---|---:|---:|
| No-change baseline | 0.04354 | 0.05767 |
| Linear regression | **0.03591** | **0.04769** |
| Neural network | 0.03607 | 0.04814 |

Both trained models outperform the no-change baseline. The linear regression model slightly outperforms the neural network on this evaluation.

## Project files

- [`notebooks/Shotprediction_final.ipynb`](notebooks/Shotprediction_final.ipynb): data preparation, features, training, and evaluation
- [`docs/ANN-Blog-Post.pdf`](docs/ANN-Blog-Post.pdf): detailed project article
- [`data/README.md`](data/README.md): dataset sources and reproducibility notes
- [`requirements.txt`](requirements.txt): Python dependencies

## Running the notebook

The notebook was developed in Google Colab and contains `/content/` paths and shell commands intended for that environment. Install the dependencies, configure Kaggle credentials using secure environment variables, and run the cells in order. The original notebook's outputs have been cleared to avoid exposing historical secrets; results above come from the original saved evaluation and write-up. Some cells may require path adjustments or API availability.

**Security:** The original notebook contained an exposed Kaggle API key. It has been removed from this copy, but the key must be revoked/regenerated in Kaggle before publishing. Do not commit secrets.

## Sources

- [NBA shots dataset on Kaggle](https://www.kaggle.com/datasets/mexwell/nba-shots)
- [nba_api](https://github.com/swar/nba_api)

## Project context

Collaborative academic machine-learning project. See the technical write-up for the original research context.
