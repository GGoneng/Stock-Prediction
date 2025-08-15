## 📌 Project Overview
- A project to explore whether **stock price patterns** can be predicted using AI.
- Focused on **Korean ETF prices** to minimize the influence of external factors.
- Collected price data by **web scraping NAVER Stock pages**.
- Includes a **Flask web application** for deployment.

<br><br>

## 🧩 Data Preprocessing
- **Data Collection**: Scraped ETF price data from NAVER Stock pages.
- **Sliding Window**: Segmented time series into windows to capture stock price patterns for training.
- **Scaling**: Experimented with multiple scaling methods and finally adopted **Robust Scaling**.

<br><br>

## 🤖 Model Training
- **Initial Approach**: Multi-Layer Perceptron (**MLP**) with layers increasing and then decreasing in size.
- **Final Model**: Switched to **LSTM**, which is more effective for sequence data.
- **Loss Function**: Used `L1 Loss`.
- **Challenges**:
  - Large stock price values caused excessively high loss values.
  - R² Score appeared abnormally high, making evaluation less meaningful.

<br><br>

## 📝 Limitations & Future Work
- **Limitations**:
  - Did not normalize stock prices across different ETFs (e.g., using rate of change or per-stock scaling).
- **Future Work**:
  - Try **Graph Neural Networks (GNN)** for graph pattern prediction.
  - Apply **transfer learning** from models already effective in stock price forecasting.

<br><br>
## 🛠️ Tech Stack

| Category        | Tools / Frameworks                |
|----------------|-----------------------------------|
| OS              | Windows 11 HOME                  |
| Language        | Python 3.8, HTML5, CSS3               |
| Libraries       | torch, sklearn, matplotlib, flask     |
| Environment     | Jupyter Notebook / VSCode             |
| Hardware        | GPU                                   |


<br><br>
## 📂 Project Structure

```bash
.
├── Stock_crawling.ipynb       # Web Scraping
├── make_csv.ipynb             # Data Preprocessing
├── stock_predict_model.ipynb  # Model Training          
└── [...]               
```

