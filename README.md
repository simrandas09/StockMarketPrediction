# 📊 Stock Price Prediction Using Deep Learning and Hybrid Models

This project investigates the performance of multiple deep learning architectures for forecasting **daily stock market closing prices**, using the historical data of **AC.PA (Accor S.A.)**. The focus is on hybrid and sequential models, combining LSTM, BiGRU, SVR, and Transformer-based GANs. Evaluation was performed using **Root Mean Squared Error (RMSE)** and **R² Score**.

---

## 🧠 Models Evaluated

### ✅ LSTM + SVR (Hybrid Model)
- **Approach**: LSTM captures temporal patterns, SVR performs the final regression.
- **Performance**:  
  - RMSE: `0.0402`  
  - R²: `0.9677`
- **Insight**: Best performing model in this study; strong at capturing long-term dependencies with stable predictions.

---

### ✅ BiGRU + LSTM
- **Approach**: Bidirectional GRU for capturing context from both past and future → LSTM for sequence memory.
- **Performance**:  
  - RMSE: `0.0422`  
  - R²: `0.9644`
- **Insight**: High accuracy, slightly less than LSTM + SVR, but good adaptability to changing trends.

---

### ❌ GAN + Transformer
- **Approach**: Transformer-based generator within a GAN framework.
- **Performance**:  
  - RMSE: `0.2445`  
  - R²: `-0.1964`
- **Insight**: Underperformed significantly. GAN instability and Transformer overfitting likely caused issues.

---

## 📌 Key Conclusions

- The **LSTM + SVR** model demonstrated the **highest accuracy** and robustness, making it most suitable for stock market prediction in this context.
- **BiGRU + LSTM** showed excellent trend-following capabilities, with only a marginal dip in performance.
- **GAN + Transformer**, while theoretically promising, failed to generalize well—suggesting further tuning or alternate architectures are necessary for regression tasks in finance.
- Advanced **visualization and preprocessing techniques** were vital to improving model effectiveness.

---

