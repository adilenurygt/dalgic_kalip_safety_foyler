# Lab 4 – Secure Remote Access

## Görev A – Mevcut / Hedef
**MEVCUT (varsayımsal güvensiz kurgu):** Uzak kullanıcı → internet → doğrudan bakım modülü → PLC. Paylaşılan hesap, sürekli açık erişim, eksik oturum kaydı.

**HEDEF:** Uzak kullanıcı → VPN + MFA → endüstriyel DMZ / Jump Server → güvenlik duvarı → izinli bakım istasyonu → kontrol PLC'si.

**Beş ilke:** (1) VPN ile şifreleme, (2) MFA ve kişisel hesap, (3) Jump server ve ağ ayrımı, (4) tam oturum kaydı, (5) varsayılan kapalı / süreli izin. Safety PLC'ye uzaktan yazma izni verilmez.

## Görev B – Functional Safety köprüsü
**1. Saldırgan içeri girerse emniyet fonksiyonu etkilenir mi?** Erişim sınırları yanlış tasarlanmışsa evet; emniyet mantığı veya güvenli durdurma yoluna müdahale ciddi yaralanmaya yol açabilir.

**2. Bağımsızlık gereksinimi:** Işık perdesi, E-stop, koruyucu kapı ve güvenli durdurma zinciri, normal PLC/uzak bakım yolu ele geçirilse dahi görevini yerine getirecek şekilde tasarlanmalı; safety mantığının uzaktan değiştirilmesi engellenmelidir.
