# UV-K5 Firmware Kullanım Kılavuzu

## 📋 Bu Firmware'in Özellikleri

Bu firmware, UV-K5 telsiz için özel olarak hazırlanmıştır ve aşağıdaki özellikleri içerir:

### ✅ **Aktif Özellikler**

#### **STOCK QUANSHENG ÖZELLİKLERİ:**
- **ENABLE_UART (1)** - Seri haberleşme
- **ENABLE_AIRCOPY (1)** - Havadan veri transferi
- **ENABLE_ALARM (1)** - Acil durum alarmı
- **ENABLE_DTMF_CALLING (1)** - DTMF çağrı sistemi
- **ENABLE_FLASHLIGHT (1)** - LED fener

#### **ÖZEL MODİFİKASYONLAR:**
- **ENABLE_BIG_FREQ (1)** - Büyük frekans gösterimi
- **ENABLE_SMALL_BOLD (1)** - Küçük kalın yazı
- **ENABLE_CUSTOM_MENU_LAYOUT (1)** - Özel menü düzeni
- **ENABLE_KEEP_MEM_NAME (1)** - Bellek isimlerini koruma
- **ENABLE_WIDE_RX (1)** - Geniş alıcı bant genişliği
- **ENABLE_NO_CODE_SCAN_TIMEOUT (1)** - Kod yok tarama zaman aşımı
- **ENABLE_AM_FIX (1)** - AM düzeltmesi
- **ENABLE_SQUELCH_MORE_SENSITIVE (1)** - Daha hassas squelch
- **ENABLE_FASTER_CHANNEL_SCAN (1)** - Hızlı kanal tarama
- **ENABLE_RSSI_BAR (1)** - RSSI çubuğu
- **ENABLE_AUDIO_BAR (1)** - Ses çubuğu
- **ENABLE_COPY_CHAN_TO_VFO (1)** - Kanalı VFO'ya kopyalama
- **ENABLE_SPECTRUM (1)** - Spektrum analizörü
- **ENABLE_SCAN_RANGES (1)** - Tarama aralıkları

#### **DERLEYİCİ SEÇENEKLERİ:**
- **ENABLE_LTO (1)** - Link time optimizasyonu

### ❌ **Pasif Özellikler**

#### **STOCK QUANSHENG ÖZELLİKLERİ:**
- **ENABLE_FMRADIO (0)** - FM radyo
- **ENABLE_NOAA (0)** - NOAA hava durumu
- **ENABLE_VOICE (0)** - Ses özellikleri
- **ENABLE_VOX (0)** - Sesle tetikleme
- **ENABLE_TX1750 (0)** - 1750 Hz ton
- **ENABLE_PWRON_PASSWORD (0)** - Güç açılış şifresi

#### **ÖZEL MODİFİKASYONLAR:**
- **ENABLE_TX_WHEN_AM (0)** - AM modunda verici
- **ENABLE_F_CAL_MENU (0)** - Frekans kalibrasyon menüsü
- **ENABLE_CTCSS_TAIL_PHASE_SHIFT (0)** - CTCSS kuyruk faz kayması
- **ENABLE_BOOT_BEEPS (0)** - Açılış sesleri
- **ENABLE_SHOW_CHARGE_LEVEL (0)** - Şarj seviyesi gösterimi
- **ENABLE_REVERSE_BAT_SYMBOL (0)** - Ters batarya sembolü
- **ENABLE_REDUCE_LOW_MID_TX_POWER (0)** - Düşük/orta güç azaltma
- **ENABLE_BYP_RAW_DEMODULATORS (0)** - Ham demodülatörler
- **ENABLE_BLMIN_TMP_OFF (0)** - Geçici arka ışık kapatma

#### **HATA AYIKLAMA:**
- **ENABLE_AM_FIX_SHOW_DATA (0)** - AM düzeltme veri gösterimi
- **ENABLE_AGC_SHOW_DATA (0)** - AGC veri gösterimi
- **ENABLE_UART_RW_BK_REGS (0)** - UART BK register okuma/yazma

#### **DERLEYİCİ SEÇENEKLERİ:**
- **ENABLE_CLANG (0)** - Clang derleyici
- **ENABLE_SWD (0)** - SWD debug
- **ENABLE_OVERLAY (0)** - Overlay sistemi

UV-K5 bellek yetersizliğinden dolayı bazı özellikler kısıtlanmıştır.

---

## 🚀 **Kurulum Talimatları**

### **1. Firmware Yükleme**

#### **Gerekli Yazılım:**
- **K5prog_IJV_V3** uygulaması (UV-K5 firmware yükleyici)

