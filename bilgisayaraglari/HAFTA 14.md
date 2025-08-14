
*10.3 Tehditler*
- Güvenliği bozmaya yönelik tehlikeler tehdit olarak adlandırılır
- Bilgi sistemleri üzerinde güvenliği bozmaya yönelik hareketler, sisteme zarar vermek veya bilgi çalma amaçlı hareketler ise atak (saldırı) olarak adlandırılır
- Ataklar aktif ve pasif olmak üzere 2 sınıfa ayrılır.
- Aktif Ataklar
	- Bu atak türünde saldırgan trafiği dinleyerek, iletilen veriyi bozabilir, değiştirebilir veya iletimi kesebilir
	- Saldırgan sisteme zarar vermeyi, durdurmayı veya bozmayı amaçlar
	- Saldırgan dışarıdan bir kullanıcı olabileceği sistem içerisinde yer alan bir kullanıcı da bu işlemi gerçekleştirebilir
	- BU tür atak türü çoğunlukla çabuk fark edilir
	- Bunların bazıları DOS, DDoS, SYN Attack, Spoofing.
- Pasif Atak
	- Pasif atakta saldırgan sadece trafiği dinleyerek iletilen veriyi
	- okumayı, ele geçirmeyi amaçları
- Burada elde edilen bilgiler aktif atak için kullanılabilir.


- İç Tehditler
	- Ağa yetkili veya yetkisiz olarak dahil olan kullanıcılar tarafından oluşan tehditleri İçerir
	- Bu tür kullanıcılar ağ içerisinde oldukları ve normal yoldan kullandıkları için büyük riskler oluşturmaktadır
	- Bu tür tehditler genellikle bilgi sızdırmayla ilgilidir,
- Dış Tehditler
	- Bu tür tehditler çoğunlukla internet üzerinden ve bir yazılım (malware) aracılığı ile gerçekleştirilir
	- Bu tür saldırılarda çeşitli yöntemler kullanılarak saldırgan kendisini rahatlıkla gizleyebilmektedir
	- DOS, DDoS ve Exploit dış tehdit türüdür.


*10.4.1 Servis Reddetme (Denial of Service - DoS Attack)*
- Sunucuların veya sistemlerin çalışamaz hale getirilmesi için kullanılan bir atak türüdür
- Sisteme arka arkaya sürekli olarak istek gönderilmesi ve sistemin kapasitesinin aşılması sonucu sistem hizmet veremez hale gelir
- Yerel ağ üzerindeki DOS ataklarının tespiti kolaydır
- İnternet Üzerinden zombİe makinalarla yapılanlar ise zordur
- DOS ataklarının amacı;
	• Sunucuya aşırı istek göndererek sunucunun yükünün aşılması
	• Ağa sızmak ve yetkili kullanıcı erişimini engellemek,
	• Önemli bilgileri ele geçirmek.

- DoS ve DDoS (Distributed Denial of Service attack) olmak üzere 2 başlık altında incelenebilir
- DOS ataklarında tek bir kaynaktan hedefe saldırılarak sadece bir paket hedefe gönderilir
- DDoS ataklarında ise zombie makinalardan hedefe çoklu paket gönderimi gerçekleştirilir
- Gönderilen paket sayısı zombie makine sayısı orantılıdır ve çoğunlukla saldırıyı yapan makine tespit edilemez.

*Dos Atak Türleri*
- *Smurf:* Hedef alınan sunucudan bağlı olduğu ağın yayın adresine ICMP (TCP) isteği gönderilir ve ağdaki tüm bilgisayarlardan sunucuya cevap gelir
- *Fraggle:* Smurf ile aynı çalışma mantığına sahip olup UDP kullanır
- *Ping Flood (flood:baskın, bombardıman):* Hedef sistemi çalışamaz duruma getirmek için hedefe sonsuz sayıda ICMP paketi gönderilir
- Ping-of-Death: Ping işleminde büyük boyutlu paketler gönderir
- SYN Flood: TCP protokollünde kullanılan 3 aşamalı el sıkışma üzerindeki açıkları kullanır
- Land Atak: Bu atak türünde paket içerisindeki kaynak ve hedef IP adresleri değiştirilerek her ikisi de hedefin IP adresini içerir
- TearDrop: Büyük veri paketleri ağda iletilirken parçalara ayrılır ve hedefte birleştirilir.
- DNS Poisoning: DNS kayıtlarının bozularak istemcilerin isteklerinin başka sunuculara yönlendirilmesi sağlanır
- Permanent DOS Atakları: PDoS saldırıları ağ üzerindeki sunucuveya başka bir bilgisayarı hedef almak yerine ağdaki bir yazıcı, router gibi ağ cihazını hedef alır

