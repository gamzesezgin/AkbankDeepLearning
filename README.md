# Cats vs Dogs - CNN Hiperparametre Optimizasyonu

## Projenin Amacı
Bu proje, **Cats vs Dogs** veri setini kullanarak bir **Convolutional Neural Network (CNN)** modeli eğitmeyi ve **Keras Tuner** ile hiperparametre optimizasyonu yapmayı amaçlamaktadır.  
Amaç, modelin doğruluk (accuracy) değerini maksimize ederken **overfitting** ve **underfitting** durumlarını da gözlemleyip değerlendirmektir.

## Veri Seti Hakkında
- **Kaynak:** Kaggle – Cats vs Dogs  
- **İçerik:** 25.000’den fazla kedi ve köpek resmi  
- **Boyut:** Tüm resimler 128x128 boyutuna küçültülerek CNN modeline beslenmiştir  
- **Label:** İki sınıf – `Cat` ve `Dog`  

## Kullanılan Yöntemler
- **CNN Modeli:**  
  - 1 veya 2 convolutional katman  
  - MaxPooling katmanları  
  - Flatten + Dense katmanları  
  - Dropout ve L2 regularization ile overfitting önlemleri  
- **Hiperparametre Optimizasyonu:**  
  - Keras Tuner (RandomSearch) kullanıldı  
  - Denenen parametreler: filtre sayısı, kernel boyutu, dense layer boyutu, dropout oranı, learning rate  
  - Maksimum deneme sayısı (`max_trials`) 5 olarak belirlendi  
- **Optimizer:** Adam  

## Elde Edilen Sonuçlar
- Validation accuracy değerleri her trial için gözlemlendi.  
- Hiperparametre kombinasyonları arasında en iyi performans gösteren model seçildi.  
- Overfitting ve underfitting durumları **epoch vs accuracy/loss grafikleri** ile incelendi.

## Kaggle Notebook
Projeyi detaylı olarak incelemek ve çalıştırmak için Kaggle Notebook linki:  
[Kaggle Notebook – Cats vs Dogs CNN Hiperparametre Optimizasyonu](https://www.kaggle.com/code/gamzesezgin/catanddogs)
