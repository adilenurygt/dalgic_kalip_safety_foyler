# Laboratuvar 7 – Incident Workflow

**Makine:** Dalgıç Kalıp için örnek progresif sac kalıplama presi.

**Senaryo:** Saat 10:15. Presin bakım hesabına gece 03:00'te tanınmayan bir konumdan giriş tespit edildi. PLC konfigürasyonu değişmiş olabilir; ışık perdesi ve emniyet parametreleri henüz doğrulanmadı. Makine çalışıyor. Vardiya sorumlususunuz.

## Görev – Zaman çizelgesi

**1. 10:15 – İlk 15 dk: Kimi ararsınız? İlk üç eyleminiz?**
Vardiya amiri, iş güvenliği/emniyet sorumlusu ve OT/BT olay ekibi haberdar edilir. (1) Pres kontrollü biçimde güvenli duruma alınır ve yeniden başlatma önlenir. (2) Şüpheli uzaktan erişim yetkili ekipçe kapatılır. (3) Olay saati ve ilk gözlemler kaydedilir.

**2. İlk 2 saat: E-stop güvenli mi – nasıl doğrularsınız? Hangi kanıt korunur? Hangi hesap kapatılır?**
Yetkili emniyet personeli, güvenli test prosedürüyle acil durdurma ve ışık perdesini doğrular; doğrulanmadan üretim başlamaz. PLC program sürümü/karşılaştırması, erişim günlükleri, alarm kayıtları, ağ ve bakım oturumu kayıtları korunur. Şüpheli bakım hesabı devre dışı bırakılır; deliller silinmez.

**3. 24 saat – CRA erken uyarı: Hangi bilgi hazır olmalı?**
Olayın başlangıç zamanı, etkilenen ürün/sistem, bilinen sömürü veya yetkisiz erişim belirtileri, emniyet ve üretim etkisi, ilk önlemler ve belirsizlikler hazır olmalıdır. CRA bildirim yükümlülüğü, ürünün kapsamına ve sorumlu ekonomik operatöre göre hukuk/uyum ekibince değerlendirilir.

**4. 72 saat – CRA bildirim: Kök neden, etki, önlem – kim ne yapıyor?**
OT/BT ekibi teknik analiz ve kök neden incelemesini; emniyet ekibi fiziksel risk ve doğrulamayı; yönetim/uyum ekibi kapsam ve gerekiyorsa resmi bildirimi koordine eder. Bilinen etki, alınan önlemler ve güncel bulgular yazılır.

**5. 14 gün – Son rapor: Hangi loglar/kayıtlar korunmuş olmalı?**
VPN/bakım hesabı girişleri, jump server kayıtları, PLC değişiklik geçmişi ve yedekleri, HMI/SCADA alarmları, güvenlik test tutanakları, zaman çizelgesi, kararlar ve kanıt bütünlüğü kayıtları korunmalıdır.

**Önemli:** CRA'daki 24 saat / 72 saat / 14 gün takvimi her siber olay için otomatik geçerli değildir. Gerçek bildirim türü, yükümlü taraf ve süreler ilgili mevzuat kapsamında ayrıca doğrulanmalıdır. Önce emniyet, sonra kanıt; delilleri silmek için sistem sıfırlanmaz.
