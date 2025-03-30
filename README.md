# 🎯 Phân Tích Cảm Xúc Bình Luận Mạng Xã Hội

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.8%2B-blue.svg"/>
  <img src="https://img.shields.io/badge/PyTorch-2.0%2B-red.svg"/>
  <img src="https://img.shields.io/badge/Transformers-4.0%2B-yellow.svg"/>
  <img src="https://img.shields.io/badge/Streamlit-1.0%2B-orange.svg"/>
</div>

## 📝 Giới Thiệu

Dự án này sử dụng mô hình BERT và kỹ thuật Transfer Learning để phân tích cảm xúc từ bình luận tiếng Việt trên mạng xã hội. Hệ thống có khả năng phân loại bình luận thành ba loại: Tích cực (Positive), Tiêu cực (Negative), và Trung lập (Neutral).

## 🚀 Tính Năng

- Phân tích cảm xúc từ văn bản tiếng Việt
- Sử dụng PhoBERT - mô hình BERT được huấn luyện cho tiếng Việt
- Giao diện web thân thiện với người dùng
- Kết quả phân tích trực quan với biểu tượng cảm xúc

## 🛠️ Công Nghệ Sử Dụng

- Python 3.8+
- PyTorch
- Transformers (Hugging Face)
- Streamlit
- Scikit-learn
- Pandas
- NumPy

## 📦 Cài Đặt

1. Clone repository:
```bash
git clone https://github.com/hoangnguyenkhac/Sentiment-Analysis.git
cd Sentiment-Analysis
```
## 🔄 Luồng Xử Lý Dự Án

```mermaid
graph TD
    subgraph Training
    A[Comments.csv] --> C[Raw Data]
    B[Social Media Data] --> C
    C --> D[Preprocessing]
    D --> E[Labeled Corpus]
    E --> F[PhoBERT Training]
    F --> G[Trained Model]
    end

    subgraph Testing
    H[User Input] --> I[Preprocessing]
    I --> J[Model Prediction]
    J --> K[Softmax Classifier]
    K --> L[Positive]
    K --> M[Neutral]
    K --> N[Negative]
    G --> J
    end

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style B fill:#f9f,stroke:#333,stroke-width:2px
    style C fill:#bbf,stroke:#333,stroke-width:2px
    style D fill:#dfd,stroke:#333,stroke-width:2px
    style E fill:#dfd,stroke:#333,stroke-width:2px
    style F fill:#fdd,stroke:#333,stroke-width:2px
    style G fill:#fdd,stroke:#333,stroke-width:2px
    style H fill:#f9f,stroke:#333,stroke-width:2px
    style I fill:#dfd,stroke:#333,stroke-width:2px
    style J fill:#fdd,stroke:#333,stroke-width:2px
    style K fill:#fdd,stroke:#333,stroke-width:2px
    style L fill:#bfb,stroke:#333,stroke-width:2px
    style M fill:#fbf,stroke:#333,stroke-width:2px
    style N fill:#fbb,stroke:#333,stroke-width:2px
