---
title: Kullanıcı Sözleşmesi (EULA) — Frejya
layout: default
---

# Frejya — Son Kullanıcı Lisans Sözleşmesi (EULA)

**Yürürlük Tarihi:** 14 Mayıs 2026
**Son Güncelleme:** 11 Haziran 2026

İşbu Son Kullanıcı Lisans Sözleşmesi ("Sözleşme"), **Müjdat TELLİ** (bundan sonra "biz" veya "Hizmet Sağlayıcı") tarafından sunulan **Frejya** mobil uygulamasının ("Uygulama" veya "Hizmet") kullanım koşullarını düzenler.

Uygulamayı indirip kullanarak, bu Sözleşme'nin tüm hükümlerini okuduğunuzu, anladığınızı ve kabul ettiğinizi beyan edersiniz. Kabul etmiyorsanız Uygulamayı kullanmayınız.

İletişim: **iletisim@frejya.app**

---

## 1. Hizmetin Tanımı

Frejya, **18 yaş ve üzeri** yetişkinler için tasarlanmış, "yavaş flört" (slow dating) felsefesine dayalı bir sosyal ve tanışma uygulamasıdır. Hizmet aşağıdakileri sunar:

- Profil oluşturma ve eşleştirme (cinsiyet ve doğum yılı kayıttan sonra **değiştirilemez**)
- Karşılıklı kelime alışverişiyle, **özel saklanan** fotoğrafların kademeli açıldığı **kazıma (scratch)** mekaniği
- **Gerçek uçtan uca şifrelenmiş (E2EE — NaCl/Curve25519) özel mesajlaşma** — özel anahtar yalnız cihazınızda; şifre sıfırlama/değişimi eski mesajları okunamaz hale getirebilir
- **Ses perdesi maskelemeli** sesli tanıtım (opsiyonel)
- **Frejya Aura** sembolik sosyal akış
- **Kapı Zili** sistemi ile sınırlı ilk iletişim
- **AI profil fotoğrafı doğrulaması** (gerçek insan / yüz / 18+ / cinsiyet / NSFW denetimi)

Hizmet, Apple App Store ve Google Play Store üzerinden dağıtılır.

---

## 2. Hesap Açma ve Yaş Şartı

### 2.1. Yaş Şartı
**Frejya'yı kullanabilmek için 18 yaşını doldurmuş olmanız zorunludur.** Yaşınızı kayıt sırasında beyan edersiniz. Sahte beyan tespit edildiğinde hesabınız **derhal ve kalıcı olarak** silinir.

### 2.2. Gerçek Bilgi
- Profilinizde **kendi gerçek fotoğrafınızı** kullanmanız zorunludur. AI inceleme sistemi sahte / başkasına ait / hayvan / illüstrasyon fotoğrafları reddeder.
- Kullanıcı adı, biyografi ve diğer profil bilgilerinizin **doğru ve güncel** olmasından sorumlusunuz.
- Bir kişi yalnızca **bir hesap** açabilir. Birden fazla hesap (sahte / sybil) tespit edildiğinde tüm hesaplar kalıcı olarak kapatılır.

### 2.3. Hesap Güvenliği
- Şifrenizi **kimseyle paylaşmayın**. Şifre bizim sunucularımızda bcrypt + salt ile saklanır; biz bile okuyamayız.
- Hesabınızdan yapılan tüm faaliyetlerden **siz sorumlusunuz**.
- Hesabınızda yetkisiz erişim şüphesi varsa derhal **iletisim@frejya.app** adresine bildirin.

---

## 3. Kabul Edilebilir Kullanım

Aşağıdaki davranışlar **kesinlikle yasaktır**:

### 3.1. İçerik ve Davranış Yasakları
- **Cinsel içerikli fotoğraf, video veya metin paylaşmak** (çıplaklık, müstehcen pozlar dahil),
- **18 yaş altı kişilere yönelik veya onları içeren içerik** paylaşmak — bu durumda derhal yetkili makamlara bildirimde bulunulur,
- **Şiddet, taciz, nefret söylemi, ayrımcılık** içeren mesajlaşma,
- **Spam, reklam, ticari pazarlama** mesajları,
- **Sahte profil, başkasının fotoğrafı, ünlü kimliği kullanımı**,
- **Dolandırıcılık girişimleri** (kripto, yatırım, "para gönder" şemaları),
- **Kişisel bilgi paylaşımı için baskı** (banka bilgisi, ev adresi, çıplak fotoğraf isteme),
- **Şantaj, tehdit, intihar / kendine zarar tehdidi**,
- **Telif hakkı ihlali** (başkasına ait fotoğraf, müzik, vb.).

### 3.2. Sistem Manipülasyonu
- Uygulamayı tersine mühendislik ile çözmeye, kaynak kodunu çalmaya, otomatik bot kullanmaya çalışmak,
- Eşleştirme algoritmasını sahte etkileşimlerle manipüle etmek,
- API'yi izinsiz kullanmak veya hız limitlerini aşmak,
- Diğer kullanıcıları toplu olarak engelleyerek arama sonuçlarını bozmak.

