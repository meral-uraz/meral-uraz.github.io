
*7.4. TCP/IP Mimarisi*
• Transmission Control Protocol/lnternet Protocol
• TCP/IP bir yerden diğerine veri iletişimini olanaklı kılan pek çok veri iletişim  rotokolüne verilen genel addır.
• TCP/IP aslında iki farklı protokolden oluşmaktadır.
- TCP, verinin iletilmesinden önce paketlere ayrılması ve alıcı tarafında bu paketlerin tekrar birleştirilmesini sağlar.
- IP ise iletimi yapılacak paketlerin istenilen hedefe yönlendirilmesini sağlar.

• TCP/IP mimarisi OSI referans modelinde olduğu gibi katmanlara ayrılmıştır
• OSI referans modelinde 7 katman bulunurken TCP/IP mimarisinde 4 katman bulunmaktadır. 
![[Pasted image 20240518135813.png]]

*• Fiziksel Katmanı :* Bu katman verinin kablolar üzerinden iletiminden sorumludur
• Verinin içeriğiyle ilgilenmez 
• Verinin elektrik, ışık veya radyo sinyallerine çevrim şekli ve aktarımını tanımlar
• İletimi gerçekleştirilecek veri IP başlığı içerisinde kaynak ve hedef IP adreslerini tutar

*• İnternet Katmanı :* IP katmanı olarak ta anılır
• IP adreslerinin veriye eklendiği ve yönlendirmenin yapıldığı katmandır
• Taşıma katmanından gelen veriler bu katmanda paketler haline getirilir
• Bu katman taşıma katmanından gelen veriyi alıcıya hatasız ulaştırmakla yükümlüdür
• Paketin hedefe en iyi yoldan gönderilmesi de bu katması sorumluluğudur.

*• Taşıma Katmanı :* Uygulama katmanından gelen veriyi paketler halinde internet katmanına aktarır
• Eğer veri tek seferde gönderilemeyecek kadar büyükse parçalara ayrılır (segment) ve her bir parçaya sıra numarası verilir
• İnternet katmanından aldığı veriyi de birleştirerek üst uygulama katmanına aktarır
• Servis kalitesi (QoS), güvenli veri aktarımı, akış kontrolül hata kontrolü gibi işlemlerin yapıldığı katmandır.

*• Uygulama Katmanı :* Kullanıcıya en yakın katman olup kullanıcı tarafından çalıştırılan
tüm uygulamalar bu katmanda yer alır 
• UygulamaIar ile ağ arasındaki arabirimdir
• Dosya paylaşımı, e-mail veya veri tabanı yönetimi gibi işlemlerin gerçekleştirildiği katmandır

*TCP/IP ve OSI Arasındaki Benzerlikler ve Farklılıklar*
• Her iki model de katmanlı yapıdadır
• Her iki model de paket anahtarlama kullanır
• TCP/IP veri iletimi karmaşık olduğundan daha basit alt görevlere bölünür
• OSI de de karmaşıktır ama OSI veri iletimi için her aşamayı farklı bir katmanda tanımlayarak çözmüştür
• TCP/lP'de kullanılan port kavramı OSI'de bulunmamaktadır.
• TCP/lP taşıma katmanında UDP'de kullanılabildiği için UDP kullanıldığında veri güvenliği OSI'deki kadar sağlam değildir.

*7.4.1. Uygulama Katmanı Protokolleri*
TCP/IP uygulama katmanında :
- DHCP                    • TLS/SSL
- DHCPv6                • SSH
- DNS                      • TELNET
- SMTP                    • SNMP
- IMAP                     • NNTP
- IRC                        • RMON
- SOCKS                  • TFTP
protokolleri kullanılmaktadır.

*• DHCP (Dynamic Host Configuration Protocol) :*
• DHCPlnin temel görevi ağ üzerindeki cihazlara IP dağıtımı yapmaktır.
• Cihazlara IP adresi statik ve dinamik olmak üzere iki şekilde atanır.
• DHCP tarafından cihazlara verilen IP adreslerinin belirli bir kira süresi vardır ve bu süre DHCP konfigürasyonunda ayarlanabilir.

