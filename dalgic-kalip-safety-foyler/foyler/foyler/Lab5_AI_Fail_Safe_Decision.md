# Laboratuvar 5 – AI Fail-Safe Decision

Makine: Dalgıç Kalıp – örnek progresif sac kalıplama presi.
Varsayım: Kamera ve yapay zekâ, sac parçalarını OK/RED olarak sınıflandırır.

## 1. Model yanlış sınıflandırdı
Kusurlu parça otomatik kabul edilmez. İkinci kontrol ve operatör onayı istenir.

## 2. Girdi manipüle edildi
Görüntü bütünlüğü ve kamera bağlantısı kontrol edilir. Şüpheli parça ayrılır, olay kaydedilir.

## 3. Confidence düştü
Örnek eşik %90'dır. Altında otomatik onay verilmez, insan kontrolüne geçilir. Gerçek eşik testlerle belirlenmelidir.

## Karar tablosu
| Başarısızlık | Güvenli davranış |
|---|---|
| Yanlış sınıflandırma | İkinci kontrol ve insan onayı |
| Manipüle edilmiş girdi | Veri doğrulama ve parçayı ayırma |
| Düşük confidence | Otomatik onayı durdurma ve manuel kontrol |

Emniyet gereksinimi: Yapay zekâ hataları ışık perdesi, koruyucu kapı veya acil durdurma fonksiyonlarını etkileyememelidir.

Not: Bu sistem eğitim amaçlı varsayımsal bir mimaridir.