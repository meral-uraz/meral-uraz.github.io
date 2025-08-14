
*5.3. Frame Relay*
• X.25'e göre hata kontrol mekanizması daha zayıf ama veri iletim hızı daha yüksektir
• X.25'de olduğu gibi Paket Anahtarlama teknolojisinin Sanal Devre yaklaşımını kullanır ve 64 Kbps ile 2 Mbps arasırıda veri iletim hızlarına sahiptir
• Fiber optik ve sayısal veri aktarımı gibi teknolojileri desteklemektedir.
• Paket anahtarlama teknolojisi ile veriyi frame olarak adlandırılan küçük paketlere bölerek gönderir
• Veri iletimi öncesi kaynak ve hedef cihazlar arasında sanal bir devre kurulur, bu sanal devrelere DLCI (Data Link Connection Identifier - Veri Linki Bağlahtı Tanıtıcısı) denilen bir numara verilmiştir
• İletilen her çerçevenin başlığında kararlaştırılan DLCI numarası yer alır.
• Temel olarak DT E ve DCE olmak üzere iki cihaza ihtiyaç vardır
	- DTE cihazlara örnek terminaller, bilgisayar, bridge ve router verilebilir
	- DCE İse ağ İçin anahtarlama servisleri gibi servisler İçin taşıyıcı cihazlardır.

• Ayrıca, Frame Relay servisine ulaşmak için üçüncü bir öğe olarak Frame Relay ağı gereklidir.
![[Pasted image 20240514202617.png||500]]
• Frame Relay İletişimi:
- DTE, iletilecek veri çerçevesini router'a gönderir.
- Router paketi alır ve sanaldevreyi tanımlayan DLCI numarasını ekleyerek CSU/DSU birimine gönderir.
- CSU/DSU (Channel Service Unit/Data Service Unit) sayısal sinyali alır ve onu DCE tarafından anlaşılacak şekle çevirir ve veriyi Frame Relay ile hedefe gönderir.
- Hedefte CSU/DSU tarafından veri alınarak hedefe ulaştırılır. ![[Pasted image 20240515171850.png||500]] ![[Pasted image 20240515172013.png||500]]
  
• Frame Relay servisinde ücretlendirme port hızına, CIR'e ve EIR'e bağlıdır.
- CIR (Committed Information Rate -Taahhüt Edilen Bilgi Oranı), ağın belli koşullar altında bir PVC üzerinden taşımayı taahhüt ettiği bilgi oranıdır.
- EIR (Excess Information Rate - Fazla Bilgi Oranı), kullanıcının hattı üzerinde kullanılabilir bant genişliği olması durumunda, şebekenin koşulları ugun olduğu sürece CIR'ın üzerinde gönderebileceği fazla bilgi oranıdır. ![[Pasted image 20240515172822.png]]

*5.4. ISDN*
• ISDN (Integrated Services Digital Network): Tümleşik Hizmetler Sayısal Şebekesi
• Mevcut analog telefon şebekesinin sayısal alternatifi olup telefon hatları üzerinden sayısal veri transferi için kullanılır.
• ISDN' in diğer servislere göre avantajı ses, veril yazı, grafikl müzik, video gibi farklı türdeki iletişimler için farklı bağlantılar gerektirmemesidir.
• ISDN sayesinde görüntülü telefon, arayan numarayı görme, görüşme süresi, kontör sayısını öğrenme, video konferans gibi özelliklerden yararlanılabilir. 
• Bir ISDN hattında aynı anda 8 cihaz bağlanabildiği halde bunlardan sadece 2 tanesi eş zamanlı olarak kullanılabilir.
• Hem devre hem de paket anahtarlamalı sayısal verinin standart telefon kabloları üzerinden iletilebilmesini sağlar.
![[Pasted image 20240515173703.png||400]]
• Kullanım amacı ve bant genişliği farklı olmak üzere 3 adet kanal kullanılmaktadır.
• Bu kanallar bağlantının kurulması ve veri iletimi için kullanılır
- B Kanalı (BearerCahannel): ISDN teknolojisinin temelini oluşturur ve veri transferi için kullanılır.
	- Her bir kanal 64 Kbps bilgi taşıma kapasitesine sahiptir.
	- Full-duplex modda çalışır.
	- Hata sezme özelliğine sahip değildir
