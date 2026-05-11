# Makine-Ogrenmesi-Algoritmalari-ile-Ortopedik-Veri-Siniflandirmasi

ortopedik hastaların biyomekanik özelliklerine dayalı sınıflandırma modellerimin performansını ve ardından uyguladığım K-Ortalama (K-Means) kümeleme analizinin sonuçlarını sunuyorum.

1. Sınıflandırma Modelleri Performansı
Veri setimi eğitim ve test kümelerine ayırdıktan sonra (test oranı %15), farklı sınıflandırma algoritmalarını uyguladım ve test doğruluklarını aşağıdaki gibi elde ettim:

- Lojistik Regresyon: Test doğruluğu %78.72 olarak gerçekleşti. Eğitim doğruluğu ise %74.90 idi.

- K-En Yakın Komşular (KNN): k=12 değeri için %78.72 test doğruluğu elde ettim. En uygun k değerini bulmak amacıyla 1'den 50'ye kadar farklı k değerleri için yaptığım denemelerde, doğruluğun k değerine göre nasıl değiştiğini gözlemledim.

- Destek Vektör Makinesi (SVM): Bu model, %85.11 ile oldukça yüksek bir test doğruluğu sergiledi.

- Karar Ağacı: Karar Ağacı modelimin test doğruluğu %78.72 oldu.

- Rastgele Orman (Random Forest): Tıpkı SVM gibi, Rastgele Orman modeli de %85.11 ile en yüksek test doğruluğuna ulaşan modellerden biri oldu.

Sonuç: Yaptığım analizler sonucunda, Destek Vektör Makinesi (SVM) ve Rastgele Orman algoritmalarının bu veri setinde en iyi performansı gösterdiğini ve her ikisinin de %85.11'lik bir test doğruluğu elde ettiğini görüyorum. Lojistik Regresyon, KNN ve Karar Ağacı modelleri ise benzer bir performansla yaklaşık %78.72'lik doğruluk seviyesinde kaldılar.

2. K-Ortalama (K-Means) Kümeleme Analizi
Sınıflandırma modellerine ek olarak, veri setindeki doğal grupları keşfetmek amacıyla K-Ortalama kümeleme algoritmasını kullandım. Öncelikle 'Elbow Metodu'nu kullanarak optimum küme sayısını belirlemeye çalıştım. K-Means Inertia değerinin 'küme sayısı (K)' ile değişimini gösteren grafiğe göre, optimal K değeri için bir dönüş noktasını gözlemledim.

Ardından, n_clusters = 2 olarak belirlenen bir K-Ortalama modeli uyguladım. Sonuçları görselleştirdiğimde, veri setinin iki ana kümeye ayrıldığını gördüm (kırmızı ve yeşil noktalar). Merkezlerin (sarı noktalar) konumları da küme yapısını destekler nitelikteydi. Başlangıçta 3 ayrı veri kümesi oluşturmuş olsam da, K-Means algoritmasının 2 küme ile bu yapıyı yakaladığını fark ettim.
