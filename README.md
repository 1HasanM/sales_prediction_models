Veri Seti Özeti:
Veri seti, 8523 satır ve 12 sütundan oluşmaktadır. Temel verilerin genel özellikleri aşağıda özetlenmiştir:

Eksik Veriler: Veri setinde eksik veri bulunmamaktadır. Tüm sütunlar eksiksiz doldurulmuş, bu da veri ön işleme sürecinin düzgün bir şekilde tamamlandığını gösterir.
Temel İstatistiksel Özellikler:
Item_Weight: Ortalama 11.69 kg, minimum değer 0 kg, maksimum değer ise 100 kg.
Item_Visibility: Ortalama 0.066, oldukça düşük bir değere sahip, bu da verinin büyük kısmının düşük görünürlük değerlerine sahip olduğunu gösteriyor.
Item_MRP: Ortalama 140.99, fiyatlar arasında geniş bir dağılım var.
Item_Outlet_Sales: Ortalama satış değeri 2181.29, geniş bir dağılım sergileyerek mağaza satışları konusunda çeşitlilik olduğunu gösteriyor.
Kar: Ortalama 13.41, yüksek bir kar marjına sahip ürünler mevcut.
Model Performansı:
Modelin farklı algoritmalarla eğitilen versiyonlarının performansı aşağıdaki gibi özetlenmiştir:

1. Gradient Boosting:
MSE: 1.067890e+06
RMSE: 1033.39
R²: 0.6071
Yorum: Gradient Boosting, en düşük RMSE ve en yüksek R² değeri ile en iyi performansı gösteren modeldir. Bu, modelin veriyi anlamada ve tahminlerde iyi bir doğruluk sağladığını gösterir.
2. Random Forest:
MSE: 1.152738e+06
RMSE: 1073.66
R²: 0.5759
Yorum: Random Forest, Gradient Boosting'e kıyasla biraz daha yüksek hata (RMSE) ve daha düşük doğruluk (R²) sergiliyor, ancak yine de güçlü bir modeldir ve genellikle yüksek doğruluk sağlar.
3. XGBoost:
MSE: 1.257383e+06
RMSE: 1121.33
R²: 0.5374
Yorum: XGBoost, diğer ağaç tabanlı modellere kıyasla daha düşük performans sergilemiştir. Ancak, yine de güçlü bir modeldir ve hiperparametre optimizasyonlarıyla daha iyi sonuçlar elde edilebilir.
4. Linear Regression:
MSE: 1.277034e+06
RMSE: 1130.06
R²: 0.5302
Yorum: Lineer Regresyon, genellikle daha basit ve hızlı sonuçlar sunan bir model olmasına rağmen, bu durumda diğer modellerin gerisinde kalmıştır. Lineer olmayan ilişkiler nedeniyle performansı sınırlıdır.
5. Decision Tree:
MSE: 2.247645e+06
RMSE: 1499.21
R²: 0.1730
Yorum: Decision Tree modeli, yüksek hata (RMSE) ve düşük doğruluk (R²) ile en zayıf performansı sergileyen modeldir. Ağaç tabanlı modelde aşırı uyum (overfitting) riski yüksek olabilir.
Özellik Önemliliği:
Modelde kullanılan ağaç tabanlı algoritmalar için, özelliklerin önem sırası belirlenmiş ve aşağıdaki gibi sıralanmıştır:

Önemli Özellikler:
Item_MRP (Ürün Fiyatı): Modelin tahminlerinde önemli rol oynayan ilk özelliktir.
Outlet_Type (Mağaza Türü): Farklı mağaza türlerinin satışlara etkisi belirleyici olmuştur.
Outlet_Establishment_Year (Mağaza Kuruluş Yılı): Mağaza kuruluş tarihi de modelin sonuçlarını etkileyen bir faktör olarak önemli bulunmuştur.
Hiperparametre Optimizasyonu:
Gradient Boosting Modeli İçin Optimizasyon Sonuçları:
Best Parameters: learning_rate: 0.05, max_depth: 3, n_estimators: 100
Optimizasyon Sonuçları:
MSE: 1.0574636863231026
RMSE: 1028.33
R²: 0.6109
Yorum: Hiperparametre optimizasyonu sonucunda Gradient Boosting modelinin performansı iyileşmiş ve hem MSE hem de RMSE değeri azalmıştır. Ayrıca, R² değeri 0.61 seviyesine yükselmiş, bu da modelin veri setini daha iyi açıklamakta olduğunu göstermektedir.
Görselleştirme:
Gerçek ve tahmin edilen değerlerin görselleştirilmesi, modelin performansını görsel olarak değerlendirmeye olanak sağlamaktadır. Ayrıca, farklı modellerin tahminlerini karşılaştıran grafik, her modelin doğruluğunun görsel bir temsilini sunar.
Sonuç ve Öneriler:
En Başarılı Model: Gradient Boosting, optimize edilmiş hiperparametrelerle birlikte en iyi sonucu elde etmiştir. Bu model, satış tahminlerinin doğruluğunu artırmak için tercih edilmelidir.
Düşük Performans Gösteren Model: Decision Tree, aşırı uyum (overfitting) nedeniyle en düşük performansı sergileyen modeldir. Diğer modellere göre çok daha fazla hata yapmaktadır.
Özellik Seçimi: Item_MRP (Ürün Fiyatı), Outlet_Type ve Outlet_Establishment_Year gibi özellikler, modelin doğruluğu üzerinde önemli bir etkiye sahiptir.
