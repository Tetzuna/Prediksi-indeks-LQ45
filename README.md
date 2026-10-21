# Prediksi Indeks Harga Saham LQ45 Menggunakan Machine Learning & Deep Learning

Repositori ini berisi proyek analisis dan peramalan (*time series forecasting*) untuk memprediksi pergerakan nilai indeks harga saham **LQ45** di Bursa Efek Indonesia (BEI). Proyek membandingkan performa antara model statistik klasik, *ensemble learning*, dan model berbasis *Deep Learning* (Neural Network dengan *epoch*).

---

## 📌 Fitur & Metodologi
- **Sumber Data:** Data historis sekunder dari konstituen LQ45 (diambil melalui Kaggle).
- **Data Preprocessing & Aggregation:** Menggabungkan data emiten menjadi deret waktu harian indeks LQ45.
- **Feature Engineering:** 
  - `Lag_1` (Harga penutupan hari sebelumnya)
  - `MA_5` & `MA_20` (Moving Average 5 dan 20 hari)
- **Model yang Diuji:**
  1. **Linear Regression** (Regresi Linier)
  2. **Random Forest Regressor** (Model Berbasis Ensemble)
  3. **Neural Network / ANN** (Model Berbasis *Epoch* menggunakan TensorFlow/Keras)
- **Metrik Evaluasi:** $R^2$ Score, *Mean Squared Error* (MSE), *Root Mean Squared Error* (RMSE), *Mean Absolute Error* (MAE), dan *Mean Absolute Percentage Error* (MAPE).

---

## 📊 Hasil Perbandingan Performa
| Model | $R^2$ Score (Akurasi) | MSE (Error) |
| :--- | :---: | :---: |
| **Linear Regression** | **0,9683** | **2292,04** |
| **Random Forest Regressor** | 0,9155 | 6110,66 |
| **Neural Network (Epoch)** | Disesuaikan | Disesuaikan |

---

## 🛠️ Kebutuhan Sistem (Dependencies)
Pastikan Anda telah memasang pustaka Python berikut sebelum menjalankan skrip:
```bash
pip install pandas numpy scikit-learn tensorflow matplotlib seaborn