# MovieLens Recommendation
Deep Learning Final Project

---

## Project Overview
Movie platforms rely on personalization to drive engagement and retention.  
However, building effective recommender systems under **implicit feedback only** (watch counts, no ratings) and **extreme sparsity (~98%)** is a major challenge.  

This project applies **deep learning models (MLP, CNN, GRU)** to the MovieLens dataset to answer the question:  
**Can sequential neural models improve accuracy and coverage compared to traditional baselines?**

---

## Objectives
1. Compare deep models (MLP, CNN, GRU) against baselines (MostPopular, MF, ItemKNN).  
2. Evaluate trade-offs between **accuracy, interpretability, and coverage**.  
3. Test **debiasing strategies** to mitigate popularity bias.  
4. Translate technical findings into **business implications** for personalization.  

---

## Dataset
This project uses the **MovieLens Latest Dataset** (GroupLens Research),  
which contains user–movie interactions with timestamps.  

- Dataset link: [MovieLens Latest](https://grouplens.org/datasets/movielens/latest/)

---

## Methodology
1. **Data Preparation**  
   - Construct user sequences and apply train/validation/test splits  
   - Negative sampling to simulate implicit feedback  
   - Handle class imbalance and sparsity  

2. **Baselines**  
   - MostPopular, Personal Top-K  
   - ItemKNN, Matrix Factorization  

3. **Deep Models**  
   - Multi-Layer Perceptron (MLP)  
   - Convolutional Neural Network (CNN)  
   - Gated Recurrent Unit (GRU)  

4. **Training & Evaluation**  
   - Metrics: Recall@K, Hit Rate, MRR  
   - Ablations: sequence length, negative ratio, embedding size  
   - Debiasing with popularity penalty (α=0.1)  

5. **Interpretation & Insights**  
   - Compare models’ trade-offs  
   - Examine long-tail coverage vs. accuracy  
   - Translate findings to personalization strategy  

---

## Key Findings
- **GRU** achieved the best overall balance between recall and interpretability.  
- **Debiasing** (α=0.1) improved coverage to **82%** with minimal accuracy loss.  
- **Long-tail exposure**: 77.6% of recommendations came from less-popular movies (vs. 22.4% popular).  
- Deep models consistently outperformed baselines in Recall@K and Hit Rate.  

---

## Business Value
- Move beyond **popularity bias**, ensuring broader personalization.  
- Improved **coverage** supports both heavy and light users.  
- Stronger **long-tail exposure** can enhance engagement and retention.  

---

## Conclusion & Next Steps
**Conclusion**  
Deep learning not only improves accuracy, but also expands long-tail coverage —  
striking a better balance between **accuracy, diversity, and fairness**.  

**Next Steps**  
- **Algorithms**: Explore Transformers, two-tower models, hybrid recommenders.  
- **Data**: Incorporate metadata (text, audio, genre embeddings) for multimodal learning.  
- **Deployment**: Build re-rank + interpretation loops to improve fairness and transparency.  

---

## Repository Contents
- `MovieLens_Notebook_DLFinalProject.ipynb` → Full analysis and modeling notebook  
- `MovieLens_Slides_DLFinalProject.pdf` → Presentation slides  
- `README.md` → Project overview and documentation
