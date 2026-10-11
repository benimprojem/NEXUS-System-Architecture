# Bellek Hiyerarşisi ve Yönetilen Depolama Tasarımı

## 1. Bellek Birinci Sınıf Katman Olarak

NEXUS mimarisi, belleği pasif bir depo yerine temel bir sistem bileşeni olarak ele alır.

Bu yaklaşım gereklidir çünkü modern yapay zeka ve yüksek performanslı iş yükleri, giderek daha çok bellek hareketi ve erişim kalıpları tarafından hakimdir.

## 2. Temel Gereksinimler

Bellek katmanı şunları desteklemelidir:

- sıcak veriler için düşük gecikme
- soğuk veriler için büyük kapasite
- verimli paralel erişim
- hızlandırıcılar için kontrollü hazırlama
- sayfa adreslendirilebilir veya sanallaştırılmış erişim modelleri
- uygulama durumu ile paylaşılan sistem verisi arasında ayrım

## 3. Bellek Bölümlendirmesi

Pratik bir NEXUS bellek modeli en azından aşağıdakileri ayırır:

### Uygulama Belleği
Doğrudan kullanıcı durumu, nesne grafikleri ve iş yükü yerel verileri için kullanılır.

### Veri Belleği
Ara veri setleri, matrisler, vektörler ve büyük akışları tutar.

### Sayfa Adreslendirilebilir Bellek
Sanallaştırılmış veya sayfalı tahsis sağlar, böylece bellek flat tampon yerine adreslendirilebilir yönetilen yürütme yüzeyi olarak yönetilebilir.

### Hızlandırıcı Tamponları
GPU, NPU, FAPU veya programlanabilir birimler için optimize edilmiş yerel erişim için bağlı özelleştirilmiş bellek bölgeleri.

## 4. Ayrıştırma Stratejisi

Önemli tasarım hedefi:

- merkezi bir CPU yolu üzerinden her bellek işlemini zorlamayın
- özelleştirilmiş işlem birimlerin yerel veya yüksek bant genişlikli bellek bölgeleriyle çalışmasına izin verin
- bellek çekişmesini ve durma davranışını azaltın

## 5. MOSRAM ile Bağlantı

MOSRAM yönü bu konseptle hizalanır; bu, belleği daha düşük güç ve daha ölçeklenebilir erişim kalıplarına sahip özelleştirilmiş bir fiziksel yapı olarak yeniden tasarlamayı amaçlar. Belleğin genel mimari sezgisini yansıtır; bellek genel aşağı adımlı bir blok yerine yeniden mühendislik yapılmalıdır.

## 6. Özet

NEXUS, belleğin planlama, iş yükü bölümlendirmesi ve özelleştirilmiş işlem verimliliğini destekleyen bir yürütme kaynağı olarak işlev gördüğü yönetilen bir bellek hiyerarşisini varsayar.
