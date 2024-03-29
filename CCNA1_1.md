# 1 GEÇMİŞTEN GÜNÜMÜZE İNTERNET
|“Fixed” Computing   |Bring Your Own Device   |Internet Of Things   |Internet Of Everything   |
|---|---|---|---|
|Eskiden cihazlara kullanıcının fiziksel olarak gitmesi gerekirdi. Bilgisayarlar sabittiler.   |Cihazların kolayca taşınabilir hale gelmesiyle şirketlerde ve kurumsal ofislerde kişisel cihazların kullanılması trendidir. <br />**-Güvenlik risklerini artmıştır.** <br />**-Ağ yöneticilerine yeni yük binmiştir** </span>|Age of devices olarak bilinen teknolojik gelişmedir. Fiziksel objelerin, toplu olarak ve internet yoluyla iletişimini gerçekleştirme teknolojisidir.	   |İnsanlar, işlemler, veriler ve cisimler gibi birçok  nesnenin internet aracılıyla iletişim kurması teknolojisidir.   |

**İnternetin Temel Gelişim Aşamaları**
- HTTP (Hypertext-Transport-Protocol) Dönemi: Statik text bazlı sitelerin olduğu dönem olarak tarif edilir.
-  WEB 2.0 Dönemi: Interaktif, dinamik Web sitelerinin yaygın olmasıyla oratya çıkan dönemdir.
-  IoT (Internet of Things) Dönemi: Yalnızca insanlarla değil birbirliyle konuşan cihazların oluşturduğu (Machine-to-Machine, M2M), insan kaynağına gerek duymayan otomasyonla çalışan sistemlerin olacağı dönemdir.

**Local Area Networks-LAN (Yerel Alan Ağları)**
-	İki ya da daha fazla node'un haberleştiği dijital ortama **Network** denir.
- 	Aynı coğrafyada/bölgede bulunan ağlara **LAN** adı verilir, "Same location" olarak ifade edilir.
**Çeşitli Boyutlu Ağlar:**
- SOHO (Small Home Office) ağları
- Şirket ağları
- Global ağlar

***

**Ağ Bileşenleri: Client-Server İlişkisi | Host Kavramı | Intermediary Devices | Network Media**

- 	Ağda bulunan son kullanıcı cihazları **host** ya da **end points** kavramlarıyla  ifade edilir. Pcler, ağa bağlı yazıcılar, VOIP’ler, telefonlar vb. gibi IP üzerinden haberleşme yapan end point'ler **NIC (Network Interface Card)** ile networke bağlanırlar. NIC’in diğer bir adı da **Ethernet Card**’dır.

*NIC (Network Interface Card), cihazların yerel ağa bağlanması sağlayan bileşendir. Neredeyse her host cihazında NIC yani Ethernet kartı bulunur. NIC'ler bazen anakartın içerisine gömülü olarak bulunabilir.*

- **Server** dediğimiz aslında bir host işlemidir. İçerisinde diğer hostların kullanacağı hizmetleri bulundurduğu için bu ismi almıştır. **Client** ise ağ yoluyla serverdan hizmet  **isteyen** cihazlara denir. 

*Server bir cihaz değildir, bir işlemdir. Server işleminin daha hızlı/optimize yapılnası için server bilgisayarları geliştirilmiştir.*

- Cihazların server işlemini yapmak için özel bir server bilgisayarı olma zorunluluğu yoktur, günlük kullanımdaki host ya da end user cihazları da server işlemlerini kısıtlı kapasitede de olsa yapabilmektedir. Bu duruma **Peer-to-Peer (P2P)** denir. Cihaz P2P sırasında **hem server hem de client** olarak davranır. Torent bağlantılarında kullanılan teknoloji P2P'dir. Ayrıca kripto para benzeri teknolojilerde de P2P'den yararlanılır.

