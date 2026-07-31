# 6. T3 Gemstone O1 ile Aviyonik Mimarisi

Önceki bölümlerde genel İHA teorisini gördük. Bu bölümde, bu teoriyi
somut bir donanım seçimine indirgiyoruz: T3 Gemstone O1 kartının bir
İHA'nın otopilot kartı olarak nasıl konumlandığını ele alıyoruz.

T3 Gemstone O1'in kart kurulumu (imaj yazma, ilk açılış vb.) bu
dokümanın kapsamı dışındadır; bunun için T3'ün resmi dokümantasyonuna
bakınız: [docs.t3gemstone.org](https://docs.t3gemstone.org).

## Aviyonik Sistem Mimarisi

Aviyonik sistem mimarisinde ihtiyaçlara ve performans beklentilerine
göre farklı bileşen konfigürasyonları kullanılabilir. Bu projede
esas alınan temel sistem bileşenleri şunlardır:

| Bileşen | Seçim |
|---|---|
| Uçuş Kontrolcüsü | T3 Gemstone O1 |
| Kumanda & Alıcı | Flysky FS-i6X & FS-iA10B |
| Güç Dağıtımı & ESC | Bireysel 30A ESC'ler + Matek PDB veya 4'ü 1 arada (4in1) ESC çözümleri |
| Motorlar | A2212 veya SunnySky X2212 serisi fırçasız motorlar |
| Batarya & Güvenlik | 3S / 4S Li-Po Batarya ve Emniyet Akım Kesici |
| Otopilot Kartı | T3 Gemstone O1 & ArduPilot |
| Otopilot Yazılımı | Farklı araç türlerini destekleyen, gelişmiş ve açık kaynaklı ArduPilot altyapısı |
| Entegre Sensör Desteği | Kart üzerinde dahili IMU, pusula, barometre |

## Otopilot Kartı: T3 Gemstone O1 & ArduPilot

<p align="center">
  <img src="images/06-gemstone-mimarisi/t3-gemstone-o1.png" width="300" alt="T3 Gemstone O1 kartı">
</p>

T3 Gemstone O1, üzerinde ArduPilot çalıştırılarak farklı araç
türlerini destekleyen, gelişmiş ve açık kaynaklı bir otopilot altyapısı
oluşturur.

### Entegre Sensör Desteği

- **IMU (Atalet Ölçüm Birimi):** InvenSense ICM-20948 (SPI arayüzü) ile
  hassas konum/yönelim takibi.
- **Pusula & Barometre:** Dahili AK09916 manyetometre ve yüksek
  hassasiyetli LPS22DFTR yükseklik sensörü.
- **Güç ve Batarya İzleme:** ADS1115 (16-bit ADC) entegresi ile 4
  kanallı anlık voltaj ve akım takibi.

### Haberleşme ve Çevre Birimleri

- **CAN Bus:** Güvenilir veri iletimi için TCAN1462-Q1 sürücüsü.
- **GPS & RC:** UART üzerinden GPS ve SBUS kumanda alıcı bağlantısı.
- **Motor/Servo Kontrolü:** 7 adet donanımsal PWM çıkışı.

> **Not:** Bu bölümdeki sensör ve arayüz bilgileri, kartın genel
> donanım yeteneklerini özetler. GPIO pin haritası ve fiziksel
> bağlantı detayları projeye özgüdür ve her kartta `gpiodetect` /
> `gpioinfo` ile doğrulanmalıdır.

---

Devam etmek için
[07-ornek-yapilandirmalar-ve-eklentiler.md](07-ornek-yapilandirmalar-ve-eklentiler.md).