*DoS/DDoS Ataklarını Engelleme ve Saldırı Kaynağı Tespiti*
- Sistem güvenliği İçin DOS ataklarının analizlerinin İyi yapılması ve saldırının kaynağının tespit edilmesi gerekmektedir
- DOS atklarında ilk akla gelen bağlantı hızında düşme ve mail gönderme alma gibi problemler olabilir
- DOS saldırılarını karşı korunmak için çoğunlukla trafik sınırlama ve istekleri cevaplama araçları gibi saldırı tespit sistemlerinin kombinasyonu kullanılır
- DOS veya DDoS ataklarını önlemek için firewell, switch , router, IPS, DDS araçlarının sınırlama ve güvenlik önlemleri kullanılabilir

*10.4.2 Spoofing (Aldatma) Atakları*
- Spoofing ataklarında saldırgan kendisine ait olmayan adres veya kimlik bilgileri ile saldırıda bulunur
- IP Spoofing: İnternet veya ağ içerisindeki bağlantılarda bağlantı kuran kişinin kimliğini yani IP adresini sahte bir IP adresi ile değiştirerek yaptığı bağlantılardır
- ARP Spoofing: Saldırgan ağa kendi MAC ve IP adresi yerine saldırıda bulunulacak sistemin MAC adresini bilgisini yayınlar
	- Böylece hedef sisteme ulaşması gereken bilgiler sahte MAC adresi ve kendi IP 	adresi üzerinden saldırgana ulaşır
	- Bu tür saldırılardan korunmak için MAC ve İP adresi dölüşümü için static ARP tabloları kullanılabilir,
- E-mail Spoofing: Güvenilen ve sahte bir e-mail adresi kullanılarak mail gönderimi yapılır
- DHCP Spoofing: Saldırgan ağ içerisine sahte bir DHCP yerleştirerek ağdaki  ihazlara saldırgan tarafından belirlenen ağ bilgilerinin dağıtımını sağlar
- Web Spoofing: Bu saldırı türünde gerçeğinin birebir aynısı sahte bir web sayfası oluşturularak saldırı gerçekleştirilir
- Phishing: Kullanıcılar sahte bir mail gönderilerek sahte (fake) bir siteye erişimleri sağlar
- DNS Spoofing: Sahte DNS sunucuları kullanılarak yapılan saldırılardır


*10.4.3 Sniffing (Paket Dinleyici)*
- Sniffing ataklarında saldırgan ağ üzerinde iletimi gerçekleştirilen veri paketlerinin
içeriğini izleyerek önemli bilgilere erişmeyi amaçlar
- Keylogger'da sniffer türünde bir tehdittir.

*10.4.4 Password Atakları*
- Password atakları kullanıcılara ait şifrelerinin ele geçirilmesini amaçlar
- Pasif Online Atak: Saldırgan şifreleri çalmak için kullanıcı hesabı ile doğrudan temasta bulunmaz
- Aktif Online Atak: Saldırılarda doğrudan şifre tahmini yapılamaya çalışılır
- Offline Atak: Saldırı sistem dışından yapılır
- Non-technical Attack: Teknik bilgi gerektirmeyen insanlarla yüz yüze veya telefonla etkileşimde bulunarak bilgi etme veya istenilen işlemi yaptırmadır.
- Wire Sniffing: Kablolu veya kablosuz ağ ortamlayında ağın dinlenerek şifrelerin ele geçirilmesini amaçlar
- Man in the Middle Attack: Saldırgan hedef ve kaynak arasındaki veri trafiğini kendi üzerinden geçirerek ağ üzerindeki veri paketlerini okur
- Replay Attack: Sniffing gibi yöntemlerle kullanıcı ve sunucu arasındaki paketleri takip edilirik daha sonra saldırgan tarafından tekrar sunucuya gönderilmesini temel alır
- Password Guessing: Saldırgan şifreyi bulmak için olası tüm kombinasyonları dener veya oluşturulmuş bir kelime sözlüğünü kullanabilir
- Dictionary Attack: En basit ve hızlı saldırı türüdür
- Hybrid Attack: Şifreyi bulmak için sözlük dosyası ile başlar ve Dictionary Attackla ek olarak semboller ve numaraları da sözlük dosyasında kullanır
- Brute Force Attack: Şifre bulmak için en fazla zaman harcayan saldırı türüdür
- Precomputed Hash Attack: Eğer elde edilen şifre dosyası okunabilir formatta ise saldırgan haşh fonksiyonlarını kolaylıkla tespit edebilir
- SylIabIe Attack: Şifre birden fazla kelimeden oluştuğu durumlarda kullanılır
- Rule Based Attack: Saldırgan şifre hakkında bilgi sahibi olduğunda kullanılan saldırı yöntemidir
- Rainbow Attack: Precomputed Haşh ataklarının biraz daha gelişmiş türüdür.