• DHCP'nin çalışma prosedüründe 4 temel durum söz konusudur :
1. DHCP discover
2. DHCP offer
3. DHCP request
4. DHCP acknowledgement

• DHCP request mesajını alan sunucu IP adresi/ ağ maskesi/ DNS adresi bilgilerini istemciye yollar
• DHCPv6: DHCP ile aynı özelliklere sahip olup IPv6 için otomatik IP verilmesi işlemini gerçekleştirir.

*• DNS (Domain Name System) :* İnternet üzerinde barındırılan tüm web sitelerinin isimlerinin yanı sıra IP adresleri bulunmaktadır
• DNS sistemi isim sunucuları ve çözümleyicilerden oluşmaktadır.
• İsim sunucuları, web sitesinin adresine karşılık gelen IP adresini tutarken
• Çözümleyiciler ise DNS istemciler olarak çalışır ve DNS sunucuların adreslerini tutar

*HTTP (HypertextTransfer Protocol)*
• HTTP, internet üzerinde sunucu ve istemci arasında veri transferinin kurallarını ve yöntemlerini düzenler
• Bu protokolü kullanarak HTML tabanlı belgeleri görüntülemek için tarayıcılar(browser) kullanılır.

*HTTPS (Transfer Protocol Secure)*
• İnternette sunucular ve istemci arasında veri transferi "başkaları tarafından"  okunamayacak şekilde nasıl aktarılacağına dair kuralları ve yöntemleri düzenler
• HTTPS ile bağlantı kurulan sitelerde transferi yapılan veri sadece istemci ve sunucu tarafında okunabilecek şekilde şifrelenir.

*FTP (File Transfer Protocol)*
• TCP/IP protokolünü kullanarak internet üzerinde dosya aktarımı ve paylaşanı sağlayan bir protokoldür.
• Windows'ta ftp.exe isimli bir konsol uygulaması vardır
• FTP amaçlı FileZilla FTP Client. CuteFTP, FTP Explorer veya SmartFTP gibi programlar FTP'nin tüm hizmetlerinden faydalanmak için oluşturulmuş özel programlardır.

*TFTP (Trivial File Transfer Protocol)*
• FTP'nin temel özelliklerini barındıran dosya transfer protokolüdür
• Bu nedenle veri depolama donanımı olmayan router gibi cihazlar için uygundur.

*FTP ve TFTP arasındaki temel farklar*
• FTP genel amaçlıı TFTP özel amaçlı dosya transfer protokolüdür
• FTP hem dosya gönderme hem de dosya alma için kullanılabilir, TFTP sadece tek yönlü transfere izin verir
• FTP dosya transferinin TCP üzerinden gerçekleştirdiği için güvenilirdir, TFT ise dosya transferini UDP üzerinden gerçekleştirdiği için daha az bellek kullanmasına rağmen dosya transferinde neredeyse hiç bir güvenlik kontrolü yoktur
• FTP kullanıcı kimlik doğrulaması sağlarken, TFTP'nin bu özelliği yoktur
• FTP dosya transferi için TCP 20 ve 21 noIu portları kullanırken, TFTP dosya transferi için çok fazla bilinmeyen UDP 69 noIu portu kullanılır.

*SMTP (Simple Mail Transfer Protocol)*
• E-posta göndermek için sunucu istemci arasındaki iletişim şeklini belirleyen protokoldür
• Standart bir e-posta adresi aşağıdaki biçimdedir.
• Kullanıcı_adi@domain_adı
• E-posta göndermek veya almak için HTTP tabanlı bir web sayfası(gmail.com, hotmail.com, yahoo.com) veya e-posta işlemleri için özel yazılmış bir program(Outlook, Pegasus Mail) gereklidir.

Aşağıda posta hizmetlerinden faydalanmak İçin sık kullanılan terimlerin anlamları verilmiştir
• CC (Karbon kopya): Aynı postanın gideceği farklı kişilerin e-posta adresleri
• BCC (Görünmez karbon kopya): Postayı alan kişiler To ve CC deki adresleri görebilirken BCC(BIind Carbon Copy) alanındaki adresleri göremezler

