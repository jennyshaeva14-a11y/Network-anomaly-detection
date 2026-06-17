# 🔐 Network Anomaly Detection System

Aplikasi deteksi anomali jaringan menggunakan **CNN + Attention Mechanism**.

**UAS Kecerdasan Buatan — Cyber Security**

---

## 🚀 Demo Aplikasi

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://your-app-name.streamlit.app)

---

## 📋 Fitur Aplikasi

| Fitur | Keterangan |
|-------|-----------|
| 🔍 Deteksi Manual | Input fitur jaringan secara manual |
| 📂 Deteksi via CSV | Upload file CSV untuk prediksi batch |
| 📊 Performa Model | Visualisasi metrik evaluasi |
| ℹ️ Tentang | Detail penelitian & referensi |

---

## 🧠 Model

- **Metode Usulan:** CNN + Attention Mechanism
- **Baseline:** CNN, LSTM, Random Forest
- **Dataset:** CICIDS2017
- **Task:** Binary Classification (BENIGN vs ATTACK)

### Hasil Eksperimen

| Model | Accuracy | F1-Score | AUC-ROC |
|-------|----------|----------|---------|
| CNN (Baseline) | 94.1% | 93.6% | 94.5% |
| LSTM (Baseline) | 95.3% | 94.9% | 95.7% |
| Random Forest | 94.4% | 94.0% | 94.8% |
| **CNN+Attention ⭐** | **97.4%** | **97.1%** | **97.9%** |

---

## 🗂️ Struktur Project

```
network_anomaly_app/
├── app.py                  # Streamlit app utama
├── requirements.txt        # Library yang dibutuhkan
├── README.md               # Dokumentasi ini
└── models/                 # Folder model (opsional)
    ├── best_cnn_attention.keras
    └── scaler.pkl
```

---

## ⚙️ Cara Jalankan Lokal

```bash
# 1. Clone repo
git clone https://github.com/USERNAME/network-anomaly-detection.git
cd network-anomaly-detection

# 2. Install library
pip install -r requirements.txt

# 3. Jalankan app
streamlit run app.py
```

---

## 🏗️ Arsitektur CNN + Attention

```
Input (40 fitur, 1)
    ↓
CNN Block 1 (Conv1D 64 + BatchNorm + MaxPool)
    ↓
CNN Block 2 (Conv1D 128 + BatchNorm)
    ↓
Attention Layer  ← NOVELTY
    ↓
Dense(128) → Dropout(0.3)
    ↓
Dense(64)  → Dropout(0.3)
    ↓
Output: Sigmoid → BENIGN / ATTACK
```

---

## 📚 Referensi

1. Wang et al. — CNN-LSTM-Transformer, PLOS ONE, 2025
2. Yin et al. — Multi-Head Attention Transformer, Scientific Reports, 2025
3. Alsharaiah et al. — LSTM+Attention NIDS, IJDNS, 2024
4. Tang — Transformer NIDS, CSCE 2024
5. Elsayed et al. — CNN-LSTM SDN, ACM, 2021
