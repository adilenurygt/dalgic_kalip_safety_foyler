# Laboratuvar 5 – AI Fail-Safe Decision

**Makine:** Dalgıç Kalıp için örnek progresif sac kalıplama presi. **Varsayım:** Kamera, yapay zekâ modeliyle parçayı uygun (OK) / kusurlu (RED) sınıflandırır. Bu yapay zekâ, presin emniyet kontrolörü değildir.

**Örnek akış:** Kamera → YZ modeli → OK/RED kararı → kontrollü ayırma mekanizması → operatör kontrolü.

## Görev – Üç başarısızlıkta güvenli davranış

**1. Model yanlış sınıflandırdı: Kusurlu parçaya OK verdi. Sistem ne yapmalı? İkinci kontrol / insan onayı var mı?**
Şüpheli parça otomatik olarak üretime kabul edilmemeli; ikinci ölçüm veya operatör kalite onayı istenmelidir. Hatalı kararın presin emniyet fonksiyonlarını etkilemesine izin verilmez.

**2. Girdi manipüle edildi: Kamera verisi bozuk/sahte. Nasıl fark edilir? Şüpheli girdide ne yapılır?**
Görüntü bütünlüğü, kamera bağlantısı, beklenen çözünürlük ve anormal örüntüler kontrol edilir. Şüpheli veriyle otomatik onay verilmez; parça incelemeye ayrılır, olay kaydedilir.

**3. Confidence düştü: Eşik ne olmalı? Altında dur / insana sor / fallback?**
Eğitim örneği olarak güven skoru eşiği **0,90** seçilir; gerçek eşik doğrulama testleriyle belirlenmelidir. Eşik altındaysa otomatik OK kararı verilmez, insan kontrolüne geçilir. Tehlikeli hareket riski varsa emniyet sistemi bağımsız olarak durdurur.

## Karar tablosu – AI Fail-Safe Decision

| Başarısızlık | Güvenli davranış (kavram) |
|---|---|
| Model yanlış sınıflandırdı | İkinci kontrol, insan onayı, yanlış kabulü önleme |
| Girdi manipüle edildi | Veri doğrulama, şüpheli parçayı ayırma, olay kaydı |
| Confidence düştü | Eşik altı otomatik onay yok; manuel kontrol/fallback |

**Emniyet gereksinimi:** YZ'nin hatası, ışık perdesi, koruyucu kapı veya acil durdurma işlevlerini devre dışı bırakamamalıdır.
