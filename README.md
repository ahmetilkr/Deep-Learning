# Deep-Learning



### GİRİŞ



Bu proje, derin öğrenme (deep learning) teknikleri kullanarak kedi ve köpek görüntülerini ikili sınıflandırma (binary classification) amacıyla geliştirilmiştir. Kaggle platformundan alınan "dogs-vs-cats" veri seti kullanılmıştır. Veri seti, eğitim için toplam 25.000 görüntü (kedi ve köpek sınıfları eşit dağılımlı, her sınıf yaklaşık 12.500 görüntü) ve test için sınırlı sayıda görüntü içermektedir. Görüntüler 224x224 piksel boyutunda ve RGB renk kanallı olarak işlenmiştir.

Proje kapsamında şu adımlar izlenmiştir:



###### **Veri Seti Yükleme ve İnceleme:**



Eğitim ve test setlerinin boyutları hesaplanmış: Eğitim verisi şekli (25000, 224, 224, 3), test verisi şekli (1, 224, 224, 3)

Sınıf sayısı: 2 (kedi ve köpek).

Eğitim setinden rastgele seçilen 20 görüntü, Matplotlib kullanılarak görselleştirilmiş ve veri setinin içeriği (kedi/köpek dağılımı) gözlemlenmiştir.Bu adım veri setini görselleştirmek amacıyla yapılmıştır.



### METRİKLER



###### **Modellerin Geliştirilmesi ve Eğitimi:**



Temel CNN Modeli: Sıfırdan tasarlanmış bir Convolutional Neural Network (CNN) modeli kullanılmıştır. Model, konvolüsyon katmanları, pooling katmanları, dropout ve fully connected katmanlardan oluşmaktadır. Bu model, veri seti üzerinde eğitilmiş ve doğrulama  seti ile test edilmiştir.

Transfer Learning Modeli: Önceden eğitilmiş MobileNetV2 modeli temel alınarak transfer learning yaklaşımı uygulanmıştır. MobileNetV2'nin özellik çıkarım katmanları dondurulmuş ve üst katmanlara sınıflandırma katmanları eklenmiştir.





###### **Performans Karşılaştırması:**



Her iki modelin son epoch'taki doğrulama doğrulukları  karşılaştırılmıştır.



Temel CNN Modeli: Yaklaşık %65 doğrulama doğruluk oranı.

Transfer Learning Modeli : Yaklaşık %95 doğrulama doğruluk oranı.(Önceden ImageNet veri seti üzerinde eğitilmiş olması sayesinde daha iyi genelleme yaptığını düşünüyorum.)





Karşılaştırma, Matplotlib ile bar grafiği olarak görselleştirilmiştir. Grafikten görüldüğü üzere, transfer learning modeli temel CNN'e göre belirgin şekilde daha yüksek performans göstermiştir. Bunun nedeni, transfer learning'in önceden öğrenilmiş ağırlıkları kullanarak özellik çıkarımını hızlandırmasıdır. Temel CNN ise sıfırdan öğrenme gerektirdiği için daha fazla epoch ve veri ihtiyacı duymakta, bu da düşük performansla sonuçlanmaktadır.





###### **Kullanılan Kütüphaneler ve Araçlar:**



Veri İşleme ve Görselleştirme: os, random, matplotlib.pyplot (görselleştirme için), pandas (veri çerçeveleri için),

Derin Öğrenme: Proje,  TensorFlow veya Keras ile modellenmiştir.



### SONUÇ VE GELECEK ÇALIŞMALAR



Bu projeyi bootcamp sonrası daha kullanışlı ve etkileyici hale getirmek istiyorum. Şu basit adımları planlıyorum:



Kullanıcı Arayüzü: Streamlit ile bir web uygulaması yapacağım. Kullanıcılar kendi kedi/köpek fotoğraflarını yükleyip sınıflandırma sonucunu görebilecek.

Veri ve Model İyileştirmesi: Daha fazla hayvan türü (ör. kuş) ekleyerek sınıflandırmayı genişleteceğim. Ayrıca, veri artırma ile modelin doğruluğunu artıracağım.

Mobil Uygulama: Modeli mobil cihazlarda çalıştırılabilir hale getirip basit bir hayvan tanıma uygulaması yapacağım.

Paylaşım ve Güncelleme: Projeyi GitHub’da düzenli tutacağım ve yeni özellikler ekleyerek portföyümde öne çıkaracağım.



Öğrenmek İstediğim Teknolojiler: Web uygulamaları (Streamlit), mobil AI (TensorFlow Lite) ve daha iyi model eğitimi için pratik araçlar.

Kariyer Hedefi: Bilgisayarlı görü (computer vision) alanında AI/ML Engineer olmak.(Teknofest takımında görüntü işleme alanında çalışmam ile başladı.)

