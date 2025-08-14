
**1.9. Ağ Mimarileri**
Ağ üzerindeki cihazların iletişim şekline göre ağlar.

*• Peer-to-Peer (Eşler Arası) Mimari*
![[Pasted image 20240506160353.png||500]]

*• CIient-Server (İstemci-Sunucu) Mimarisi*
	Ağdaki her bilgisayarın rolü farklıdır.
	Bu roller Client (istemci) ve server (Sunucu) olabilir.
	Client-Server mimarisi server yerleşimi açısından 2 katmanlı (2-tier) ve 3 katmanlı (3-tier) olmak üzere ikiye ayrılır.
	*2-Katmanlı:* Bu modelde istemci doğrudan sunucu ile iletişime geçebilir.
	![[Pasted image 20240506163338.png||500]]
	*3-KatmanIı:* Bu mimaride istemci ve sunucu arasında ara bir katman bulunur. 
		Bu katman istemciden gelen tüm istekleri alır ve kimlik doğrulama yaptıktan sonra sunucuya iletir.
		İstemci, uygulama ve sunucu olmak üzere 3 katman vardır.
		![[Pasted image 20240506163649.png||500]]

*Sunucu (Server) Tipleri*
<u>• File Server (Dosya Sunucusu)</u>
<u>• Database Server (Veri Tabanı Sunucusu)</u>
	• Örneğin : SQL Server, MySQL veya Oracle en çok bilinen veri tabanı sunuculardır.
<u>• Transaction (İşlemsel) Sunucu</u>
<u>• Web Sunucusu</u>
<u>• ISA (internet Securit and Acceleration) Server</u>
<u>• Proxy Server (Vekil Sunucu)</u>

