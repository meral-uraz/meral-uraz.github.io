
*AĞ MASKESİ (SUBNET MASK)
- 255.x.x.x şeklinde kullanılan IP adresleri ağ maskesini göstermektedir.
- Ağ maskesil oluşturulan ağı tanımlamak veya alt ağlara bölmek için kullanılmaktadır.
- Oluşturulan bir ağın ağ maskesi Network ID bitlerinin 1, Host ID bitlerinin 0 yapılması ile elde edilir.
- IP adresi 192.168.1.5 olan bir cihaz ise
- C sınıfı IP kullandığı için Network ID ilk 3 oktet
- Host ID son oktetdir
- Bu tür bir ağın ağ maskesi 255.255.255.0 olur.

*Ağ Geçidi (Gatway)*
- Ağ geçidi bir ağdan diğer ağa geçişler için kullanılır.
- Örneğin, bir bilgisayar internete çıkarken bilgisayarırüğ geçidi numarası için internete çıkış sağlayan modemin IP adresi kullanılır.

*IP Sınıfları*
- A, B, C, D ve E olmak üzere 5 IP sınıfı tanımlanmaktadır.
- A, B ve C sınıfı IP'ler Network ID ve Host ID gibi ağ içi adreslemeler için kullanılır.
- D sınıfı IP'ler multicast kullanım için ayrılmıştır.
![[Pasted image 20240612144313.png]]
- Aynı IP adres sınıfında birden fazla ağ oluşturulabilir.
- A sınıfı IP'ler ile 125 farklı ağ oluşturulabilir.
- A sınıfında iki farklı ağdaki bilgisayarlar birbirini göremeyecektir.

*8.1.1 A Sınıfı Adresler*
- A sınıfı adreslerde 4 oktetlden ilk oktet networklu, diğer 3 oktet networkldeki host sayısını belirler.
- Ağ üzerinde çok fazla host içeren ağ yapıları için uygundur.![[Pasted image 20240612145811.png]]
- A sınıfı adreslerde Network ID kısmının ilk biti 0'dır. Geriye kalan 7 bit Network ID için kullanılır.
- 2⁷ =128 adet network oluşturulabilir gibi görünse de A sınıfı adreslemede 2⁷-2=126 adet Network ID yani ağ tanımlanabilir.
- Host ID'e ait bitlerin tamamı «o» yapıldığında elde edilen sonuç Network ID için kullanılır.
- Bitlerin tamamı 1 yapıldığında elde edilen sonuç Yayın ID için kullanılır.![[Pasted image 20240612152440.png]]!![[Pasted image 20240612152623.png]]
-  U oktet'i ı ile 126 arasında olduğu için A sınıfı bir IP'dır.
- İlk okted IP aralığı 0000 0001 ile 0111 1110 arası. 
- 1.0.0.1 ile 126.255.255.254 arası
- 00000001 00000000 00000000 00000001

*8.1.2 B Sınıfı Adresler*
- ilk iki oktet network'u
- diğer 2 oktet network'deki host sayısını belirler
- Çok fazla host içermeyen orta veya büyük ölçekli işletmeler için uygundur
- B sınıfı adreslerde Network ID kısmının ilk iki biti 1 0'dır.
- Geriye kalan 14 b Network ID için kullanılır
-  2¹⁴-2=16.382
- 16 bit bit Host ID ile 2¹⁶-2=65.534 adet host tanımlanabilir.
- Network ve Yayın ID leri çıkarılmalıdır.
![[Pasted image 20240612154350.png]]
- İlk iki oktedin IP aralığı 1000 0000 ile 1011 1111 arası 
- 128.0.0.1 ile 191.255.255.254 arası
- 10000000 00000000 00000000 00000001
- 10111111111 111111111111 111111111111 11111111110
![[Pasted image 20240612154637.png]]
- U oktetli 128 ile 191 arasında olduğu için B sınıfı bir IP'dir
- Network IDlsi için Y ve Z oktetlerine ait bitler 0 sıfır yapılır
- Yayın ID'si için Y ve Z oktetlerine ait bitler 1 yapılır.

*8.1.3 C Sınıfı Adresler*
- C sınıfı adreslerde 4 oktet'den
	- ilk 3 oktet network'u
	- diğer 1 oktet network'deki host sayısını belirler
- Çok fazla host içermediği için küçük ölçekli ağlar için uygundur.
- C sınıfı adreslerde Network ID kısmının ilk ü biti 1 1 0 'dır
- Geriye kalan 21 bit Network ID için kullanılır
- 2²¹-2= 2.097.152 adet network oluşturulabilir
- 8 bit Host ID i e 2⁸-2=254 adet host tanımlanabilir
 - Network ve Yayın ID leri çıkarılmalıdır.
