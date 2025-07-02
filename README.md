# Horse Race Prediction Model

Bu proje, at yarışı sonuçlarını tahmin etmek için geliştirilmiş bir makine öğrenimi modelini ve ilgili kodları içerir. TJK (Türkiye Jokey Kulübü) verilerini kullanarak LSTM tabanlı tahminleme yapar.

## Özellikler

* At yarışı verilerinin analizi ve temizlenmesi
* Gelişmiş özellik mühendisliği
* LSTM tabanlı makine öğrenimi modeli
* Veri ön işleme ve görselleştirme
* Model performans değerlendirmesi

## Proje Yapısı

```
├── csv-to-df(1).ipynb          # CSV verilerini DataFrame'e dönüştürme
├── date(2).ipynb               # Tarih verilerinin işlenmesi
├── vis&numeric(3).ipynb        # Veri görselleştirme ve sayısal analiz
├── idman-prep(4).ipynb         # İdman verilerinin hazırlanması
├── modelling(5).ipynb          # Model eğitimi ve değerlendirme
├── anne_tablosu.csv            # Anne at verileri
├── antrenor_tablosu.csv        # Antrenör verileri
├── at_id_tablosu.csv           # At kimlik verileri
├── baba_tablosu.csv            # Baba at verileri
├── jokey_tablosu.csv           # Jokey verileri
├── sahip_tablosu.csv           # Sahip verileri
├── yarışlar_temiz.csv          # Temizlenmiş yarış verileri
├── lightgbm_model.pkl          # Eğitilmiş model dosyası
└── README.md                   # Bu dosya
```

## Kurulum

1. Bu repoyu klonlayın:
```bash
git clone https://github.com/yahakn/HorseRacePredictionModel.git
cd HorseRacePredictionModel
```

2. Gerekli Python paketlerini yükleyin:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow lightgbm jupyter
```

## Kullanım

1. Jupyter Notebook'ları sırasıyla çalıştırın:
   - `csv-to-df(1).ipynb`: Veri yükleme ve temel işlemler
   - `date(2).ipynb`: Tarih verilerinin düzenlenmesi
   - `vis&numeric(3).ipynb`: Veri analizi ve görselleştirme
   - `idman-prep(4).ipynb`: İdman verilerinin hazırlanması
   - `modelling(5).ipynb`: Model eğitimi ve tahminleme

2. Model eğitimi tamamlandıktan sonra `lightgbm_model.pkl` dosyası oluşacaktır.

## Veri Kaynakları

Proje aşağıdaki veri kaynaklarını kullanır:
- TJK (Türkiye Jokey Kulübü) yarış sonuçları
- At kimlik bilgileri (anne, baba, sahip)
- Antrenör ve jokey istatistikleri
- İdman performans verileri

## Model Özellikleri

- **Algoritma**: LightGBM (Gradient Boosting)
- **Özellikler**: At performans geçmişi, antrenör/jokey istatistikleri, idman verileri
- **Hedef**: Yarış sonuçlarının tahmin edilmesi
- **Performans**: Model doğruluğu ve metrikleri notebook'larda detaylandırılmıştır

## Gereksinimler

* Python 3.8+
* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
* tensorflow
* lightgbm
* jupyter

## Katkı

Katkıda bulunmak isterseniz:
1. Bu repoyu fork edin
2. Yeni bir branch oluşturun (`git checkout -b feature/yeni-ozellik`)
3. Değişikliklerinizi commit edin (`git commit -am 'Yeni özellik eklendi'`)
4. Branch'inizi push edin (`git push origin feature/yeni-ozellik`)
5. Pull Request oluşturun

## Lisans

Bu proje MIT lisansı ile lisanslanmıştır.

## İletişim

Sorularınız için GitHub Issues kullanabilirsiniz.

## Not

Bu proje geliştirme aşamasındadır ve sürekli iyileştirilmektedir. Model performansı ve doğruluğu garanti edilmez. 