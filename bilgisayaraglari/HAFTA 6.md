
**4. LAN TEKNOLOJİLERİ VE STANDARTLAR**
• Ağ içerisindeki hız Gigabit seviyesine kadar ulaşabilir.
• Topoloji olarak
- Ortak Yol
- Halka
- Yıldız
- Örgü topolojileri kullanılmaktadır.

*4.1. IEEE 802.x Standardı*
• LAN, MAN ve FAN haberleşme standartları 198011erde IEEE (Institute of Electrical and Electronics Engineers) tarafından belirlenmiştir.
• IEEE 802 standartları komitesi kendi içinde 802.1'den 802.231e kadar çalışma gruplarına ayrılmıştır
• IEEE 802'nin içerdiği standartlar OSI referans modelinin son iki katmanı (Veri Bağı ve Fiziksel Katman) ile ilgilidir.
![[Pasted image 20240513190135.png||500]]
• En çok kullanılan LAN modeli IEEE 802.3 diğer adıyla ethernettir.
• İlk olarak XEROX tarafından geliştirilmiştir.
• Ağ üzerindeki cihazlara merkezde bulunun HUB veya Switch'e bağlantısı için NIC kullanılır.
• Ethernetler kullanılan kablolar ve iletişim hızlarına göre ayrıca sınıflandırılır.
- 10 Mbps hızında olanlar Ethernet
- 100 Mbps hızında olanlar Fast Ethernet
- 1000 Mbps hızında olanlarda Gigabit Ethernet olarak adlandırılır.
![[Pasted image 20240513191047.png||600]]

*Ethernet (IEEE 802.3)*
• Ethernet ağlar broadcast mantıksal topolojisini kullanır.
• Eğer yıldız topolojisinde merkezde switch kullanılmışsa veri sadece hedef bilgisayar tarafından görülür.
• Ethernet ağları ağ erişim yöntemi olarak 1960'lı yıllarda Hawaii Üniversitesi tarafından geliştirilen CSMA/CD (Carrier Sense Multiple Access With Collision Detection) tekniğini kullanırlar. ![[Pasted image 20240513193538.png]]
- Preamble ve SOF: Verinin iletileceği cihaz ile alıcı arasındaki saat senkronizasyonu için kullanılır
- DA (Destination Address) ve SA (Source Address): Veriyi gönderen ve alıcı adreslerini belirler
- Type/Length: Veri bir üst katmana iletilirken hangi protokolün kullanılacağı ve gönderilecek verinin uzunluğunu belirler
- Data: İletimi yapılacak veridir. Gönderilecek veri 48 byte'dan az ve 1500 byte'dan çok olmamalıdır
- PAD: İletilecek veri 46 byte'dan az ise geriye kalan kısım FAD tarafından doldurulur
- CRC: İletilecek verinin hata kontrolü İçin kullanılacak bilgi

*4.2.1. CSMA/CD*
• Ağ üzerindeki cihazlar veri gönderimi için aynı hattı kullanmakta ve bazen yoğunluktan dolayı çarpışmalar meydana gelmektedir
• Ağ üzerinde veri iletimi yapacak bilgisayarlar ağın boş olup olmadığını kontrol eder ve ağ boş ise bilgi gönderimini başlatır
• Eğer iki veya daha fazla ağ cihazı aynı anda bu işlemi gerçekleştirirse çarpışma (collision) oluşur.
• CSMA/CD half duplex çalışan ethernet sistemlerinde veri iletişimini kontrol ederek bu tür çarpışmaların önüne geçmekte, hata tanıma ve düzeltme yapmaktadır
• OSI referans modelinin Veri Bağı katmanının alt katmanı MAC kısmında yer alır.
• CSMA/CD, eski ethernet türlerinde ve HUB kullanılan sistemlerinde kullanılmıştır.

*4.2.2. «5-4-3 Kuralı» (Ağı Genişletmek)*
• Repeater ve HUB kullanılarak ağ genişletilmek ve alt ağlar oluşturmak istendiğinde bazı sınırlar vardır.
• 5-4-3 kuralı aşağıdaki üç maddeyi içerir;
- Maksimum 5 segment 
- Maksimum 4 Repeater veya HUB
- Maksimum 3 populated segment

