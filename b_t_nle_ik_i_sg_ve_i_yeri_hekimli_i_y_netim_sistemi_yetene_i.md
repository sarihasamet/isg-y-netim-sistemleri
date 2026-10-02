# Bütünleşik İSG ve İşyeri Hekimliği Yönetim Sistemi Yeteneği

## Description
Bu yetenek; hem çoklu hem de tekli sektörlerde hizmet veren İş Sağlığı ve Güvenliği (İSG) Uzmanları ve İşyeri Hekimlerinin ortak kullanımı için tasarlanmıştır. Ulusal mevzuat (6331 Sayılı Kanun ve yönetmelikler) ile uluslararası standartları (ISO 45001, OSHA, ILO) temel alarak; firma bilgilerinden, personellerin eğitimi, mesleki yeterlilik belgelerinin takibi, risk analizinden, İş sağlığı ve güvenliği kurullarına, çalışan temsilcisi seçim ve atamaları, eğitim tutanaklarının ve sertifikalarının oluşturulması ve takibi, makine ve ekipmanların periyodik kontrollerinin takibi, düzeltici önleyici faaliyet (DÖF) formlarının oluşturulması ve takibi, kişisel koruyucu donanımların takibi ve iş izinlerine kadar tüm İSG süreçlerini yapılandırılmış, denetlenebilir, sektöre ve firmaya özgü formatta yönetir.

## Workflow
Kullanıcı herhangi bir İSG modülüyle ilgili işlem yaptığında veya veri sorguladığında aşağıdaki adımları ve kuralları işlet:

1. **Firma & Sektör Profilleme:** İşlemin yapılacağı firmanın temel bilgilerini (Çalışan Sayısı, NACE Kodu, Tehlike Sınıfı, Adres, Telefon Numarası, İş Güvenliği Uzman Bilgisi, İşyeri Hekimi Bilgisi, İşveren Bilgisi) doğrula veya yapılandır. NACE koduna göre sektörel yasal yükümlülükleri (Kurul zorunluluğu, uzman/hekim çalışma süreleri) dinamik olarak belirle. Çalışan sayısına göre sektörel yasal yükümlülükleri (Kurul oluşumu ve üyelerin belirlenmesi, acil durum ekiplerinin sayısı, Çalışan temsilcisi sayısı, ilk yardımcı sayısı) dinamik olarak belirle ve yapılandır.
2. **Sağlık ve Personel Takibi (Ortak Çalışma):** 
   - İSG Uzmanı için: İşe giriş/periyodik muayene takvimleri, KKD zimmet durumları, eğitim eksikliklerini ve mesleki yeterlilik belgelerini analiz et. İş kazası bildirim formlarını mevzuata göre hazırla.
   - İşyeri Hekimi için: Personel sağlık gözetimleri, kronik hastalık takipleri, iş kazası/meslek hastalığı bildirim formlarını mevzuata uygun formatta hazırla.
3. **Eğitim ve Tatbikat Planlama:** Sektörün tehlike sınıfına göre yasal eğitim sürelerini (Az Tehlikeli: 8 saat (3 yılda 1), Tehlikeli: 12 saat (2 yılda 1), Çok Tehlikeli: 16 saat (1 yılda 1)) kontrol et. Yıllık tatbikat (Yangın, deprem, tahliye vb.) senaryoları ve katılım tutanakları şablonları üret.
4. **Risk Analizi & 5x5 Matris:** Sektörel faaliyetlere göre tehlikeleri tanımla. 5x5 L Tipi Karar Matrisi metodolojisini kullanarak (Risk Skoru = İhtimal x Şiddet) riskleri puanla (1-25 arası). Kabul edilebilir seviyenin üzerindeki riskler için Kontrol Hiyerarşisine (Eliminasyon -> İkame -> Mühendislik Kontrolleri -> İdari Kontroller -> KKD) uygun olarak Düzeltici Önleyici Faaliyet (DÖF) planı oluştur. Her DÖF için sorumlu kişi ve termin süresi belirle.
5. **Dönemsel Dokümantasyon (Yıllık Plan & Rapor):** 
   - Yıllık Çalışma Planı: Yıl içinde yapılacak eğitim, ölçüm, periyodik kontrol, risk analizleri, acil durum eylem planları tatbikatlar, saha gözetimleri ve toplantıları takvimlendir.
   - Yıllık Değerlendirme Raporu: Yıl ve ay sonu kaza sıklık oranları, eğitimler, risk analizleri, sağlık gözetim raporları, ortam ölçümleri, makine ve teçhizatların periyodik kontrolleri ve DÖF kapanma oranlarını içeren resmi şablonu doldur.
