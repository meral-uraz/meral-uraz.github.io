
**6. KABLOSUZ AĞ TEKNOLOJİLERİ**

• Kablosuz ağlarda kullanılacak standartlar 1997 yılından itibaren IEEE (Institute of Electrical and
Electronics Engineerings) geliştirilmeye başlanmıştır
• IEEE 802.11 standartları içerisinde yer almaktadır
•802.11 standardının zamanla yetersiz kalması sonucu 802.11x standartları geliştirilmiştir.
![[Pasted image 20240518173359.png||600]]
En önemlileri a, b,g   şuan kullandığımız ac
![[Pasted image 20240518173442.png||600]]![[Pasted image 20240518173658.png||600]]

*6.1.KabIosuz LAN (Wireless LAN-WLAN*
•WLAN/ mevcut LANIların kablosuz olarak oluşturulması veya kablolu LAN'a kablosuz özellik eklenmesi ile sağlanır
• Bu tür ağlarda iletişim kablo kullanılmaksızın radyo frekansları veya kızılötesi ile gerçekleştirilir
• Kablosuz LAN standartları IEEE 802.11 a/b/g/n ile belirlenmiştir
• WLAN'Iar ad-hoc (peer-to- peer) ve infrastructure (altyapı) olmak üzere 2 yöntemle oluşturur.

 *Kablosuz LAN (Wireless LAN-WLAN*
• Ad-hoc: Bu yöntemde kablosuz ağdaki her cihaz diğer ile doğrudan kablosuz bağlantı kurar.
• Infrastructure (Altyapı): BU kablosuz yöntemde merkezde bulunan kablosuz dağıtıcı (ör. Access Point) ile cihazlar haberleşir.
•WLAN üzerindeki ağ cihazlarının kablosuz ağa bağlanabilmesi için kendi üzerlerinde Wireless NİC
(WNIC - Kablosuz ağ kartı) bulundurmaları gerekir.     
• Bazı cihazlar (ör. Laptop) üzerinde bu kart standart olarak gelirken masaüstü bilgisayarlarda bulunmayabilir
• Bu tür durumlarda USB, PCI veya PCMCIA arayüzler yardımıyla harici olarak WNIC'ler kullanılabilir.
![[Pasted image 20240518173338.png||500]]

*6.2. PAN (Personel Area Network)*
• Ortalama 10 metrelik bir alanı kapsamakla birlikte ideal koşullar altında 100 metreye kadar çıkabilir
• PAN mobil cihazların birbiriyle haberleşmesinin yanı sıra internete bağlanmak veya üzerindeki internetil paylaştırmak için de kullanılabilir
• Kablolu PAN’Iar cihazın USB veya FireWire portlarıyla bilgisayara bağlanarak veya kablosuz olarak IrDA,Bluetooth, Wireless USB, Z-Waveı ZigBee, HomeRF gibi ağ teknolojileriyle de kurulabilir
• PAN için standartlar IEEE 802.15 ile belirlenmiştir.

*bilgisayarınıza fareyi küçük bir usb ile bağlarsak radyo frekansları ile iletişim sağlar.

*6.2.1. Bluetooth*
Radyo frekansları ile kablosuz olarak iletişim sağlayan bir teknolojidir
Bluetooth teknolojisi 2.4GHz frekans bandında, 24Mbpsla kadar ve 10 ile 100 metre arası mesafede iletişime olanak sağlamaktadır
Bir bluetooth cihaz bir veya birden fazla cihazla ad-hoc yöntemini kullanarak haberleşmektedir

Bluetooth cihazlar ile oluşturulan PAN piconet ve scatternet olarak adlandırılmaktadır.
• Piconet'te en fazla 8 adet master-slave ilişkisinde bulunan cihaz bulunabilir
• Piconet'e ilk bağlanan cihaz master cihaz olur ve bu cihazla haberleşecek diğer cihazlar slave cihaz olur
• Her piconette sadece bir tane master bulunur
• Bir piconet içerisinde 7 adet aktif slave bulunabileceği gibi 255 adet de pasif slave bulunabilir
• İki veya daha fazla piconetin bağlanmasıyla oluşturulan PAN türü de scatternet olarak adlandırılır.
• Bir diğer PAN teknolojisi de Skinplex dir
• İnsan cildine yakın olan kapasitif alan üzerinden iletim sağlar
• Skinplex insan vücudundan bir metreden fazla uzaklıkta bulunan cihazları bile fark ederek iletişim kurabilir
• Bu teknoloji günümüzde kapı kilitlerinin kontrolünde ve üstü açılabilir araçların parazit koruma sistemlerinde kullanılmaktadır.

*6.2.2. IrDA ( Infrared Data Association)*
• Kızılötesi ışınlar kullanılarak oluşturulan kablosuz PAN teknolojisidir
• En çok bilinen IrDA cihaz televizyon kumandalarıdır
• IrDA ile cihazların haberleşebilmesi için birbirinin görüş açısında ve kısa mesafede bulunmalıdır
• IrDA ile en fazla 4Mbps hıza çıkılabilmekle birlikte 16Mbpsı 100 Mbps, 512Mbps ve 1Gbps hızlarına çıkabilen versiyonları da geliştirilmektedir
• Görüş hattı (direct beam, line of sight),
• Yansıma (diffused beam) yöntemi ile kullanılabilir
• Doğal olarak görüş hattı yöntemi diğerine oranla daha fazla veri iletimi sağlamaktadır
• Ancak uygulamada daha geniş alanı kapsaması için yansıma yöntemi tercih edilmektedir.

*6.2.3. Wireless USB (WUSB)*
• Wireless USB, kısa mesafede ve yüksek bant genişliğinde radyo frekansları kablosuz iletim ortamı sağlar
• 3 metreye kadar mesafelerde 480 Mbps
• 10 metreye kadar mesafelerde 110 Mbps hızlarında veri transferi gerçekleştirilebilir
• WUSB oyun konsolları, yazıcılar, tarayıcıları dijital kameralar gibi donanımların bilgisayar ile kablosuz haberleşmesi için kullanılmaktadır
• WUSB mimarisi 127 cihaza kadar bağlantıya izin vermektedir
• WUSB hublar ile USB 2.o cihazlar kablosuz olarak kullanılabilmektedir.
![[Pasted image 20240518173801.png||500]]

*6.2.4. Z-Wave*
• Uzaktan kontrol gerektiren uygulamalar için tasarlanan kablosuz iletişim teknolojisidir
• Aydınlatma, eğlence sistemleri/ev elektroniği gibi cihazların kablosuz olarak kontrolü ve kendi aralarında haberleşmesi için kullanılmaktadır
• Uzaktan kumanda, yangın ve güvenlik sensörleri gibi pille çalışan cihazlar içerisinde gömülü olarak bulunmaktadır
• Panjur, termostat gibi gömülü olarak Z-Wave içermeyen cihazlara da Z-Wave kontrolü ile bu özellik eklenebilir
• Z-Wave teknolojisi akıllı ev oluşturma uygulamalarında çoğunlukla kullanılmaktadır.
• Z-Wave 9600 bps ile 40 Kbps arasında bant genişliğine sahip olup yaklaşık 30 metre mesafede haberleşebilmektedir.

*6.2.5. ZigBee*
• ZigBee güvenilir, düşük maliyetli, güç tüketimi düşük ve kablosuz PAN teknolojisidir
• Z-Wave'de olduğu gibi kontrol sistemlerinde sensörler veya cihazlar ile haberleşmeyi sağlamaktadır
• Veri İletim hızı 20 ile 900 Kbps arasında değişir
• 868 MHz - 20 Kbpsı 915 MHz - 40Kbps ve 2.4 GHz - 250Kbps olarak 3 farklı hızda çalışır
• 10 ile 75 metre aralığındaki mesafelerden kullanılabilir
• ZigBee, sensör veya giriş cihazlarından sürekli olmayıp periyodik veya aralıklı olarak veri iletimi için uygun olup bu tür cihazlara kablosuz iletim olanağı sunmaktadır
• Bu tür cihazlar kendi içlerinde barındırdıkları piller ile enerjilerini sağlamaktadır.
![[Pasted image 20240518173854.png||500]]

*6.2.6. HomeRF*
• HomeRF, ev ve küçük işyerleri için geliştirilen kablosuz erişim standardıdır
• Özellikleri Mart 19981de kurulan Home Radio Frequency Working Group (HomeRF WG) isimli çalışma grubu tarafından duyurulmuştur
• HomeRF evde bulunan PC, telefon ve diğer cihazlar arasında iletişim kablosuz olarak sağlamaktadır
• 2.4 GHz frekans bandında, maksimum 10 Mbps hızında ve yaklaşık olarak 50 metre mesafeye kadar kablosuz iletişim sağlar
• 50 metre mesafe işyerleri uygulamaları için kısa kalabilir ama ev uygulamaları için yeterlidir.
-ÖR klimalar aydınlatma sistemi vb bunları dişardan kontrol edebilmemizi sağlar

*6.3. WIMAX (Worldwide Interoperability for Microwave Access )*
• Mikrodalga Erişimi için Evrensel Uyumluluk
•Wi-Filnin çok daha büyük ve güçlü versiyonu olup IP tabanlı, geniş band kablosuz erişim teknolojisidir
• MAN'lar için tasarlanmıştır
• Sabit istasyonlar ile 50 kmı mobil istasyonlar ile 5-15km arasında kapsama alanına sahiptir.
• 75 Mbps hıza sahiptir
• 2011 yılında geliştirilmesiyle birlikte sabit istasyonlarda 1Gbps üzerinde hızlara ulaşabilmektedir
• Kablosuz iletişim teknolojisi 4G'nin bir parçasıdır.
• Wimax IEEE 802.16 standardının 2002 yılında onaylanması ile başlar ve 802.16a, 802.16d şeklinde devam eder.

*• 802.16 ile 802.16a ve 802.16d standartları arasındaki temel farklar:*
• LOS (Line of Sight - cihazların görüş açısında olması)/non-LOS olmaları
• kapsama alanları,
- sabit/mobil olması
- bant genişlikleridir
• Wimax teknolojisi IEEE 802.16e ile mobil (4G) özellik kazanmıştır ve kullanıcı hareket halinde iken hizmet alabilmektedir

• Wimax kullanılarak aynı hat üzerinden hem telefon, hem internet, hem de televizyon altyapısı kullanılabilir.
![[Pasted image 20240518174054.png||600]]
• Wimax'ın sunmuş olduğu  bant genişliği aşağıdaki uygulamalar için kullanılabilir;
• Çeşitli cihazlar yardımıyla şehirler ve ülkeler arasında geniş bant kablosuz iletişim olanağı sağlar.
• Sundugu geniş bant ve kablosuz erişimi ile DSL'e alternatiftir.
• Veri iletimi, VolP ve IPTV uygulamaları kullanılabilir.
![[Pasted image 20240518174132.png||500]]

[https://bidb.itu.edu.tr/seyir-defteri/blog/2013/09/07/pan-(personal-area-network---ki%C5%9Fisel-alan-a%C4%9F%C4%B1)](https://bidb.itu.edu.tr/seyir-defteri/blog/2013/09/07/pan-(personal-area-network---ki%C5%9Fisel-alan-a%C4%9F%C4%B1))