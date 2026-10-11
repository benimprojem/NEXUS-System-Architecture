# NEXUS Sistem Mimarisi

## Özet

Bu makale, CPU'nun artık yürütmenin tek merkezi olmadığı yeni nesil bilgisayarı için birleşik bir mimari sunar. Bunun yerine, sistem derleyici tarafından yönetilen bir görev grafı, özelleştirilmiş donanım birimleri, yönetilen bir bellek hiyerarşisi ve yapay zeka tabanlı çalışma zamanı kontrolörü ile oluşturulan bir yürütme fabrikası olarak modellenir.

Mimari, akış yönelimli derleyici tasarımı, analog spektral hızlandırması, bellek yeniden konfigürasyonu ve uyarlanabilir planlama fikirlerini tek bir kavramsal sistem içinde entegre eder. Makale, modern yapay zeka ve paralel iş yüklerin daha esnek, heterojen ve kalıp bilincine sahip bir yürütme modeli gerektirdiğini savunur.

## 1. Giriş

Modern bilgisayar sistemlerinin tasarımı, merkezileştirilmiş CPU yürütmesinin sınırları tarafından giderek daha çok kısıtlanmıştır. İş yükleri daha paralel, daha bellek sınırlı ve daha yapay zeka odaklı hale geldikçe, darboğazlar yalnızca aritmetik verim değil, aynı zamanda orkestrasyon, kaynak tahsisi ve bellek hareketi konularında da görülür.

NEXUS mimarisi farklı bir model önerir: niyet, yürütme, bellek ve optimizasyonun koordine katmanlara ayrıldığı bir sistem. Bu modelde, derleyici bir orkestrasyon motoruna dönüşür, donanım görev sınıfına göre özelleştirilir ve yapay zeka sadece bir uygulama katmanı değil, çalışma zamanı optimizatörü olarak işlev görür.

## 2. Sistem Mimarisi

Mimari beş büyük katmandan oluşur:

1. niyet ve derleyici katmanı
2. planlayıcı ve yürütme planlayıcısı
3. bellek hiyerarşisi ve veri hazırlama
4. özelleştirilmiş işlem fabrikası
5. yapay zeka çalışma zamanı optimizasyon katmanı

Bu katmanlı ayrılması gereklidir çünkü modern iş yükleri tek bir üniform yürütme yolu için çok heterojendir.

## 3. Derleyici Tarafından Yönetilen Yürütme

Derleyici, kullanıcı niyetini bir yürütme grafına dönüştürür. Bu grafik bağımlılıkları, sahipliği, geri dönüş davranışlarını ve olası paralel yürütme gruplarını ifade eder. Akış semantiği, yapılandırılmış bir dilde görev devri, doğrulama ve kurtarmanın açık olduğu bir yürütme modeline yakındır.

Bu, derleyiciyi basit bir çeviri aracından çok yönüne kadar bir çalışma zamanı planlayıcısı haline getirir.

## 4. Yönetilen Kaynak Olarak Bellek

NEXUS mimarisi, belleği pasif bir blok yerine yönetilen bir sistem katmanı olarak ele alır. Bunu uygulama durumu, veri depolama, sayfa adreslendirilebilir bölgeleri ve hızlandırıcı yerel tamponlara ayırır.

Bu, bellek çekişmesini azaltmak ve yürütme birimleri arasında daha iyi erişim kalıplarını etkinleştirmek için gereklidir.

## 5. Özelleştirilmiş İşlem Birimleri

Yürütme fabrikası çeşitli özelleştirilmiş alanlar içerir:

- hafif skaler işlemler ve genel kontrol için CPU
- paralel sayısal görevler için GPU
- öğrenme odaklı optimizasyon ve çıkarım hızlandırması için NPU
- analog Fourier alanı veya spektral hızlandırma için FAPU
- görev özel hızlandırma veya yeniden konfigürasyon için programlanabilir mantık

Ana nokta, her birimin diğerlerinin yerini alması değil, her birinin farklı bir verimlilik sınıfı ile katkı sağlamasıdır.

## 6. Analog ve Fourier Hızlandırması

Analog işlem katmanı, güçlü spektral yapısı veya fiziksel olarak anlamlı salınımlı davranışı olan iş yükleri için ilgilidir. FAPU konsepti, verinin faz ve genlik bilgisine nasıl kodlanabileceğini ve dalga girişimi ilkeleri kullanılarak nasıl işlenebileceğini gösterir.

Bu, dijital kontrolün ihtiyacını ortadan kaldırmaz, fakat analog veya frekans alanı yürütme için doğal olarak uygun olan iş y��kleri için özelleştirilmiş yüksek verimlilik yolu sağlar.

## 7. Yapay Zeka Çalışma Zamanı Kontrolü

Yapay zeka kontrolörü, çalışma zamanı davranışını izler ve sistem politikasını gerçek zamanda uyarlar. İş yükü yönlendirmesini, bellek yerleşimini, kuyruk önceliklerini ve güç tahsisini değiştirebilir.

Bu, sistemin zamanla kendisini daha etkili bir şekilde planlamayı öğrendiği uyarlanabilir bir döngü oluşturur.

## 8. Paralel Yürütme Modeli

NEXUS yürütme modeli temelde paralel ve heterojendir. İş, doğası ve sistemin durumuna göre yönlendirilir. CPU, GPU, NPU, analog işlem ve bellek alt sistemleri, verim, verimlilik ve doğruluğu vurgulayan bir planlayıcı altında birlikte çalışır.

## 9. Mimarinin Uyumu

Genel mimari aşağıdakiler birleştirildiğinde uyumlu hale gelir:

- derleyici tarafından yönlendirilmiş yürütme grafları
- özelleştirilmiş donanım gönderimi
- bellek ayrıştırması ve hazırlama
- yapay zeka odaklı çalışma zamanı optimizasyonu
- uygun görev sınıfları için analog işlem

Bu, basit bir CPU artı hızlandırıcı düzenlemesinden çok daha uyarlanabilir ve ölçeklenebilir bir sistem oluşturur.

## 10. Sonuç

NEXUS, yeni nesil bilgisayarım için birleşik bir görüş sunar; sistemin tek bir merkezi işlemci tarafından tanımlanmadığı, fakat bir yürütme fabrikası tarafından tanımlandığı görüş. Derleyici, bellek, çalışma zamanı planlayıcısı, analog işlem yolu ve yapay zeka optimizatör tümü, modern yapay zeka ve paralel iş yüklere daha uygun olan koordine bir mimaride yer alır.