*Peer-to-Peer sorumluluk almaktır: Kurulumu ve kulanımı kolaydır ve karmaşıklığı azdır. Host-Client yöntemine göre maliyeti düşüktür ve basit görevler için kullanışlıdır, ancak P2P'nin merkezi yönetimi yoktur bu sebepten dolayı güvenli ve ölçeklenebilir değildir ve performans düşüklüğü yaratır. Ayrıca serverların 7/24 açık olması ve cevap verebilir olması beklenir.*

- Switch, Router, Wireless Router, ve Firewall etc. gibi ağ cihazlarına **intermediary devices** (ara cihazlar) denir. Intermediary device'ların temel görevleri host cihazlarını ağa bağlamak ve ağ içerisinde yönlendirmektir. Temelinde 2 intermediary cihaz vardır, bunlar router ve switch'tir.

-  **Switch:** Hostları **kablolu** şekilde yerel (local) networke dahil eden cihazdır. Kablosuz cihazlar switche bağlanmak isterse önce **Access Point** adlı cihaza kablosuz şekilde hava aracılığıyla (air) bağlanır, bağlantıdan sonra access point bu bağlantıyı switche kablolu şekilde aktarır.
Geleneksel switch cihazlarının NIC'leri bulunmamaktadır, bu sebepten dolayı MAC adresleri yoktur.
    - Cisco Catalyst bir switch cihazıdır. 

*Access Point (Kablosuz Erişim Noktası) switch felsefesi ile çalışır.*

- **Router:** Network'ün en temel taşı bu cihazdır. Farklı networkleri birbirine bağlayan cihazdır. Ağdaki paketlerin takip etmesi gereken yolu belirler.
    
    - Cisco ISR bir router cihazıdır.

#####  *Foreshadowing: BGP protokolü ağ hattında kısa yolu bulmaya yarayan protokoldür.*

- **Firewall:** Güvenlik özellikleri arttırılmış router cihazları olarak özetlenebilir. Ağın trafik akışını, belirlenmiş ve konfigüre edilmiş kurallara uygun olarak denetler. Günümüzde kullanılmaya başlanan daha kalietli yeni filtremeli özelliklere sahip firewallara **next-generation firewalls** denmektedir.
    - Cisco ASA ve Cisco Firepower birer firewall cihazıdır.

*Burada bahsettiğimiz cihaz firewall, ağdaki cihazların içersinde bulunan yazılımsal firewalllar farklıdır. Yazılımsal firewalllar **host-based firewall** olarak adlandırılır.*

- Ağlarda iletişimin gerçekleştiği ortama **Medium, Media** ya da **Network Media** denir. Bir Network Associate medium tasarlarken göz önüne bulundurduğu şeyler şunlardır:

Kurulum **maliyeti** gereksiz yere yüksek olmamalıdır.
Kurulumda kullanılacak **kabloların** maksimum **uzunluk** kapasiteleri göz önüne alınmalıdır.
Kurulumun gerçekleştirileceği ağın maksimum  data taşıma **kapasitesine** dikkat edilmedilir.
Kurulumun gerçekleştirileceği **environment** (çevresel özellikler) dikkata alınmalıdır, örneğin kablosuz access point cihazının duvarların arkasına gelecek şekilde konulmaması gibi.

Ayrıca bazı media tipleri  ise şunlardır: 

**Copper Wire**, elektirik ile veri iletmi yapar, **UTP (Untwisted Shielded Pair)** kablo kullanır.
**Fiber Optic**, ışıkla veri iletim yapar. Single Mode ve Multi Mode gibi alternatifleri vardır.
**Wireless İletim**,hava yoluyla iletim yapar. Elektromanyetik dalgalar kullanır.

***