### 3.3. Yasal Düzenlemelere Uyum
- Türkiye Cumhuriyeti yasalarına aykırı her türlü içerik ve davranış yasaktır,
- 5651 sayılı Kanun, 6698 sayılı KVKK ve TCK hükümleri uygulanır.

---

## 4. İhlal Sonuçları

Kuralları ihlal eden kullanıcılara aşağıdaki yaptırımlar uygulanır:

| İhlal | Sonuç |
|---|---|
| Reddedilen profil fotoğrafı (art arda 5. kez) | 1 gün geçici yükleme kısıtı (onayla veya 30 günde sıfırlanır) |
| Şikâyet edilen mesaj (kanıtlı) | Uyarı, 7 gün ban veya kalıcı ban |
| Cinsel / illegal içerik | **Anında kalıcı ban** + yetkililere ihbar |
| 18 yaş altı tespiti | **Anında kalıcı ban** + Storage temizliği |
| Sahte profil / kimlik hırsızlığı | **Anında kalıcı ban** |
| Dolandırıcılık girişimi | **Anında kalıcı ban** + yetkililere ihbar |

Banlanmış kullanıcı, aynı e-posta / telefon / cihaz ID ile yeni hesap açamaz.

---

## 5. İçerik Hakları

### 5.1. Sizin İçeriğiniz
- Profil fotoğrafınız, biyografi, mesajlar, sosyal akış paylaşımlarınız **sizin mülkiyetinizdedir**.
- Frejya, bu içerikleri yalnızca Hizmeti sunmak için (depolama, görüntüleme, eşleştirme) **sınırlı, ücretsiz, geri alınabilir lisans** ile kullanır.
- Hesabınızı sildiğinizde içerikleriniz **hemen** silinir; hesap kaydı 15 gün boyunca anonim tutulur, sonra kalıcı olarak silinir. İşlem geri alınamaz.

### 5.2. Frejya'nın İçeriği
- Uygulamanın kendisi, logo, animal icon SVG'leri, hieroglif klavye sembolleri, kazıma sistemi tasarımı **Müjdat TELLİ'nin mülkiyetindedir**.
- Bu içerikleri kopyalayamaz, dağıtamaz, satamazsınız.

### 5.3. AI İşleme Onayı
Profil fotoğrafınızın yapay zekâ sistemleri tarafından (Google Gemini, Groq) içerik uygunluğu açısından otomatik incelenmesine açık rıza verirsiniz. Bu işlem **anonim** olarak (kullanıcı kimliği olmadan) yapılır. Detaylar: Gizlilik Politikası §3.

### 5.4. Sesli Mesaj Süre Sınırı
Sohbet içinde gönderilen sesli mesajlar mahremiyetiniz için **15 gün** boyunca saklanır; bu süre dolunca otomatik bir görev tarafından sunucudan kalıcı olarak silinir. Sohbet penceresinde "Sesli mesajın süresi doldu" etiketi görünür ve mesaj artık dinlenemez. Metin ve görsel mesajları bu sınırdan etkilenmez (onlar sohbet sona erene kadar durur).

---

## 6. Premium Üyelik (Frejya Premium)

Şu an Hizmet **tamamen ücretsizdir**. Gelecekte premium özellikler ücretli sunulabilir; bu durumda:

- Fiyatlar uygulama içinde açıkça gösterilir,
- Apple App Store / Google Play üzerinden satın alma yapılır,
- İade politikaları ilgili mağazanın kurallarına tabidir,
- Otomatik yenileme istenirse her zaman iptal edilebilir.

---

## 7. Hizmetin Kullanılabilirliği

- Hizmeti **olduğu gibi** ("as is") sunarız. Kesintisizlik, hatasızlık veya belirli bir sonuç **garanti edilmez**.
- Bakım, yazılım güncelleme veya teknik arıza nedeniyle Hizmet geçici olarak kesintiye uğrayabilir.
- Yasal yükümlülük, mücbir sebep (deprem, savaş, salgın, hükümet kararı) veya altyapı sağlayıcısı (Supabase, Apple, Google) sorunu nedeniyle Hizmeti durdurmak zorunda kalabiliriz.

---

## 8. Sorumluluk Sınırlandırması

### 8.1. Kullanıcılar Arası Etkileşim
- Frejya **yalnızca bir platformdur**; kullanıcılar arasındaki iletişimden, buluşmalardan veya gerçek hayattaki sonuçlardan **sorumlu değildir**.
- Diğer kullanıcılara güvenmeden önce mantıklı ihtiyat gösteriniz. **Tanışmadığınız kişilere kişisel bilgi, banka hesabı, çıplak fotoğraf vermeyiniz.**
- İlk buluşmaları **kamuya açık yerlerde** yapınız ve güvendiğiniz birine haber veriniz.

