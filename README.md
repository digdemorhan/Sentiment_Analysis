# Sentiment_Analysis

# Projenin Ana Teması
Bu projede, bir sosyal medya veri seti üzerinde GRU ve LSTM modelleri ile ofansif yorumların sınıflandırılması gerçekleştirilmiştir. Veri ön işleme, metin temizleme, dönüştürme ve makine öğrenmesi modellerinin eğitimi gibi adımlar kapsamında detaylı bir analiz yapılmış ve modellerin performansları karşılaştırılmıştır.

# Kullanılan Kütüphaneler ve Framework'ler
Bu projede kullanılan kütüphaneler aşağıdaki gibidir:
<ul>
  <li><b>Pandas</b></li>
  <li><b>Numpy</b></li>
  <li><b>Matplotlib</b></li>
  <li><b>Tensorflow</b></li>
  <li><b>Keras</b></li>
  <li><b>NLTK</b></li>
</ul>

# Veriseti
Proje, sosyal medyada bulunan ofansif yorumları içeren bir veri seti üzerinde çalışılmıştır. Veri setinde "text" ve "label" olmak üzere iki temel sütun bulunmaktadır. Veri seti eğitim aşamasında %80 eğitim ve %20 test verisi olarak ayrıştırılmıştır.
Verisetinin linki: https://www.kaggle.com/datasets/toygarr/turkish-offensive-language-detection?resource=download&select=test.csv

# Preprocessing Adımları
<ul>
  <li><b>Lower Casing</b></li>
  <li><b>Removal of Emojis</b></li>
  <li><b>Removal of Punctunations</b></li>
  <li><b>Removal of Stopwords</b></li>
</ul>

# GRU Modeli
Proje kapsamında geliştirilen GRU modeli toplamda 5 katmandan oluşmaktadır.
<li><b>Embedding Layer</b></li>
<li><b>GRU Layer (64 nöron)</b></li>
<li><b>GRU Layer (32 nöron)</b></li>
<li><b>GRU Layer (16 nöron)</b></li>
<li><b>Dense Layer (1 nöron)</b></li>
Aktivasyon fonksiyonu "sigmoid" olarak tercih edilmiştir. Öğrenme oranı "1e-3" şeklinde belirlenmiştir. Model 10 epoch boyunca eğitilmiş olup doğruluk oranı %95.01 ve kayıp oranı 0.2400'dür. Model örnek veriler üzerinde de test edilmiştir.

# LSTM Modeli
Proje kapsamında geliştirilen LSTM modeli toplamda 5 katmandan oluşmaktadır.
<li><b>Embedding Layer</b></li>
<li><b>LSTM Layer (32 nöron)</b></li>
<li><b>LSTM Layer (16 nöron)</b></li>
<li><b>LSTM Layer (16 nöron)</b></li>
<li><b>Dense Layer (1 nöron)</b></li>
Aktivasyon fonksiyonu "sigmoid" olarak tercih edilmiştir. Öğrenme oranı "1e-3" şeklinde belirlenmiştir. Model 10 epoch boyunca eğitilmiş olup doğruluk oranı %95.01 ve kayıp oranı 0.2400'dür.

# Model Performanslarının Karşılaştırılması
Her iki model de doğruluk değerlerine, kayıp değerlerine ve örneklerin yanlış sınıflandırılmasına göre Matplotlib grafiği üzerinden karşılaştırılmmıştır.

# Değerlendirme ve Sonuç
Model değerlendirmeleri ve karşılaştırmaları sonucunda GRU ve LSTM modelleri mevcut veri seti için benzer doğruluk ve kayıp oranlarına sahiptir. Her iki modelde de doğruluk ve kayıp oranları sırasıyla %95.5 ve 0.24'tür. Yanlış sınıflandırma sayısı ele alındığında LSTM'de 87, GRU'da 47 sayısına ulaşılmıştır. Bu durum, GRU modelinin LSTM modeline göre daha düşük hata yapma oranına sahip olduğunu göstermektedir.

----
----

# Main Theme of the Project
In this project, the classification of offensive comments with GRU and LSTM models on a social media dataset was performed. A detailed analysis of the data preprocessing, text cleaning, transformation and training of machine learning models was performed and the performance of the models was compared.

# Libraries and Frameworks Used
The libraries used in this project are as follows:
<ul>
  <li><b>Pandas</b></li>
  <li><b>Numpy</b></li>
  <li><b>Matplotlib</b></li>
  <li><b>Tensorflow</b></li>
  <li><b>Keras</b></li>
  <li><b>NLTK</b></li>
</ul>

# Dataset
The project is based on a dataset containing offensive comments on social media. There are two main columns in the dataset: “text” and “label”. The dataset was split into 80% training and 20% test data during the training phase.
Link to the dataset: https://www.kaggle.com/datasets/toygarr/turkish-offensive-language-detection?resource=download&select=test.csv

# Preprocessing Steps
<ul>
  <li><b>Lower Casing</b></li>
  <li><b>Removal of Emojis</b></li>
  <li><b>Removal of Punctunations</b></li>
  <li><b>Removal of Stopwords</b></li>
</ul>

# GRU Model
The GRU model developed within the scope of the project consists of 5 layers in total.
<li><b>Embedding Layer</b></li>
<li><b>GRU Layer (64 units)</b></li>
<li><b>GRU Layer (32 units)</b></li>
<li><b>GRU Layer (16 units)</b></li>
<li><b>Dense Layer (1 units)</b></li>
The activation function is preferred as “sigmoid”. The learning rate was determined as “1e-3”. The model was trained for 10 epochs with an accuracy of 95.01% and a loss rate of 0.2400.

# LSTM Model
The LSTM model developed within the scope of the project consists of 5 layers in total.
<li><b>Embedding Layer</b></li>
<li><b>LSTM Layer (32 units)</b></li>
<li><b>LSTM Layer (16 units)</b></li>
<li><b>LSTM Layer (16 units)</b></li>
<li><b>Dense Layer (1 units)</b></li>
The activation function is preferred as “sigmoid”. The learning rate was determined as “1e-3”. The model was trained for 10 epochs with an accuracy of 95.01% and a loss rate of 0.2400.

#  Comparison of Model Performances
Both models are compared on Matplotlib graphs according to their accuracy, loss values and misclassification of samples.

# Evaluation and Result
As a result of model evaluations and comparisons, GRU and LSTM models have similar accuracy and loss rates for the current dataset. The accuracy and loss rates of both models are 95.5% and 0.24% respectively. Regarding the number of misclassifications, LSTM has 87 and GRU has 47. This shows that the GRU model has a lower misclassification rate than the LSTM model.
