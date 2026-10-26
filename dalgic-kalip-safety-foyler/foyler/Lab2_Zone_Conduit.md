# Lab 2 – IEC 62443 Mini Workshop: Zone / Conduit

## Görev A – Zone tasarımı
| Zone | Varlıklar (örnek) | Koruma amacı |
|---|---|---|
| Kontrol | PLC, HMI, pres sürücüsü, besleyici | Üretim kontrolünün sürekliliği |
| Safety | Safety PLC, ışık perdesi, E-stop, kilitler | Emniyet fonksiyonlarının bütünlüğü |
| Mühendislik/Bakım | Bakım bilgisayarı | Kontrollü değişiklik |
| Endüstriyel DMZ | Jump server, kayıt sistemi | Dış bağlantıların aracılanması |
| Kurumsal IT | Ofis bilgisayarları | Üretimden ağ ayrımı |

**Safety PLC neden ayrı?** Emniyet fonksiyonuna yetkisiz yazma erişimini azaltmak ve üretim ağı arızalarından etkilenmeyi sınırlandırmak için.

**Conduit'ler:** Kurumsal IT ↔ DMZ ↔ bakım ↔ kontrol geçişlerinde firewall, izinli IP/port, protokol sınırlaması ve kayıt; kontrol → Safety yönünde mümkünse salt okunur izleme. Safety PLC'ye uzaktan program yazma varsayılan olarak yasak.

## Görev B – Uzaktan erişim kararı
| Karar | Seçim | Gerekçe |
|---|---|---|
| Aracı | Jump server | Doğrudan PLC erişimini önler |
| Tünel | VPN | Şifreli bağlantı |
| Kimlik | MFA | Çalınmış parolanın tek başına yetmemesi |
| Hesap | Kişisel | İzlenebilirlik |
| Kayıt | Tam oturum kaydı | Denetim |
| Zamanlama | Varsayılan kapalı | Bakım penceresinde geçici izin |
