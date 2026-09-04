# LuminaTrans

Her pencerenin üstünde duran çeviri paneli. Ekranın sağ altında, saatin hemen üstünde küçük bir bakır **balon** durur; tıklayınca panel açılır, tekrar tıklayınca kapanır. Sen başka programdayken gelen çeviriler balonda kırmızı sayaçla birikir, çeviri sürerken balon nabız atar. Sağ tık ayarları açar.

Telegram, Discord, tarayıcı, oyun sohbeti… hangi programda olursan ol:

| Kısayol | Ne yapar |
|---|---|
| `Ctrl+Alt+Enter` | Yazı alanında yazdığın metni çevirir ve **yerine koyar** (seçtiğin tonla). |
| `Ctrl+Alt+T` | Seçili metni çevirir, sonuç **Gelen** sekmesine düşer; sen uygulamanda kalırsın. |
| `Ctrl+Alt+R` | Ekranda bir bölge çizersin, içindeki mesajları okuyup çevirir (seçilemeyen yazılar için). |
| `Ctrl+Alt+V` | **Konuş:** bir kez bas, konuş, tekrar bas. Söylediğin yazıya dökülür, çevrilir; panelden Yapıştır ya da `Ctrl+0`. Ayarlar'dan "beklemeden yapıştır" açılabilir. |
| `Ctrl+Alt+L` | **Dinle:** hoparlörden ne geliyorsa (sesli mesaj, video, arama) cümle cümle yazıya dökülüp çevrilir, Gelen sekmesinde canlı akar. Tekrar bas: durur. 2 dakika konuşma olmazsa kendi durur. |
| `Ctrl+Alt+O` | **Ekran altyazısı:** ekranda bir bölge çiz (oyun diyaloğu, gömülü altyazı); yazı değiştikçe Windows OCR ile okunur, çevrilir, altyazı çubuğunda görünür. |
| `Ctrl+Alt+Space` | Paneli göster / gizle. |

## Dinleme ve altyazı çubuğu

Dinle ve Ekran altyazısı açıkken ekranın altında saydam bir **altyazı çubuğu** belirir: büyük yazı çeviri, altında küçük yazı orijinal. Tıklamaları geçirir, altındaki videoyu ya da oyunu engellemez. Ayarlar → Altyazı çubuğu'ndan kapatılabilir, boyutu değişir, orijinal satırı gizlenir.

Bir dinleme oturumu bittiğinde karttaki **Özetle** düğmesi konuşulanları maddeler, senden istenenleri ve kararları çıkarır. **Oku** düğmesi çevirileri sesli okur.

## Dosya ve belge çevirisi (Pro)

- **Belgeler, düzen korunarak:** PDF, Word (docx), PowerPoint (pptx) ve Excel (xlsx) dosyasını panele bırak ya da Gelen → **Dosya çevir** ile seç. PDF'de metin kendi kutusunun içine yeniden yazılır, görseller ve sayfalar aynen kalır; Word'de yazı tipi, tablo, üst ve alt bilgi korunur; PowerPoint'te her slayt ve not; Excel'de sadece metin hücreleri çevrilir, sayı ve formüller dokunulmaz. Çıktı `Belgeler\LuminaTrans` içine `ad.en.pdf` gibi yazılır, çevrilen satırlar kartta da görünür.
- **Çıktıyı sen seç** (Ayarlar → Belge çevirisi): aynı düzen, ya da başlık ve paragraflarla yeniden kurulmuş okunaklı nüsha (görseller okuma sırasında; Word, PDF ya da ikisi), ya da ikisi birden; isteğe bağlı çift dilli (her paragrafın altında orijinal); Hızlı ya da Dikkatli çeviri (önceki paragraf bağlam, tutarlı terimler). Taranmış PDF'ler Windows OCR ile okunur.
- **Ses ve video:** mp3, mp4, m4a, ogg, webm, mkv… ya da metin/altyazı (txt, md, srt, vtt). Çıktılar: `ad.en.srt` (çeviri), `ad.en+orig.srt` (üstte çeviri, altta orijinal), `ad.orig.srt`, `ad.en.txt` (yan yana).
- **Düzelt:** Yabancı dilde kendin yazdığın metni çevirmeden, anadili gibi düzeltir (dil bilgisi, yazım, doğal ifade); Yaz sekmesinde Çevir'in yanındaki düğme.
- Panele ekran görüntüsü yapıştır (Ctrl+V): ekran bölgesi gibi okunup çevrilir (ücretsiz).
- **Gelen Kutusu** klasörü: `Belgeler\LuminaTrans\Gelen Kutusu` içine attığın her ses, video veya altyazı dosyası otomatik çevrilir.
- İzlediğin bir videoyu çevirmek için indirmek gerekmez: video oynarken **Ctrl+Alt+L** (Dinle) canlı altyazı verir.