![[Pasted image 20240612162849.png]]
 - İlk üç oktedin IP aralığı 1100 0000 işe 1101 1111 arası 
 - 192.0.0.1 ile 223.255.255.254 arası
 - 11000000 00000000 00000000 00000001
 - 1101111111 111111111111 111111111111 111111111110
![[Pasted image 20240612163518.png]]
- U oktet'i 192 ile 223 arasında olduğu için C sınıfı bir IP'dir
- Network ID'si için Z oktetine ait bitler 0 sıfır yapılır
- Yayın ID'si için Z oktetine ait bitler 1 yapılır.

*8.1.4 D ve E Sınıfı Adresler*
- D sınıfı adresler multicast yani birden fazla hoşta bilgi göndermek için kullanılır
	- D sınıfı adreslerin ilk okteti 224 ile 239 arasındadır
	- İlk oktete ait ilk 4 bit 1110 şeklindedir
	- D sınıfı adresler özel amaçlar için kullanılmaktadır
- E sınıfı adreslerin ilk okteti 240 ile 255 arasındadır
	- İlk oktete ait ilk 4 bit 1111 şeklindedir
	-  E sınıfı adresler gelecekteki ihtiyaçlar ve araştırmalar için ayrılmıştır.
![[Pasted image 20240612165139.png]]
- D Sınıfı adreslerde İlk oktedin IP aralığı 1100 0000 ile 1110
	- 224.0.0.1 ile 239.255.255.254 arası
	- 11100000 00000000 00000000 00000001
	- 1110111111 111111111111 111111111111 111111111110
- E Sınıfı adreslerde İlk oktedin IP aralığı 1111 0000 ile 1111 1111 arası
	- 240.0.0.1 ile 255.255.255.254 arası
	- 11100000 00000000 00000000 00000001
	- 11111111 11111111 11111111 111111110

*Özel IP Adresleri*
- IPV4 de bulunan sazı IP aralıkları ise özel amaçlara adanmış olduğundan internet üzerinde kullanılmamaktadır
	- Ağ içinde mesajlaşma amacı ile kullanılan 155.101.0.0 ile 155.101.255.255 adresleri
	- İç ağlarda lokal IP dağıtımları için ayrılmış üç grup IP aralığı
		- 10.0.0.0 İle 10.255.255.254 arası (A sınıfı)
		- 172.16.0.0 ile 172.31.255.255 arası (B sınıfı)
		- 192.168.0.0 ile 192.168.255.255 (C sınıfı)
		- 127.0.0.0 ile 127.255.255.255 arası (Yerel çevrim)
![[Pasted image 20240612170625.png||500]]

*8.2 Altağ (Subnet) Oluşturma*
- IP adres sınıflarının kendi içerisinde parçalanarak yeni oluşturulan networkler, alt ağlar (subnets) olarak ifade edilmektedir
- Bir IP sınıfı üzerinden alt ağlar oluşturulurken o sınıfa ait Host ID kısmı bitlerinin bir kısmı Network ID olarak kullanılır.

*Altağ Maskesi (Subnet Mask)*
- Bir IP adresinin kaç bitinin ağlı kaç bitinin hoştu tanımladığı altağ maskesi ile ifade edilir
- Bir IP adresine ait subnet mask adresi network kısımları için 1, ağ kısımları için 0 bitini içerir
- Örneğin, 192.168.1.10 IP adresi C sınıfı bir adrestir ve ilk 3 oktet (24 bit) network'ü, son oktet (8 bit) hostları göstermektedir
- BU durumda altağ maskesi 255.255.255.0 yani 11111111 11111111 11111111 0000000 olacaktır.
- Ayrıca, bir cihazın hangi ağa ait OldUğUnU anlamak için sadece IP adresi yetedi olmamaktadır.
- IP adresi ile altağ maskesi AND işlemine tabi tutularak ağ adresi (Network D) bulunur
- AND işleminde sadece 1 AND 1 işleminin sonucu 1'dir
- Diğer durumlarda işlem sonucu 0 olacaktır
- Örneğin, IP adresi 192.168.1.10 ve ağ maskesi 255.255.255.0 oolan bir cihazın ağ adresi  192.168.1.0 olacaktır
- Özellikle alt ağlarda bu duruma dikkat edilmelidir.