**Sınava Özel Bazı Notlar:**   
- Kamusal alanda kablo çekmek yasaktır. Yalnızca **ISP (Internet Service Provider)** kablo çekme/ kablolama hakkına sahiptir. ISP'lerin çektiği özel ağlara **leased lines** denir. Leased Lines (private line), kurumların telekominikasyon şirketleri aracılığıyla kiraladığı hususi, özel ağlardır.
-   Router farklı networkleri birbirine bağlar. Yani router'ın farklı interfaceleri farklı ağlara bakar, genelde bir interface ISP'ye diğer interface ise yerel ağa bağlıdır. 
-   Modem dediğimiz cihazlar temelinde içerisinde access point, switch, router ve DHCP server bulunan routerlardır.
-  Özel, fiziksel ağa bağlanma portlarına  **Interface** denir.
*Port ve Interface birbirinin yerine kullanılan terimlerdir ancak TCP/UDP protokollerindeki portlarla karıştırılmamalıdır.*
-  End device'ları networke bağlayan fiziksel porta **NIC** denir.
-  İki farklı ağı birbirine bağlanmayacaksa router alınmamalıdır.
- Eskiden telefon ve internet ağları ayrıydı. Günümüzde  ise bu ağlar birleşik şekildedir, bu duruma **Converged Networks** denmektedir. Converged Networks siber güvenlikçilerin işini zorlaştırmaktadır.

***

**Ağ Tipleri:** 

- LAN (Local Area Network): Yerel ağlardır.
- WAN (Wide Area Network): Uzak ağları birbirine bağlamak için kullanılır. LAN'ların ISP kullanılarak bağlanmasıyla WAN oluşur.
- Internet: Temelinde bir WAN'dır. Dünya üzerindeki WAN'ların birleşmesiyle oluşan bir ağdır. 
- Intranet: Kurum içi ağdır. Kurumun bütün iç LAN'ları WAN kullanılarak bağlanmıştır.
- Extranet: Kurum içerisindeki özel ağların diğer kurumların ağlarına bağlanmasıyla oluşturulmuş kısıtlı, kontrollü ağdır.
- MAN (Metropolitan Area Network): LAN'lardan büyük, WAN'lardan küçük, kentlerde ya da Universitelerde bulunan hatlara verilen genel isimdir.
- WLAN (Wireless LAN).
- SAN (Storage Area Network): Sunucuların, hard disk sunucusu ile olan ağlarına SAN denmektedir. Günümüzde ise hard diskler sunucuların içerisinde bulunmaktadır bu teknolojiye **hyperconversion** denilmektedir . 

Unutulmamalıdır ki her ağ internete bağlı olmak zorunda değildir. Askeri hatlar, devlet kurumlarına bağlı özel ağların internetle bağı yoktur.

***

**Reliable networks**
Bir networkü güvenilir yapan 4 temel kavram vardır bunlar:
**1 - High Fault Tolerance**
- Ağ sistemindeki bazı routerlar ve switchlerin çökmesine rağmen sistemin sorunsuz çalışmaya devam etmesi yüksek "hata tahammüllü" ağ olduğunu gösterir.
- Hata tahammüllü yüksek sistemler **redundant** sistemler  olarak ifade edilir, kelime anlamı olarak yedek cihazı olan sistemler demektir.

 **2 - Scalability of Network**
- Kurulan ağın, gelecekte büyüme işleminde sorun çıkarmayacak şekilde hazırlanması demektir, kelime anlamı olarak büyütülebilirlik olarak çevrilebilir.

 **3 - Quality of Service (QoS)**
- Ağlarda düşük ping olmalıdır.
- Bazı durumlarda bazı cihazlara öncelik verilmelidir.
- "Reliable delivery" gerçekleştirilmelidir.
- "Low latency" olmalıdır, yani gecikme olmamalıdır.
- Ağ üzerindeki data isteme durmunun data tahsilinden yüksek olmasından kaynaklı trafiğe ya da sıkışmaya network **congestion** denmektedir.

*Not: Converged network kavramı ile congestion karıştırılabilinmektedir. **Converged network** aynı network üzerinden farklı tipte iletişim bilgilerinin geçebildiği (video, data, sound vb.) networkleri ifade ederken network congestion ağdaki yüksek data trafiğinden kaynaklı sıkışma demektedir.*