## Diğer

- **Sözlük** (Ayarlar): `kaynak = hedef` satırları; isimler ve terimler her çeviride sabit kalır.
- **Pano izleme** (Ayarlar, varsayılan kapalı): kopyaladığın her metin Gelen'e çevrilmiş düşer.
- **Sesli okuma** (Ayarlar): gelen çevirileri ya da kendi konuşmanın çevirisini Microsoft'un doğal Türkçe/İngilizce sesiyle okur (internet ister).
- Çıktılarda uzun tire, "İşte çeviri:" gibi yapay zekâ izleri temizlenir; çeviri insan yazmış gibi durur.

Panelin içinde: `Ctrl+Enter` çevirir, `Ctrl+Shift+Enter` çevirip son kullandığın pencereye yapıştırır, `Ctrl+0` hızlı çeviriyi, `Ctrl+1/2/3` ilgili tonu yapıştırır, `Esc` paneli gizler.

Her çeviri iki aşamada gelir: önce **hızlı çeviri** (~0,3 s), arkasından üç ton: **Kurumsal**, **Doğal**, **Duygusal**; yanında bağlam-ton analizi ve kültürel not (~4 s). Yerinde değiştirme Doğal tondayken hızlı şeridi kullanır, metin yarım saniyede değişir.

Türkçe çıktıda sabit kurallar var: sohbet, oyun, arkadaş ortamında **sen**; iş dilinde **siz** ve "Yılmaz Bey" tarzı hitap; oyun argosu Türk oyuncuların yazdığı gibi kalır ("gg", "clutchladık"); kaynakta olmayan emoji veya nezaket eklenmez.

Küçük modellerin kaçırdığı bir şey daha var: yabancı kelimelere gelen eklerde ünlü uyumu ("troll'liği" yerine "trollüğü"). Bunu model yerine [trfix.py](trfix.py) içindeki kural tabanlı düzeltici yapar; kaynağı TDK Yazım Kuralları (ek, kelimenin **söylenişine** göre gelir: alkol/alkolü; özel ad değilse kesme işareti konmaz). Tablo yaygın oyun ve sohbet alıntı kelimelerini kapsar; yeni kelime eklemek için o dosyadaki listeye satır eklemek yeterli.

## Kurulum (kurulum paketiyle)

`Output\LuminaTrans-Setup-0.2.0.exe` dosyasını çalıştır. İlk ekranda dil seç (Türkçe / English / Español); arayüz o dilde açılır, "benim dilim" o olur (karşı dil İngilizce, İngilizce seçene Türkçe). İlk açılışta Kurulum sekmesi Ollama'yı kurdurur ve modeli indirtir (9,6 GB, bir kez). Ayrıntı ve yayınlama: [RELEASE.md](RELEASE.md), İngilizce tanıtım: [README.en.md](README.en.md).

## Kurulum (kaynak koddan)

1. Python 3.10+ kurulu olsun.
2. `LuminaTrans.bat` dosyasına çift tıkla. İlk açılışta bağımlılıkları kurar, sonra paneli açar.
3. Varsayılan motor **Ollama** (bilgisayarında çalışan ücretsiz model). Ollama kurulu ve model indirilmişse panel doğrudan "Hazır" der. Değilse Ayarlar sekmesinde **Yeni model indir** kutusuna model adını yazıp İndir de.

