
**2. AĞ BAĞLANTI CİHAZLARI**

*2.1. Ağ Arayüz Kartı (NIC-Network Interface Card)*
• Masaüstü bilgisayarlarda PCI yuvaya takılan bu kart günümüzde bir çok anakartta tümleşik olarak gelmektedir.
• Dünya üzerindeki tüm ethernet kartlarını birbirinden ayırmak için üzerlerinde MAC (Media Access Contol) adı verilen bir adres barındırırlar ve her kartın MAC adresi
birbirinden farklıdır.
• MAC 48 bitlik bir adrestir.
• Bu nedenle 2⁴⁸ adet MAC adresi yani ağ arayüz kartı tanımlamak mümkündür.

*2.2. HUB*
• Yıldız topolojisindeki ağlarda merkezde bulunur ve ağdaki tüm cihazlar ethernet kartı üzerinden hubla bağlıdır.
• Ağın tamamına veriyi dağıttığı için ağda fazla trafik oluşumuna neden olur.
• Sadece bit seviyesinde işlem yapmaktadır.
• Token ring topolojisinde merkezde MAU bulunur ve görevi hub'la aynıdır.
	![[Pasted image 20240513131453.png]]

*2.3. Switch (Anahtar Cihazı)*
• Temel görev olarak hub'larla aynı olmakla beraber çalışma şekli farklıdır
• Veri iletimi anahtarlamalı olarak gerçekleştirilir
• Üzerlerinde bulundurdukları MAC adres tablosu sayesinde her bir portta bağlı cihazın MAC adresini bilir ve veriyi ilgili porta yönlendirir.
• Yıldız topolojisinde merkezde kullanılabildiği gibi paket anahtarlamalı farklı ağları da birbirine bağlamak için kullanılabilir.
• Switch'ler birbirine bağlanarak ağ genişletilebilir.
• Switchler üzerinde çoğunlukla hublarda olduğu gibi upIink portu yoktur.
• Ya da 24 portlu ise 25 ve 26 nolu portlar uplink için ayrılmış olabilir.
• Switchler veri iletim türüne yani kullanılan paket anahtarlamaya göre iki moda sahiptir;
- Cut Through Mod: İletilecek veri switche geldiğinde ilgili porta yönlendirilerek veri iletimi gerçekleştirilir.
- Store and Forward Mod: Bu tür switchlerde iletilecek veri switch üzerinde bufferla atılarak hata kontrolü gerçekleştirilir.

• Switchler OSI katmanında bulunduğu yere göre 2'ye ayrılır;
• Buraya kadar bahsedilenler Katman 2 anahtarar (Layer 2 switch ) olup OSI katman 2 (Veri Bağı Katmanı)'de yer almaktadır.

• *Katman 3 anahtarlar (Layer 3 switch)* yönetilebilirdirler.
- Katman 2 yani yönetilemez swtichlerin tüm özelliklerini barındırır ve üzerlerinde barındırdıkları yazılımlar sayesinde ağ üzerindeki trafik kontrol edilebilir.
- Ağdaki cihazların izlenmesi için Simple Network Management Protocol (SNMP) barındırılar.
- VLAN oluşturulabilir.
- Portlar üzerinde güvenlik ptrotokolIerİ uygulanabilir.
- İstenilen port kapatıp açılabilir.
- Kısaca yönetilebilir switchler, switch ve router'ın ortak özelliklerine sahiptir.
![[Pasted image 20240513140801.png||500]]

- **Sınav Ödevi : Türkiye'de kullanılan ve internette satış yapılan Switch markalarını inceleyin**

*2.4. Repeater (Tekrarlayıcı)*
• Repeaterı alınan sinyali bit seviyesinde yenileyerek yani güçlendirerek ve zamanlayarak tekrar iletilmesini sağlar.
• Sinyali güçlendirmenin yanı sıra bozulan sinyallerin iyileştirilmesini sağlar.
• Çoğunlukla kablosuz ortamlarda kullanılır.
• KabloIu ortamlarda kullanılan switch, hub ve router gibi cihazlar aynı zamanda tekrarlayın olarak çalışmaktadır.

*2.5. Bridge (Köprü)*
• Aynı protokolü kullanan iki veya daha fazla ağı birbirine bağlamak için kullanılır.
• Bu işlem yapılırken NIC'ler üzerinde bulunan MAC adresleri kullanılır ve haberleşen cihazların kendi içerisinde mi yoksa diğer ağ da mı olduğuna karar verir
• Birbirine bağlanacak ağlar farklı topolojide olmak zorunda değildir
• Bir ağ donanımı olabileceği gibi bir bilgisayar ve yüklü yazlım veya işletim sistemi de bu görevi gerçekleştirebilir.
	![[Pasted image 20240513154533.png]]