**4 - Network Security**
Ağ güvenliğinde temel 3 durum korunmalıdır, bunlar:
- Confidentialty: Ağ gizliliğinin korunması,
- Integrity: Ağ bütünlüğünün korunması,
- Availability: Ağa erişilebilirliğin korunmasıdır.

***
**İnternet Erişim Teknolojileri**
- Bandwidth, bant genişliği bir ağ üzerinden belli bir zaman aralığında aktarılabilecek veri miktarıdır, birimi datadır.
- ISP (Internet Sevice Provider): Internet Servis Sağlayıcı olarak çevrilir. 
- **Homeplug**: Bakır (copper) elektrik kablolar kullanan, evdeki priz üzerinden ağ sağlanması teknolojisidir. Kablo kalabalığını engeller. Veriyi evdeki bütün pluglara yollar.
- **WISP** (Wireless Internet Service Provider): **Rural** (kırsal), alanlarda kullanılması daha uygun olan, DSL veya kablo internetin olmadığı yerlerde kullanılan, kablolama gerektirmeyen bir bağlantı teknolojisidir, **802.11 Wireless LAN** standartını kullanır bu bağlantı kullanıcıların evdeki ADSL modeme bağlanmasına benzer şekilde çalışır.
- Broadband **Cable**: **TV** hatlarında kullanılan coaxiel TV kablosu ile internet bağlantısının sağlanması teknolojisidir.
- Broadband **Digital Subscriber Line** (DSL): **Telefon** hatlarından aktarılan, elektiriksel yolla iletilen, yüksek hızlı çalışan bağlantı teknolojisi. Bazen "Business DSL" olarak da geçer. Bazı çeşitleri vardır, bunlar:
1 - **Asymmetrical** Digital Subscriber Line (A-DSL): Genelde daha popüler olan, evlerde kullanılan, yükleme hızı indirme hızından çok daha düşük olan cinsteki DSL aboneliğidir.
2 - **Symmetrical** Digital Subscriber Line (S-DSL): Genelde kurumlarda kullanılan hem yüksek indirme hem yüksek yükleme hızına sahip olan DSL aboneliğidir.
- Wireless WANS: Mobile Broadcast olarak da bilinir. 3G, 4G, LTE, 5G gibi teknolojileri içerir.
- Leased Lines (private line): Kurumların, telekomünikasyon şirketleri aracılığıyla kiraladığı hususi, özel ağlardır.
- Metro Ethernet: Metropolitan Area Network (MAN) olarak da bilinir.
- Dail Up Telephone: Türkiyede 146 nuamralı hattın aranıp bağlanmasıyla çalışan eski bir telefon teknolojisidir, bu hatta internet erişimi çok yavaş ve sıkıntılıdır.
- Satellite genellikle fiziksel kablolamanın yapılamadığı yerlerde kullanılır. Ancak ormanlık bölgelerde kullanılması önerilmez.
- Cellular cep telefonlarınında bulunan, 2G, 3G, 4G ve 5G gibi teknolojilerin kullanıldığı kablosuz iletişim teknolojisidir.

***
**ADSL Modemin İçeriği:**
Bir ADSL modem aşağıda verilen 4 cihazın birleşmesiyle oluşmuş bir cihazdır:
- Router: Routerın bir interface'i yerel ağa bakarken diğer interface'i WAN'a bağlıdır.
- Switch: Routerın LAN'a bağlı olan interface'i switchin portuna bağlıdır.
- DHCP Sunucusu: Yerel ağda IP atamasından sorumludur, switche bağlıdır.
- Access Point: Kablosuz yerel haberleşmede kullanılan bileşendir, switche kablosuz bağlanmak isteyen cihazlar switche access point cihazı aracılığıyla bağlanır.
***

**Yeni Trendler:**

