---
title: Gizlilik Politikası — Frejya
layout: default
---

# Frejya — Gizlilik Politikası

**Yürürlük Tarihi:** 14 Mayıs 2026
**Son Güncelleme:** 14 Mayıs 2026

İşbu Gizlilik Politikası, **Müjdat TELLİ** (bundan sonra "biz", "Frejya" veya "Hizmet Sağlayıcı" olarak anılacaktır) tarafından sunulan **Frejya** mobil uygulamasının (bundan sonra "Uygulama") kullanıcılarından (bundan sonra "siz" veya "Kullanıcı") topladığı kişisel verileri, bu verilerin kullanım amaçlarını, üçüncü taraflarla paylaşım koşullarını ve haklarınızı açıklar.

İletişim: **tellimujdat@gmail.com**

Bu Politika, **6698 sayılı Kişisel Verilerin Korunması Kanunu (KVKK)** ve uygulanabildiği ölçüde **Avrupa Birliği Genel Veri Koruma Tüzüğü (GDPR)** kapsamında düzenlenmiştir.

---

## 1. Veri Sorumlusu

Frejya uygulamasının veri sorumlusu, gerçek kişi sıfatıyla **Müjdat TELLİ**'dir. KVKK kapsamındaki başvurularınızı yukarıdaki e-posta adresine iletebilirsiniz.

---

## 2. Topladığımız Kişisel Veriler

Frejya'yı kullanırken aşağıdaki veri kategorilerini topluyoruz:

### 2.1. Kimlik ve İletişim Bilgileri
- **E-posta adresi** (hesap oluşturma ve hesap kurtarma için)
- **Telefon numarası** (SMS doğrulaması ve hesap güvenliği için, opsiyonel)
- **Kullanıcı adı / Görünen ad** (profil oluştururken siz belirlersiniz)
- **Şifre** (asla düz metin saklanmaz; bcrypt ile hash'lenir ve salt eklenir)

### 2.2. Profil Bilgileri (Sizin Sağladığınız)
- **Profil fotoğrafı** (zorunlu, aşağıda detaylı açıklanmıştır)
- **Sesli tanıtım kaydı** (opsiyonel)
- **Doğum yılı** (18 yaş kontrolü için zorunlu)
- **Cinsiyet** (eşleşme algoritması için)
- **Boy, kilo, medeni durum** (opsiyonel profil verileri)
- **Eğitim, meslek** (opsiyonel)
- **Yaşam tarzı tercihleri:** içki, sigara, evcil hayvan, dans, din, dövme, LGBT durumu, mobil oyun, seyahat (opsiyonel, sansürsüz "Vazgeç" hakkıyla)
- **Hobiler, üç kelimelik tanım, biyografi** (serbest metin)

### 2.3. Konum Verileri
- Kayıt sırasında **GPS koordinatlarınızı (enlem, boylam)** isteriz. Bu koordinatlar **yalnızca ters geocoding** ile **şehir, ilçe ve ülke** bilgisine dönüştürülmek için kullanılır.
- **Ham GPS koordinatları profilinizde veya başka bir kullanıcıya görünür şekilde saklanmaz.**
- Veritabanında yalnızca: **şehir, ilçe, ülke** metin alanları tutulur.
- İstisna: dolandırıcılık ve "Impossible Travel" (imkânsız konum değişimi) anomali tespiti için **son giriş koordinatları** ve **zaman damgası** ayrı bir alanda kısa süreli olarak tutulur; bu veri yalnızca güvenlik ihlali analizi için sistem tarafından okunur, hiçbir kullanıcıya gösterilmez.

### 2.4. İletişim ve İçerik Verileri
- **Mesajlarınız:** Diğer kullanıcılarla aranızdaki mesajlar **AES-256 ile şifrelenir (at-rest depolama)**. Sunucularımız mesaj içeriğini **çözemez**. Mesaj **metadata**'sı (gönderen ID, alıcı ID, zaman damgası, okundu bilgisi) hizmet işlevselliği için saklanır.
- **Gönderiler (post'lar):** Frejya Aura sosyal akışına paylaştığınız içerikler (semboller / SVG referansları). Diğer kullanıcılara görünür.
- **Etkileşimler:** Beğeni, yorum, eşleşme, kapı zili çalma kayıtları (kim kime, ne zaman).
- **Engelleme / şikâyet listeleri:** Kişisel güvenliğiniz için.

### 2.5. Teknik Veriler
- **Cihaz tanımlayıcı (Device ID):** Sybil (sahte hesap) saldırılarını önlemek için. Cihaz ID'si Apple/Google'ın sağladığı anonim tanımlayıcıdır; reklam takibinde kullanılmaz.
- **Push notification token'ı:** Bildirim göndermek için Expo Push Service üzerinden Apple APNs / Google FCM'e iletilir.
- **Uygulama sürümü, işletim sistemi sürümü:** Hata ayıklama ve uyumluluk kontrolü için.

### 2.6. Otomatik Toplanan Veriler
- **Crash / hata raporları:** Uygulama çöktüğünde stack trace ve cihaz bilgisi anonim olarak toplanır (Sentry servisi üzerinden, AB / Almanya sunucularında).
- **Kullanım istatistikleri:** Günlük etkileşim sayısı (beğeni, yorum, eşleşme) gibi sayaçlar oran limiti uygulamak için tutulur.

---

## 3. AI Tabanlı İçerik İnceleme (Yapay Zekâ Kullanımı)

Frejya, kullanıcı güvenliği için **profil fotoğrafınızı** otomatik yapay zekâ servislerine analiz ettirir. Bu inceleme:

- **Yapay zekâ servisi:** Profil fotoğrafları, Google Gemini yapay zekâ API'sine **anonim olarak** (kullanıcı kimliğiniz olmadan) gönderilir. Kullanılan model güncel ihtiyaca göre Frejya yönetimi tarafından seçilir (örn. Gemini 1.5 Flash veya Gemini 3). Yedek servis olarak Groq da yapılandırılmıştır.
- **Yer:** Bu servis Türkiye dışında (Google sunucuları) çalışır. Fotoğrafınız işleme tabi tutulduktan sonra Google'ın kendi gizlilik politikası gereği saklanmaz (Gemini API üzerinden gönderilen veriler model eğitimi için kullanılmaz, geçici işleme tabi tutulup atılır).
- **Yüz tespiti:** Fotoğraftaki yüz tespiti AI servisi tarafından yapılır (cihazınızda ön tarama yoktur). AI hem yüz varlığını hem de içerik uygunluğunu tek bir çağrıda denetler.
- **Onay:** Profil oluştururken AI işlemeye onay vermeniz istenir. Onay vermediğinizde Frejya'yı kullanamazsınız (çünkü profil fotoğrafı doğrulaması zorunludur).
- **Sonuç:** Fotoğrafınız onaylanır, reddedilir veya manuel inceleme için bekletilir. Reddedilen fotoğraflar Storage'dan silinir.

**Önemli:** Biyografi (bio), hobiler veya diğer metin alanları AI ile analiz edilmez.

---

## 4. Kişisel Verilerin İşlenme Amaçları

Verilerinizi yalnızca aşağıdaki amaçlarla işleriz:

1. **Hizmetin sağlanması:** Eşleştirme algoritması, mesajlaşma, sosyal akış.
2. **Hesap güvenliği:** Sahte hesap önleme (Device ID), dolandırıcılık tespiti (Impossible Travel), şüpheli faaliyet kayıtları.
3. **İçerik moderasyonu:** Profil fotoğrafı AI incelemesi, şikâyet / engelleme sistemleri.
4. **İletişim:** Bildirimler, hesap kurtarma e-postaları.
5. **Hizmet iyileştirme:** Anonim crash raporları (Sentry).
6. **Yasal yükümlülükler:** Mahkeme talebi, dolandırıcılık ihbarı vb.

**Verilerinizi ASLA:**
- Reklam veya pazarlama amacıyla üçüncü taraflara satmıyoruz.
- Siyasi, dini veya ticari profilleme amacıyla işlemiyoruz.
- E-posta listesi olarak üçüncü taraflara devretmiyoruz.

---

## 5. Üçüncü Taraf Hizmet Sağlayıcılar

Aşağıdaki hizmet sağlayıcıları kullanırız. Hepsi kendi gizlilik politikalarına tabidir:

| Hizmet | Amaç | Konum | Veri Türü |
|---|---|---|---|
| **Supabase** | Veritabanı, kimlik doğrulama, depolama, realtime | AB (Frankfurt / İrlanda) | Tüm profil, mesaj metadata, fotoğraf |
| **Sentry** | Crash & hata izleme | AB (Almanya) | Anonim crash raporları, kullanıcı UUID |
| **Google Gemini API** | Profil fotoğrafı AI incelemesi | ABD / AB | Yalnızca fotoğraf (anonim, kullanıcı kimliği yok) |
| **Groq API** | Profil fotoğrafı AI incelemesi (yedek) | ABD | Yalnızca fotoğraf (anonim) |
| **Expo Push Service** | Push notification iletimi | ABD (Apple APNs / Google FCM transit) | Sadece push token + mesaj başlığı |
| **Apple App Store / Google Play** | Uygulama dağıtımı | Global | Indirme verisi (bizimle paylaşılmaz, sadece istatistik) |

Her hizmet sağlayıcısıyla veri işleme sözleşmeleri (DPA) yürürlüktedir veya yürürlüğe konulacaktır.

---

## 6. Veri Saklama Süreleri

| Veri Türü | Saklama Süresi |
|---|---|
| Aktif hesap verileri | Hesap aktif olduğu sürece |
| Mesajlar (E2EE) | Hesap silindiğinde silinir; resim mesajları okunmadan 48 saat, okunduktan sonra 2 dakika sonra otomatik silinir |
| Hesap silme sonrası anonim kayıt | 60 gün (yasal ihbar / dolandırıcılık şikâyeti için) |
| Crash logları (Sentry) | 90 gün |
| Audit logları (yasal yükümlülük) | 1 yıl |
| Reddedilmiş profil fotoğrafları | Anında silinir |

---

## 7. KVKK Kapsamındaki Haklarınız

KVKK m.11 uyarınca aşağıdaki haklara sahipsiniz:

1. Kişisel verilerinizin işlenip işlenmediğini öğrenme,
2. İşlenmişse buna ilişkin bilgi talep etme,
3. İşlenme amacını ve amacına uygun kullanılıp kullanılmadığını öğrenme,
4. Yurt içinde / yurt dışında aktarıldığı üçüncü tarafları bilme,
5. Eksik / yanlış işlenen verilerin düzeltilmesini isteme,
6. **Verilerinizin silinmesini isteme** (Uygulama içindeki "Hesabımı Sil" butonu ile anında yapılabilir),
7. Düzeltilen / silinen verilerin üçüncü taraflara bildirilmesini isteme,
8. Otomatik sistemlerle analiz sonucu aleyhinize bir sonuç çıkmasına itiraz etme,
9. Kanuna aykırı işleme sonucu zarara uğradıysanız tazminat talep etme.

Bu hakları kullanmak için **tellimujdat@gmail.com** adresine yazılı talep gönderebilirsiniz. Talebiniz en geç **30 gün içinde** ücretsiz olarak yanıtlanır.

---

## 8. Çocukların Gizliliği

Frejya **18 yaş ve üzeri** kullanıcılar içindir. **18 yaşından küçük** kişilerin hesap oluşturması yasaktır. Yaşınızı kayıt sırasında beyan etmeniz istenir; sahte beyan tespit edildiğinde hesap derhal silinir. 18 yaş altı bir kişinin Frejya'da hesap açtığını fark ederseniz lütfen bize bildirin (**tellimujdat@gmail.com**), hesabı 24 saat içinde sileriz.

---

## 9. Veri Güvenliği

Verilerinizi korumak için aşağıdaki teknik ve idari tedbirleri uygularız:

- **At-rest şifreleme (AES-256):** Mesaj içerikleri sunucularımıza yazılmadan önce cihaz tarafında AES-256 ile şifrelenir. Bu, veritabanı yedekleri veya yetkisiz erişim durumunda mesaj içeriklerinin düz metin olarak okunamamasını sağlar. NOT: Şu anki uygulamamızda paylaşılan tek bir uygulama anahtarı kullanılmaktadır; bu nedenle bu mekanizma teknik anlamda "uçtan uca şifreleme" (E2EE) olarak nitelendirilmez. İleride Signal Protocol benzeri tam E2EE'ye geçiş hedeflenmektedir.
- **Şifre güvenliği:** Bcrypt hash + salt; düz metin şifre saklanmaz.
- **Veritabanı güvenliği:** Supabase Row Level Security (RLS) ile her satır için izin kontrolü.
- **SSL/TLS:** Tüm trafik HTTPS ile şifrelenir; sertifika sabitleme (SSL pinning) aktiftir.
- **Erişim kontrolü:** Veritabanına sadece yetkili sistem servisleri erişebilir; biz dahil hiçbir personel kullanıcı şifrelerini okuyamaz.
- **Hız sınırlaması (rate limiting):** Brute-force ve spam saldırılarına karşı.
- **Anomali tespiti:** Şüpheli oturum açma girişimleri tespit edilir.

**Veri ihlali durumunda:** KVKK m.12/5 uyarınca, kişisel verilerin yetkisiz kişiler tarafından elde edildiğini öğrendiğimiz andan itibaren **en geç 72 saat içinde** Kişisel Verileri Koruma Kurulu'na ve etkilenen kullanıcılara bildirim yapacağız.

---

## 10. Yurt Dışına Veri Aktarımı

Bazı hizmet sağlayıcılarımız (Gemini, Groq, Expo) Türkiye dışında bulunur. Bu nedenle:

- Profil fotoğrafınız AI inceleme için anonim olarak ABD / AB'ye aktarılabilir.
- Push notification token'ınız Apple APNs (ABD) veya Google FCM (ABD) üzerinden iletilir.

Bu aktarımlar **KVKK m.9** kapsamında **açık rızanız** alınarak gerçekleştirilir; kayıt sırasında size bu konuda bilgi verilir ve onay istenir.

---

## 11. Çerezler ve İzleme

Frejya mobil bir uygulama olduğu için **çerez (cookie) kullanmaz**. Web sitemizde (https://mujdattelli.github.io/velvet/) yalnızca işlevsel çerezler kullanılabilir (oturum açmadığınız için kullanıcı izleme yapılmaz).

**Reklam SDK'sı yoktur. Analitik SDK'sı yoktur. Facebook / Google Analytics yoktur.**

---

## 12. Politika Değişiklikleri

Bu politikayı zaman zaman güncelleyebiliriz. Önemli değişiklikler için uygulama içi bildirim ve / veya e-posta ile haberdar edileceksiniz. Güncel sürüm her zaman bu adreste yayınlanır:

**https://mujdattelli.github.io/velvet/legal/privacy.tr.html**

---

## 13. İletişim

Sorularınız, şikâyetleriniz veya KVKK talepleri için:

**Müjdat TELLİ**
E-posta: **tellimujdat@gmail.com**

KVKK kapsamında resmi başvuruları **yazılı olarak** veya **kayıtlı elektronik posta (KEP)** yoluyla göndermeniz tercih edilir.

---

*Bu metin avukat onayı için taslak olarak hazırlanmıştır. Yürürlüğe girmeden önce hukuk danışmanı tarafından gözden geçirilmesi önerilir.*
