# Lab 1 – Safety Architecture

## 1. Tehlikeli hareket
Pres koçunun aşağı stroku sırasında kalıp arasında ezilme; sac besleyicide sıkışma; keskin sacdan kesilme.

## 2. Safety function
Işık perdesi kesildiğinde, kapı kilidi açıldığında veya acil durdurmaya basıldığında presin tehlikeli hareketi güvenli şekilde durdurulmalı; yeniden başlatma manuel onay gerektirmelidir.

## 3. Safety-related control system
**Işık perdesi / E-stop / kapı kilidi → Safety PLC (veya emniyet rölesi) → güvenlik çıkışları → presin güvenli durdurma elemanları → safe state.**

## 4. PLC ve Safety PLC farkı
PLC üretim sırasını yönetir; Safety PLC emniyet sinyallerini hata algılama ve gerekli güvenilirlik koşullarıyla işler.

## 5. PL / SIL
PL veya SIL, risk değerlendirmesiyle belirlenen gerekli emniyet performansını ifade eder. Gerçek seviye saha verileri ve standartlara göre hesaplanmalıdır; bu föyde atanmaz.

## 6. Safe state
Presin tehlikeli strokunun durması ve kontrolsüz yeniden başlamanın önlenmesi. Yalnızca motor gücünün kesilmesi her pres tipinde yeterli olmayabilir; fren ve depolanmış enerji de değerlendirilmelidir.

## 7. Dijital bağımlılıklar
PLC/HMI yazılımı, safety mantığı, sürücü arayüzü, bakım bağlantıları ve konfigürasyon yönetimi.

## 8. Siber-fiziksel kesişim
Yetkisiz bakım oturumu kontrol parametrelerini değiştirirse beklenmedik strok riski doğabilir. Safety fonksiyonu uzaktan müdahaleyle devre dışı bırakılamamalıdır.