Sistem tepsisinde bir simge belirir: sağ tık ile göster/gizle, ekrandan çevir, çıkış.

## Çeviri motorları

Ayarlar → Sağlayıcı. Hepsi aynı LuminaTrans promptunu kullanır, sadece beyin değişir.

| Sağlayıcı | Ücret | Sınır | Gizlilik | Ne zaman |
|---|---|---|---|---|
| **Ollama** (yerel) | Sıfır | Yok | Tam, metin bilgisayardan çıkmaz | Varsayılan. Günlük sohbet çevirisi için yeterli, internet gerekmez. |
| **Google Gemini** | Sıfır, kart yok | ~15 istek/dk, ~1.500 istek/gün | Zayıf: ücretsiz katmanda metinler model eğitiminde kullanılabilir | Daha iyi nüans istediğinde, gizlilik önemli değilse. |
| **Groq** | Sıfır, kart yok | 6K token/dk, model başına 1.000–14.400 istek/gün | Orta | Hızlı bulut alternatifi. |
| **Cerebras** | Sıfır, kart yok | 5 istek/dk, 1M token/gün | Orta | Büyük model (gpt-oss-120b) ücretsiz. |
| **OpenRouter** | Sıfır | 50 istek/gün | Değişken | Denemelik. |
| **Özel uç nokta** | – | – | – | LM Studio, llama.cpp server, Jan, vLLM. |
| **Claude** | Ücretli | Yok | İyi | En ince nüans, en iyi Türkçe. |

Ollama modeli önerisi (bu bilgisayarda ölçüldü, ayrıntı [RESEARCH.md](RESEARCH.md)):

| Model | Ne zaman | VRAM | Hız |
|---|---|---|---|
| `gemma4:e4b` (varsayılan) | Günlük kullanım, en iyi denge | ~5 GB | ~110 tok/s, tam yanıt ~6 s |
| `gemma4:e2b` | En az yer, eski/zayıf kart | ~2 GB | ~180 tok/s, tam yanıt ~4 s |
| `gemma4:12b` | 12 GB+ kartta en iyi kalite | 8 GB+ | 8 GB kartta 16 tok/s, yavaş |

Ollama modelleri panelden indirilebilir; ekran görüntüsü çevirisi (`Ctrl+Alt+R`) için görsel destekli bir model gerekir (gemma4, qwen3.5 ailesi görsel okur).

## Ses

Ses tanıma bu bilgisayarda çalışır (Whisper large-v3-turbo, ekran kartında, ~0,5 s); hiçbir ses dışarı gitmez. Ayarlar → Ses bölümünde:

- **Mikrofon**: kulaklık mikrofonunu seç (SteelSeries Sonar gibi sanal cihazlar çoğu zaman sessiz gelir). "Mikrofonu test et" 1,5 saniye kaydedip seviye gösterir.
- **Dinlenecek hoparlör**: Discord/Telegram/tarayıcı hangi çıkışa çalıyorsa o (Sonar kullananlarda genelde "Sonar - Gaming" veya "Sonar - Chat").
- **Model**: turbo en doğru; ekran kartı dolarsa otomatik olarak işlemcide küçük modele düşer.

## Ayarlar

- **Düşünme (reasoning)**: yerel modellerde "Kapalı" en hızlısı; kalite farkı çeviri için küçük.
- **Yerinde çeviri tonu**: `Ctrl+Alt+Enter` ile hangi ton yapıştırılsın (varsayılan: Doğal).
- **Hedef dil**: Otomatik (Türkçe ise İngilizceye, değilse Türkçeye) veya sabit bir dil.
- **Kısayollar**: `ctrl+alt+t`, `f9`, `ctrl+shift+space` gibi yazılır; kaydedince hemen geçerli olur. Kısayol tuşları uygulamaya iletilmez (Türkçe Q klavyede `Ctrl+Alt` = `AltGr` olduğundan aksi hâlde `Ctrl+Alt+T` seçili metnin üstüne `₺` yazardı; bu ölçüldü ve kapatıldı).
- **Ekran görüntüsü modeli** (Ollama): metin modeli ile görüntü modeli ayrı seçilir; bu makinede `gemma4:e4b` görüntü okuyamadı, `gemma4:12b` okudu. Bölge çevirisi bu yüzden 10–20 saniye sürer.