#### **Detaylı Yükleme Adımları:**
1. **Telsizi tamamen kapatın.**
2. **USB programlama kablosunu** bilgisayara ve telsize takın.
3. **K5prog_IJV_V3** programını başlatın.
4. Üstteki **Serial port** menüsünden, bağlı olan portu (ör: COM4) seçin.
5. **Serial speed** kısmında **38400 - k5/k6** seçili olmalı.
6. Programda `'COM4' opened at 38400 Baud` mesajını görmelisiniz.
7. **Telsizi programlama moduna alın:**
   - Telsiz kapalıyken **PTT (büyük yan tuş) tuşuna** basılı tutun.
   - Basılıyken telsizi açın.
   - Telsiz ekranı boş kalabilir veya programlama modunda olduğunu gösteren bir belirti olmayabilir (bu normaldir).
8. **Write Firmware** butonuna tıklayın.
9. Açılan pencerede **firmware.packed.bin** dosyasını seçin ve **Aç** butonuna tıklayın.
10. Yükleme işlemi otomatik olarak başlayacaktır. Programda ilerleme ve mesajları takip edin.
11. Yükleme tamamlandığında **"Write Flash Complete"** mesajını göreceksiniz.
12. Telsizi kapatıp tekrar açın.

#### **Önemli Notlar:**
- Yükleme sırasında **telsizi kapatmayın** ve **USB bağlantısını kesmeyin**.
- Yükleme **2-3 dakika** sürebilir.
- Hatalı yükleme veya bağlantı kopması durumunda işlemi baştan başlatın.
- Yanlış port seçerseniz program hata verebilir, doğru COM portunu seçtiğinizden emin olun.
- Yükleme sırasında kanal ve ayarlarınız silinebilir, isterseniz "Read Configuration" ile yedek alabilirsiniz.

### **2. İlk Açılış**
- Telsiz normal şekilde açılacak
- Tüm ayarlar varsayılan değerlerde
- Kanal listesi boş olacak

### **3. Fabrika Ayarlarına Sıfırlama (ÖNEMLİ!)**
**Tüm özelliklerin düzgün çalışması için:**
1. **Telsizi kapatın**
2. **Yan tuş 1 + PTT tuşuna** aynı anda basılı tutun
3. **Telsizi açın** (RELEASE ALL KEY yazısını görene kadar tuşları bırakmayın)
4. **Özel menü** açılacak
5. **RESET** menüsüne gidin
6. **ALL** seçeneğini seçin
7. **Fabrika ayarlarına** sıfırlanacak
8. **Telsizi yeniden açın**

**Bu işlem tüm özelliklerin aktif olmasını sağlar!**

---

## 🎛️ **Temel Kullanım**

### **Frekans Ayarlama**
- **VFO Modu:** Sayı tuşları ile frekans girin
- **Kanal Modu:** Önceden kaydedilmiş kanallar
- **Adım:** 12.5 kHz, 25 kHz, 50 kHz seçenekleri

### **Verici Kullanımı**
- **PTT:** Push-to-Talk düğmesi ile konuşma
- **Güç:** Düşük/Orta/Yüksek seçimi
- **Mod:** FM, AM seçenekleri

### **Alıcı Kullanımı**
- **Squelch:** Otomatik (hassas)
- **Bant Genişliği:** Geniş (daha iyi ses)
- **Ses:** Ayarlanabilir seviye

---

## 📡 **Özel Özellikler**

### **1. AIRCOPY - Havadan Veri Transferi**

#### **Erişim:**
- **Yan tuş 2'ye basılı tutarak** telsizi açın
- Ekranda "AIR COPY(RDY)" görünür

#### **Kullanım:**
```
Gönderen Cihaz:
1. Yan tuş 2 + açılış
2. Frekans gir (örn: 410025)
3. MENU tuşuna basın
4. "SND:0" görünür

Alıcı Cihaz:
1. Yan tuş 2 + açılış
2. Aynı frekansı gir
3. EXIT tuşuna basın
4. "RCV:0 E:0" görünür
```

#### **Transfer Edilen Veriler:**
- Kanal listesi ve frekanslar
- Kanal isimleri
- CTCSS/DCS tonları
- Güç ayarları
- Diğer kanal parametreleri

### **2. Spektrum Analizörü**

#### **Aktif Etme:**
- **Yan fonksiyon olarak** atanabilir
- Menüden yan fonksiyon ayarlarına gidip "SPECTRUM" seçeneğini seçin

#### **Kullanım:**
- **Frekans Aralığı:** 18-1300 MHz
- **Tarama Hızı:** Optimize edilmiş
- **Hassasiyet:** Yüksek
- **Adım:** 10 kHz

#### **Yorumlama:**
- **Yüksek çubuklar:** Güçlü sinyaller
- **Düşük çubuklar:** Zayıf sinyaller
- **Boş alanlar:** Sinyal yok
- **Sürekli çubuklar:** Parazit

### **3. Alarm Sistemi**

