# E-Ticaret Müşterilerinin Harcama Davranışlarının Tahmini

Bu projede, bir e-ticaret firmasına ait müşteri verileri kullanılarak müşterilerin yıllık harcama tutarlarını etkileyen faktörler analiz edilmiş ve çoklu doğrusal regresyon modeli ile tahmin edilmiştir.

## Projenin Amacı

- E-ticaret müşterilerinin davranışsal verileri kullanılarak yıllık harcama tutarlarının tahmin edilmesi.
- Mobil uygulama kullanımı, web sitesi kullanımı, oturum süresi ve üyelik süresi gibi faktörlerin etkilerinin analiz edilmesi.

## Kullanılan Veri Seti

- Kaynak: [Kaggle Dataset](https://www.kaggle.com/datasets/iyadavvaibhav/ecommerce-customer-device-usage/data)
- Müşteri sayısı: 500
- Kullanılan bağımsız değişkenler:
  - `Avg. Session Length` (Ortalama oturum süresi)
  - `Time on App` (Mobil uygulamada geçirilen süre)
  - `Time on Website` (Web sitesinde geçirilen süre)
  - `Length of Membership` (Üyelik süresi)
- Bağımlı değişken: `Yearly Amount Spent`

## Kullanılan Yöntem

- **Model:** Çoklu Doğrusal Regresyon (Multiple Linear Regression)
- **Veri bölme:** %70 eğitim / %30 test (train_test_split, random_state=42)
- **Araçlar:**
  - Python
  - pandas, matplotlib, seaborn, scikit-learn

## Sonuçlar

- **Model Katsayıları:**
  - Time on App: +38.60
  - Length of Membership: +61.67 (en güçlü etken)
  - Avg. Session Length: +25.72
  - Time on Website: +0.46 (önemsiz)

- **Performans Ölçütleri:**
  - R² (Determination Coefficient): **0.984**
  - MAE (Mean Absolute Error): **8.42**
  - RMSE (Root Mean Squared Error): **10.19**

- **Rezidü Dağılımı:** Normal dağılmış, sistematik hata yok.

## Yorumlar ve Öneriler

- Mobil uygulama ve üyelik süresi, harcama üzerinde en etkili faktörlerdir.
- Web sitesi etkileşimi düşük etkiye sahiptir; kullanıcı deneyimi gözden geçirilebilir.
- Gelecekte, yaş, gelir gibi demografik verilerle analiz zenginleştirilebilir.

## Proje Dosyaları

| Dosya Adı                     | Açıklama                                      |
|------------------------------|-----------------------------------------------|
| `Ecommerce_DonemOdevi.ipynb` | Jupyter Notebook, analiz ve modelleme süreci  |
| `grup9-proje.docx`           | Rapor dökümanı                                |

## Kaynaklar

- https://www.kaggle.com/datasets/iyadavvaibhav/ecommerce-customer-device-usage/data  
- https://pandas.pydata.org/docs/  
- https://matplotlib.org/  
- https://seaborn.pydata.org/  
- https://scikit-learn.org/  
