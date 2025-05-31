# BLIP ile Görsel Açıklama Üretimi

Bu repo, OBSS Stajyer Yarışması 2025 (Kaggle) için yaptığım kodlamaları içerir:  
[https://www.kaggle.com/competitions/obss-intern-competition-2025/](https://www.kaggle.com/competitions/obss-intern-competition-2025/)  
Kaggle profilim: [https://www.kaggle.com/mehmetnurkavan](https://www.kaggle.com/mehmetnurkavan)

---

## Proje Amacı

Bu projenin amacı, BLIP modeli kullanarak görseller için kaliteli açıklamalar (caption) üretmek ve yarışmanın değerlendirme metriğine göre sonuçları iyileştirmektir. Prompt kullanmadan ve prompt ile olmak üzere iki farklı yöntem denedim. Prompt kullanımı skoru anlamlı şekilde iyileştirdi.

---

## Kullanılan Teknolojiler & Kütüphaneler

- Python  
- PyTorch  
- Hugging Face Transformers  
- BLIP (Bootstrapping Language-Image Pre-training)  
- Kaggle API  

---

## Klasör Yapısı

/training_example/
├── training_model.ipynb # BLIP modelini eğitimi için örnek kod
/score_0.17392/
├── blip-fine-tuning.ipynb # Prompt olmadan BLIP modelini eğittiğim kısım
├── run_caption_and_eval.ipynb # Eğitilen model ile test.csv’den caption üretip submission.csv oluşturan kod
├── submission.0.17392.csv # üretilen .csv dosyam

/score_0.15963/
├── blip-fine-tuning-with-prompt.ipynb # Prompt ile BLIP modelini eğittiğim kısım
├── sub.ipynb # Eğitilen model ile test.csv’den caption üretip submission.csv oluşturan
├── submission.0.15824.csv # üretilen .csv dosyam

---

## Sonuçlar

- Prompt kullanılmadan:  
  **Skor:** 0.17392  

- Prompt kullanılarak:  
  **Skor:** 0.15963 (daha iyi)  
  **Sıralama:** 69.

---
