
**1.1. AĞ (NETWORK) NEDİR?**
Birden fazla cihazın mevcut kaynakları ortak kullanımına imkan sağlayan yapılar ağ (network) olarak adlandırılır. Ağ denilince ilk akla gelen cihazlar;
- Bilgisayar
- yazıcı
- faks
- kamera
- modem vb.

**1.2. Ağ Kullanımının Yararları**
- Güvenlik
- Veri Paylaşımı 
- Ağ Kaynaklarının Paylaşımı 
- Haberleşme 
- İnternet Erişimi 
- Oyunlar 

**1.3. Temel Ağ Bileşenleri**
- Kullanım şekline göre çeşitli ağ tipleri mevcuttur. Bunlar;
	- İntranet: Şirketlere özel ağlardır.
	- Extranet: intranet sistemlerden daha kapsamlıdır.
- Server (Sunucu) :
- Client (İstemci) :
- NIC (Network Interface Card - Ağ Arabirim Kartı) :

**1.4. Veri İletimi**
- Verinin bir noktadan diğer bir noktaya iletilmesi işlemine veri iletimi denilmektedir.
- BiIgisayarIarın internete çıkışları hem sayısal hem de analog iletişimi kullanmaktadır.
- Bilgisayarda gerçekleştirilen iletim sayısal ama telefon hattı üzerinde gerçekleştirilen iletim analogdur. 
	Parelel İletim
	- Sayısal verinin aynı anda 8 ayrı veri iletim hattı üzerinden 8 bitin aynı anda iletilmesi paralel iletim olarak adlandırılmaktadır. 
	![[Pasted image 20240309160654.png||300]]
	Seri iletim
	- Sayısal verinin tek bir veri iletim hattı üzerinden ardışık olarak iletilmesi seri iletim olarak adlandırılmaktadır.
	![[Pasted image 20240309160809.png||400]]

**1.4.2.1. Asenkron (Eşzamansız) Seri İletim**
- Asenkron iletimin kullanımı kolay olmasına rağmen verimli bir iletim yöntemi değildir.
- Asenkron iletim ile gönderilen her bilgi başında START biti ve sonunda STOP biti bulundurmak zorundadır.
- START biti her zaman O (sıfır), STOP biti 1 (bir) dir.
![[Pasted image 20240309161621.png]]-Hat üzerinden veri gönderilmediği sürece sürekli 1 verisi hat üzerindedir.

*Eşlik Biti*
- Eşlik biti ya da parity bit olarak bilinen bu bit, ikilik tabandaki bitlerin tek veya çift olması esasına göre kontrol amaçlı olarak kullanılan bittir. 

**1.4.2.2. Senkron (Eşzamanlı) Seri İletim**
- İletişimin sürekli ve hızlı olması gereken durumlarda senkron seri iletim kullanılır.
-Senkron seri iletimde START ve STOP bitleri olmaksızın veri iletimi gerçekleştirilir.
![[Pasted image 20240309173140.png]]

**1.4.3. Veri İletim Hızı (Bandwith)**
- Her veri iletim kanalının kapasitesine bandwith (bant genişliği) denilmektedir.
- Bant genişliği iletişim kanalı üzerinden belirli bir sürede taşınabilecek bilgi miktarını göstermektedir.

*Örnek :*
- 8 Mb/s bant genişliğine sahip bir ağ üzerinden 1 GB boyutunda bir veri transfer edilmek istendiğinde verinin yaklaşık transfer süresi ne olur?
1 GB = 1000 MB
1000 MB = 8000 Mb 
$$
\begin{align}
\frac{8000Mb}{8Mb/s}=1000s = \frac{1000}{60}=17dk
\end{align}
$$
