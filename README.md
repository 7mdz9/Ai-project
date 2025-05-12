# Car Transmission Classifier 🚗⚙️

A beginner‑friendly machine‑learning project that guesses whether a used car is **manual** or **automatic** by reading its basic specs.

---

## 1. What this project does

* Uses a public dataset of 34 000 Indian used‑car ads.
* Cleans and tidies the raw data so a computer can understand it.
* Trains a small neural‑network model.
* Reaches about **91 % accuracy** on cars it hasn’t seen before.
* Saves the model and a helper script so you can test new cars easily.

---

## 2. Where the data comes from

We use the **Used Cars Dataset – CarDekho** on Kaggle.
[https://www.kaggle.com/datasets/sukritchatterjee/used-cars-dataset-cardekho](https://www.kaggle.com/datasets/sukritchatterjee/used-cars-dataset-cardekho)


---

## 3. Results

On a held‑out validation set the best model achieved:

| Metric               | Manual   | Automatic |
| -------------------- | -------- | --------- |
| Precision            | 0.92     | 0.89      |
| Recall               | 0.97     | 0.72      |
| F1‑score             | 0.94     | 0.80      |
| Overall accuracy |   91 %   |   –       |

---

## 4. How it works (short version)

1. **Feature Engineering** – keep 15 useful columns (like engine size, mileage) and fix messy text with regular expressions.
2. **Pre‑processing** – fill missing numbers with the median, scale all numbers to 0‑1, and one‑hot encode text columns.
3. **Model** – a feed‑forward neural network with three hidden layers (128‑64‑32) and a sigmoid output.
4. **Tuning** – test different optimizers, learning rates, and batch sizes. Best combo: RMSprop (lr 0.01) with batch 64.
5. **Saving** – store the trained model (`final_rmsprop_model.keras`) and the data‑cleaning pipeline (`preprocessing_pipeline.pkl`).

---

## 5. Credits

* Dataset by **Sukrit Chatterjee** on Kaggle.
* Code and write‑up by **Your Name** (feel free to fork or star!).

---

## 6. License

You can use it without crediting me.
