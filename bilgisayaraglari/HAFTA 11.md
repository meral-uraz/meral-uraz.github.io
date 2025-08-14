
**7.4.3. İnternet Katmanı Protokolleri**

• TCP/lP internet katmanında temel olarak IP (IPV41 IPv6)ı ICMPI ICMPv61 IP sec, RIP protokolleri tanımlıdır
*• IP (internet Protocol - IPV4, IPv6) :* Bir Üst katmandan gelen seğmentleri alıcıya uygun yoldan ulaştırmakla sorumludur
• Bu amaçla gelen segmentlere IP başlık bilgisi eklenir
• IPV4 adresler 32 bit olup 232 farklı adresleme yapmaya olanak sağlar
• IPv6 geliştirilmiştir ve 128 bit adresleme (2128 farklı adres) yapar. IPv6'da olan trafik işgal edici paket başlıkları kaldırılarak bir hız artırımına gidilmiştir
• Ayrıca yeni eklenen şifreleme sistemleriyle daha güvenli iletimler sağlanmaktadır.
![[Pasted image 20240526160727.png||600]]
*• İnternet Header Length :* Başlık bilgisinin uzunluğunu  belirler
*• Differentiated Services Code Point :* Başlangıçta "Type of Service (Hizmet Türü)" olarak adlandırılan bu alan şu anda bu ismi kullanmaktadır. Yeni teknolojilerde (VolP) gerçek zamanlı veri akışı gerekmektedir ve bu alan tanımlama için kullanılır.
*• Explicit Congestion Notification :* Uçtan Uca iletimi gerçekleştirilen veri için ağ tıkanıklığını bildirmek için kullanılır
*• Total Length :* Oluşturulan IP paketinin toplam Uzunluğunu (veri + başlık) bildirir
• Bir IP paketi en az 20 byte en fazla 65-535 byte uzunluğunda olabilir
*• Identification :* Bir veri parçalar halinde iletildiğinde parçaların ait veriyi tanımlamak için kullanılır 
• Böylece parçalar halinde gelen veri bu bilgiye göre birleştirilir.
*• Flags :* Bayraklar 3 bit bilgi (3 adet bayrak) içerir ve veri parçalarını tanımlamak ve kontrol için kullanılır
- DF (Don't Fragment) biti verinin parçalanıp parçalanmadığını gösterir
- MF (More Fragments) biti arkadan aynı veriye ait başka bir parça gelip gelmediğini gösterir
- Üçüncü bit yani bayrak ise saklı tutulmuştur.

*• Fragment Offset :* Parçalara ayrılarak iletilen verinin ilgili parçasının bütündeki yerini gösterir

*• Time to Live :* İletilen verinin ağ üzerinde dolaşım için harcayacağı süreyi belirler
- Yani verinin yaşam süresidir
- Bu alanda gönderici tarafından verilen değer her düğümden geçişinde bir azaltılır
- Değer sıfır olduğunda varış düğümüne ulaşmadıysa veri yok edilir

*• Protocol :* Üst katmana ait hangi taşıma protokolünün kullanıldığını belirtir
- Alıcı bu bilgiye bakarak kendisine gelen veriyi bir üst katmanda hangi protokole aktaracağına karar verir

*• Header Checksum :* Başlık içerisindeki hataları tespit etmek için kullanılır
- Başlık içerisinde hata içeren paketler yok edilir.

*• Source IP Address ve Destination IP Address :* IP paketini gönderen ve alacak bilgisayarların IP adreslerini içerir

*• Options :* BU alan protokolün daha sonraki sürümlerine kolaylık tanımak için tasarlanmıştır
- Sürüm 4 için planlanan seçenekler güvenlik, kaynak yönlendirme, yolun kaydedilmesi, zaman bilgilerinin tutulması içindir
- Bu alanın kullanım zorunluluğu olmamakla birlikte kullanıldığı zaman 32 bitin katları şeklinde olmalıdır

*• Data :* Bir üst katmandan gelen TCP segmenti (TCP başlığı + veri) veya UDP datagramını (UDP başlığı + veri) içerir.

*ICMP (internet Control Message Protocol)*
- Hata mesajları ve TCP/IP uygulamalarında mesaj trafiği için kullanılır
- ICMP aslında oluşan hata mesajlarını iletmek için IP'yi kullanmaktadır
- ICMP paketleri veri iletimi için geri bildirim sağlayarak oluşan hataları göndericiye bildirir
- ICMP kullanan komutlara örnek olarak ping ve traceroute verilebilir
- ICMP mesajlarının amacı haberleşme sırasında meydana gelebilecek problemler hakkında yönlendiricilere veya gönderici bilgisayarlara bilgi vermektir.
![[Pasted image 20240526162616.png||500]]
- Type: Mesaj tipini tanımlar
- Code: Mesaj tipinin alt tipini belirler
- Checksum: ICMP mesajının hata kontrolü için kullanılır
- Rest of Header: ICMP type ve code bilgisine göre farklılık gösterir ve oluşan hata hakkında bilgi içerir
- ICMPv6: ICMP protokolünün IPv6 adreslemeye göre kullanım şeklidir.

*IPsec (Internet Protocol Security)*
• TCP/lP protokolü çok fazla güvenlik özelliği içermemektedir
• IPsec protokolü ile ağ üzerinde veriler güvenli bir şekilde hedefe ulaştırılır
• IPsec güvenlik mimarisi
• Bütünlük (Integrity) iletilen verinin zarar görmeden alıcısına Ulaşıp ulaşmadığını kontrol eder,
• Kimlik Doğrulama (Authentication) iletişimde bulunacak cihazlar arasında kimlik  doğrulama sağlayarak diğer kullanıcıların iletişime müdahalesini engeller
• Gizlilik (Confidentiality) iletimi yapılan verinin ağ üzerinde şifrelenerek iletilmesini sağlar
• Diğer kullanıcılar (sniffer) tarafından anlaşılması veya değiştirilmesi engellenmiş olur.

*RIP (Routing Information Protocol)*
• Ağ üzerindeki yönlendiricilerin (router) birbirini otomatik tanıması için kullanılır
• Uzaklık vektörü yönlendirme algoritması temellidir
• En iyi yol seçiminde atlama sayısına bakar
• Maksimum 15 atlamaya izin verir
• 16 ve sonrası atlamalarda destination unreachable (hedefe erişilemiyor) hatası döner.
• Bu protokolde bir yönlendirici kendisine bağlı olan ağ sayısını 30 saniyede bir komşu yönlendiricilerine bildirir.

**7.4.4. Fiziksel Katman Protokoller**
• Fiziksel katmanda tanımlı herhangi bir protokol bulunmamakla birlikte ağa erişim kurallarını belirleyen
• Ethernet,
• Tokern BUS
• Token Ring
• FDDI yapıları bu katmanda kullanılır
• OSI referans modeli veri bağı katmanında yer alan protokolleri de Internet katmanı ile bu katman arasında yer almaktadır.

*ARP/ nARP(Adress Resolution Protocol/lnverse ARP)*
• Ethernet arayüzlü ağlarda veri iletimi ethernetin MAC adresi üzerinden yapılmaktadır
• TCP/IP mimarisi ise fiziksel katmana kadar veriyi sürekli olarak IP adresi
• Verinin fiziksel katman sonrası hedefe iletimi MAC adres ile yapılmakta olup ARP protokolü ile IP adresi ve MAC adresi arasında çözümleme yapılır
• Yani ARP protokolü IP adresi verilen bir ağ cihazının MAC adresini tespit eder
• Bu işlem yapılırken IP adresi karşılığı MAC adresleri içeren ARP tabloları kullanılır.
• İki bilgisayar ağ üzerinde haberleşeceği zaman MAC adresinin tespiti için ağdaki tüm bilgisayarlara alıcının IP adresini içeren ARP request packet (ARP istek paketi) gönderilir
• Bu paketi alan ağdaki tüm bilgisayarlardan kendisini ilgilendiren bilgisayar bu pakete cevap olarak MAC adresini gönderir
• MAC adresi öğrenme sürecini kısaltmak için bazı cihazlar üzerinde ARPtabloları kullanılmaktadır
• Örneğin, kullandığınız bilgisayarda "arp -a" komutu ile ön bellektebulunan MAC tablosunu görebilirsiniz.
![[Pasted image 20240526163523.png||600]]
![[Pasted image 20240526163604.png||500]]

*• HTYPE (Donanım Tipi) :* Ağ için kullanılan protokol tipini belirler. Örneğin, Ethernet için değeri içerir.
*• PTYPE (Protokol Tipi) :* ARP isteğinde bulunan protokol tipini belirler. Örneğinı IPV4 için değerini içerir.
*• HLEN (Donanım Adres Uzunluğu):* Pakette donanım adreslerinin byte olarak Uzunluğunla içerir
*• PLEN (Protokol Adres Uzunluğu)*: Pakette protokol adreslerinin byte olarak Uzunluğunu içerir
*• OPER (Operasyon):* Paketin request mi reply mi olduğunu  içerir. Eğer paket ARP request ise ı, ARP reply ise o değerini içerir
*• SHA (Gönderici Donanım Adresi):* Göndericinin fiziksel adresini (MAC) içerir
*• SPA (Gönderici Protokol Adresi):* Göndericinin IP adresini içerir
*• THA (Hedef Donanım Adresi):* Aranan alıcının fiziksel adresini (MAC) içerir
*• TPA (Hedef Protokol Adresi):* Aranan alıcının IP adresini içerir.
*• InARP (Inverse ARP):* Bir alt katman adresinden bir üst katman adresini bulmak için kullanılır
*• RARP (Reverse ARP):* Üzerinde disk barındırmayan cihazlar fiziksel adrese (MAC adresi) sahipken IP adresleri belirli değildir
*• NDP (Neighbor Discovery Protocol):* IPv6 ile kullanılan ve bağlantıda olan düğümleri bulan, komşu düğümlere yollar hakkında bilgi veren bir protokoldür
• IPv4'te ARP, ICMP ve yeniden yönlendirme bileşenleri tarafından gerçekleştirilen görevler

*• PPP (Point-to-point Protocol):* İki ağ düğümünün doğrudan bağlantısını içi kullanılan bir protokoldür
- Bağlantıda kimlik doğrulama
- Şifreleme
- sıkıştırma sağlar
- İki ağ geçidi arasında doğrudan bağlantı için kullanılan protokoldür

*• SLIP (Şerial Line Interface Protocol):* Seri port ve modem bağlantıları üzerinde çalışmak için tasarlanmış İnternet Protokolünün bir kapsüllemesidir

**7.5. Veri Paketleme (Data Encapsulation**)

• İletimi gerçekleştirilecek veri öncelikle encapsulation(paketleme) işlemine tabi tutularak iletilir
• Encapsulation işleminde her katman veriye yeni bilgiler  ekler ve fiziksel katmana kadar bu işlem devam eder • Gönderici uygulama katmanından itibaren fiziksel katmana kadar encapsulation yaparak veriyi alıcısına gönderir ve alıcı bilgisayarda bu işlemlerin tersi gerçekleştirilir.
![[Pasted image 20240526164225.png||500]]

*Veri Paketleme Adımları*
• Uygulama katmanı iletilecek taşıma katmanına kadar getirir
• Taşma katmanı gelen veriyi segment adı verilen bölümlere ayırır ve iletim için kullanılacak protokole gönderir
• Ağ katmanı veya İnternet katmanına gelen veri paketlere ayrılır ve IP başlığı eklenerek bir alt katmana gönderilir.
• Bir sonraki katmanda veri artık framelere çevrilir ve MAC adresleri eklenerek son katmanda bitlere ayrılır ve iletilir.


(BU KISIMDA SAYI SİSTEMLERİ SLAYTINI ANLATTI)
![[B_Aglari08b-Sayilar-ogr.pdf]]


 **8. IP ADRESLEME**

• TCP/IP mimarisi kullanan iki cihaz arasındaki iletişim IP adresleri ve sonrasında MAC adresleri üzerinden gerçekleştirilir
• Aynı ağ içerisindeki cihazların IP adresleri birbirinden farklı ama aynı yapıda (IP sınıfı) olmak zorundadır
- Statik IP adresleme
- Dinamik IP adresleme

• Statik IP atamadaki en büyük sıkıntı aynı IP adresinin birden fazla cihaza atanabilecek olmasıdır.

**8.1. IPV4 Adresleri ve Sınıflar**

• IPV4 adresler 32 bitten oluşmaktadır
• 32 bit 4 oktet (8 bit) ile ifade edilmektedir
• 232 adet yaklaşık 4-3 milyar farklı IP adresi oluşturulabileceğini gösterir
• Bu adreslerin bir kısmı özel kullanım (yaklaşık 18 milyon adres) ve çoklu yayın (yaklaşık 270 milyon adres) için ayrılmıştır
• IPV4 adresleri kullanılırken ikili sayısı sistemi yerine onluk sayı sistemi ile ifade edilir
• Her oktet 8 bit değer içerdiği için o (00000000) ve 255(11111111) arasında değer alabilir.
• 192.168.10.120 (11000000.10101000.00001010.01111000)
• IPV4 ile oluşturulan IP adresleri
- Network ID kısmı oluşturulan ağı tanımlayan numarayı
- Host ID ise ağ içerisindeki bilgisayar veya ağ cihazının IP adresidir

• Her adres sınıfı içerisinde oluşturulabilecek ağ sayısı ve bağlanabilecek cihaz sayısı oktetllerin ayrılma şekline göre değişmektedir.

![[Pasted image 20240526165135.png||400]]

• Network ID belirlenirken Host ID için ayrılan oktet kısmın alacağı minimum değer kullanılır
• Host ID yani IP adresi 192.168.1.5 olan bir cihazın bulunduğu ağ C sınıfı IP kullandığı için Network ID değeri ilk 3 oktet olur ve Network ID’si
192.168.1.0'dır
• IP aralığı 192.168.1.1 ile 192.168.1.254 arasındadır.

*Yayın (Broadcast) ID*
•Ağ üzerindeki tüm cihazlara mesaj göndermek için kullanılır
• Host ID için kullanılabilecek en son değerler Yayın ID’yi Oluşturur
• Host ID yani IP adresi 192.168.1.5 olan bir cihazın bulunduğu ağ C sınıfı IP kullandığı için Host ID son oktet olur ve Yayın ID değeri 192.168.1.255 dir.