- D Kanalı (Delta Channel): Bu kanal veri iletimi öncesi karşılıklı iki ISDN cihazının bağlantısının kurulması İçin kullanılır
	- D kanallarının bant genişliği B kanalı sayısına bağlı olarak 16 Kbps veya 64 Kbps olabilir
	- Full-duplex modda çalışır.
- H Kanalı: B kanalında oldu gibi veri transferi İçin kullanılır ve daha fazla bant genişliğine sahiptir.
	- H kanalı yüksek hıza veri, yüksek kalitede ses, telekonferans, video servisleri ve LAN bağlantıları gibi uygulamalarda kullanılır, 3 farklı türü vardır.
	- H Kanalı Türleri:
	- H0, 384 Kbps (6 tane B kanalı)
	- H11, 1536 Kbps (24 tane B kanalı)
	- H12, 1920 Kbps (30 tpne B kanalı)
- N Kanalı: Yeni bir kanal olan N kanalı H kanalına benzer olarak değişken hızlı uygulamalar için tanımlanmıştır.
	- Nx64 Kanal diye adlandırılır
	- Bu kanal 64Kbps ile 1.536 Mbps hızları arasında 64Kbps'Iık artışlarla değişebilen bant genişliğine sahiptir.

• ISDN teknolojisi temel olarak iki sınıfa ayrılır. Bunlar;
-  Dar Bant ISDN (Narrow Band ISDN - N-ISDN): Yaygın olarak kullanılan ISDN teknolojisidir.
	- İki çeşittir. Bunlar;
	- Temel Erişim (BasicAccess) ISDN veya BRI (Basic Rate Interface) ISDN
	- Birincil Erişim (Primary Access) veya PRİ (Primary Rate Interface) ISDN
- Genişband ISDN (Broadband ISDN - B-ISDN) ![[Pasted image 20240515180203.png||500]]

• ISDN BRI (Basic Rate Interface -Temel Hız Erişimi) 
- İki B kanalı ve bir D kanalına sahiptir (2B+D)
- B kanalı 64 Kbps bant genişliğindedir ve veri iletimi için kullanılır 
- D kanalı ISDN cihazlar arası bağlantı için kullanılır ve 16 Kbps bant genişliğine sahiptir
- Kapasitesi aynı anda veri ve ses iletimi için kullanılabilecek boyuttadır
- Kullanıcı 2 adet B kanalını istediği gibi (ses ve veri) kullanabilir
- En fazla 8 cihaz bağlanabilir ama eş zamanlı sadece 2 tanesi kullanılabilir
- Küçük ofisler veya ev kullanıcıları için uygundur.

• ISDN PRİ (Primary Rate Interface - Öncelikli Hız Erişimi)
- 30 adet B kanalına ve 1 adet D kanalına sahiptir (30B+D)
- D kanalının bant genişliği 64 Kbps'dır
- 30B+D Avrupa ve dünyanın birçok ülkesipde E1 olarak adlandırılan standarttır
- Kuzey Amerika ve Japonya'da 23B+D kanalından oluşur ve standardın adı T1'dir.

*ISDN Cihazları*

• TE1 (Terminal Endpoint 1 - Son Nokta Uçbirimi 1): ISDN özelliğine sahip cihazları gösterir
- ISDN telefon, ISDN ağ kartı
- BU tür cihazlar S referans noktasından bağlanır
- ISDN'e çift burgulu (4 telli) hat üzerinden bağlantı sağlar

• TE2 (Terminal Endpoint 2 - Son Nokta Uçbirimi 2): Hiçbir ISDN özelliğine sahip olmayan cihazlardır
- Bu tür cihazlar R referans noktası üzerinden bağlanır.

• NT1 (Network Termination 1 - Ağ Uçbirimi 1) : 4 telli abone bağlantısını 2 telli hale dönüştürür
- Fiziksel katman işlevlerini yerine getiren ve son kullanıcıları ISDN ağa bağlayan cihazdır.

• NT2 (Network Termination 2 -Ağ Uçbirimi 2): 4 telli abone bağlantısını 2 telli hale dönüştürür
- Veri bağlantıları ve ağ katmatll işlevlerini yerine getiren cihazdır
- Özellikle PBX'lerde bulunur.
- NT2 birden fazla terminali kontrol etmekte, NT1 ise servis sağlayıcı ile olan fiziksel bağlantıyı kontrol etmektedir.

• NT 1/2 (Network Termination 1/2 - Ağ Uçbirimi 1/2): NT1 ve NT2 özelliklerini tek bir cihaz üzerinde birleştirir.
![[Pasted image 20240515195048.png||500]]

