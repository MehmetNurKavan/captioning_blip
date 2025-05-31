# BLIP ile Görsel Açıklama Üretimi

Bu repo, OBSS Stajyer Yarışması 2025 (Kaggle):  
[https://www.kaggle.com/competitions/obss-intern-competition-2025/](https://www.kaggle.com/competitions/obss-intern-competition-2025/)  
Kaggle profilim: [https://www.kaggle.com/mehmetnurkavan](https://www.kaggle.com/mehmetnurkavan)

---

## Proje Amacı

Bu projenin amacı, BLIP modeli kullanarak görseller için kaliteli açıklamalar (caption) üretmek ve yarışmanın değerlendirme metriğine göre sonuçları iyileştirmektir. Prompt kullanmadan ve prompt ile olmak üzere iki farklı yöntem denedim. Prompt kullanımı skoru anlamlı şekilde iyileştirdi.

---

## Kullanılan Teknolojiler & Kütüphaneler

- Programlama Dili: Python
- Derin öğrenme: PyTorch
- Veri işleme: pandas, PIL, sklearn
- Model ve eğitim: Hugging Face Transformers "BLIP (Bootstrapping Language-Image Pre-training)"
- Diğer: os, random, tqdm (yardımcı kütüphaneler)
- Jupyter Notebook
- Kaggle

---

## Klasör Yapısı

/training_example/\
├── training_model.ipynb # BLIP modelini eğitimi için örnek kod\
/score_0.17392/\
├── blip-fine-tuning.ipynb # Prompt olmadan BLIP modelini eğittiğim kısım\
├── run_caption_and_eval.ipynb # Eğitilen model ile test.csv’den caption üretip submission.csv oluşturan kod\
├── submission.0.17392.csv # üretilen .csv dosyam\

/score_0.15963/\
├── blip-fine-tuning-with-prompt.ipynb # Prompt ile BLIP modelini eğittiğim kısım\
├── sub.ipynb # Eğitilen model ile test.csv’den caption üretip submission.csv oluşturan\
├── submission.0.15824.csv # üretilen .csv dosyam\

---

## Sonuçlar

- Prompt kullanılmadan:  
 ![Kaggle Score](https://img.shields.io/badge/Score-0.17392-blue)

- Prompt kullanılarak:  
 ![Kaggle Score](https://img.shields.io/badge/Score-0.15963-blue)
 ![Kaggle Rank](https://img.shields.io/badge/Kaggle%20Rank-69-orange)

# rank

![rank](https://github.com/user-attachments/assets/8763f691-9f3d-47c4-9582-7fa0bdbf31c8)

# scores
![score](https://github.com/user-attachments/assets/e6617950-cbf4-47b9-bcd3-4dbfbc602676)

---
