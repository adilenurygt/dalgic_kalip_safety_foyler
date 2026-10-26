# Lab 3 – Threat & Risk + Risk Matrix

Bu değerlendirme **temsili senaryoya** aittir. **L:** olasılık, **S:** şiddet, **E:** maruziyet; her biri 1–3. **Skor = L × S × E**. Sınıflar ders için örnek olarak 1–6 düşük, 7–12 yüksek, 13–27 kritik alınmıştır; **S=3 ise düşük skor dahi ayrıca ele alınır.**

| Senaryo (kim → kapı → zincir → sonuç) | L | S | E | Skor | Öncelik |
|---|---:|---:|---:|---:|---|
| Saldırgan → uzaktan bakım → pres parametresini değiştirir → beklenmedik strokla ezilme | 3 | 3 | 3 | 27 | Kritik |
| Yetkisiz kullanıcı → HMI hesabı → besleyici zamanlamasını bozar → operatör sıkışır | 2 | 3 | 2 | 12 | Yüksek |
| Bakım personeli → taşınabilir USB → hatalı konfigürasyon yükler → tehlikeli hareket oluşur | 1 | 3 | 1 | 3 | Düşük skor; S=3 öncelikli inceleme |

**En yüksek öncelik:** Uzaktan bakım yoluyla kontrol parametrelerinin değiştirilmesi; erişim olasılığı, yaralanma şiddeti ve maruziyet birlikte yüksektir.

**S=3 düşük skor örneği:** USB kaynaklı yanlış konfigürasyon. Puanı düşük olsa da ağır yaralanma olasılığı nedeniyle tedbir gerekir.

**Önlemler:** Varsayılan kapalı bakım erişimi, MFA, izinli değişiklik süreci, güvenli yedekler, taşınabilir medya kontrolü, bağımsız emniyet fonksiyonlarının periyodik testi.
