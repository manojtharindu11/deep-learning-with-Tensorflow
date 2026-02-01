# Deep Learning with TensorFlow (Practice Notebooks)

A small personal collection of hands-on notebooks while learning deep learning with **TensorFlow / Keras**.
The goal of this repo is to keep experiments easy to run, easy to find, and easy to reuse later.

## Quickstart

### 1) Create + activate a virtual environment

Windows (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 2) Install dependencies

```powershell
pip install -r requirements.txt
```

### 3) Run notebooks

- Recommended: open the repo in **VS Code** and run the `.ipynb` notebooks.
- If you want to run via Jupyter in a terminal, you may need to install it first:

```powershell
pip install notebook
jupyter notebook
```

## TensorBoard

If you’ve run notebook training that writes logs under `logs/`, you can visualize them with:

```powershell
tensorboard --logdir logs/
```

Then open the URL TensorBoard prints in the terminal.

## Project layout

Common folders:

- `data/` – small datasets used by notebooks (CSV/JSON/text)
- `datasets/` – larger datasets (e.g., flower photos)
- `images/` – small image samples used in simple demos
- `logs/` – TensorBoard logs
- `model/` – exported models (SavedModel / Keras / TFLite)

## Notebooks (index)

### Fundamentals

- [Activation functions](activation%20functions.ipynb)
- [Neural network for handwritten digits (MNIST)](neural%20network%20for%20handwritten%20digits.ipynb)

### Optimization (Gradient Descent)

- [Batch gradient descent](gradient_decent/batch_gradient_decent.ipynb)
- [Stochastic gradient descent](gradient_decent/stochastic_gradient_decent.ipynb)
- [Mini-batch gradient descent](gradient_decent/mini_batch_gradient_decent.ipynb)
- [Gradient descent (intro)](gradient_decent/gradient_decent.ipynb)
- [Gradient descent for neural network](gradient_decent/gradient_decent_for_neural_network.ipynb)

### Regularization & Overfitting

- [Dropout regularization](dropout%20regularization.ipynb)
- [Data augmentation to address overfitting](data%20augmentation%20to%20address%20overfitting.ipynb)

### Computer Vision (CNN)

- [Image classification using CNN](image%20classification%20using%20cnn.ipynb)
- [Transfer learning](transfer%20learning.ipynb)
- [GPU benchmarking in image classification](gpu%20benchmarking%20in%20image%20classification.ipynb)

### Input pipelines & performance

- [TensorFlow input pipeline](tensorflow%20input%20pipeline.ipynb)
- [Prefetch and cache](prefetch%20and%20cache.ipynb)

### NLP

- [Word embedding using Keras embedding layer](word%20embedding%20using%20keras%20embedding%20layer.ipynb)
- [Word2Vec](word2vec.ipynb)

### Practical ANN example

- [Customer churn prediction using ANN](customer%20churn%20prediction%20using%20ann.ipynb)

### Tooling

- [TensorBoard notebook](tensorboard.ipynb)

## Datasets used

- `data/customer_churn.csv` – used by the churn ANN notebook
- `datasets/flower_photos/` – used for transfer learning / augmentation notebooks
- `data/spam.csv`, `data/Cell_Phones_and_Accessories_5.json` – used for NLP notebooks

If a notebook fails due to missing files, check the `data/` and `datasets/` folders first.

## Saved outputs

- `logs/` – TensorBoard event files created during training
- `model/` – exported models, including TFLite versions

## Notes (future reference)

- If training is slow on Windows, consider CPU vs GPU setup differences (Windows-native TensorFlow GPU support may vary by version and driver; WSL2 is often the easiest path).
- Keep notebooks self-contained: prefer reading datasets via relative paths like `data/...`.