*POP (Post Office Protocol)*
• Postaların alınmasını ve posta kutularının yönetilmesini sağlayan protokoldür
• Bu yapıya göre kullanıcı postaları tek bir dizinde (InboxzPosta kutusu) tutulur
• Sunucu üzerinde postaların kopyası kalmaz
• Postalar bilgisayara otomatik olarak aktarıldıktan sonra internet bağlantısına gerek kalmadan postaları okunabilir.

*IMAP (internet Message Access Protocol)*
• POP gibi sunucuya gelen postalan almak için kullanılan protokoldür
• Web tabanlı posta istemcisi kullanan bütün sunucuIar IMAP kullanır
• Outlook, Apple Maili, Outlook Express gibi posta istemciler kullanıldığında posta sunucusunun desteklediği protokole bağlı olarak IMAP veya POP3 kullanılabilir.

*POP ve IMAP arasındaki farklılıklar*
• POP3 bütün mesajlar istemciye çeker (Off-Line çalışılır), IMAP her postayı sunucudan okur (On-Lin çalışır)
• POP3 bir postayı ilk indiren kullanır, IMAP posta sunucu üzerinde kalacağı için aynı anda birden fazla lâullanıcı postayı görebilir
• IMAP kullanıldığında mesajı açmadan ekli dosya bilgisayarına indirilebilir, POP3'te ise mesaj içeriği ve ekler bir bütündür mesaj açılmadan ekli dosyalar görülemez.

*SOCKS (SOCKet Secure)*
• Proxy server üzerinden istemci ve sunucu arasındaki veri paketlerinin yönlendirilmesini
sağlar
•Ayrıca kimlik doğrulama sağlayarak sadece yetkili kişilerin sunucuya erişimine izin verir.

*TLS/SSL (Transport Layer Security/Secure Socket Layer)*
• Netscape tarafından 1994 yılında geliştirilen Secure Sockets Layer (Güvenli yuva Katmanı) protokolü internet üzerinden şifrelenmiş veri iletişimi sağlar 
• 1996 yılında çıkan 3.0 versiyonuyla web tarayıcıların tamamı tarafından desteklenen bir standart haline gelmiştir
• Şifreleme yönteminin gücü şifre anahtarının uzunluğuna bağlıdır.
• SSL protokolü günümüzde 128 bitlik şifreleme kullanılmaktadır
• 128 bitlik bir şifreleme 2¹²⁸ farklı değer alabilir ve bu şifrenin çözülmesi çok büyük maliyet ve zaman gerektirir
• SSL anahtarları uluslararası güvence altındadır
• InstantSSL, VeriSign ve Thawte gibi uluslararası güvenlik kuramlardan para karşılığı alınırlar.

*SSH (Secure Shell)*
• Ağ üzerinden başka bilgisayarlara erişim sağlamak, uzak bir bilgisayarda komutlar çalıştırmak ve bir bilgisayardan diğerine dosya transferi amaçlı geliştirilmiş bir  protokoldür
• POP servisini SSH üzerinden aktararak şifreli ve güvenli hale getirilebilir.

*TELNET*
• Uzaktaki bir bilgisayara bağlanarak o bilgisayarın bir terminaliymiş gibi çalışmak için kullanılır
• Windows içerisinde telnet.exe isimli bir konsol uygulamasıyla TELNET sunuculara bağlanılabilir 
• "Başlat-Çalıştır-Telnet" yolunu izleyerek program çalıştırılabilir

*SNMP (Simple Network Management Protocol)*
• AğIar üzerindeki routerı switch ve HUB gibi cihazları denetlemek amacıyla kullanılır
• TCP/IP protokolünün bir parçası olan SNMP; ağ yöneticilerinin ağ performansını arttırması, ağ problemlerini bulup çözmesi ve ağlardaki genişleme için planlama yapabilmesine olanak sağlar.

*NNTP (Network News Transfer Protocol)*
• HTML öncesinde metin içerikli verilerin taşınması amacıyla kullanılmıştır
• Günümüzde Usenet (dünya üzerindeki milyonlarca ağ kullanıcısının çok değişik konularda haberler, yazılar gönderdiği bir tartışma platformu) üzerindeki yeni makaleleri news server ve kullanıcı arasında taşıyan bir protokoldür. 