*4.3. Token Bus (IEEE 802.4)*
• IEEE 802.4 standardı olan Token BUS IBM tarafından geliştirilen, 4 Mbps hızında, koaksiyel kablo , Token Ring teknolojisi ve Ortak yol (boş) topolojisini kullanmaktadır.
• Veri iletimi jeton ile yapıldığı için ağ üzerinde çakışma oluşmaz.
• Özellikle endüstriyel uygulamalar İçin kullanılır.![[Pasted image 20240514103257.png||512]]![[Pasted image 20240514103511.png]]

*4.4. Token Ring (IEEE 802.5)*
• IBM tarafından 1970 yılında tanımlanmış ve IEEE 802.5 ile standartlaştırılmıştır.
• OSI referans modelinin veri bağı katmanında yer alır.
•Ağın yerleşimi halka biçimdedir.
• Ağ üzerinde veri iletimi jeton (token - 3 byte) yardımıyla yapılır.
• Jeton ağ üzerinde sürekli dolanır ve veri gönderecek cihaz jeton boş ise veriyi jetona yükler ve hedef adresi ile birlikte ağa tekrar bırakır.

*4.5. FDDI (Fiber Distributed Data Interface-Fiber Dağıtık Veri Arabirimi)*
• Yüksek hızlı bir bilgisayar ağıdır ve fiber optik kabloları kullanır
• 200 Km'yi aşan mesafelerde 100 Mbps hızında veri transferi gerçekleştirir
• Mantıksal topolojisi jetonlu halka olmasına rağmen token bus standardını kullanır
• Fiber optik rrine bakır kablo kullanılan versiyonları CDDI (Copper Distributed Data Interface) olarak adlandırılır
• OSI referans modelinin Fiziksel ve Veri Bağı katmanında yer alır.
• FDDI ağlarda çift kablolama tekniği kullanılır
• Kablolardan birisi saat yönünde iletim gerçekleştirirken diğeri saat yönünün tersinde iletişim gerçekleştirir
• FDDI ağlarda 3 tür cihaz kullanılmaktadır;
- *SAS (Single Attachment Station):* SAS İle ağa eklenecek cihaz FDDI'ın sahip olduğu iki halkadan sadece bir tanesine bağlanır
- *DAS (Dual Attachment Station):* DAS ile ağa eklenecek cihaz FDDl'ın sahip olduğu iki halkadan her ikisine de bağlanır
- *Concentrator:* SAS bağlantı arayüzüne sahip cihazları veya FDDI olamayan cihazları FDDI ağa eklemek İçin kullanılır.![[Pasted image 20240514104839.png]]


**5. WAN Teknolojileri**
• Coğrafi açıdan LAN ve MAN'dan daha büyüktür
• Bir ülke veya dünya geneline yayılmış ağdır
• Ağlar ası bağlantı fiber optik kablo ile veya uydular yardımıyla gerçekleştirilebilir
• Bu ağlarda LAN'Iardan farklı olarak yönlendirici (router) cihazları kullanılmaktadır
• En çok bilinen WAN internettir
*• WAN teknolojileri 3 grupta sınıflandırılır :*
- Bağlantı Durumuna Göre;
	- Noktadan Noktaya (Peer to Peer): Kiralık hatlar(Leased Line)
	- Bulut Teknolojisi: X.25, ISDN ve Frame Relay
-  Anahtarlama Yönetimine Göre;
	- Devre Anahtarlamalı (örn: Telefon)
	- Paket AnahtarIamalı
	- Hücre Anahtarlamalı (örn: GSM Operatörleri)
- Topolojilerine Göre;
	- Hiyerarşik: Cihazlar işlevlerine göre sıralanarak bir ağaç yapısında bağlanırlar
	- Örgü: Birçok WAN yapısı örgü topolojisinde oluşturulmaktadır. Ağın yerleşiminde fiziksel bir yapı söz konusu değildir.

