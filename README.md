# UV-K5 Firmware Kullanım Kılavuzu

## Genel Bakış

Bu kılavuz, UV-K5 telsiz cihazı için özel firmware'in kullanımını açıklar. Firmware, telsiz cihazının menü sistemini, özelliklerini ve işlevlerini genişletir.

## Önemli Uyarılar

### Yasal Uyarı
- Bu firmware sadece eğitim ve araştırma amaçlıdır
- Yerel radyo yönetmeliklerine uygun kullanım kullanıcının sorumluluğundadır
- Yasadışı frekanslarda yayın yapmak kesinlikle yasaktır
- Firmware kullanımından doğacak tüm sorumluluk kullanıcıya aittir

### Teknik Uyarılar
- Firmware yükleme işlemi risklidir, cihaz zarar görebilir
- Yedekleme yapmadan firmware yüklemeyin
- Sadece UV-K5 cihazı için tasarlanmıştır
- Yanlış firmware yükleme cihazı kullanılamaz hale getirebilir

## Kurulum

### Gereksinimler
- UV-K5 telsiz cihazı
- USB-C kablo
- K5prog_IJV_V3 uygulaması
- Firmware dosyası (.bin uzantılı)

### Kurulum Adımları

1. **Cihazı Programlama Moduna Alın**
   - Cihazı kapatın
   - PTT tuşunu basılı tutun
   - Açma tuşuna basın ve PTT'yi bırakın
   - Ekranda "PROG" yazısı görünmelidir

2. **K5prog_IJV_V3 Uygulamasını Açın**
   - Uygulamayı yönetici olarak çalıştırın
   - Port seçin (genellikle COM3 veya COM4)
   - Hız: 115200 baud
   - "Connect" butonuna basın

3. **Firmware Yükleyin**
   - "Open File" ile firmware dosyasını seçin
   - "Program" butonuna basın
   - İşlem tamamlanana kadar bekleyin
   - Cihazı yeniden başlatın

### **Fabrika Ayarlarına Sıfırlama (ÖNEMLİ!)**
**Tüm özelliklerin düzgün çalışması için:**
1. **Telsizi kapatın**
2. **Yan tuş 1 + PTT tuşuna** aynı anda basılı tutun
3. **Telsizi açın** (RELEASE ALL KEY yazısını görene kadar tuşları bırakmayın)
4. **Özel menü** açılacak
5. **RESET** menüsüne gidin
6. **ALL** seçeneğini seçin
7. **Fabrika ayarlarına** sıfırlanacak
8. **Telsizi yeniden açın**

## Menü Sistemi

### Ana Menü Başlıkları

#### Temel Ayarlar
- **Step**: Frekans adımı (2.5kHz, 5kHz, 6.25kHz, 10kHz, 12.5kHz, 25kHz)
- **TxPwr**: Verici gücü (LOW, MID, HIGH)
- **RxDCS**: Alıcı DCS kodu (OFF, D001N-D754N, D001I-D754I)
- **RxCTCS**: Alıcı CTCSS tonu (OFF, 67.0Hz-254.1Hz)
- **TxDCS**: Verici DCS kodu (OFF, D001N-D754N, D001I-D754I)
- **TxCTCS**: Verici CTCSS tonu (OFF, 67.0Hz-254.1Hz)
- **TxODir**: Verici offset yönü (OFF, +, -)
- **TxOffs**: Verici offset frekansı (0.00000-69.99999 MHz)
- **W/N**: Kanal bant genişliği (WIDE, NARROW)
- **Scramb**: Scrambler (OFF, 2600Hz-3500Hz)
- **BusyCL**: Meşgul kanal kilidi (OFF, ON)
- **Compnd**: Compander (OFF, TX, RX, TX/RX)
- **Demodu**: Modülasyon tipi (FM, AM)

#### Kanal Yönetimi
- **ScAdd1**: Tarama listesi 1'e ekleme (OFF, ON)
- **ScAdd2**: Tarama listesi 2'ye ekleme (OFF, ON)
- **ChSave**: Kanal kaydetme (0-999)
- **ChDele**: Kanal silme (0-999)
- **ChName**: Kanal adı düzenleme (0-999)

#### Tarama Ayarları
- **SList**: Tarama listesi (LIST1, LIST2, ALL)
- **SList1**: Tarama listesi 1 ayarları
- **SList2**: Tarama listesi 2 ayarları
- **ScnRev**: Tarama devam modu (TIMEOUT, CARRIER, STOP)