*Ödünç Bit Almak*
- Altağlar oluşturulurken host kısmından belirli bir miktar bit ödünç alınarak network bitleri kısmına dahil edilir
- Ödünç alınan her bit 2ⁿ adet ağ oluşturmak için kullanılır
- Örneğinı A sınıfı bir adres bloğundan 4 adet alt ağ oluşturulacaksa 24 bit olan Host kısmından 2 bit alınarak network kısmına dahil edilir
- Yani, network kısmı 10 bit, host kısmı 22 bit olur.![[Pasted image 20240613123750.png||400]]
- Oluşturulan alt ağların Network ve Yayın ID'leri: ![[Pasted image 20240613124200.png||500]]

*Örnek 1:* 192.168.10.20 IP adresine sahip bir bilgisayar ile 192.168.10.40 IP adresine sahip başka bir bilgisayar (her ikisinin de subnet mask'ı 255.255.255.192)  haberleşebilir mi? 
![[Pasted image 20240613124845.png||400]]
- Network ID leri aynı olduğundan haberleşirler.


*Örnek 2:* 192.168.10.20 IP adresine sahip bir bilgisayar ile 192.168.10.70 adresine başka bir bilgisayar (her ikisinin de subnet masklı 255.255.255.192 haberleşebilir mi?
- Kaç alt ağ tanımlanmıştır?
![[Pasted image 20240613131616.png||450]]
![[Pasted image 20240613131748.png||500]]
 ![[Pasted image 20240613131848.png||500]]
- IP adreslerinin yanında "/" işaretinden sonra değer yazılı ise bu değer Network ID için kullanılacak bit sayısını göstermektedir.
- Yani altağ maskesi için bit değeri 1 olan bitlerin sayısını gösterir.
- Örneğin, 192.168.10.5/27 şeklinde bir kullanım Network ID için 27 bit kullanıldığını yani 3 bit ödünç alındığını göstermektedir
- Standart C sınıfı bir ağda bu değer ne olur?
	- 24 olur, 194.27.49.12/24 alt ağ maskesi de 255.255.255.0 olur.

![[Pasted image 20240613132913.png||500]]
![[Pasted image 20240613133533.png||500]]
![[Pasted image 20240613133718.png]]
![[Pasted image 20240613133759.png]]

*8.3. IPv6 Adresleme*
- İnternet protokolü sürüm 6 (IPv6) internetle bağlanacak cihazların adreslemesi ve iletişimi için geliştirilen yeni nesil internet protokolüdür
- IPv41un yetersiz kalması sorıUCU IPv6 çıkartılmıştır
- IPv6 128 bit adresleme yapısına sahiptir
- Ayrıca, trafik yoğunluğunu artıran bazı başlık bilgileri IPv6'da çıkartılarak hız artırımı sağlanmıştır ve yeni şifreleme yöntemleri ile güvenlik düzeyi artırılmıştır
- IPv6 iletimi gerçekleştirilen veri ses veya görüntü ise veri paketlerine öncelik atanarak iletim gerçekleştirlir.

- IPv6'nın getirdikleri;
	- Genişletilmiş adres alanı
	- Yeni Güvenlik Özellikleri
	- Sadeleştirilmiş Başlık Yapısı
	- Gelişmiş Servis Kalitesi Özellikleri
	- Otomatik Adres Yapılandırılması
	- Komşu Düğümlerle Etkileşim İçin Yeni Protokol (ICMPv6)
	- Dolaşılabilirlik
	- Genişletilebilirlik
![[Pasted image 20240613134208.png||400]]
- Version: Kullanılan IP versiyonunu gösterir ve değeri 6'dır.
- Trafffic Class: İletimi gerçekleştirilecek paketlere öncelik atamak için kullanılır
	- IPv6 tavsiyesi FTP için 4, Telnet için 6, haber için 1 kullanılmasıdır.
- Flow Label: İletilecek veri paketinin özellikleri veya isteklerini belirlemek için kullanılır
	- Böylece, geçtiği yönlendiricilerin paketin isteğini cevaplaması sağlanabilir.
- Payload Length: Başlık alanı (40 byte) hariç toplam ne kadar veri olduğu belirtilir.
- Next Header: Bu paketten sonra paket gelip gelmeyeceğini belirler
- Hop Limit: İletilen verinin geçebileceği düğüm sayısını belirtir
	- Eğer veri burada belirlenen sayı kadar düğümden geçti halde hala hedefe ulaşamamışsa yok edilir.
- Source Address ve Destination Address: Bu alanlar veriyi gönderen ve alan noktalara ait adresleri içerir
	- IPv6 adresler 128 bit olduğu için bu alanlar da 128 bittir.
![[Pasted image 20240613134647.png]]

*IPv6 Adres Mimarisi*
- Bir IPv6 adres 128 bit olup temel olarak ikilik düzende gösterildiğinde 128 adet 1 veya 0'ın birleşiminden oluşmaktadır.
- Bu bitler 16 bituzunluğunda 8 bölümden oluşmaktadır
- Bu tür gösterimlerin kullanıcılar tarafından anlaşılması zor olduğu için daha anlaşılır şekilde onaltılık sistemde gösterilmektedir. 
![[Pasted image 20240613134843.png||300]] ![[Pasted image 20240613134902.png||200]]
- IPv6 adreslerde Netwvork ID yani ağ adresinin kaç bit olduğu IPv6 adresinden sonra"/" ile belirtilir
- Onaltılık sayı düzeninde gösterilirken her 16 bitlik blok arasına ":" konulur

*8.4 CIDR (Classles Inter-Domain Routing)*
- CIDR, IPV4 İle oluşturulacak IP adresi sayısının yetersizliği ve IPv6 İle elde edilebilecek IP adresi sayısının fazlalığı sonucu ek yük getirdiği için oluşturulmuş bir yapıdır
- Yani, yeni bir adresleme tekniği sunar
- Örneğin, internet servis sağlayıcılarından belirli bir IP bloğu alındığında (192.168.10.2 /28) IP adresinin ait olduğu sınıfın tamamı yerine sadece belirli bir kısmını müşteriye tahsis eder.
- Aslında, CIDR değeri olarak adlandırılan kısım IP adresinden sonra şeklinde yazılan kısımdır
- Bu kısım alt ağlara bölmede olduğu gibi IP bloğunun kaç bitinin network için kullanılacağını belirtir.

*9.1. IPtv (internet Protocol Television)*
- Paket anahtarlamalı bir ağ üzerinden televizyon hizmetlerinin IP kullanılarak gerçekleştirilmesine IPtv denilmektedir
- IPtv'de temel olarak TCP/IP protokolü üzerinden görüntü ve ses aktarımı gerçekleştirilir.
- IPtv hizmetleri genel olrak 3 grupta sınıflandırılır. Bunlar;
	• TV (Canlı TV Yayını):
	• Time-Shifted TV (Zaman Kaydırmalı TV):
	• Video on Demand (VOD - İsteğe Bağlı Video):
- IPtv'nin geleneksel TV sistemlerine göre en önemli avantajı her kullanıcının farklı bir yayım izleyebilmesi
	- çift yönlü İletişimi desteklediği için kullanıcının yayın üzerinde durdurma
	- ileri ve geri sarma gibi özellikleri kullanabilmesidir
- İnternet servis sağlayıcılar kullanıcılara "Tripleplayll paketi adı altında görüntü, veri ve telefon iletişimini aynı paketten sunabilmektedir.
- IPtv yayınları bilgisayar üzerinden izlenebileceği gibi özel cihazlar (IPtv alıcıları - Set Top Box) ile de izlenebilir
- Türkiye'de Telekom tarafından sunulan Tivibu Ev, genişbant internet bağlantısı üzerinden IPtv alıcısı ile sunulan IPtv sistemidir. 
![[Pasted image 20240613140811.png||400]]

*9.2 VolP (Voice over İP)*
- IP protokolü üzerinden ses iletiminin gerçekleştirilmesidir
- •VoIP teknolojisi paketlenmiş ses verilerinin gerçek zamanlı olarak ve taşıma protokollerini (TCP, UDP) kullanılarak ağ üzerinden iletilmesini sağlar
- VolP servislerinin bazıları sadece bilgisayar veya VolP cihaz üzerinden çalışırken bazı VolP servisleri adaptör yardımıyla normal telefonlarında VolP üzerinden görüşmesine izin verir.
- VolP sistemi temel olarak sesin sıkıştırılarak gönderilmesi ve alıcıya ulaştırılması olarak tanımlanabilir
- Sesin sıkıştırılmasında
	• G.729 (8 kbps),
	• G.723 (5-3 ve 6.3 kbps),
	• G.726 (32 kbps)ı
	• G.711 (64 kbps) gibi algoritmalar kullanılmaktadır
	• En çok sıkıştırma sağlayan G. 723 olmasına rağmen
	• en çok G. 729 codeci
	• Nedeni ses kalitesinden çok fazla ödün vermek istenmeyişidir.