#### **Erişim:**
- **Menüde "AlarmT" seçeneği**
- Menü listesinde bulunur

#### **Alt Menüler:**
- **SITE:** Konum bazlı alarm
- **TONE:** Sesli ton alarmı

#### **Kullanım:**
- **Alarm Gönderme:** Alarm tuşu veya menüden
- **Alarm Alma:** Otomatik uyarı
- **SOS Sinyali:** Acil yardım çağrısı

### **4. DTMF Çağrı Sistemi**

#### **Kullanım:**
- **Kod Formatı:** 0-9, A-D, *, # karakterleri
- **Çağrı Gönderme:** DTMF kodları ile
- **Çağrı Alma:** Otomatik yanıt
- **Grup Çağrıları:** Desteklenir

#### **Özellikler:**
- 3 haneli kod sistemi
- Otomatik yanıt
- Grup çağrıları
- Acil durum çağrıları
- Kişi listesi (16 kişi)

---

## 🎨 **Görsel Özellikler**

### **Büyük Frekans Gösterimi**
- Frekans büyük ve net görünür
- Daha okunabilir ekran
- Hızlı frekans kontrolü

### **Küçük Kalın Yazı**
- Küçük yazılar kalın gösterilir
- Daha iyi okunabilirlik
- Kontrast artışı

### **RSSI Çubuğu**
- Sinyal gücü göstergesi
- Çubuk grafik şeklinde
- Anten yönlendirme için

### **Ses Çubuğu**
- Ses seviyesi göstergesi
- Mikrofon ayarlama için
- Ses kalitesi kontrolü

---

## 🔧 **Menü Navigasyonu**

### **Ana Menü Erişimi**
- **FUNC + 0:** İlk menü
- **Yukarı/Aşağı:** Menü gezinme
- **MENU:** Seçim onaylama
- **EXIT:** Geri dönüş

### **Önemli Menü Öğeleri**
1. **Step:** Frekans adımı
2. **TxPwr:** Verici gücü
3. **RxDCS:** Alıcı DCS kodu
4. **RxCTCS:** Alıcı CTCSS tonu
5. **TxDCS:** Verici DCS kodu
6. **TxCTCS:** Verici CTCSS tonu
7. **AlarmT:** Alarm ayarları (40. sırada)
8. **Reset:** Sıfırlama menüsü (VFO, ALL seçenekleri)

### **Reset Menü Seçenekleri**
- **VFO:** Sadece VFO ayarlarını sıfırlar
- **ALL:** Tüm ayarları fabrika ayarlarına sıfırlar

---

## 📱 **Pratik Kullanım Senaryoları**

### **Günlük Kullanım**
1. **Açılış:** Normal açılış
2. **Frekans:** VFO veya kanal seçimi
3. **İletişim:** PTT ile konuşma
4. **Tarama:** Otomatik kanal tarama

### **Profesyonel Kullanım**
1. **Spektrum Analizi:** Yan fonksiyon olarak atanmış spektrum analizörü
2. **Frekans Keşfi:** Spektrum ile sinyal arama
3. **Kanal Programlama:** AIRCOPY ile veri transferi
4. **Grup İletişimi:** DTMF çağrıları

### **Acil Durum Kullanımı**
1. **Alarm:** Alarm menüsünden SOS
2. **Yüksek Güç:** Maksimum menzil
3. **Geniş Bant:** En iyi sinyal kalitesi
4. **Fener:** Acil aydınlatma

---

## ⚠️ **Önemli Notlar**

### **Güvenlik**
- **Lisans:** Amatör telsiz lisansı gerekli
- **Frekans:** İzin verilen frekansları kullanın
- **Güç:** Yasal güç sınırlarına uyun

### **Bakım**
- **Pil:** Düzenli şarj
- **Anten:** Temiz ve sağlam
- **Firmware:** Güncel tutun

### **Sorun Giderme**
- **Sinyal Yok:** Anten kontrolü
- **Ses Yok:** Ses ayarları
- **Pil Sorunu:** Şarj kontrolü
- **Firmware Hatası:** Yeniden yükleme

---

## 📞 **Destek**

Bu firmware ücretsiz olarak paylaşılmaktadır. Herkes istediği gibi kullanabilir, değiştirebilir ve dağıtabilir. Sorumluluk kullanıcıya aittir.

### **Özellikler:**
- ✅ UART Haberleşme
- ✅ AIRCOPY Veri Transferi
- ✅ DTMF Çağrı Sistemi
- ✅ Alarm Sistemi
- ✅ Fener
- ✅ Büyük Frekans Gösterimi
- ✅ Spektrum Analizörü (Yan fonksiyon olarak)
- ✅ Gelişmiş Squelch
- ✅ Hızlı Tarama
- ✅ Görsel Göstergeler

Bu kılavuz, firmware'inizin tüm özelliklerini ve kullanım yöntemlerini açıklamaktadır.

