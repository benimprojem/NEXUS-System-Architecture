# NEXUS Sistem Mimarisi

NEXUS, yeni nesil bilgisayar sistemleri için birleşik bir mimari konseptidir. Derleyici tarafından yönetilen bir yürütme modeli, yapay zeka çalışma zamanı optimizasyonu, özelleştirilmiş donanım hızlandırması ve ayrılmış bir bellek hiyerarşisini birleştirir.

Bu depo, birkaç birbiriyle ilişkili fikri tek bir uyumlu mimariye sentezler:

- NEXUS-New-PC-Architecture: genel sistem ve yürütme tasarımı
- OMNI-CORE-v2-NEXUS-FLOW: derleyici, görev grafı, akış semantiği ve yürütme modeli
- Fourier-Analog-Processing-Unit-FAPU-: analog Fourier alanı hızlandırması
- MOSRAM: bellek yeniden tasarımı ve yüksek oranda özelleştirilmiş depolama katmanı

## Temel Tez

Mevcut bilgisayar sistemlerinin temel sınırlaması, sırf ham işlem gücü değildir; CPU merkezli orkestrasyon, parçalanmış bellek erişimi ve uyarlanabilir sistem seviyesi optimizasyon eksikliğinden kaynaklanan mimari darboğazıdır.

NEXUS, farklı bir model savunur:

- kullanıcı niyeti yapılandırılmış bir görev grafına derlenmiş
- iş en uygun yürütme birimine gönderilmiş
- bellek, pasif depolama değil yönetilen bir kaynak olarak ele alınmış
- yapay zeka sistem optimizatörü ve çalışma zamanı planlayıcısı olarak işlev görmüş
- analog ve programlanabilir hızlandırıcılar dijital heslamayı tamamlamış

## Mimari Katmanlar

### 1. Derleyici / Niyet Katmanı
Derleyici, kullanıcı niyetini bağımlılık bilincine sahip bir görev grafına çevirir. Bu grafik yürütme düğümleri, veri sahiplik sınırları, kaynak kısıtları ve hata yollarını içerir.

### 2. Planlayıcı / Çalışma Zamanı Katmanı
Çalışma zamanı planlayıcısı, her görevin nerede çalışması gerektiğine karar verir:

- CPU orkestrasyon ve skaler kontrol için
- GPU vektörleştirilmiş paralel işlemler için
- NPU öğrenilmiş optimizasyon ve çıkarım hızlandırması için
- FAPU analog Fourier alanı heslaması için
- Veri yoğun akışlar için özelleştirilmiş bellek yolları

### 3. Bellek Fabrik Katmanı
Bellek birden çok kategoriye ayrılmıştır:

- uygulama belleği
- veri belleği
- sayfa adreslendirilebilir veya sanallaştırılmış bellek
- özelleştirilmiş işlem birimleri için yüksek hızlı tamponlar

Bu, merkezi CPU bellek trafiğinin hakimiyetini azaltır.

### 4. Özelleştirilmiş İşlem Katmanı
NEXUS, tek bir evrensel işlem borusunun yerine birden çok yürütme alanı içerir. Özelleştirilmiş işlem, temel bir mimari konsepti haline gelir.

### 5. Yapay Zeka Kontrolörü Katmanı
Yapay zeka kontrolörü, bellek basıncı, termal durum, gecikme, kuyruk uzunluğu ve başarı/başarısızlık eğilimleri gibi çalışma zamanı davranışını gözlemler. Daha sonra planlama, iş yükü yerleştirme ve sistem seviyesi politikayı optimize eder.

## Bu Mimari Neden Önemli

Bu model, modern hesaplamada tekrar eden birkaç sorunu çözmek amaçlanmıştır:

- CPU darboğazları
- verimsiz bellek erişimi
- katı yürütme boruları
- işlem birimleri arasında zayıf iş yükü eşleştirmesi
- uyarlanabilir sistem optimizasyonu eksikliği

## Depo İçeriği

- `docs/architecture-overview.md`: yüksek seviye sistem modeli
- `docs/compiler-flow.md`: derleyici ve yürütme semantiği
- `docs/memory-hierarchy.md`: bellek ve depolama modeli
- `docs/analog-compute.md`: analog ve Fourier tabanlı işlem birimi
- `docs/ai-runtime-controller.md`: yapay zeka optimizasyonu ve çalışma zamanı kontrolü
- `docs/parallel-execution-model.md`: eşzamanlılık ve planlama modeli
- `docs/roadmap.md`: gelecek geliştirme yolu
- `paper/NEXUS-System-Architecture.md`: uzun form sentez makalesi

## Önerilen Okuma Sırası

1. `TR/docs/architecture-overview.md`
2. `TR/docs/compiler-flow.md`
3. `TR/docs/memory-hierarchy.md`
4. `TR/docs/analog-compute.md`
5. `TR/docs/ai-runtime-controller.md`
6. `TR/docs/parallel-execution-model.md`
7. `TR/paper/NEXUS-System-Architecture.md`

## Özet

NEXUS, bilgisayarı yeniden tasarlanan bir yürütme fabrikası olarak tasarlamaktadır: derleyici planlama, özelleştirilmiş işlem, yönetilen bellek ve yapay zeka tabanlı çalışma zamanı optimizasyonundan oluşan koordine bir ortam.
