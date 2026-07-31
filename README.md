# T3 Gemstone İHA — Eğitim ve Yapım Dokümantasyonu

T3 Gemstone kartı kullanılarak bir İnsansız Hava Aracı (İHA/drone)
tasarlamak ve inşa etmek isteyenler için hazırlanmış eğitim
dokümantasyonu. Bu doküman, "İHA Temelleri" ve "Sıfırdan Quadcopter
Yapımı" başlıklı iki eğitim sunumunun (Seda Nur Boduroğlu, Türkiye
Teknoloji Takımı Vakfı) tek bir kaynakta birleştirilip
genişletilmesiyle oluşturulmuştur. Orijinal sunum dosyalarına
[kaynak-sunumlar](kaynak-sunumlar) klasöründen erişilebilir.

T3 Gemstone kartının kurulumu (imaj yazma, ilk açılış vb.) gibi genel
konularda T3'ün resmi dokümantasyonuna yönlendiriyoruz:
[docs.t3gemstone.org](https://docs.t3gemstone.org). Bu doküman
yalnızca İHA'ya özgü teori, tasarım kararları ve parça seçimi konularına
odaklanır.

## İçindekiler

### Temel Kavramlar

- [1. Giriş: İHA Nedir, Türleri ve Temel Alt Sistemler](docs/01-giris-ve-iha-turleri.md)
- [2. Mekanik Temeller](docs/02-mekanik-temelleri.md)
- [3. Aviyonik ve Güç Sistemleri](docs/03-aviyonik-ve-guc-sistemleri.md)
- [4. Yazılım ve Kontrol Mantığı](docs/04-yazilim-ve-kontrol-mantigi.md)

### Uygulama

- [5. Parça Seçimi, Montaj ve Tasarım Süreci](docs/05-parca-secimi-montaj-ve-tasarim-sureci.md)
- [6. T3 Gemstone O1 ile Aviyonik Mimarisi ve Örnek Yapılandırmalar](docs/06-t3-gemstone-o1-mimarisi-ve-ornek-yapilandirmalar.md)

### Referans

- [7. Kaynakça](docs/07-kaynakca.md)

## Nasıl Okunmalı?

Dokümanlar sırayla okunacak şekilde tasarlanmıştır; her dosyanın
sonunda bir sonraki bölüme yönlendiren bir bağlantı bulunur. İlk kez
bir İHA tasarlayacaklar için 1'den 6'ya kadar sırayla okumak,
doğrudan T3 Gemstone O1'e özgü donanım bilgisine ulaşmak isteyenler
için ise doğrudan [6. bölüme](docs/06-t3-gemstone-o1-mimarisi-ve-ornek-yapilandirmalar.md)
geçmek önerilir.

## Proje Özeti

Bu doküman, döner kanat (quadcopter) bir İHA'nın uçtan uca tasarım
sürecini kapsar: aracın hareketini tanımlayan eksenler ve itki-kuvvet
dengesinden, motor/ESC/pervane/batarya seçim kriterlerine, PID tabanlı
kontrol mantığından T3 Gemstone O1 kartı üzerinde ArduPilot çalıştıran
somut aviyonik yapılandırmalara kadar uzanan bir kapsamı içerir.

## Katkı

Bir hata fark ederseniz veya eksik bir konu eklemek isterseniz, ilgili
`docs/*.md` dosyasını düzenleyip bir pull request açabilirsiniz.
