# İSG Risk Değerlendirme Prosedürleri (5x5 ve Fine-Kinney)

## Description
Bu yetenek, iş sağlığı ve güvenliği süreçlerinde tespit edilen tehlikelerin ve potansiyel risklerin matematiksel olarak skorlanması, sınıflandırılması ve bu skorlara göre uygun düzeltici/önleyici faaliyetlerin (DÖF) belirlenmesi için kullanılır. Kullanıcının talebine veya durumun niteliğine göre **5x5 L Tipi Karar Matrisi** veya **Fine-Kinney** metodolojilerini işletir.

## Workflow & Metodolojiler

Kullanıcı bir tehlike senaryosu verdiğinde veya bir risk analizi tablosu talep ettiğinde, belirtilen metoda göre aşağıdaki hesaplama tablolarını kullan:

### YÖNTEM 1: 5x5 L Tipi Karar Matrisi
**Formül:** Risk Skoru = İhtimal x Şiddet

**İhtimal (Olasılık) Skalası:**
* 1: Çok Küçük (Yılda bir defa)
* 2: Küçük (Üç ayda bir defa)
* 3: Orta (Ayda bir defa)
* 4: Yüksek (Haftada bir defa)
* 5: Çok Yüksek (Her gün)

**Şiddet (Etki) Skalası:**
* 1: Çok Hafif (İş saati kaybı yok, ilk yardım)
* 2: Hafif (İş günü kaybı yok, ayakta tedavi)
* 3: Orta (Hafif yaralanma, yatarak tedavi)
* 4: Ciddi (Ciddi yaralanma, meslek hastalığı)
* 5: Çok Ciddi (Ölüm, sürekli iş göremezlik)

**Risk Skorlaması ve Aksiyonlar:**
* **1 (Önemsiz):** Kayda gerek yok.
* **2 - 6 (Düşük - Katlanılabilir):** Mevcut kontrolleri sürdür.
* **8 - 12 (Orta):** En az 6 ay içinde iyileştirici tedbir planla.
* **15 - 20 (Ciddi):** Birkaç hafta içinde aksiyon al. Kontrollü çalışma yürüt.
* **25 (Kabul Edilemez):** İş derhal durdurulmalı, risk düşürülene kadar başlanmamalı.

---

### YÖNTEM 2: Fine-Kinney Metodolojisi
**Formül:** Risk Skoru (R) = Olasılık x Frekans x Şiddet

**Olasılık (Şans) Skalası:**
* 10: Beklenir, Kesin
* 6: Yüksek / Oldukça mümkün
* 3: Olası
* 1: Mümkün fakat düşük
* 0.5: Beklenmez fakat mümkün
* 0.2: Beklenmez

**Frekans (Maruz Kalma) Skalası:**
* 10: Hemen hemen sürekli (saatte birkaç defa)
* 6: Sıklıkla (günde bir/birkaç defa)
* 3: Ara Sıra (haftada bir/birkaç defa)
* 2: Sık Değil (ayda bir/birkaç defa)
* 1: Seyrek (yılda birkaç defa)
* 0.5: Çok Seyrek (yılda bir veya daha az)

**Şiddet (Tahmini Zarar) Skalası:**
* 100: Birden fazla ölümlü kaza / Çevresel felaket
* 40: Öldürücü kaza / Ciddi çevresel zarar
* 15: Kalıcı hasar (iş kaybı)
* 7: Önemli hasar (dış ilk yardım)
* 3: Küçük hasar (dahili ilk yardım)
* 1: Ucuz atlatma (hasar yok)

**Risk Skorlaması ve Aksiyonlar:**
* **R < 20 (Önemsiz):** Kontrole gerek yok.
* **20 <= R < 70 (Düşük):** Mevcut kontrolleri sürdür.
* **70 <= R < 200 (Önemli Risk):** En az 6 ay içinde aksiyon planla.
* **200 <= R < 400 (Ciddi Risk):** Birkaç hafta içinde aksiyon al.
* **R >= 400 (Kabul Edilemez Risk):** İşi hemen durdur.

---

## Genel Kurallar & Çıktı Formatı (Kontrol Hiyerarşisi)

1. Değerlendirme yaparken daima Kontrol Hiyerarşisini işlet: 
   *(Tehlikeyi Ortadan Kaldır -> İkame Et -> Mühendislik Kontrolleri -> İdari Kontroller -> KKD Kullanımı)*
2. İstenen analizi her zaman standart İSG-KATİP uyumlu Markdown tablosu olarak sun.
3. Tablo sütunları şu şekilde olmalıdır: 
   `| Faaliyet/Bölüm | Tehlike | Risk | [İhtimal/Olasılık] | [Frekans (Sadece Kinney)] | Şiddet | Risk Skoru | Risk Seviyesi | Alınacak Önlemler (DÖF) | Sorumlu |`
4. Kod yorumlayıcısını (Python) kullanarak çarpım işlemlerini gerçekleştir ve skorları teyit et. Sıfır hata ile risk skorunu belirle.