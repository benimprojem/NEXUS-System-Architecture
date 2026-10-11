# Paralel Yürütme Modeli

## 1. Yürütme Felsefesi

NEXUS yürütme modelinin merkezi prensibi, sistemin tek bir seri kontrol yolu tarafından hakim olunmaması gerektiğidir. Bunun yerine, özelleştirilmiş yürütme alanlarında paralel olarak çalışan bileşenlerden oluşması gerekir.

## 2. Yürütme Birimleri

Sistem birden çok yürütme sınıfı içerir:

- CPU: orkestrasyon ve genel kontrol
- GPU: yoğun sayısal ve tensor iş
- NPU: uyarlanabilir çıkarım ve optimizasyon
- FAPU: analog ve spektral hesaplama
- bellek alt sistemi: hazırlama ve erişim yönetimi

## 3. Görev Planlama

Derleyici görevlerin bir grafını üretir ve planlayıcı bunları iş yükü karakteristiği, kaynak durumu ve beklenen fayda temelinde yürütme birimlerine eşler.

## 4. Paralellik Modeli

Görevler çeşitli modlarda çalıştırılabilir:

- paralel bağımsız görevler
- bağımlı görev zinciri
- veri paralel aşamalar
- doğrulama sınırları ile karışık yürütme

## 5. Faydalar

Bu model şunları sağlar:

- azaltılmış sistem darboğazları
- heterojen iş yükleri üzerinde daha hızlı verim
- özelleştirilmiş donanımın daha verimli kullanımı
- esnek planlama aracılığıyla iyileştirilmiş esneklik

## 6. Özet

NEXUS temelde paralel ve görev odaklıdır. Uzmanlıktan yararlanmaya, uyumlu orkestrasyon ve doğruluğu korumaya çalışır.
