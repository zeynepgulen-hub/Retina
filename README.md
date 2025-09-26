# Retina OCT Sınıflandırma

Bu projede kullanılan veri seti, **Kaggle Retinal OCT Dataset**’tir.  
Bu projenin temel amacı, **göz hastalıklarının erken teşhisine katkı sağlamak**  için retina OCT (Optical Coherence Tomography) görüntülerini  **CNN tabanlı derin öğrenme algoritmaları** ile sınıflandırmaktır. 

OCT görüntüleri, retina tabakalarının detaylı incelenmesine olanak sağlayan önemli bir tanı yöntemidir. Bu proje kapsamında kullanılan CNN tabanlı modeller sayesinde, farklı retina hastalıklarının otomatik olarak sınıflandırılması hedeflenmiştir. Böylece klinik süreçlerde doktorlara yardımcı olabilecek bir karar destek sistemi geliştirilmesi amaçlanmaktadır.

## Veri Seti
- Kaynak: [Retinal OCT C8 (Kaggle)](https://www.kaggle.com/datasets/obulisainaren/retinal-oct-c8)  
- Veri seti toplamda **8 farklı sınıf** içermektedir:  
  - **CNV (Choroidal Neovascularization)**  
  - **DME (Diabetic Macular Edema)**  
  - **DRUSEN (Yaşlanmaya bağlı retina değişimleri)**  
  - **NORMAL (Sağlıklı retina)**  
  - **AMD (Age-related Macular Degeneration)**  
  - **MH (Macular Hole)**  
  - **ODC (Optic Disc Cupping)**  
  - **OTHERS (Diğer retina bozuklukları)**  
- Görseller eğitim (`train/`), doğrulama (`val/`) ve test (`test/`) klasörlerine ayrılmıştır.  

## Kullanılan Yöntemler
### Derin Öğrenme Mimarisi
- **Convolutional Neural Network (CNN)**  
- Conv2D katmanları  
- MaxPooling katmanları  
- Flatten katmanı  
- Dense (Fully Connected) katmanlar  
- Dropout (overfitting’i önlemek için)  

### Aktivasyon Fonksiyonları
- **ReLU (Rectified Linear Unit)** – gizli katmanlarda  
- **Softmax** – çıktı katmanında  

### Optimizasyon ve Kayıp Fonksiyonu
- **Optimizer:** Adam  
- **Loss Function:** Categorical Crossentropy  

### Eğitim Parametreleri
- Epoch sayısı: 35 
- Batch size: 32  
- Learning rate: 0.001  
- Veri artırma (Data Augmentation): Resizing, Normalizasyon  

### Kullanılan Kütüphaneler ve Araçlar
- **Python**  
- **TensorFlow / Keras**  
- **NumPy**  
- **Pandas**  
- **Matplotlib & Seaborn**  
- **Scikit-learn**  
- **Kaggle GPU** ortamı  

## Elde Edilen Sonuçlar

- **Test Doğruluğu (Accuracy): 95.57%**

### Classification Report
| Sınıf   | Precision (%) | Recall (%) | F1-Score (%) | Destek (Support) |
|---------|---------------|------------|--------------|------------------|
| AMD     | 100.00        | 100.00     | 100.00       | 350 |
| CNV     | 91.64         | 94.00      | 92.81        | 350 |
| CSR     | 98.59         | 100.00     | 99.29        | 350 |
| DME     | 96.43         | 84.86      | 90.27        | 350 |
| DR      | 100.00        | 98.86      | 99.43        | 350 |
| DRUSEN  | 95.67         | 88.29      | 91.83        | 350 |
| MH      | 100.00        | 99.71      | 99.86        | 350 |
| NORMAL  | 84.39         | 98.86      | 91.05        | 350 |

**Genel Ortalama:**  
- Macro Avg: **95.84%**  
- Weighted Avg: **95.84%**  

Bu sonuçlar, modelin retina OCT görüntülerini sekiz farklı sınıfta yüksek başarıyla sınıflandırabildiğini göstermektedir.


Notebook dosyalarında:  
- Eğitim ve doğrulama doğruluk/kayıp grafikleri  
- Confusion matrix ve classification report  
- Örnek tahmin sonuçları  
detaylı olarak sunulmuştur.

 ### Linkler
 -https://www.kaggle.com/datasets/obulisainaren/retinal-oct-c8

 
 -https://www.kaggle.com/code/zeynepgulen/retina


