# Mimari Genel Bakış

## 1. Problem Açıklaması

Modern iş yükleri, klasik CPU merkezli modelin sınırlarını giderek daha fazla zorluyorlar. Yapay zeka sistemleri, veri ağır işlem hatları ve özelleştirilmiş işlem görevleri şunları talep ederler:

- daha iyi paralellik
- daha düşük gecikme
- daha verimli bellek davranışı
- merkezi darboğazlar olmadan yüksek verim
- uyarlanabilir sistem seviyesi optimizasyon

NEXUS mimarisi, tüm sistemi tek bir CPU merkezli makine yerine koordine edilmiş bir yürütme fabrikası olarak yeniden tasarlayarak bu sorunları ele alır.

## 2. Temel Prensip

Ana tasarım fikri basittir:

> İş, tek bir CPU borususundan geçirilmek yerine, en uygun yürütme alanına gönderilmelidir.

Bu, özelleştirilmiş işlem, uyarlanabilir bellek kullanımı ve çalışma zamanı optimizasyonu için temeli oluşturur.

## 3. Sistem Katmanları

### A. Niyet Katmanı
Kullanıcı isteği veya program niyeti yapılandırılmış bir plana dönüştürülür. Buna şunlar dahil olabilir:

- görev grafları
- bağımlılık eşleştirmesi
- açık kaynak kısıtlamaları
- geri dönüş ve hata geçişleri

### B. Derleyici / IR Katmanı
Derleyici, bir orkestrasyon motoruna dönüşür. Kaynak kodu çevirmekle yalnızca ilgilenmek yerine, görev yürütme sırasını ve kaynak kullanımını tanımlayan bağımlılık bilincine sahip bir ara gösterim yayınlar.

### C. Çalışma Zamanı Planlayıcısı
Planlayıcı, görevleri doğru işlem birimine atar:

- CPU: kontrol akışı, orkestrasyon, skaler mantık
- GPU: vektörleştirilmiş ve paralel sayısal iş
- NPU: uyarlanabilir çıkarım ve optimizasyon görevleri
- FAPU: analog ve spektral hesaplama
- bellek fabrikası: verimli veri hazırlama ve alma

### D. Yönetilen Bellek Katmanı
Bellek, birinci sınıf bir sistem kaynağı olarak ele alınır.

Bu şekilde bölünür:

- uygulama belleği
- aktif veri belleği
- sayfa adreslendirilebilir veya sanallaştırılmış bellek
- hızlandırıcı tamponları
- sıcak/ılık/soğuk veri yönetimi katmanları

### E. Yapay Zeka Kontrolörü Katmanı
Yapay zeka kontrolörü, çalışma zamanı davranışını izler ve planlama davranışını zaman içinde ayarlar. Bunu optimize eder:

- birim atanması
- güç tahsisi
- termal denge
- bellek kullanımı
- gecikme azaltması

## 4. Bu Neden Gerçek Mimari Değişim

Geleneksel sistemler yürütmeyi CPU'nun yakınında merkezileştirir. NEXUS yaklaşımı, yürütmeyi heterojen bir fabrika üzerine dağıtırken, derleyici ve planlayıcı semantiği aracılığıyla kontrol ve doğruluğu korur.

Bu değişim, koordinasyondan ödün vermeden paralel uzmanlık sağlar.

## 5. Özet

NEXUS sistemi, bilgisayarı tek bir CPU merkezli cihaz yerine dağıtılmış bir yürütme fabrikası olarak kavramsallaştırır. En büyük gücü sadece hızlandırma değildir; yapılandırılmış planlama, bellek yönetimi, uzmanlık ve kendi kendini optimizasyonun birleşimidir.