6. **Kurul ve Temsilci Yönetimi:** Çalışan sayısı baremlerine göre zorunlu Çalışan Temsilcisi sayısını hesapla. Seçim/atama tutanakları ile İSG Kurul toplantı gündemlerini, kurul ekiplerini, kurul kararlarını oluştur.
7. **Mevzuat Çapraz Kontrolü:** Çıktılarda ulusal mevzuatın yanı sıra uluslararası iyi uygulama standartlarına (OSHA kılavuzları, ISO 45001 maddeleri) atıfta bulun.

## Tools & Capabilities
- **Matematiksel Hesaplama (Kod Çalıştırma):** Risk skoru (Olasılık x Şiddet), çalışan sayısına göre temsilci sayısı tespiti ve kaza istatistikleri (İş Kazası Sıklık Hızı vb.) hesaplamalarında kod aracını kullanarak sıfır hata ile çalış.
- **Modüler Çıktı Üretimi:** Kullanıcının talep ettiği modüle göre (Örn: Risk Değerlendirmesi, Acil Durum Eylem Planı şablonu, Personel Eğitim Kayıt Takip Tablosu, İş Güvenliği kurulları formları ve iş kazası olay ve araştırma tutanakları) özelleştirilmiş Markdown tabloları ve doküman yapıları sun.

## Quality Standards
- Sistem çoklu sektör yapısına uygun olmalı; farklı çalışma alanlarının (örneğin bir ofis ile bir üretim fabrikasının) tehlike sınıflarını (Az Tehlikeli/Tehlikeli/Çok Tehlikeli) net bir şekilde ayırt ederek firmaya özgü çıktı üretmelidir.
- **Kritik Kural:** Üretilen tüm tablolar, formlar, tutanaklar ve veri kayıt yapıları Türkiye'deki resmi **İSG-KATİP Excel formatı** ve denetim standartları ile %100 uyumlu olmalıdır.
- İşyeri hekimliği süreçlerinde KVKK ve hasta mahremiyeti ilkelerine uygun terminoloji kullanılmalıdır.

## Examples

### Example 1: Yeni Firma Kaydı ve Yasal Zorunluluk Tespiti
**User Input:** "Firma Adı: X Lojistik, Çalışan Sayısı: 65, NACE Kodu: 49.41.01 (Karayolu ile şehirlerarası yük taşımacılığı), Adres: İskenderun/Hatay. Bu firma için yasal İSG gereksinimlerini çıkar."
**Agent Output:**
### X Lojistik - İSG Yasal Uyumluluk ve Gereksinim Raporu

#### 1. Firma Kimlik Bilgileri
*   **İşveren/Şirket:** X Lojistik (İskenderun / Hatay)
*   **Çalışan Sayısı:** 65 Personel
*   **NACE Kodu & Tehlike Sınıfı:** 49.41.01 - **Tehlikeli Sınıf**
*   **Adres:** İskenderun / Hatay
*   **İş Güvenliği Uzmanı (Belge No):** [Uzman Adı ve Belge No Girilecek]
*   **İşyeri Hekimi (Belge No):** [Hekim Adı ve Belge No Girilecek]

#### 2. Zorunlu Kurullar ve Atamalar
*   **İSG Kurulu:** Çalışan sayısı 50'nin üzerinde ve iş 6 aydan uzun sürdüğü için **İSG Kurulu kurulması zorunludur**.
*   **Çalışan Temsilcisi:** 51-100 çalışan baremi uyarınca **en az 2 Çalışan Temsilcisi** seçimle belirlenmeli veya atanmalıdır.
*   **Destek Elemanı:** Arama, kurtarma ve tahliye için 3, yangınla mücadele için 3, ilkyardım için en az 7 (10 kişiye 1 ilkyardımcı) olmak üzere toplam **13 Destek Elemanı** görevlendirilmelidir.

#### 3. Sağlık ve Eğitim Süreçleri (İşyeri Hekimi & Uzman Ortak Takip)
*   **Temel İSG Eğitimi:** Tehlikeli sınıfta bulunan her çalışan için 2 yılda bir en az **12 saat** eğitim zorunludur. (Sektörel bazda sürücüler için yük bağlama, defansif sürüş vb. eklenecektir).
*   **Sağlık Gözetimi:** Periyodik muayeneler Tehlikeli sınıfta **en az 3 yılda bir** tekrarlanmalıdır. (Ağır vasıta sürücüleri için ek tetkikler ve psikoteknik testler zorunludur).
*   **Yıllık Planlar:** Yıllık Çalışma Planı, Yıllık Eğitim Planı ve Yıllık Değerlendirme Raporu hazırlanarak işverene onaylatılmalıdır.