• TA (Terminal Adapter - Uçbirim Uyarlayıcısı): ISDN özelliği olmayan cihazları ISDN ağa bağlamak için kullanılır
- TA ile birlikte ISDN sinyalleşmeyi anlayabilir duruma gelir
- TA bağımsız bir cihaz olabileceği gibi bir cihaz içerisine yerleştirilen donanım da olabilir

• R-Referans Noktası: BU referans noktasına ISDN olmayan cihazlar (ör. Analog telefon) bağlanır
- ISDN UYUmIU olmayan cihazlar ile TA cihazı arasındaki referans noktasıdır

• S-Referans Noktası: ISDN uyumlu cihazlar bağlanır
- ISDN uyumlu cihaz ile NT 2 cihazı arasındaki referans noktasıdır.

*Geniş Band ISDN (B-ISDN)*
• Geniş band ISDN (B-ISDN)I veri haberleşmesi için ATM teknolojisini kullanan bir devre anahtarlamalı hizmettir
• Fiber optik kabloları kullanır
• B-ISDN, N-ISDN ile uyumludur
- 3 adet B-ISDN hizmeti vardır:
- 155.2 Mbps Full-duplex kanal
- 622.08 Mbps Ful-duplex kanal
- 2 simplex kanallı asimetrik hizmet
	- Upstream: 155.2 Mbps
	- Downstream: 622.08 Mbps

*ISDN Hizmetlerin Telefon Şebekesine Katkıları*
• DDI: Arayanların "ön ek+ dahili abone numarası" çevirerek doğrudan dahili aboneye ulaşabilme özelliğidir
• UUS: Kısa mesaj veya ölçekli veri iletişiminin D işaretleşme kanalı kullanılarak gerçekleştirilmesi özelliğidir.
• AOC: Arama ile ilgili ücret bilgileri veya kontur sayısının çağrı kurulma sırasında , çağrı süresince veya çağrı sonunda görülebilmesi özelliğidir
• CLIP/CLIR: Bu fonksiyon arayan abonenin numarasını, aranılan abone terminalinde gösterilmesini veya gizlenmesini sağlar.
• Closed User Group: Bu özellik İle bir grup aboneye sadece grup İçindeki abonelerin çağrı yapması sağlanır. Grup dışında bir abone grup içindeki herhangi bir aboneyi arayamaz.
• COLP-COLR: Bağlantı kurulan terminalin numarasını     görebilme/görememe özellikleridir
• Çağrı Tutma: Abonenin konuştuğu aboneyi bekletmeye alarak başka bir çağrı yapabilme özelliğidir
• Arama Kısıtlama: Abonenin cihazını tüm çıkan aramalara veya bir kısmına kapatıp açabilme özelliğidir
• Çağrı Bekletme: Abone meşgul durumda iken kendisine gelen çağrıda haberdğr edilir
• Çağrı Yönlendirme: Gelen çağrıların daha önce belirlenmiş numaralara yönlendirilmesi özelliğidir
• Konferans Görüşme: İkiden fazla abonenin birbirleri ile aynı anda görüşebilmesidir
• Terminal Taşınırlığı: Abonenin terminal cihazını iletişim devam ettiği sırada park edip aynı erişime bağlı başka bir sokete takıp iletişime devam etmesi özelliğidir
• CCBS: Aranılan numaranın meşgul olması durumunda meşguliyet bittiğinde otomatik olarak aramanın gerçekleştirilmesi durumudur.

*5.5. ATM(çok önemli bir konu değil)*
• ATM (Asynchronous Transfer Mode): Eşzmansız İletim Modu
• Veri iletim tekniği olarak paket anahtarlama iletim tekniğinin bir türü olan hücre aktarım tekniğini kullanmaktadır
• Veriler 53 byte uzunluğundaki sabit boyutlu hücreler şeklinde iletilir
• 53 byte hücre boyutunun 5 byte'ı başlık 48 byte'ı da veri kısmını oluşturur
• Her hücre başlığında bulunan VCI (Virtual Circuit Identifier-Sanal Devre Tanımlayıcısı) ile taşınır
• ATM bu tanımlayıcıları kullanarak veriyi hızlı bir şekilde hedefine ulaştırır.
• Verinin gecikmeye tahammülü olmadığından hızlı ve güvenilir bir şekilde çalışır
• 155 Mbps - 922 Mbps hızında ATM ağlar bulunmaktadır
• ATM ağlar bakır, koaksiyel ve fiber optik kablolamayı destekler
• ATM yerel bir ağ kurmak için ATM switch'lere ve her bir ağ cihazında ATM adaptöre gerek vardır.