- BYOD (Bring Your Own Device): Cihazların, kullanıcının yanında kolayca taşınabilir hale gelmesiyle şirketlerde ve kurumsal ofislerde kişisel cihazların kullanılması teknolojisidir.
-Güvenlik riskleri artmıştır.
-Ağ yöneticilerine yeni yük binmiştir.
- Collabration: Online iş birliği aplikasyonları ve teknolojilerinin geneli collabration uygulamlarını oluşturur. Toplantıların artık online gerçekleşmesi bu trendin gelişmesinde etkili olmuştur.
- Video İletişim: Video dosya tipler günümüzde networklere yüklenen yüklerin büyük bir kısmını oluşturmaktadır. 
- Cloud Computing: Dünya üzerinden herhangi bir kişinin, kurumun ya da cihazın uzaktaki bir cihaza internet üzerinden bağlanarak hizmetlerine erişme teknolojisidir. Sunucu kurma ve işletmenin yüksek maliyeti olduğundan kullanıcılar sunucuları kiralama yoluna gitmektedir. (Google Drive, Gmail, AWS, etc...) 

***

**Veri Merkezleri (Data Centers)**
- Yüksek hızlı sanal sunucular bulundururlar.
- SAN teknolojisini kullanarak yedekli depolama sağlarlar.
- Elektirik kesintilerine karşı yedek güç kaynakları bulundururlar, veri merkezlerindeki server cihazların 7/24 çalışması beklenir.
- Yedek veri iletişim kanalları bulundururlar, birçok ISP'ye bağlantıları vardır ve redundant bir ağ mimarisi kullanırlar.
- Fiziksel ve yazılımsal kontroller içerirler.
*Data Centerlar bakım yönüyle yüksek maliyetlidir, işletilmesi zordur.*

***

**Güvenlik Tehditleri**
- Spyware: Gizlice veri toplayan malwaredır.
- DoS Attack: Denail of service, yani **availability**nin kesilmesidir.
- DDos: Distirbuted DoS Attack: Compromised bilgisayarlarla gerçekleştirilir.
- Zero Day Attack: Yazılımda ortaya çıkmış açığın ilk kez kullanılarak saldırı gerçekleştirilmesidir. Sürekli yamalama exploitleri engeller. Mavi takım zero day açıklarına çözüm üretir.
- Identity Theft: Başka bir kişi gibi davranarak dolandırıcılık yapılması (**fraud**).

*3 Temel sızma yolu vardır, E-mail, OS exploits, physical devices (USB gibi).*
*Viruslerle mücadele asla bitmez.*
**Security Solutions (Güvenlik Çözümleri)**
- Antivirus.
- Firewall.
- IPS: Intrusion Preventation Systems
- VPN: Güvenli bağlantı sağlar.
- ACL: Ağ trafiğinin kontrolünü sağlar. Genelde source ve destination adreslerine bakar. TCP packet header kısmına ya da UDP source ve destination portlarına bakar.

**Güvenlikle İlgili Sınav Bilgileri**

- **Internal threats are far worse then external threats**. External'da kullanılan hız 2/4/8/10 Mbit hızlarındayken Internal'da bu hız 1000 Mbitlere çıkabilir.
- Firewall dışarıdan gelen birçok tehditi önler. Firewall **cihazı** iç ağda yoktur. Yazılımsal firewall'lar iç ağda bulunurlar.
- **ADSL** routerler NAT yapar. NAT varsa dışarıdan içeriye erişim yapılamaz.
*Statik IP de olsa NAT'a erişilmez.*
*Evdeki akıllı ampüle aynı hatta bağlı cihazla yapılamaz. Sebebi NAT'dır. Cihazdan servera, serverdan da ampüle bağlantı sağlanır. **Doğrudan erişim yoktur**.*
- Evlerde ve küçük ofislerde minimum güvenlik önlemi sağlamak adına firewall, anti-malware ve anti-virus kullanımı  yeterliyken, büyük kurumlarda bunlara ek olarak IPS (Intrusion Prevention System) ve IDS'ler (Intrusion Detection System) eklenebilir.








 			

	
	