*2.6. Router (Yönlendirici)*
• LAN-LAN, LAN-WAN, WAN-WAN gibi ağlar arası haberleşme için kullanılır.
• Router'ın işlemcisil EPROM'u ve işletim sistemi (IOS -Internal Operating System) vardır.
• Dinamik router, iletilecek veri için kullanılacak en iyi yolu kendisi belirler.
• Statik routerda kullanılacak yol elle belirlenir ve hep belirlenen yol kullanılır.
	![[Pasted image 20240513160557.png||500]]

*2.7. Gateway (Ağ Geçidi)*
• Farklı tipteki ağları birbirine bağlamak için kullanılır
• Bu sayede IP-IPX veya ISDN- X25 gibi farklı protokolleri kullanan ağlar haberleşebilir
• Bu cihaz bridge, switch veya router olabileceği gibi yazılımsal olarak da  gerçekleştirilebilir. 

*2.8. Transciever (Dönüştürücü)*
• Farklı fiziksel yapıya sahip kabloların birbirine bağlanması için kullanılır
• Örneğin, biri UTP diğeri fiber optik olan kabloların birbirine bağlanması için kullanılabilir.

*2.9. Firewall (Güvenlik Duvarı)*
• Birçok filtreleme özelliği sayesinde ağ ile internet arasında gelen ve giden veri paketlerini denetleyerek istenmeyen trafiği veya erişimleri engellemek için kullanılır.
• IP filtreleme, port filtreleme, web filtreleme ve içerik filtreleme gibi özelliklere sahiptir.
• Yazılımsal firewallar çqğunlukla ev kullanıcıları İçindir
• Donanımsal firewall ise genellikle ağ sistemlerini korumak içindir
- Stateful Inspection Firewall; İletilen veriyi kaynağından hedefine kadar takip eder ve veri paketi içerisinde daha önce zararlı olarak tanıtılmış koda rastlarsa verinin iletimine izin vermez.
- Application Layer Firewall ise verinin sadece başlık kısımlarını kontrol eder ve uygulama katmanında kısıtlama yapar.	![[Pasted image 20240513161327.png||500]]![[Pasted image 20240513163258.png||500]]

- **Sınav Ödevi : Türkiye'de kullanılan ve internette satış yapılan Firewall markalarını inceleyin**

*2.10. Access Point (Erişim Noktası)*
• Kablolu ağ ortamının kablosuza dönüştürülmesi veya kablosuz ağ ortamının etki alanın genişletilmesi için kullanılır.
• Kablosuz ağın etki alanın yeterli olmadığı durumlarda AP kullanarak mevcut kablosuz ağın sinyallerini güçlendirip etki alanın genişletebilir.

*2.11. Modem*
• Modemler, telefon hatları yardımıyla bilgisayarların internete bağlanmasını sağlayan
cihazlardır. 
• Modülatör ve Demodülatör kelimelerinin ilk hecelerinin birleşiminden oluşur.
1. *Dial-Up modemler;* sayısal verileri analog sinyallere veya analog sinyalleri sayısal verilere çevirir.
2. *Sayısal modemler;* herhangi bir sayısal analog dönüşümü yapmaz.
	- Veriyi sayısal olarak iletir.
3. *ADSL modemler;* telefon hatları üzerinden internet erişimi sağlanır ve kablonun her iki ucunda ADSL modem bulunur.
	- ADSL modem kullanılan telefon hatlarında internetle eş zamanlı olarak telefon görüşmesi de gerçekleştirilebilir.
	- Telefon görüşmeleri o KHz-4 KHz arasında frekans aralığını, veri iletimi 4 KHz - 1100 KAZ arasında frekans aralığını kullanır.
4. *DSL modemler;* Senkron çalışan modemlerdir.



**3. OSI BAŞVURU MODELİ**
• İki bilgisayar arasındaki iletişimi biçimsel olarak tanımlayan ilk kuruluşlardan birisi ISO (International Organization for Standardization)'dur.
• ISO uluslararası veri iletişimi standartları geliştiren bir kuruluştur.
• ISO 1970'lerde OSI (Open Systems Interconnection) mimarisini geliştirmiştir.
• OSI ile birlikte farklı üreticilere ait donanımlar arası uyumsuzluk ortadan kalkmıştır.
• OSI yedi katmana ayrılmıştır ve iletişim esnasında kullanılan protokoller ve donanımlar bu katmanlarda yer alır.
• Veri alanda ise gelen veri en alt katmandan başlar ve üste doğru devam eder.
• En üst katman kullanıcıya daha yakın olup uygulamaları içerirken alt katmanlara doğru veri makine diline ve en son bit seviyesine kadar düşer.
• OSI modeli sayesinde bir donanım veya protokolün ağ içerisindeki görevi daha kolay açıklanabilir. 