*RMON (Remote Monitoring)*
• LAN'ların analiz edilmesi ve hataların tespit edilmesi için geliştirilmiştir
• SNMP'nin uzantısıdır silk versiyonu olan RMON1 OSI referans modeli fiziksel ve veri bağı katmanında yer alırken,
• RMON2 versiyonu ağ ve uygulama katmanında izleme özelliklerihe sahiptir.

*RPC (Remote Procedure Call)*
• İstemci ve sunucu arasındaki iletişim için tasarlanmıştır
• Uygulama geliştirirken bir RPC çağrısı program içerisindeki bir fonksiyonu çağırmakla eşdeğer zorluktadır
• Program akışı devam ederken sunucuya istek gönderilir ve sunucu isteğinden sonra program rutin olarak işlemine devam eder.

*LDAP (Lightweight Directory Access Protocol)*
• TCP/IP üzerinde çalışan dizin servislerini sorgulama ve değiştirme amacıyla kullanılır
• Dizinler içerisinde :
- ağdaki bilgisayarlar,
- cihazlar,
- şirketteki kişi listeleri gibi bilgiler tutulabilir
• Dizin sunuculara örnek olarak OpenLDAP, Syn Directory Server, Microsoft Active Directory verilebilir
• LDAP protokolü TCP/IP protokolünü kullandığı için dizinlere web üzerinde de erişim imkanı sağlar.

*LDIF (LDAP Data interchange Format)*
• LDAP sunuculara istemcilerin bağlanabilmesi ve bilgilere erişebilmesi için LDIF
kullanılmaktadır
• LDIF sayesinde herhangi bir programlama dili kullanılarak LDAP sunucuya erişip dizin
bilgileri sorgulanabilir.

*NTP (Network Time Protocol)*
• NTP, değişken gecikmeye sahip paket anahtarlamalı ağlar üzerindeki bilgisayarların saatlerinin eş zamanlanmasının sağlanması için kullanılan bir protokoldür
• Saatlerin eşitlenmesi için UDP protokolünü kullanır
• NTP sayesinde cihaz zaman bilgisini farklı bir kaynaktan alabilmektedir.
• ULAKBİM NTP Servisi; kamuya açık 3 adet IPV4 ve 2 adet IPv6 sunucuIarı ile hizmet vermektedir
• Bu sunucular :
- ntpl.ulak.net.tr
- ntp2.uIak.net.tr
- ntp3.uIak.net.
- ntp6ntpl.uIak.net.tr
- ntp6ntp2.uIak.net.tr

*7.4.2. Taşıma Katmanı Protokolleri*
• TCP/IP taşıma katmanında temel olarak TCP ve UDP protokolleri kullanılmaktadır
• TCP (Transmission Control Protocol): TCP/lP protokol kümesinin iletim kısmını oluşturur
- HTTP, POP3, FTP, SMTP gibi birçok protokol veri iletimi için TCP'yi kullanmaktadır
- TCP verinin alıcısına hatasız bir şekilde ulaştırılmasını garanti eder.

*TCP (Transmission Control Protocol)*
• TCP ile yapılan haberleşmelerde gönderici ve alıcını IP adresleri ve aktarım için kullanılacak port numaraları belirlenir
• Internet Protokolü (IP) bağlantısız yani paketlerin hedefe ulaşmasını garanti etmediği için TCP ile birlikte kullanılır.
• TCP ile gönderilecek veri uzunluğunda bir sınırlama yoktur
• Her segment iletilecek veri ve TCP başlık bilgisi olmak üzere iki bölümden oluşur.
![[Pasted image 20240518153902.png]]
*• Source Port ve Destinatıon Port :* Veriyi gönderecek ve alacak bilgisayarların iletişim için kullanacakları port numaralarını belirler
- Her ikisi de 16 bit uzunluğundadır.
*• Sequence Number :* Gönderilecek verinin sıra numarasını belirler
- Çok büyük boyutlardaki verinin alıcı tarafta da aynı sırada birleştirilmesi için kullanılır ve 32 bit uzunluğundadır
*• Acknowlegment Number :* Alıcının veriyi aldığını onaylamak için kullanılır ve sonraki gönderilecek segmentin sıra numarasını içerir
*• Header Length :* Gönderilen veri içerisinde başlık uzunluğunu belirlemek için kullanılır ve 32 bit uzunluğundaki sözcük sayısını içerir
- 4 bit uzunluğundadır
- Buradaki değer minimum 5 ve maksimum 15 değerini içerir
*• Reserved :* Gelecekteki gereksinimler için ayrılmıştır ve varsayılan olarak o değeri içerir.