*5.1. Leased Line (Kiralık Hatlar)*
• İki cihaz arasından sürekli olarak sağlanan bir bağlantı yardımıyla noktadan noktaya iletişim sağlar
• Türk Telekom tarafından 2 Mbps altındaki hızlarda; kullanıcı en yakın santrale bakır kablo ile modem üzerinden bağlanır
• Santraller arası bağlantı Fiber kablo ile sağlanır
• 2 Mbit/sn üstündeki hızlarda, 10 Gbit/sn hızına kadar, cihaz ve santral arasında fiber optik hat kullanılır.
![[Pasted image 20240514192000.png||600]]

*5.2. X.25*
• ITU (Internationla Telecommunications Union) tarafından 1970'li yıllarda geliştirilen, bulut teknolojine dayalı ve paket anahtarlamalı WAN teknolojisidir
• 9.6 Kbps ile 256 Kbps arasında hızlara sahiptir ve mevcut telefon hatları, ISDN veya kiralık hatlar üzerinden kurulur
• Uzaktaki bir terminalin merkezdeki sunuçuya bağlantısı veya uzaktaki bir LANIın merkezdeki bir LAN'a bağlantısı için kullanılır.
• Güvenli olmaları nedeniyle ilk uygulamaları askeri ağlar ve havayolları olmuştur
• X.25 ağlarda iletişim gerçekleştirileceği zaman cihazlardan birisi talep gönderir ve diğer cihaz talebi kabul ederse iletişim full-duplex olarak gerçekleşir.
3 tür ağ cihazı kullanılır;
1. DTE (Data Terminal Equİpment): DTE, X. 25 ağları üzerinde iletişim kuran uç cihazlardır. Çoğunlukla bilgisayarlardır
2. DCE (Data Circuit-Terminating Equipment): DCEI modem gibi özel iletişim cihazlarıdır. D E ve PSE arasında arayüz oluştururlar
3. PSE (Packet Switching Exchange): Ağın büyük çoğunluğunu oluşturan switch/router gibi cihazlardın DTE iler arasında veri aktarımını gerçekleştirirler
• Yazıcı veya aptal terminal gibi cihazların kullanımı durumunda DTE ve DCE arasına PAD (Packet Assembler/DisassembIer) yerleştirilir.
![[Pasted image 20240514193136.png||500]]
PAD ler 3 işlevi yerine getiri;
• Buffering: DTE'den gönderilen veri buffera atılır
• Packet Assembly: DT E'den gönderilen veriyi birleştirerek DCE'ye yönlendirir
• Packet Disassembly: DCE'den gelen veriyi parçalayarak DTE'ye gönderir

• Aslında X.25 bir ağ teknolojisi olmayıp ağ cihazı İle kullanıcı arasında bir arayüz tanımlaması yapar.
![[Pasted image 20240514193305.png||500]]

• Fizikseli veri bağı ve paket katmanı olmak üzere 3 katman içerir ve bu katmanlar OSI referans modelinin Fiziksel, Veri bağı ve Ağ katmanına karşılık gelir.
- Fiziksel Katman: DTE ve DCE arasındaki bağlantı yapısı da bu katmanda tanımlanmıştır
- Veri Bağı Katmanı: İki cihaz arasında sorunsuz bir şekilde çerçevelerin iletiminin gerçekleştirilmesini sağlar
- Paket Katmanı: Bu katmanda verinin alıcısına ulaştırılması için kullanılacak olun belirlenmesi sağlanır.

• Sanal devre yaklaşımının iki farklı türünü kullanmaktadır:
- PVC (Permanent Virtual Circuit - Kalıcı Sanal Devre)
	- Sürekli ve yoğun olarak veri aktarımı yapılan bağlantılarda kullanılır ve iletişim için bağlantı kurulmasına ve a sonlandırılmasına gerek duyulmaz
	- DTE ihtiyaç duyduğu her an veri aktarımı gerçekleştirebilir
- SVC (Switched Virtual Circuit - Anahtarlanmış Sanal devre)
	- SVC sürekli olarak veri aktarımı yapılmayan bağlantılar için kullanılır ve iki DTE iletişime geçeceği zaman bağlantı kurulur.
	- İletişim sonrasında bağlantı sonlandırılır

