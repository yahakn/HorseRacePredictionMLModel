# At Yarışı Sıralama Tahmini / Horse Race Ranking Prediction

## Proje Hakkında / About the Project

Bu proje, at yarışı verilerini kullanarak her yarışta atların sıralamasını tahmin etmeyi amaçlamaktadır.  
Veri setindeki antrenman (idman) süreleri, at-jokey ve pist uyumu gibi özellikler çıkarılarak LightGBM regresyon modeli ile sıralama tahmini yapılmıştır.

This project aims to predict the ranking of horses in each race using horse racing datasets.  
Features like training times, horse-jockey compatibility, and track suitability were engineered, and a LightGBM regression model was trained to predict horse rankings.

---

## Veri Hazırlığı / Data Preparation

- Atların yarış öncesi antrenman süreleri (örneğin 400m, 600m süreleri) saniyeye çevrildi.  
- Antrenmanlardan elde edilen ortalama değerler yarış bazında eklendi.  
- At-jokey, at-pist uyumu ve mesafe tercihi gibi yeni özellikler oluşturuldu.  
- Tarih bilgisi eksik olan satırlar temizlendi ve yarışlar tarih bazında sıralandı.  
- Veri seti yarış bazında %80 eğitim, %20 test olarak bölündü ve yarışlar karıştırıldı.

- Training times before races (e.g., 400m, 600m times) were converted to seconds.  
- Average values from recent trainings were added per race.  
- Features such as horse-jockey compatibility, horse-track compatibility, and distance preference were created.  
- Rows with missing date information were dropped and races sorted by date.  
- Dataset was split into 80% train and 20% test by race, shuffling races to prevent data leakage.

---

## Modelleme / Modeling

- LightGBM regresyon modeli kullanıldı.  
- Hedef değişken olarak atların gerçek sıralaması (At No) kullanıldı.  
- Derece_saniye (yarış derecesi) özelliği modelden çıkarıldı, çünkü modelin sıralamayı ezberlemesini engellemek amaçlandı.  
- Modelin performansı RMSE ile ölçüldü ve tahmin sonuçları yarış bazında değerlendirildi.

- A LightGBM regression model was used.  
- Target variable was the true horse ranking (At No).  
- The feature `Derece_saniye` (race time) was removed to prevent the model from memorizing rankings.  
- Model performance was evaluated with RMSE, and predictions were analyzed per race.

---

## Değerlendirme / Evaluation

- Model yarışlardaki at sıralamasını tahmin etti.  
- İlk iki atın sırasız doğru tahmin edilme oranı yaklaşık %66 olarak bulundu.  
- Özellik önemleri incelendiğinde derece_saniye hariç antrenman süreleri ve uyum skorları önemli bulundu.  

- The model predicted horse rankings within races.  
- The unordered accuracy for the top two horses was approximately 66%.  
- Feature importance showed training times and compatibility scores were influential, excluding race times.

---

## Kullanım / Usage

- Veri dosyasını `df` olarak yükleyin.  
- Veri hazırlık ve feature engineering kodlarını çalıştırın.  
- Modeli eğitmek için ilgili kod bloğunu çalıştırın.  
- Modeli kaydedebilir ve yeni verilerle tahmin yapabilirsiniz.

- Load the dataset as `df`.  
- Run data preparation and feature engineering scripts.  
- Train the model with the training script.  
- Save the model and make predictions on new data.

---

## Gereksinimler / Requirements

- Python 3.x  
- pandas  
- numpy  
- scikit-learn  
- lightgbm  
- joblib (model kaydetmek için)

---

## İletişim / Contact

Her türlü soru ve öneri için iletişime geçebilirsiniz.
# HorseRacePredictionMlModel
