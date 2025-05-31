# BLIP ile Görsel Açıklama Üretimi (Image Captioning with BLIP)

## Proje Amacı

Bu proje, [OBSS 2025 Datathon](https://www.kaggle.com/competitions/obss-intern-competition-2025/) kapsamında sağlanan bir görüntü açıklama (image captioning) verisi üzerinde gerçekleştirilmiştir. Amaç, test görselleri için anlamlı ve doğru açıklamalar (caption) üretmektir.

Bu doğrultuda BLIP (Bootstrapping Language-Image Pretraining) modeli kullanılmış ve iki farklı yaklaşım denenmiştir: prompt kullanmadan ve prompt destekli. Prompt kullanımı, modelin görselleri daha iyi anlamlandırmasını sağlayarak değerlendirme skorunu anlamlı bir şekilde iyileştirmiştir. Projede temel hedef, görseller için yüksek kaliteli açıklamalar üreterek yarışmanın değerlendirme metriğine göre performansı artırmaktır.

## Kullanılan Teknolojiler & Kütüphaneler

- Programlama Dili: Python
- Derin öğrenme: PyTorch
- Veri işleme: pandas, PIL, sklearn
- Model ve eğitim: Hugging Face Transformers "BLIP (Bootstrapping Language-Image Pre-training)"
- Diğer: os, random, tqdm (yardımcı kütüphaneler)
- Jupyter Notebook
- Kaggle

## Klasör Yapısı

/training_example/\
├── `training_model.ipynb` BLIP modelini eğitimi için örnek kod\
/score_0.17392/\
├── `blip-fine-tuning.ipynb` Prompt olmadan BLIP modelini eğittiğim kısım\
├── `run_caption_and_eval.ipynb` Eğitilen model ile test.csv’den caption üretip submission.csv oluşturan kod\
├── `submission.0.17392.csv` üretilen .csv dosyam

/score_0.15963/\
├── `blip-fine-tuning-with-prompt.ipynb` Prompt ile BLIP modelini eğittiğim kısım\
├── `sub.ipynb` Eğitilen model ile test.csv’den caption üretip submission.csv oluşturan\
├── `submission.0.15824.csv` üretilen .csv dosyam

---

## Dataset

###  Klasör Yapısı
- `train/` – 21,367 adet eğitim görseli (.jpg formatında).
- `test/` – 3,771 adet test görseli (.jpg formatında).
Tüm görseller RGB renk formatında ve standart JPEG formatındadır.

###  Dosyalar
- `train.csv` – Eğitim görsellerine ait açıklamaları içerir.
- `test.csv` – Test görsellerine ait yalnızca görsel ID’lerini içerir, açıklama yoktur.
- `sample_submission.csv` – Tahmin edilen dosyayi içerir.

#### `train.csv`
| Sütun Adı  | Açıklama |
|------------|----------|
| `image_id` | Görselin adı (örnek: `150.jpg`) |
| `caption`  | Görsel için insan tarafından yazılmış açıklama |

 ```
image_id,	caption
0, The image features a comic-style panel depicting a scene from a story, with dialogue and narration a...
1, Colorful postcard featuring "Greetings from Cherry Grove Beach, S.C." with images of beach scenes an...
2, Two vending machines display a variety of drinks, illuminated with colorful lights, in a train stati...
3, A man speaks at the eGovernment Conference 2013, with multiple logos displayed on computer monitors ...
4, A close-up of several silver coins stacked together, showcasing their shiny surfaces and engraved de...
5, A woman speaking at a podium, surrounded by seated officials, with a building and event branding in
 ```

#### `test.csv`
| Sütun Adı  | Açıklama |
|------------|----------|
| `image_id` | Test görselinin adı (örnek: `100375.jpg`) |

 ```
image_id,
100000,
100001,
100002,
100003,
100004,
100005,
 ```

#### `submission.csv:`
| Sütun Adı  | Açıklama |
|------------|----------|
| `image_id` | Test görseli adı (test.csv ile birebir aynı) |
| `caption`  | Modelin tahmin ettiği açıklama cümlesi |

 ```
image_id,	caption
100000,	the image features a large billboard for " abracabara," displaying athletic activities and slogans related to water activities.
100001,	a hand rests on a beach table, holding a watch, with a knife and wallet nearby, set against a snowy backdrop.
100002,	a rustic building features a storefront with signs, a bicycle parked nearby, and colorful posters on the walls.
100003,	a red asus laptop is displayed on a table, surrounded by other laptops at an exhibition.
 ```

### Hedef
Test kümesindeki her bir görsel için bir adet doğal dil açıklaması üretmek. Oluşturulan `submission.csv` dosyası, `sample_submission.csv` yapısına uygun olmalıdır.

> 📎 Not: Görsel isimleri `.jpg` uzantılıdır ve `train/` ile `test/` klasörleri altındaki görsellerle birebir eşleşir.



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

Kaggle profilim: [mehmetnurkavan](https://www.kaggle.com/mehmetnurkavan)

