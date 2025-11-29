# 🌿 Sentiment Classification of Green Product Reviews in Turkish E-commerce

## 📜 Proje Özeti

Bu çalışma, Türkiye'nin önde gelen online pazaryerlerinden Trendyol'dan alınan, **çevreye duyarlı ("yeşil") ürünlerle** ilgili Türkçe e-ticaret yorumlarına uygulanan üç farklı duygu sınıflandırma yaklaşımının etkinliğini araştırmaktadır. Amacımız, **Logistic Regression (LR)** ve **Support Vector Classification (SVC)** gibi klasik makine öğrenimi yöntemlerini, **fine-tuned BERTurk** modelinin performansı ile karşılaştırarak, Türkçe gibi morfolojik açıdan zengin bir dildeki duygu analizindeki en iyi yaklaşımı belirlemektir.

## 📊 Veri Seti ve Kapsam

* **Kaynak:** Trendyol'dan alınan gerçek dünya kullanıcı yorumları.
* **Odak Alanı:** Veri, özellikle **sürdürülebilirlik odaklı temalara** atıfta bulunan kullanıcı yorumlarına yoğunlaşmak için filtrelenmiş ve ön işlenmiştir. Bu, çalışmanın yeşil ticaret bağlamında alan özgü derin öğrenmenin değerini göstermesini sağlamıştır.

## 💻 Değerlendirilen Modeller

Çalışmada, duygu sınıflandırma görevi için üç ana yaklaşım test edilmiştir:

1.  **Logistic Regression (LR):** Temel bir klasik makine öğrenimi modeli.
2.  **Support Vector Classification (SVC):** Güçlü bir klasik sınıflandırma algoritması.
3.  **Fine-tuned BERTurk:** Türkçe diline özel önceden eğitilmiş, en yeni nesil bir **transformer** modeli.

## ✨ Temel Sonuçlar ve Performans

Modeller, genel performansı ve sınıf dengesizliğine karşı hassasiyeti değerlendirmek için **doğruluk (accuracy)** ve **makro ortalama F1-skoru** gibi standart metrikler kullanılarak değerlendirilmiştir.

| Model | Doğruluk (Accuracy) | Makro F1-Skoru | Notlar |
| :--- | :---: | :---: | :--- |
| **LR** | Yüksek | Düşük | Nötr duygu ayrımında zorlanmıştır. |
| **SVC** | Yüksek | Düşük | Nötr duygu ayrımında zorlanmıştır. |
| **BERTurk** | **0.91** | **0.67** | Genel performansı en yüksek modeldir. |

### Öne Çıkan Bulgular

* **BERTurk Üstünlüğü:** BERTurk modeli, klasik yöntemlere göre **en yüksek genel performansı** göstermiştir. Özellikle pozitif ve negatif duyguları tespit etmede belirgin bir avantaj sağlamıştır.
* **Nötr Duygu Zorluğu:** LR ve SVC gibi klasik yöntemler makul bir doğruluk sunsa da, Türkçe duygu görevlerinde yaygın olarak karşılaşılan bir sorun olan **nötr duyguyu** etkili bir şekilde ayırt etmede zorlanmıştır. BERTurk modeli de bu zorluğu tam olarak aşamamıştır.
* **Dilin Etkisi:** Bulgular, transformatör tabanlı modellerin, Türkçe gibi **morfolojik açıdan zengin dillerden** duygu çıkarmada, özellikle duygusal nüans ve dilsel belirsizliğin yaygın olduğu alanlarda, **açık bir avantaj** sunduğunu göstermektedir.

## 🤝 Katkı ve İş Çıkarımları

Bu çalışma, hem duygu analizi literatürüne hem de Yönetim Bilişim Sistemleri (YBS) araştırmalarına önemli katkılarda bulunmaktadır:

* **Tüketici Analitiği:** Yeşil ticarette tüketici analitiği için alana özgü derin öğrenmenin değerini kanıtlamaktadır.
* **İş Pratikleri:** İşletmelerin sürdürülebilir ürünlere yönelik **kamu tutumlarını anlamalarına** ve bunlara yanıt vermelerine yardımcı olacak pratik çıkarımları vurgulamaktadır.

## 🚀 Gelecek Çalışmalar

* **Veri Seti Genişletme:** Türkçe duygu veri setlerini artırmaya odaklanmak.
* **Sınıf Dengesizliği:** Sınıf dengesizliğini gidermeye yönelik yeni yöntemler geliştirmek.
* **Model İyileştirme:** Eko-bilinçli tüketici ifadesinin inceliklerini daha iyi yakalamak için model mimarilerini geliştirmek.
