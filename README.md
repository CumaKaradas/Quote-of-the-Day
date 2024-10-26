# Quote of the Day (Günün Sözü)

Bu projede, kullanıcılara her gün yeni bir alıntı sunan basit bir web uygulaması geliştirilmiştir. Kullanıcılar beğendikleri alıntıları favorilerine ekleyebilir, karanlık ve aydınlık tema arasında geçiş yapabilir, alıntıyı sesli dinleyebilir ve alıntıyı kopyalayarak paylaşabilir.

## Özellikler

- **Yeni Alıntı Getir**: Kullanıcı bir butona basarak rastgele bir yeni alıntı yükleyebilir.
- **Favorilere Ekle**: Beğenilen alıntılar favorilere kaydedilebilir. Favorilere eklenen alıntılar, sayfa yenilense veya tarayıcı kapatılsa bile yerel depolama (LocalStorage) kullanılarak saklanır.
- **Tema Değiştirme**: Aydınlık ve karanlık tema arasında geçiş yapılabilir. Seçilen tema, yerel depolama ile kaydedilir.
- **Alıntıyı Dinle**: Alıntıyı sesli olarak dinlemek için `Web Speech API` kullanılır.
- **Alıntıyı Kopyala**: Alıntı kolayca kopyalanabilir, böylece kullanıcılar başka bir yerde paylaşabilir.
- **Bildirim ve Yükleniyor Göstergesi**: Alıntılar yüklenirken yükleniyor göstergesi görünür ve her işlem için kullanıcılara kısa bildirimler sunulur.

## Kullanılan Teknolojiler

- **HTML5**: Uygulamanın iskelet yapısını oluşturur.
- **CSS3**: Modern ve duyarlı tasarım, tema değişikliği ve animasyon efektleri için kullanılmıştır.
- **JavaScript**: API ile veri alma, kullanıcı etkileşimlerini işleme ve yerel depolama gibi işlevler için temel programlama dilidir.
- **Quotable API**: Alıntıları rastgele almak için kullanılan API.

## Kurulum ve Kullanım

1. Bu projeyi kendi bilgisayarınıza klonlayın:
   ```bash
   git clone https://github.com/kullanıcıadınız/quote-of-the-day.git
   ```

2. Proje klasörüne gidin:
   ```bash
   cd quote-of-the-day
   ```

3. `index.html` dosyasını bir tarayıcıda açarak uygulamayı başlatın.

## Proje Yapısı

```
├── index.html         # Ana HTML sayfası
├── styles.css         # Uygulamanın stil dosyası
├── script.js          # Ana JavaScript dosyası
└── README.md          # Proje açıklamaları
```

## Özellikler ve Fonksiyonlar

### Alıntı Alma
- **fetchQuote()** fonksiyonu, Quotable API'den yeni bir alıntı almak için kullanılır. Alıntı başarıyla yüklendiğinde `displayQuote()` ile görüntülenir, hata oluşursa `displayError()` ile hata mesajı gösterilir.

### Favorilere Ekleme ve Yönetme
- **saveFavorite()**: Alıntıyı favorilere ekler ve favorilerde tekrar etmemesi için kontrol yapar.
- **addFavoriteQuote()**: Favori listeye yeni alıntıyı ekler ve yanında bir kaldırma düğmesi gösterir.
- Favori alıntılar, **yerel depolama** kullanılarak saklanır ve her sayfa yenilendiğinde geri yüklenir.

### Tema Değiştirme
- **toggleTheme()** fonksiyonu, kullanıcının aydınlık ve karanlık tema arasında geçiş yapmasını sağlar. Kullanıcı tercihleri yerel depolama ile kaydedilir.

### Alıntıyı Sesli Okuma ve Kopyalama
- **speakQuote()** fonksiyonu, alıntıyı `Web Speech API` kullanarak sesli okur.
- **copyQuote()** fonksiyonu, alıntıyı panoya kopyalar.

### Bildirimler ve Yükleniyor Göstergesi
- **showNotification()**: Kullanıcıya işlemler sonrasında kısa bildirimler gösterir.
- **showLoadingSpinner()**: Yeni bir alıntı yüklenirken yükleniyor göstergesi aktif olur.

## Geliştirme ve Katkıda Bulunma

Katkıda bulunmak istiyorsanız, lütfen bir **pull request** gönderin veya bir **issue** açın. Bu projeyi geliştirmemiz için önerilerinizi bekliyoruz.

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Daha fazla bilgi için `LICENSE` dosyasına göz atabilirsiniz.
```

Bu README dosyası, projenizin özelliklerini ve nasıl çalıştığını açıklayarak kullanıcıların projeyi anlamasına ve kullanmasına yardımcı olacaktır.