Ayar dosyası: `%APPDATA%\LuminaTrans\config.json`. API anahtarları sadece orada durur.

## Gerçek uygulama olarak (.exe)

`build_exe.bat` çalıştır: simgeyi üretir (`assets\LuminaTrans.ico`), PyInstaller ile `dist\LuminaTrans\LuminaTrans.exe` derler, Başlat menüsüne ve masaüstüne kısayol koyar. Exe'nin görev çubuğu simgesi, pencere simgesi ve tepsi simgesi aynı bakır "Lt" rozetidir; Görev Yöneticisi'nde `LuminaTrans.exe` olarak görünür ve görev çubuğuna sabitlenebilir. Rozet penceresi görev çubuğunda ayrı bir düğme açmaz.

Windows ile başlasın istersen masaüstündeki kısayolu `Win+R` → `shell:startup` klasörüne kopyala.

Kodda bir değişiklik yaptıysan `build_exe.bat` ile yeniden derle; `LuminaTrans.bat` ise kaynak koddan doğrudan çalıştırır (geliştirme için).

## Bilinmesi gerekenler

- Yönetici olarak çalışan programlara (bazı oyunlar, yönetici PowerShell) tuş gönderemez; oralarda yerinde çeviri çalışmaz, panelden kopyala-yapıştır yapılır.
- Ekrandan çevir şimdilik ana monitörü kullanır.
- Metin ve hızlı çeviri modelleri açılışta ekran kartına yüklenir ve orada kalır (yaklaşık 4,7 GB); ilk yükleme 10–15 s sürer, sonrası anlıktır. Ekran görüntüsü modeli çalışınca ötekiler geçici olarak iner, iş bitince geri gelir.
- Ollama adresi olarak `127.0.0.1` kullanılır; `localhost` yazarsan Windows her isteğe 2 s ekler (ölçüldü), uygulama bunu kendisi düzeltir.
- Ayarlar'daki "Hızlı çeviri modeli" varsayılanı metin modelidir; HY-MT seçersen 0,1 s kazanır ama Türkçede "siz" dili ve kelime hataları ölçüldü.
- Hata ayıklama için: `python app.py --debug` (WebView geliştirici araçları açılır).

## Çeviri motorları

Varsayılan model Ollama ile kendi bilgisayarında çalışır. Bulut sağlayıcı istersen kendi anahtarınla: Gemini, Groq, Cerebras, OpenRouter ve Mistral ücretsiz katman sunar; OpenAI, DeepSeek, xAI Grok ve Claude ücretlidir. Her sağlayıcıda "Model listesini getir" düğmesi anahtarının kullanabildiği modelleri gösterir, model kutusuna istediğin adı yazabilirsin ve OpenAI uyumlu her uç noktayı (Together, Fireworks, şirket içi vLLM, LM Studio) kendi adınla ekleyebilirsin.

## Diller

On bir arayüz dili: Türkçe, İngilizce, İspanyolca, Almanca, Fransızca, Portekizce, İtalyanca, Rusça, Japonca, Korece, Çince. Kurulumda seçtiğin dil uygulamanın dili ve dil çiftin olur. 28 dile çeviri; en çok kullanılan 16 dil (Türkçe, İngilizce, İspanyolca, Almanca, Fransızca, Portekizce, İtalyanca, Rusça, Japonca, Korece, Çince, Arapça, Hintçe, Felemenkçe, Lehçe, Ukraynaca) için hitap seviyesi, bölgesel çeşit, noktalama ve oyun argosu kuralları anadili konuşuru gibi uygulanır.

## Güncellemeler

Güncellemeler birkaç yüz KB: uygulama yalnızca değişen dosyalarını değiştirip yeniden başlar. Kurulum dosyası yaklaşık 120 MB; ses tanıma için GPU paketi (yaklaşık 900 MB) yalnızca NVIDIA kartlı bilgisayarlarda, bir kez iner.