**1.10. Coğrafi Açıdan Ağ Türleri**
*1.10.1. PAN (Personel Area Network - Kişisel Alan Ağı)*
*1.10.2. LAN (Local Area Netvvork -Yerel Alan Ağı)*
*1.10.3. MAN (Metropolitan Area Network - Metropol Alan Ağı)*
*1.10.4.WAN (Wide Area Network - Geniş Alan Ağları)*
*1.10.5. VPN (Virtual Private Network - Sanal Özel Ağı)*
- VPN kullanım amacına göre ikiye ayrılır:
	1. Remote Access ((Uzaktan Erişimli) VPN: gezici şirket çalışanlarının şirket ağına herhangi bir yerden dahil olmalarını sağlar, Ya da şirketlerin farklı ofislerinin merkezle haberleşmesi için kulanılır. 	![[Pasted image 20240509144508.png]]
	2. Site to Site VPN: farklı şirketlerin VPN üzerinden haberleşmesini ve şirketin farklı ofislerinin merkezle haberleşmesi İçin kullanılır, Remote Access VPN'den farkı VPN İşlemi gerçekleştiren iki nokta arasında VPN sunucu bulunmasıdır.![[Pasted image 20240509145529.png]]
*1.10.6. CAN (Controller Area Network)*
- Otomotiv otomasyonlarında kullanılmak üzere 1980'Ierİn ortalarında Bosch tarafından geliştirilen şeri ağ teknolojisidir
- CAN asıl olarak otomotiv sistemleri İçin araçlar İçerisindeki elektronik elemanların seri bir yol üzerinden tek bir merkezi yönetici elemana veri göndermesi prensibine göre çalışan bir sistemdir
- Örneğin: ABS, ASR gibi kısa sürede cevap verilmesi gereken sistemlerin tek bir merkezden yönetilebilmesini sağlar
- CAN kullandığı yol yapısı ve çift burgulu kablo sayesinde kalabalık kablolama yapısını ortadan kaldırır
- CAN ağ yapısında en yaygın kullanılan topoloji ortak yol olmasına rağmen yıldız ve halka topolojileri de kullanılabilir.
*1.10.7. SAN (Storage Area Network - Depolama Alan Ağı)*
- Ağ üzerindeki sunucuların depolama alanlarının yetersiz olmaya başlamasıyla ortaya çıkmış bir ağ türüdür
- SAN yüksek miktarlarda verinin depolanması ve iletimi İçin kullanılan LAN'lardır
- Sunucular ve depolama üniteleri arasında fiber optik kablo ile hızlı ve güvenilir bir bağlantı sağlar
 - Ağ üzerinde bulunan depolama birimi sadece bir sunucuya ait olmayıp ağın ortak malıdır.	![[Pasted image 20240509151531.png]]

**1.11.TopoIojilerine Göre Ağ Türleri**
- Topolojil bir ağı oluşturan cihazların fiziksel ve mantıksal yapısını oluşturur
- Ağ cihazlarının bağlantı şekilleri
	• kullanılan kablolar ve standartları
	• kabloların yerleşim düzeni
	• ağ cihazlarının ağ üzerindeki konumları fiziksel topolojiyi oluşturur
- Ağ üzerindeki cihazların haberleşme şekilleri ve iletişim protokolleri mantıksal topolojiyi oluşturur.

*1.11.1. Fiziksel Topoloji*
- Ağı oluşturan cihazların fiziksel olarak yerleşim düzeni ve kullanılan kablo türleri fiziksel topolojiyi oluşturur
- Fiziksel topolojiler :
	1. Ortak Yol
	2. Halka
	3. Yıldız
	4. Genişletilmiş Yıldız
	5. Örgü
	6. Ağaç

*1.11.1.1. Ortak Yol (BUS) Topolojisi*
• Bus topolojisinde iletişim tek bir kablo üzerinde gerçekleştirilir ve ağ cihazları bu kablo üzerine bağlanır.
• Bu tek kabloya segment (bölüm), backbone (omurga) veya trunk denilebilir.
• İnce koaksiyel kablo kullanıldığında maksimum 185 metre, kalın koaksiyel kullanıldığında maksimum mesafe 500 metredir.
• Maksimum 30 ağ cihazı kullanılabilir.
![[Pasted image 20240512194150.png||500]]
• Bu topolojide ağa bağlı her cihaz ağ üzerindeki her işlemi ve veri iletimi dinler ve kendisine ait iletim söz konusu ise verir alır.
![[Pasted image 20240512195208.png||650]]

*1.11.1.2. Halka (Ring) Topolojisi*
• IBM tarafından geliştirilmiştir ve ağın yerleşimi halka biçimdedir
• Ağ üzerinde iletilen veri hedefine ulaşıncaya kadar ağ üzerindeki her cihazdan geçer
• Çünkü ağdaki iki cihaz arasında sadece bir yol vardır
• Bu topolojide ağ üzerindeki sinyalin zayıflaması en düşük düzeydedir çünkü Sinyal uğradığı her cihazında gÜçlendirilerek bir sonraki cihaza aktarılır
• Ağ üzerinde veri iletimi jeton (token - 3 byte) yardımıyla yapılır, jeton ağ üzerinde
sürekli dolanır ve veri gönderecek cihaz jeton boş ise veriyi jetona yükler ve hedef adresi ile birlikte ağa tekrar bırakır
• Ağ yapısı merkezde bulunan MAU (Multistation Aşcess Unit) cihazı ile bu cihaza
bağlı ağ cihazlarından oluşur
• Ağ yapısı merkezde bulunan MAU (Multistation Access Unit) cihazı ile bu cihaza
bağlı ağ cihazlarından oluşur
• Çift burgulu (TP) kablolar kullanılmaktadır
• İlk halka topolojileri 4 Mbps (Cat3 UTP), sonrakiler 16 Mpbs (Cat4 ve üstü ya da STP
Tip 4) hızlarında çalışmaktadır.
![[Pasted image 20240512200941.png||500]]
![[Pasted image 20240512201114.png||650]]

*1.11.1.3. Yıldız (Star) Topolojisi*
• Günümüzde en çok kullanılan ağ topolojisidir
• Ağ üzerindeki her cihaz merkezde bulunan switch veya hub'a bağlıdır
• Ağ üzerindeki verinin dolaşımı merkezde bulunan switch ile gerçekleştirilir
• Switchlde oluşacak bir problem ağın tamamını etkiler ama ağ cihazlarında oluşan problem sadece o cihazı etkiler
• Çift burgulu kablolar kullanılır
• Ağ cihazlarının merkez cihaza uzaklığı maksimum 100 metredir.
![[Pasted image 20240512201621.png||500]]![[Pasted image 20240512201816.png||600]]

*1.11.1.4.GenişIetiImişYıldız (Extended Star) Topololisi*
• Yıldız top ojİsİnİn daha geniş ve büyütülmüş halidir
• Merkezde bulunan hub/swtich'e yeni hub /swtİch'lerİn eklenmesiyle ağın genişletilmesi sağlanır 
![[Pasted image 20240512202222.png||500]]

*1.11.1.5. Örgü (Mesh) Topolojisi*
• Ağda bulunan her cihaz diğer cihazlarla bağlıdır
• Çoğunlukla WANllarda kullanılır
• LAN'Iarda kullanıldığında ağdaki her cihazın diğerleriyle bağlanmasına gerek yoktur
• X ağdaki cihaz sayısı olmak üzere ağda kullanılan bağlantı sayısı : $$\frac{x.(x-1)}{2}$$![[Pasted image 20240512203345.png||500]]
![[Pasted image 20240512203435.png||650]]

*1.11.1.6. Ağaç (Hierarchical Tree) Topolojisi*
• Genellikle yıldız topolojisindeki ağlar olmak üzere farklı ağları birbirine bağlamak için kullanılır
• Genişletilmiş yıldız topolojisinden farklı olarak ağların birleştirilmesi için merkezde cihaza ihtiyaç duymaz
• Ortak yol ve yıldız topolojisinin karakteristik özelliklerini barındırır.
• Ağ üzerindeki cihazlar arasında hiyerarşik bir düzen söz konusudur
• Ağın en başında ağaç kökünden hatırlayacağımız root (kök) görevi gören bir cihaz vardır
• Diğer ağlardan gelen bağlantılar root üzerine yapılır
• Bu topoloji çok büyük ağların ogalarını olşturmak için kullanılır
![[Pasted image 20240512204600.png||500]]
![[Pasted image 20240512204717.png||650]]

*1.11.2. Mantıksal Topoloji*
• Mantıksal topoloji kabloların bağlantı şekillerinden ziyade ağ üzerindeki cihazların haberleşme şekilleri ve iletişim protokolleri mantıksal topolojiyi oluşturur.
Yaygın olarak 2 tür mantıksal topoloji kullanılır;
- *Yayın Topolojisi (Broadcast Topology):* Ağdaki bilgisayarların öncelik hakkı olmaksızın ağdaki tüm cihazlara veri iletimi gerçekleştirilir
	- Bu topolojide veriyi gönderecek cihaz veriyi doğrudan hedefe gönderir veya ağa bırakır ve veri hedefini bulana kadar tüm ağı dolaşır
- *Jetonlu Geçiş Topolojisi (Token Passing Topology):* Bu topolojide ağ üzerinde tüm cihazları gezen bir jeton vardır
	- Jetonun temel görevi veriyi taşımaktır
	- Jeton ağ üzerinde dolanırken her cihaza Uğrar ve gönderilecek veya teslim edilecek veriler olup olmadığına bakar.
