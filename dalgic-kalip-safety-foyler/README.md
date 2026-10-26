# Dalgıç Kalıp – Progresif Sac Kalıplama Pres Hattı | Safety 4.0 Lab Föyleri (1–4)

**Öğrenci:** Adile Nur Yiğit  
**Ders:** Yazılım Güncel Konular / Safety 4.0  
**Kaynak firma:** [Dalgıç Kalıp – SAMİB](https://samib.org.tr/uye/dalgic-kalip/)

> **Kapsam ve doğruluk notu:** Dalgıç Kalıp bir firma adıdır. Buradaki **progresif sac kalıplama pres hattı**, firmanın doğrulanmış belirli bir marka/model makinesi değil; ders kapsamında tasarlanmış **temsili bir endüstriyel otomasyon senaryosudur**. PLC, Safety PLC, HMI, sensörler ve uzaktan erişim gibi bileşenler bu örnek senaryonun varsayımlarıdır. Gerçek ekipman özellikleri üretici dokümanıyla teyit edilmelidir.

## Makine / süreç
Sac şerit, besleyici üzerinden prese aktarılır. Pres stroku sırasında progresif kalıp sac üzerinde kesme/şekillendirme işlemleri gerçekleştirir; parçalar çıkış bölümüne taşınır.

| Bileşen (varsayımsal) | Görev |
|---|---|
| PLC + HMI | Besleme sırası, üretim sayacı ve operatör arayüzü |
| Pres kontrolü + sürücü | Pres stroku ve besleyici hareketi |
| Safety PLC / emniyet rölesi | E-stop, koruyucu kapı, ışık perdesi izlemesi |
| Güvenli durdurma elemanları | Tehlikeli hareketi durdurma; presin yapısına göre güvenli fren/enerji izolasyonu |
| Bakım istasyonu | Yetkili tanılama ve kontrollü yazılım bakımı |

**Başlıca tehlikeler:** Kalıp arasında ezilme/sıkışma, sac kenarından kesilme, beklenmedik strok, bakım sırasında kontrolsüz hareket.

## Föyler
| No | Konu | Dosya |
|---|---|---|
| 1 | Safety Architecture | [Lab1_Safety_Architecture.md](foyler/Lab1_Safety_Architecture.md) |
| 2 | IEC 62443 Zone / Conduit | [Lab2_Zone_Conduit.md](foyler/Lab2_Zone_Conduit.md) |
| 3 | Threat & Risk / Risk Register | [Lab3_Risk_Register.md](foyler/Lab3_Risk_Register.md) |
| 4 | Secure Remote Access | [Lab4_Secure_Remote_Access.md](foyler/Lab4_Secure_Remote_Access.md) |

Ek: [SWOT analizi](SWOT_Analizi.md).

## Kısa sonuç
- **Emniyet fonksiyonu:** Işık perdesi ihlal edildiğinde, koruyucu kapı açıldığında veya E-stop'a basıldığında presin tehlikeli hareketi güvenli şekilde durdurulur; yeniden başlatma kontrollüdür.
- **Zone'lar:** Kontrol, Safety, Mühendislik/Bakım, Endüstriyel DMZ, Kurumsal IT.
- **Önemli siber risk:** Yetkisiz bakım erişimi üzerinden pres hareket parametrelerinin değiştirilmesi.
- **Uzaktan erişim:** VPN + MFA + Jump Server + kişisel hesap + oturum kaydı + varsayılan kapalı.
- **Bağımsızlık:** Normal PLC veya ağ ele geçirilse bile emniyet fonksiyonları güvenli duruş sağlayabilmelidir.

> Eğitim amaçlı kavramsal risk çalışmasıdır; PL/SIL doğrulaması, devre şeması, makine uygunluk değerlendirmesi veya gerçek saha güvenlik tasarımı değildir.