---

## ⚖️ **Yasal Uyarı ve Sorumluluk Reddi**

### **Eğitim ve Araştırma Amaçlı Kullanım**
Bu firmware **sadece eğitim ve araştırma amaçlı** olarak geliştirilmiştir. Kullanıcılar bu firmware'i kendi sorumlulukları altında kullanırlar.

**ÖNEMLİ:** Bu firmware ticari, profesyonel veya ticari amaçlı kullanım için tasarlanmamıştır. Sadece eğitim, öğrenme ve kişisel araştırma amaçlıdır.

### **Yasal Sorumluluk Reddi**
- **Firmware Geliştiricisi:** Bu firmware'in kullanımından doğabilecek herhangi bir zarar, hasar, veri kaybı, donanım arızası, yasal sorun veya başka herhangi bir sorundan kesinlikle sorumlu değildir
- **Kullanıcı Sorumluluğu:** Firmware'i kullanan kişi, tüm yasal, teknik ve finansal sorumlulukları tamamen kabul eder
- **Yasal Uyumluluk:** Kullanıcı, bulunduğu ülkenin telsiz yasalarına, frekans düzenlemelerine ve iletişim kurallarına uygun kullanım sağlamakla yükümlüdür
- **Lisans Gereksinimleri:** Amatör telsiz lisansı, frekans kullanım izni veya diğer yasal gereksinimler gerekebilir. Kullanıcı bu gereksinimleri kontrol etmekle ve sağlamakla yükümlüdür
- **Yasal İhlal:** Bu firmware'in kullanımından doğabilecek yasal ihlallerden kullanıcı tamamen sorumludur

### **Teknik Uyarılar ve Riskler**
- **Donanım Hasarı:** Yanlış kullanım, yanlış programlama veya teknik hatalar donanım hasarına, kalıcı arızaya veya cihazın tamamen bozulmasına neden olabilir
- **Veri Kaybı:** Firmware güncellemesi sırasında kanal verileri, ayarlar, kişisel veriler ve diğer tüm bilgiler kalıcı olarak kaybolabilir
- **Performans Sorunları:** Bu firmware orijinal firmware'den farklı performans gösterebilir, beklenmeyen davranışlar sergileyebilir veya kararsız çalışabilir
- **Güvenlik Riskleri:** Firmware güvenlik açıkları içerebilir, veri sızıntısına neden olabilir veya güvenlik riskleri oluşturabilir
- **Uyumluluk Sorunları:** Diğer cihazlarla, yazılımlarla veya sistemlerle uyumluluk sorunları yaşanabilir
- **Garanti Kaybı:** Bu firmware kullanımı cihazın orijinal garantisini geçersiz kılabilir

### **Kullanım Koşulları ve Sözleşme**
Bu firmware'i indirerek, kullanarak veya dağıtarak aşağıdaki koşulları kabul etmiş olursunuz:

#### **Kullanıcı Yükümlülükleri:**
- Firmware'i tamamen kendi riskinizle kullanırsınız
- Geliştirici hiçbir zarar, hasar veya sorundan sorumlu değildir
- Yerel, ulusal ve uluslararası yasalara uygun kullanım sağlamakla yükümlüsünüz
- Teknik bilgi, deneyim ve uzmanlık gereklidir
- Firmware'i değiştirirseniz, değişikliklerden tamamen sorumlusunuz
- Firmware'i başkalarıyla paylaşırsanız, onları da bu uyarılar hakkında bilgilendirmekle yükümlüsünüz

#### **Yasaklanan Kullanımlar:**
- Ticari veya ticari amaçlı kullanım
- Profesyonel telsiz sistemlerinde kullanım
- Acil durum iletişim sistemlerinde kullanım
- Yasal olmayan frekanslarda veya güç seviyelerinde kullanım
- Başkalarının iletişimini engelleyecek şekilde kullanım
- Yasal düzenlemelere aykırı kullanım

#### **Sorumluluk Sınırlaması:**
- Geliştirici, bu firmware'in kullanımından doğabilecek herhangi bir zarardan sorumlu değildir
- Kullanıcı, tüm riskleri ve sorumlulukları kabul eder
- Firmware "olduğu gibi" sağlanır, hiçbir garanti verilmez
- Geliştirici, firmware'in uygunluğu, güvenliği veya hatasız çalışması hakkında hiçbir taahhüt vermez

### **Son Uyarı ve Önemli Not**
**Bu firmware sadece eğitim ve araştırma amaçlıdır. Ticari kullanım için uygun değildir. Kullanmadan önce tüm yasal gereksinimleri kontrol edin ve gerekli izinleri alın.**

**UYARI:** Bu firmware'i kullanarak tüm riskleri kabul etmiş olursunuz. Geliştirici hiçbir sorumluluk kabul etmez. 
