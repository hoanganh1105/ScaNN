# ScaNN vs Brute-Force Approximate Nearest Neighbor Search

### Advanced Data Structures and Algorithms – Talent Program  
Ho Chi Minh City University of Technology (HCMUT)

---

## 📘 Overview
This project implements and evaluates **ScaNN (Scalable Nearest Neighbors)** — a high-performance approximate nearest neighbor (ANN) search algorithm developed by **Google Research**.  
ScaNN combines **partitioning**, **vector quantization**, and **asymmetric hashing** to achieve efficient large-scale vector retrieval.  
We compare the performance of ScaNN against a baseline **brute-force** search to explore trade-offs between **accuracy**, **speed**, and **memory efficiency**.

---

## 🎯 Objectives
- Study and understand the architecture of **ScaNN** (partitioning → scoring → reordering).  
- Build an **ANN search system** using ScaNN in Python.  
- Implement a **brute-force search** as a performance baseline.  
- Conduct experiments to compare query latency, recall@K, and memory usage.  
- Visualize performance metrics through clear and reproducible plots.

---

## 🧠 Theoretical Background
ScaNN accelerates nearest neighbor search by reducing the number of distance computations required.  
Its three main components are:
1. **Partitioning** – clusters the dataset into smaller regions.  
2. **Scoring** – selects the most relevant partitions based on approximate distances.  
3. **Reordering** – re-ranks the candidates using exact distances for higher accuracy.  
Compared with other ANN methods like **Faiss**, **HNSW**, and **Annoy**, ScaNN achieves a strong balance between **speed** and **recall** for large vector databases.

---

## 🧩 Project Structure
```
scann-ann/
├── data/
│   ├── vectors.npy            # generated or preprocessed dataset
│   └── queries.npy            # sample query vectors
│
├── src/
│   ├── brute_force.py         # baseline linear search implementation
│   ├── scann_search.py        # ScaNN-based ANN search
│   ├── evaluate.py            # accuracy, timing, memory evaluation
│   ├── visualize.py           # performance plots
│   └── utils.py               # helper functions
│
├── notebooks/
│   └── demo.ipynb             # interactive demonstration and analysis
│
├── results/
│   ├── timing_plot.png
│   ├── recall_plot.png
│   └── memory_comparison.png
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation
### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/scann-ann.git
cd scann-ann
```
### 2. Install dependencies
```bash
pip install -r requirements.txt
```
**Required libraries:**
```
scann
numpy
scikit-learn
sentence-transformers
matplotlib
```

---

## 🚀 Usage
### Run the experiments locally
```bash
python src/scann_search.py
```
or open the Jupyter notebook:
```bash
notebooks/demo.ipynb
```

### Example workflow
1. Generate or load vector datasets (e.g., from images or text embeddings).  
2. Build and query the ScaNN index.  
3. Run brute-force search for baseline comparison.  
4. Evaluate average query time and recall@K.  
5. Visualize the performance metrics.

---

## 📊 Expected Outputs
- **ScaNN** achieves significant speedup over brute-force with high recall.  
- Comparative plots:
  - Query time vs. K
  - Recall@K
  - Memory usage  
Example output:
```
Average query time:
  - Brute-force: 0.285 s
  - ScaNN:       0.012 s
Recall@10: 0.97
```

---

## 🧪 Experimental Setup
- **Dataset:** Random vectors or embeddings extracted via ResNet/SBERT  
- **Dimensions:** 128–768  
- **Queries:** 100 random vectors  
- **Evaluation metrics:**
  - Average query latency  
  - Recall@K (K = 5, 10, 20)  
  - Memory usage  
- **Hardware:** CPU-based testing (optionally GPU for embedding generation)

---

## 📈 Visualization
Performance results are plotted using `matplotlib`, including:
- Query time comparison between ScaNN and brute-force  
- Recall@K curves  
- Memory utilization histogram  

Example snippet:
```python
plt.plot(k_values, query_times_scann, label='ScaNN')
plt.plot(k_values, query_times_bruteforce, label='Brute-force')
plt.xlabel('K')
plt.ylabel('Average Query Time (s)')
plt.legend()
plt.show()
```

---

## 🧰 Tools and Environment
- **Language:** Python 3.10+  
- **Libraries:** ScaNN, NumPy, Matplotlib, Scikit-learn, Sentence-Transformers  
- **Supported Platforms:** Google Colab, Jupyter Notebook, or local Python environment

---

## 👥 Authors
- **Huỳnh Hoàng Anh**   
- **Ngô Trung Tín**   
- **Huỳnh Tấn Tiến**  

---

## 📜 License
This project is for **academic and educational purposes only**.  
© 2025, Ho Chi Minh City University of Technology – Faculty of Computer Science and Engineering.

---

## 🔗 Links
- 📘 [ScaNN Official Repository](https://github.com/google-research/google-research/tree/master/scann)  
- 📄 [Project Report (PDF)](report/report.pdf)  
- ▶️ [Google Colab Demo](https://colab.research.google.com/drive/your-demo-link)