*• TCP Flags :* TCP hakkındaki denetim bilgilerini içerir
- Toplam 8 adet flag (bayrak) içermesine rağmen 6 tanesi ortak kullanım içindir
- Bunlar; ACK, SYN, FİN, ET, URG ve PSH
- ACK (Acknowledgment), Verinin karş tarafa sorunsuzca ulaştığını belirtir
- SYN (Synchronize), TCP bağlantısının kurulacağını belirtir
- FIN (Finish): TCP oturumunun sonlandırılmasını sağlar
- RET (Reset), bağlantılarda hatalar meydana geldiğinde, alıcı ve gönderici bağlantısını keserek başlangıç durumuna getirir
- URG (Urgent), urgent pointerları geçerli kılarak gelen veri parçasının öncelikli olarak işleme alınmasını sağlar
- PSH (Push), gönderilecek verinin öncelik atanarak hemen gönderilmesini sağlar.

*• Window Size :* Akış kontrolü için kullanılabilecek tampon bellek
boyutunu belirler
*• Checksum :* Başlık ve verinin hatasız olarak aktarılıp aktarılmadığım denetlemek için kullanılır
*• Urgent Pointer :* URG bayrağıyla birlikte acil olarak akarımı yapılacak veriler için kullanılır
- Acil veriler alıcı tarafından öncelikli değerlendirilir
*• Options :* Options alanının uzunluğu 32 bit ve katları şeklindedir
- Segment İçerisinde standart olarak gönderilen bilgiler dışında bilgi gönderimi için kullanılır
*• Data :* Segment içerisinde iletimi yapılacak veridir.

• TCP protokolü bağlantılı olduğu için iletim öncesi gönderici ve alıcı arasında üç aşamalı el sıkışma ile bağlantı kurulur
• A ve B cihazları arasında bağlantı kurulurken;
- A cihazı B cihazına Bağlantı istek paketi gönderir
	- Bu paketin TCP başlığında SYN=1 ve ACK=0'dır
	- Segmente ait sıra numarası x'dir.
- Paketi alan B cihazı SYN=1 ve ACK=1 bitlerini düzenleyerek kendi paketine ait sıra numarasına SEQ=y ve ACK=x+1 yaparak gönderir
- Bağlantı isteğinde bulunan A kabul paketini alır ve B'ye onay paketi göndererek bağlantı kurulur

*UDP (User Datagram Protocol)*
• TCP'den farklı olarak bağlantısız olarak iletim gerçekleştirilir
• UDP protokolü iletilen veri için alıcısına teslim garantisi sunmaz
• DNS, TFTP ve SNMP gibi istek/cevap temeline dayanan uygulamalar için kullanılır
• UDP bağlantı kurulum işlemlerini, akış kontrolü ve tekrar iletim işlemlerini yapmayarak veri iletim süresini en aza indirir
• UDP güvenilir olmayan bir aktarım protokolüdür.
• UDP üzerinden güvenilir şekilde veri göndermek isteyen bir uygulama bunu kendi yöntemleriyle yapmak zorundadır
• TCP'de başlık ve veri bütününe segment adı verilirken UDP'de datagram olarak adlandırılır
• Datagramlın segmentten temel farkı sıra numarası içermemesidir.
![[Pasted image 20240518155053.png||500]]
*• Source Port ve Destination Port :* Source port iletim süreci içerisinde alıcıdan bir cevap alınacaksa kullanılır.
*• Length :* Datagramlın byte türünden boyutunu belirler
*• Checksum :* IPV4 için opsiyonel, IPv6 için zorunlu bir alandır ve hata denetimi işin kullanılır
![[Pasted image 20240518155756.png||500]]