*ATM Çalışma Şekli*
• ATM'de hem PVC (Permanent Virtual Circuİt - Kalıcı Sanal Devre) hemde SVC (Switched Virtual Circuit - Anahtarlanmış Sanal devre) kullanımı mümkündür
• WAN' larda PVC kullanımı daha yaygındır
• Bir tek kiralık hat bağlantısı üzerinde çoklu VC kullanılmasını mümkün kılar
• Bağlantı temelli bir iletim tekniği olduğundan iletim başlamadan önce iletimi gerçekleştirilecek iki taraftan biri bağlantının kurulması için karşı tarafa bir paket gönderir
• Bu paket geçtiği yollara ve anahtarlara ihtiyaç duyduğu kaynakların bilgisini kaydeder
• Bu yollara sanal yol (Virtual path) denir.


*5.6. DSL (Digital Subscriber Line)*
• Sayısal Abone Hattı: Mevcut telefon alt yapısını kullanarak yüksek hızda veril ses, multimedya gibi iletişimlere olanak sağlayan WAN teknolojisidir
• Yapı olarak bir çift bakır kablonun iki ucuna bağlı modemler ile veri transferi gerçekleştirir
• Hattın bir ucu kullanıcı iken diğer ucu DSL hizmeti alınan kurum veya kuruluştur
• Hatta bağlı olan bu modemler sayısal hat oluşturulmasını sağlar
• DSL teknolojisi duplex yani çift veri iletimi gerçekleştirmektedir.
• DSL, Kullanıcıların yüksek hızlarda ve düşük maliyette internet kullanımına olanak sağlamaktadır.
![[Pasted image 20240518204407.png||500]]
• Aynı hizmet ISDN ile de alınabilir
• DSL teknolojisinde aynı hat üzerinden eş zamanlı olarak telefon görüşmesi ve veri iletimi gerçekleştirilebilir
• Telefon görüşmeleri 4kHz'e kadar bant genişliği, internet erişimi ise daha üstü (80 kHz'e kadar) bant genişliği kullanmaktadır
• Hattın kullanıcı tarafına eklenen splitter yardımıyla bu iki frekans bandı birbirinden ayrılır ve elde edilen iki Ucun birisi telefon diğeri DSL için kullanılabilir
• Günümüzde bazı DSL modemler aynı hat üzerinden birden fazla aboneye hizmet vermek için kullanılmaktadır.
• Bu uygulamalar sayesinde ikinci hatta ihtiyaç olmadan tek bir hat 12'ye kadar POTS (Plain Old Telephone Services - Sıradan Eski Telefon Hizmeti)'a bölünebilir
• 784 Kbps hızındaki bir HDSL hat üzerinden 12 adet 64Kbps bir adet 16Kbps senkronizasyon ve işaretleşme hattı için bir kanal sağlanarak tek hattan 12 abonenin birden görüşmesi sağlanır
• Simetrik veri iletimin de, veri gönderme ve veri alma için kullanılan bant genişlikleri aynıdır (önemli)
• Asimetrik veri iletiminde ise veri gönderme ve alma için kullanılan bant genişlikleri farklıdır.

*DSL Teknolojisi Çeşitleri*
• HDSL (High-bit-rate- Digital Subscriber Line): Bakır ve çift burgulu kablolarla oluşturulan İlk DSL teknolojisidir
• Simetrik olarak 2Mbps'a kadar veri iletimi gerçekleştirir. T1 (1.544Mbps) veya E1(2.048Mbps) hızlarında tekrarlayıcısız 4km'e kadar tekrarlayıcı ile 12 km'e kadar iletim sağlar
• Ancak, T1 için 2 hat, E1 için ise 3 hat gerekmektedir 
• Bu durum nedeniyle telefon işletmecileri tarafından pek ktbul görmemektedir
• HDSL uygulama alanları;
- Santraller arasında,
- 2Mbps bağlantı gereksinimlerinde,
- Video konferans hizmetinin sunulmasında,
- GSM baz istasyonları arasında,

*Şirketlerin kendi intarnet erişimlerinde, kullanılmaktadır.