*10.4.5. Kullanıcı Kaynaklı Tehditler*
- Bu tür tehditler teknik bir yönü olmayan bir İç tehdit türüdür
- Bu tür tehditler kullanıcılardan kaynaklı sistemin işleyişini engelleyici veya bilgi sızdırma amaçlı tehditlerdir
- Sistemler üzerinde oluşan güvenlik tehditlerinin büyük çoğunluğu sistemleri kullanan kişilerden kaynaklanmaktadır
- Bu tehditlerin önüne geçmek için en önemli etken kullanıcılara erişim yetkileri tanımlamaktır
- Eğer her kullanıcının her şeye erişim yetkisi bulunursa donanım veya yazılım kaynaklı olarak alınacak güvenlik tedbirlerinin çok fazla bir önemi kalmayacaktır
- Ayrıca kullanıcıların güvenlik alınabilecek tedbirler konusunda bilinçlendirilmesi gerekmektedir.
- Örneğin, kullanıcı sisteme erişim için kullanacağı şifreyi çok basit seçerse bu şifre saldırganlar tarafından kolaylıkla tespit edilebilmektedir
- Snoops olarak adlandırılan bazı kullanıcılar yetkisi olmasa dahi şirkete veya şirket çalışanlarına ait çeşitli bilgileri erişmek içinbgirişimlerde bulunabilir.
- Şirket içi erişimlerin denetlenmesi ve kayıt altına alınması için güvenlik tedbirlerinin bir diğer yolu ağda DHCP sunucu kullanmamaktır
- Kullanıcı temelli güvenlik bilgilerinin merkezi bir yerde tutulması ve erişimi içi LDAP protokolü kullanılabilir.

*10.5. Portlar*
- Bilgisayar ağlarındaki port kavramı iletişimde bulunacak iki sistemin karşılıklı alışverişi için kullanılacak giriş/çıkış kapılarıdır
- Öncelikli olarak,TCP ve UDP gibi Ulaşım katmanı protokolleri (Transport Layer) portları kullanır
- Numaralandırılmış binlerce (65.535) port bulunmasına rağmen bunlardan yaklaşık 250 tanesi yaygın olarak kullanılan hizmetler tarafından kullanılmaktadır.
- Port kullanımına bir diğer Örnek mail gönderme ve almadır
- Mail işlemleri için iki porta ihtiyaç duyulur
- Bunlardan birisi mail gönderme protokolü olan SMTP için 25 nolu port
- Mail almada ise POP için 110/87 ve IMAP için 143 dür.
![[Pasted image 20240613151104.png]]

*10.6. IPsec (Internet Protocol Security)*
- IP protokolünün güvehlik ihtiyaçlarını karşılamak için geliştirilmiştir
- IPsec ağ katmanında çalıştığı için uygulamadan bağımsız olarak her veriyi şifreler
- Bu özelliği ile VPN (Virtual Private Network) teknolojisinin altyapısını oluşturmaktadır ve routerı firewall ve Ipsec uyumlu cihazlar arasında güvenli iletişim sağlar
- IPsec, IP paketlerinin iki nokta arasında iletimi esnasında kimlik doğrulama ve şifreleme sağlayarak verilerin üçüncü şahıslar tarafından dinlenmesini engeller.
- IP sec mimarisinin 3 temel Özelliği vardır;
- Bütünlük (Integrity): İletilen verinin hedefe ulaştığında kaynaktan çıktığı şekliyle olup olmadığını kontrol eder
	- Bu fonksiyon haşh algoritmaları İle sağlanır
	- MD5 (Message Digest 5) ve SHA (Secure Haşh Algorithm) veri bütünlüğü için IPsec tarafından kullanılan algoritmalardır.
		- Verileri 512 bitlik parçalar halinde şifreler
		- Veri bütünlüğü kontrolü ve şifre gizleme amaçlarıyla kullanılır
		- MD5 ile şifrelenen bir veriden orijinal veri elde edilemez
	- SHA1: Veriyi 160 bitlik haşh değeri üretecek şekil şifreler
		- Güvenlik açısından MD5'ten daha güçlüdür
		- Verileri 512 bitlik parçalar halinde şifreler.
- Kimlik Doğrulama (Authentication): İletişim kurulan iki noktanın kimlik doğrulamasını sağlar
- Kimlik doğrulama için çeşitli yöntemler kullanılabilir.
- Kimlik doğrulama yöntemleri: Preshared Key - PSK (Önpaylaşımlı Anahtar): Kimlik denetimi sağlamak için belirlenen bir sayısal değer cihazlara manuel olarak girilir ve her cihaz karşısındaki cihazın değerini bildiği güvenlik ve kimlik denetimi sağlanmış olur.