*3.1. Fiziksel (Physical) Katman*
• Bu katman verinin kablolar üzerinden iletiminden sorumludur ve verinin içeriğiyle ilgilenmez.
• Verinin elektrik, ışık veya radyo sinyallerine çevrim şekli ve aktarımını tanımlar.
• Veriyi gönderen taraf 1 ve 0'lardan oluşan veriyi iletim şekline göre (ışık, radyo
veya elektrik) çevirir.
• <u>Fiziksel katman iletişim türleri; </u>
- RS-2321
- 10Base-TX
- 100Base-TX
- ISDN
- DSL vb.

*3.2. Veri Bağı (Data Link) Katmanı*
• FizikseI katmana erişim ile ilgili kuralları düzenler.
• Bu katmanda gerçekleştirilen işlemlerin büyük bölümü ağ arayüz kartı içerisinde gerçekleştirilir.
• Veri bağı katmanı LLC (Logical Link Control) ve MAC (Media Access Control) alt katmanları olmak üzere iki bölümden oluşur.
- *MAC alt katmanı,* ağ katmanından gelen veriye hata bitlerini, alıcı ve gönderici MAC adreslerini ekleyerek fiziksel katmana aktarır. Bu katmanda Ethernet, Token Ring, FDDII ATM, Frame Relay ve PPP iletişim kuralları bulunmaktadır.
- *LLC (Logical Link Control),* ağ cihazlarından Switch ve Bridge veri bağı katmanında tanımlıdır.

*3.3. Ağ (Network) Katmanı*
• Bu katman gelen veri paketlerinin ağ adreslerini kullanarak uygun ağlara yönlendirilmesini sağlar.
• Router ve yönetilebilir switch bu katmanda yer alır
• Temel görevi, Taşma katmanından gelen istekleri cevaplandırmak ve bu hizmetleri Veri Bağı katmanına iletmektir
- IP
- ARP (IP adresinden fiziksel adrese dönüşüm gerçekleştirir)
- ICMP (Sistemler arası kontrol mesajı için kullanılır)
- IPsec (IP protokolünün güvenlik ihtiyaçlarını gidermek için geliştirilmiştir)
- IPX (Netware sistemlerde adresleme için kullanılır)
- AppleTalk (Apple tarafından geliştirilen ve MAC üzerinde kullanılan adresleme protokolüdür) bu katmanda kullanılan protokollerdir.

*3.4. Taşıma (Transport) Katmanı*
• Akış kontrolü ile verinin alıcısına ulaşıp ulaşmadığını ve bölümlere ayrılan verinin aynı sırada birleştirilmesini sağlar.
• Veri iletimini gerçekleştiren 
- TCP
- UDP
- SPX
- SCTP 
- DCCP protokolleri bu katmanda yer alır.

*3.5. Oturum (Session) Katmanı*
• Veri iletimi esnasında sorun oluşursa bağlantının tekrar kurulmasını sağlar.
• Cihazlar arasındaki iletişim türü de (simplex, half-duplex,full-duplex) yine bu katmanda belirlenir.
- NetBIOS (ağa bağlı aygıtların birbiriyle haberleşmesini sağlayan bir API)
- SSL (internet üzerinde güvenli iletişim sağlayan bir yapıdır)
- SOCKS (istemci ve sunucusu arasındaki paketlerin yönlendirilmesini sağlayan bir internet protokolü) protokolleri bu katmanda yer alır.

*3.6. Sunum (Presentation) Katmanı*
• Bu katmanda veriyi;
- sıklştırma-açma
- şifreleme-şifre çözme
- Unicode-ASCII
- Tersi dönüşüm işlemleri gerçekleştirilir

• FarkIı işletim sistemleri içeren iki bilgisayar arasında veri transferi gerçekleştirilirken kodlamalar farklı olacaktır.

*3.7. Uygulama (Application) Katmanı*
• Dosya paylaşımı, e-mail veya veri tabanı yönetimi gibi işlemlerin gerçekleştirildiği katmandır. 
• Uygulama katmanında 
- HTTP
- SMTP
- POP
- DHCP
- Telnet
- DNS gibi protokoller kullanılır.

![[Pasted image 20240513181215.png]]
![[Pasted image 20240513181336.png]]