### 8.2. AI İnceleme Hatası
- Profil fotoğrafı AI incelemesi %100 doğru değildir. Yanlışlıkla reddedilen fotoğraflar için manuel inceleme talep edebilirsiniz (5 deneme hakkı sonrası tıkanırsa **iletisim@frejya.app**'a yazınız).

### 8.3. Yasal Sınırlar
Uygulanabilir yasaların izin verdiği azami ölçüde, Müjdat TELLİ aşağıdakilerden **sorumlu değildir**:

- Dolaylı, arızi veya neticede oluşan zararlar,
- Kullanıcı içeriğinden kaynaklanan zararlar (3. taraflar tarafından paylaşılan),
- Üçüncü taraf hizmet sağlayıcılarından (Supabase, Apple, Google, Gemini, Groq) kaynaklanan kesintiler,
- Sosyal etkileşimlerden, buluşmalardan veya kullanıcılar arası anlaşmazlıklardan doğan zararlar.

Toplam sorumluluğumuz, sizin son 12 ayda Frejya'ya yaptığınız ödemeleri (eğer varsa) aşamaz; Hizmet ücretsizse sorumluluk **sıfırdır**.

---

## 9. Hesap Sonlandırma

### 9.1. Sizin Hesabınızı Silmeniz
- Uygulamada **"Hesabımı Sil"** butonu ile istediğiniz anda hesabınızı silebilirsiniz.
- Verileriniz (profil, fotoğraflar, mesajlar, paylaşımlar) **anında ve geri alınamaz biçimde** silinir.
- 15 gün süreyle hesap kaydı silindi olarak işaretlenir, sadece UUID düzeyinde anonim tutulur (dolandırıcılık / yasal ihbar incelemesi için).
- 15 gün sonra otomatik bir görev hesap kaydını ve `auth.users` kaydını **tamamen siler** — Frejya'da hiçbir izi kalmaz.
- Bu 15 gün içinde aynı e-posta ile yeniden kayıt olamazsınız; sonrasında serbestsiniz.

> **Sohbet bitirme ≠ hesap silme:** Bir sohbeti bitirdiğinizde mesajlar olası adli/yasal delil için **15 gün şifreli arşivlenir** (size gösterilmez), sonra kalıcı silinir; ayrıca taraflar arasında varsayılan **60 günlük karşılıklı geçici engel** uygulanır (bu süre boyunca birbirinizi göremez, zil çalamaz, takip edemezsiniz).

### 9.2. Hesabınızı Bizim Sonlandırmamız
Aşağıdaki durumlarda hesabınızı sonlandırma hakkını saklı tutarız:

- Bu Sözleşme'nin ihlali,
- Diğer kullanıcılardan gelen kanıtlı şikâyetler,
- Yasal / mahkeme kararı,
- 12 aydan uzun süre giriş yapılmaması (sessiz hesaplar).

---

## 10. Apple App Store Ek Şartları

iOS sürümü için, aşağıdaki Apple ek şartları geçerlidir:

- Bu Sözleşme **Müjdat TELLİ ile Kullanıcı arasındadır**; Apple bu Sözleşme'nin **tarafı değildir**.
- Frejya'nın kalitesi, performansı ve uygunluğundan **münhasıran Müjdat TELLİ sorumludur**; Apple herhangi bir bakım veya destek yükümlülüğü altında değildir.
- Garanti ihlali durumunda Apple geri ödeme yapabilir; ek talepler Müjdat TELLİ'ye yöneltilir.
- Uygulamanın üçüncü taraf haklarını ihlal ettiği iddiasında bulunulursa, sorumluluk **münhasıran Müjdat TELLİ'ye aittir**.
- Apple, bu Sözleşme'nin **üçüncü taraf lehtarıdır** ve Sözleşme'yi size karşı uygulayabilir.

---

## 11. Uygulanacak Hukuk ve Yetkili Mahkeme

- Bu Sözleşme **Türkiye Cumhuriyeti** kanunlarına tabidir.
- Bu Sözleşme'den doğan uyuşmazlıklarda **İstanbul Mahkemeleri ve İcra Müdürlükleri** yetkilidir.
- Tüketici sıfatınız nedeniyle ikamet ettiğiniz yerdeki tüketici hakem heyeti veya tüketici mahkemesine başvurma hakkınız saklıdır.

---

## 12. Sözleşme Değişiklikleri

Bu Sözleşme'yi zaman zaman güncelleyebiliriz. Değişiklikler şu yollarla bildirilir:

- Uygulama içi bildirim,
- E-posta (kayıtlı e-posta adresinize),
- https://mujdattelli.github.io/frejya-legal/legal/eula.tr.html sayfasında güncel sürüm yayınlanır.

Önemli değişikliklerden sonra Uygulamayı kullanmaya devam etmeniz, **yeni sürümü kabul ettiğiniz** anlamına gelir. Kabul etmediğiniz takdirde hesabınızı silebilirsiniz.

---

## 13. İletişim

**Müjdat TELLİ**
E-posta: **iletisim@frejya.app**

Şikâyet, destek talepleri ve hukuki bildirimler bu adrese yapılır.

---

*Bu metin avukat onayı için taslak olarak hazırlanmıştır. Yürürlüğe girmeden önce hukuk danışmanı tarafından gözden geçirilmesi önerilir.*