#### Yan Tuş Fonksiyonları
- **F1Shrt**: F1 kısa basma fonksiyonu
- **F1Long**: F1 uzun basma fonksiyonu
- **F2Shrt**: F2 kısa basma fonksiyonu
- **F2Long**: F2 uzun basma fonksiyonu
- **M Long**: M uzun basma fonksiyonu

#### Sistem Ayarları
- **KeyLck**: Otomatik tuş kilidi (OFF, AUTO)
- **TxTOut**: Verici zaman aşımı (30sec-15min)
- **BatSav**: Pil tasarrufu (OFF, 1:1, 1:2, 1:3, 1:4)
- **Mic**: Mikrofon hassasiyeti (0-4)
- **ChDisp**: Kanal görüntüleme (FREQ, CHANNEL NUMBER, NAME, NAME+FREQ)
- **POnMsg**: Açılış mesajı (FULL, MESSAGE, VOLTAGE, NONE)
- **BatTxt**: Pil metni (NONE, VOLTAGE, PERCENT)
- **BackLt**: Arka ışık (OFF, 5sec, 10sec, 20sec, 1min, 2min, 4min, ON)
- **BLMin**: Arka ışık minimum (0-9)
- **BLMax**: Arka ışık maksimum (1-10)
- **BltTRX**: Arka ışık TX/RX (OFF, TX, RX, TX/RX)
- **Beep**: Bip sesi (OFF, ON)

#### Ses ve İletişim
- **Voice**: Sesli menü (OFF, CHI, ENG)
- **Roger**: Roger beep (OFF, ROGER, MDC)
- **STE**: Tail tone eliminasyonu (OFF, ON)
- **RP STE**: Repeater tail tone eliminasyonu (OFF, 1-10*100ms)

#### DTMF Ayarları
- **ANI ID**: ANI DTMF ID (8 karakter)
- **UPCode**: Yukarı kod (16 karakter)
- **DWCode**: Aşağı kod (16 karakter)
- **PTT ID**: PTT ID modu (OFF, UP CODE, DOWN CODE, UP+DOWN CODE, APOLLO QUINDAR)
- **D ST**: DTMF side tone (OFF, ON)
- **D Resp**: DTMF yanıt (DO NOTHING, RING, REPLY, BOTH)
- **D Hold**: DTMF tutma süresi (5-60 saniye)
- **D Prel**: DTMF ön yükleme (3-99*10ms)
- **D Decd**: DTMF çözme (OFF, ON)
- **D List**: DTMF liste (1-16)
- **D Live**: Canlı DTMF çözücü (OFF, ON)

#### Özel Özellikler
- **AM Fix**: AM düzeltme (OFF, ON)
- **VOX**: Sesle iletim (OFF, 1-10)
- **BatVol**: Pil voltajı görüntüleme
- **RxMode**: Alıcı modu (MAIN ONLY, DUAL RX RESPOND, CROSS BAND, MAIN TX DUAL RX)
- **Sql**: Squelch seviyesi (0-9)

### Gizli Menü (Boot Modunda Erişim)

Açılış sırasında PTT + yan tuş basılı tutularak erişilir:

- **F Lock**: Frekans kilidi
  - DEFAULT+137-174/400-470
  - FCC HAM 144-148/420-450
  - CE HAM 144-146/430-440
  - GB HAM 144-148/430-440
  - 137-174/400-430
  - 137-174/400-438
  - DISABLE ALL
  - UNLOCK ALL

- **Tx 200**: 200MHz verici (OFF, ON)
- **Tx 350**: 350MHz verici (OFF, ON)
- **Tx 500**: 500MHz verici (OFF, ON)
- **350 En**: 350MHz etkinleştirme (OFF, ON)
- **ScraEn**: Scrambler etkinleştirme (OFF, ON)
- **FrCali**: Frekans kalibrasyonu (-50 ile +50)
- **BatCal**: Pil kalibrasyonu (1600-2200)
- **BatTyp**: Pil tipi (1600mAh, 2200mAh)
- **Reset**: Sıfırlama (VFO, ALL)

### Yan Tuş Fonksiyonları

Aşağıdaki fonksiyonlar yan tuşlara atanabilir:

- **NONE**: Hiçbir işlem
- **FLASHLIGHT**: El feneri
- **POWER**: Güç açma/kapama
- **MONITOR**: Monitör modu
- **SCAN**: Tarama başlatma/durdurma
- **VOX**: VOX açma/kapama
- **ALARM**: Alarm başlatma
- **FM RADIO**: FM radyo açma/kapama
- **1750HZ**: 1750Hz ton gönderme
- **LOCK KEYPAD**: Tuş kilidi
- **SWITCH VFO**: VFO değiştirme
- **VFO/MR**: VFO/MR modu değiştirme
- **SWITCH DEMODUL**: Demodülasyon değiştirme
- **BLMIN TMP OFF**: Arka ışık geçici kapatma
- **SPECTRUM**: Spektrum analizörü

## Özel Özellikler

### Spektrum Analizörü
- **Erişim**: Yan tuş fonksiyonlarına atanabilir
- **Özellikler**:
  - Frekans aralığı: 18-1300 MHz
  - Adım sayısı: 64, 128, 256, 512
  - Tarama adımı: 2.5kHz - 1MHz
  - RSSI tetik seviyesi: -130 ile -50 dBm arası
  - Bant genişliği: 25kHz, 12.5kHz, 6.25kHz
  - Modülasyon: FM, AM
  - AGC kilidi
  - Kara liste
  - Tepe bulma
  - Frekans girişi

### AIRCOPY (Gizli Mod)
- **Erişim**: Açılış sırasında PTT + yan2 tuşu
- **İşlev**: EEPROM üzerinden veri transferi
- **Kullanım**: İki cihaz arasında kanal ve ayar kopyalama

### FM Radyo
- **Erişim**: Yan tuş fonksiyonlarına atanabilir
- **Özellikler**:
  - Frekans aralığı: 64-108 MHz
  - Otomatik tarama
  - Kanal kaydetme (20 kanal)
  - MR modu
  - Ses çıkışı

### DTMF Çağrı Sistemi
- **Özellikler**:
  - 16 kişilik rehber
  - ANI ID
  - PTT ID
  - Otomatik yanıt
  - Canlı çözücü
  - Side tone

### Alarm Sistemi
- **Modlar**: SITE (konum), TONE (ses)
- **Erişim**: Normal menüde "AlarmT" başlığı

## Kullanım İpuçları

### Menü Navigasyonu
- **MENU**: Menüye giriş
- **▲/▼**: Menüde gezinme
- **EXIT**: Menüden çıkış
- **0-9**: Değer girişi
- ***/**: Alt menüye giriş

### Frekans Girişi
- Menüde frekans girerken nokta otomatik eklenir
- MHz cinsinden giriş yapın (örn: 145500 = 145.500 MHz)

### Kanal Yönetimi
- Kanal kaydetme: MENU → ChSave → kanal numarası
- Kanal silme: MENU → ChDele → kanal numarası
- Kanal adı: MENU → ChName → kanal numarası → ad girişi

### Tarama
- Tarama listesi oluşturma: SList1/SList2 menülerinden
- Tarama başlatma: Yan tuş fonksiyonlarından SCAN
- Tarama durdurma: EXIT tuşu

### Spektrum Analizörü
- Frekans değiştirme: ▲/▼ tuşları
- Adım değiştirme: MENU + ▲/▼
- Tetik seviyesi: EXIT + ▲/▼
- Bant genişliği: */ + ▲/▼

## Sorun Giderme

### Yaygın Sorunlar
1. **Cihaz açılmıyor**: Firmware yükleme hatası, orijinal firmware'e geri dönün
2. **Menü çalışmıyor**: Tuş kilidi aktif, EXIT tuşuna basın
3. **Frekans ayarlanamıyor**: F Lock aktif, gizli menüden UNLOCK ALL seçin
4. **Pil göstergesi yanlış**: BatCal menüsünden kalibrasyon yapın

### Güvenlik
- Firmware yüklemeden önce mutlaka yedek alın
- Sadece güvenilir kaynaklardan firmware indirin
- Yükleme sırasında cihazı kapatmayın
- Hata durumunda orijinal firmware'e geri dönün

## Teknik Destek

Bu firmware açık kaynak kodludur ve topluluk tarafından geliştirilmektedir. Sorunlar için:
- GitHub repository'sini kontrol edin
- Topluluk forumlarını ziyaret edin
- Hata raporları için issue açın

---

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
