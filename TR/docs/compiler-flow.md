# Derleyici Akışı ve Yürütme Semantiği

## 1. Derleyici Olarak Orkestratör

NEXUS modelinde derleyici, yalnızca bir çevirmen değildir. Yürütme fabrikasının orkestrasyon motoruna dönüşür.

Onun rolü, kullanıcı niyetini aşağıdakileri tanımlayan yapılandırılmış bir yürütme grafına dönüştürmektir:

- görev sınırları
- bağımlılık sırası
- bellek ihtiyaçları
- doğrulama noktaları
- geri dönüş kurtarması
- paralel yürütme grupları

## 2. Akış Yönelimli Yürütme

Akış semantiği, geleneksel zorunlu yürütme modelinden daha çok görev tabanlı bir yürütme modeline yakındır. İşlemler şu şekilde yapılabilen akışlar olarak ele alınırlar:

- veriyi yakala
- bunu yürütme bölgeleri arasında taşı
- farklı işlem alanlarına yer değiştir
- geçici hata koşullarında yeniden dene
- geri dönüş yollarını taşı
- doğrulanmış çıktılar üret

## 3. Görev Grafı Modeli

Derleyici aşağıdaki gibi düğümler içeren bir grafik yayınlar:

- giriş edinimi
- bellek erişimi
- dönüşüm adımları
- vektör heslaması
- çıkarım veya model çıkarımı
- doğrulama
- çıktı emisyonu

Kenarlar düğümler arasında bağımlılık ve veri akışını temsil eder.

## 4. Yürütme Semantiği

Önemli semantikler şunları içerir:

- yakala / sahiplik bağlama
- görevler ve yürütme alanları arasında devir
- geçici hata sırasında yeniden dene veya yuvarlanan yürütme
- açık hata kurtarma yolu
- bölge tabanlı bellek yönetimi
- koşullu yürütme ve geri dönüş durumları

Bu semantikler OMNI-CORE-v2-NEXUS-FLOW'ta açıklanan daha anlatımlı, akış yönelimli model ile kavramsal olarak hizalanmıştır.

## 5. Bu Neden Önemli

Derleyici tarafından yönetilen yürütme akışı olmadan, özelleştirilmiş donanım hızla parçalanmış ve doğru şekilde planlanması zor hale gelir. Derleyici, özelleştirilmiş işlemi uyumlu ve belirleyici hale getiren katmandır.

## 6. Özet

NEXUS'taki derleyici bir sistem planlayıcısıdır. Heterojen donanım üzerinde yürütmeyi orkestre eder ve aynı zamanda doğruluk ve optimizasyon kısıtlamalarını uygular.