• *SDSL* (Symetric Digital Subscriber Line - Simetrik Sayısal Abone Hattı) : Simetrik olarak 2Mbps'a kadar veri iletimi sağlar• Genellikle kiralık hatlar için kullanılır
• SDSL ile maksimum 3 km'e kadar iletişim söz konusudur
• Bu mesafe ADSL sistemlerde 6 Mbps'a kadar hız sağlamaktadır
• HDSL'in tek hat ile oluşturulmuş bir versiyonu olup tek hat üzerinden Eli Ti hızlarını destekler ve telefon görüşmesi yapılabilir.
• *SHDSL* (Single-pair High-speed Digital Subscriber Line) : Bir veya iki hat üzerinden 6 km'e kadar simetrik veri iletimi gerçekleştirmektedir
• Tek hat kullanıldığında 2.312 Mbps, iki hat kullanıldığında 4.624 Mbps hızlara çıkılabilir
• Genellikle IP üzerinden veri ve ses iletimi için kullanılır
• Örneğin, Telekom santrallerinden kullanıcıya PRİ hatlarının ulaştırılması İçin kullanılır.
• Türk Telekom üzerinden G-SHDSL (SHDSL) hizmeti ı hat üzerinden alınabilir. Ancak, mevcut telefon hatları yerine kullanıcıya özel hat çekilmektedir

• Noktadan Noktaya SHDSL: 2 yada daha fazla noktadaki ofisler  arasında Uzak alan ağ bağlantısı gerçekleştirmek için kullanılır
• SHDSL İnternet Erişimi: Türk Telekom'un ADSL gibi en çok yaygınlaşması beklenen hizmetidir
• Bu hizmet e-posta yada web SUTIUCUSUTIIJ kendi bünyesinde barındırmak isteyen, yüksek download/upload trafiği olan firmalar için vazgeçilmez bir sistemdir
• İnternet hizmetinde maksimum hız 2 Mbps dir
• Bu hızlardan daha fazlasına ihtiyacı olan firmalar Metro Ethernet hizmetinden yararlanabilir.

• *ADSL* (Asymetric Digital Subscriber Line - Asimetrik Sayısal Abone Hattı) :Asimetrik olarak yüksek hızda veri iletimi sağlayan teknolojidir
• Asimetrik oldUğU için veri gönderme ve alma için kullanılan hızlar farklıdır ve kullanıcının veri alma hızı daha yüksektir
• HDSL'den sonra gelen ADSL, ev kbllanıcıları için düşünülmüş olup günümüzde birçok kullanıcı ve işletme tarafından kullanılmaktadır
• ADSL, bir yönde (downstream) 8Mbps'a kadar iletim sağlarken diğer yönde (upstream) 1 Mbps kadar iletim sağlar
• ADSL teknolojisinin gelişimi sonucu farklı downstream ve upstream değerlerine sahip versiyonları oluşturulmuştur.
![[Pasted image 20240518204555.png||500]]

• **RADSL** (Rate Adaptive Digital Subscriber Line): ADSL teknolojisinden türetilmiş bir DSL teknolojisidir
• Hattın kullanım Uzunluğu ve gürültü oranına göre bant genişliğini 300-400 Kbps aralıklarda dinamik olarak ayarlayabilmektedir
• Kullanıcılar uygulamalarına göre farklı bant genişlikleri kullanabilir.
• VDSL (Very High-bit-rate Digital Subscriber Line): 55.2 Mbps downstream, 19.2Kbps-3 Mbps upstream hızlarında kullanılabilir
• ADSL'den en belirgin farkı iletim mesafesi daha kısadır
• 13 Mbps hız için 1.5km, 55.2 Mbps için 300m mesafeden daha öteye erişememektedir
• VDSL, hem simetrik hem de asimetrik yapıda kullanılabilir
• Simetrik yapıda 20Mbps hızına ulaşabilmektedir
• Kiralık hatları yüksek bant genişliği gerektiren uygulamaları çok katlı binalarda katlar arası bağlantı, fiber hattın bina içerisine alınması için kullanılabilir.

*5.7. Metro Ethernet*
• Fiber optik kablo üzerinden 5 Mbps ile 10 Gbps arasında değişen hızlarda, simetrik olarak veri iletimi için kullanılan teknolojidir
• Protokol dönüşümlerine ihtiyaç duyulmaksızın Uçtan uca Ethernet teknolojisi kullanılır
• Kullanıcıya özel çekilen bir fiber hattı ve switch sayesinde ara cihazlar kullanılmadan internet kullanılabilir.
*Migros bim A101 metro eternet kullanıyor*
![[Pasted image 20240518204645.png||500]]
