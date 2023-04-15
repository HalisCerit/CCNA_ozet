## 1-GEÇMİŞTEN GÜNÜMÜZE İNTERNET
|“Fixed” Computing   |Bring Your Own Device   |Internet Of Things   |Internet Of Everything   |
|---|---|---|---|
|Eskiden cihazlara kullanıcının fiziksel olarak gitmesi gerekirdi.”Sabit” bilgisayarlar vardı.   |Cihazların kolayca taşınabilir hale gelmesidir. Şirketlerde ve kurumsal ofislerde kişisel cihazların kullanılması trendidir. <br />**-Güvenlik risklerini artmıştır.** <br />**-Ağ yöneticilerine yeni yük binmiştir** </span>|Age of devices olarak bilinen teknolojik gelişmedir. Fiziksel objelerin, toplu olarak ve internet yoluyla iletişimini gerçekleştirme teknolojisidir.	   |İnsanların, işlemlerin, verilerin ve cisimlerin gibi birçok  nesnenin dâhil olduğu internet aracılıyla iletişim kurması teknolojisidir.   |

### İnternetin Temel Gelişim Aşamaları
- HTTP (Hypertext-Transport-Protocol) Dönemi: Statik text bazlı sitelerin olduğu dönem olarak tarif edilir.
-  WEB 2.0 Dönemi: Interaktif, dinamik Web sitelerinin yaygın olmasıyla oratya çıkan dönemdir.
-  IoT (Internet of Things) Dönemi: Yalnızca insanlarla değil birbirliyle konuşan cihazların oluşturduğu (Machine-to-Machine, M2M), insan kaynağına gerek duymayan otomasyonla çalışan sistemlerin olacağı dönemdir.

### Local Area Networks-LAN (Yerel Alan Ağları)
-	İki ya da daha fazla cihazın haberleştiği ortama **Network** denir.
##### *Foreshadowing: Aynı tip cihazlar cross-over kablolama ile bağlanır.*
- 	Aynı coğrafyada/bölgede bulunan ağlara **LAN** adı verilir, "Same location" olarak ifade edilir.
### Çeşitli Boyutlu Ağlar:
- SOHO (Small Home Office) ağları
- Şirket ağları
- Global ağlar

***

### Ağ Bileşenleri: Client-Server İlişkisi | Host Kavramı | Intermediary Devices | Network Media

- 	Ağda bulunan bütün son kullanıcı cihazları **host** ya da **end devices** olarak ifade edilir. Pcler, ağa bağlı yazıcılar, VOIP’ler, telefonlar vb. gibi ip üzerinden haberleşme yapan end device'lar **NIC (Network Interface Card)** ile networke bağlanırlar. NIC’in diğer bir adı da **Ethernet Card**’dır.

*NIC cihazların yerel ağa bağlanması sağlayan kartlardır. Neredeyse her host cihazında NIC yani Ethernet kartı bulunur, NIC'ler bazen anakartın içerisine gömülü olarak bulunabilir.*

- **Server** dediğimiz aslında bir host işlemidir. İçerisinde diğer hostların kullanacağı hizmetleri bulundurduğu için bu ismi almıştır. **Client** ise ağ yoluyla serverdan hizmet  **isteyen** cihazlara denir. 

*Server bir cihaz değildir, bir işlemdir. Server işleminin daha hızlı/optimize yapılnası için server bilgisayarları geliştirilmiştir.*

- Cihazların server işlemini yapmak için özel bir server bilgisayarı olma zorunluluğu yoktur, günlük kullanımdaki host/end user cihazları da server işlemlerini kısıtlı kapasitede de olsa yapabilmektedir. Bu duruma **Peer-to-Peer (P2P)** denir. Cihaz P2P sırasında **hem server hem de client** olarak davranır. Torent bağlantılarında kullanılan teknoloji P2P'dır. Ayrıca kripto para benzeri teknolojilerde de P2P'den yararlanılır.

*Ancak Peer-to-Peer sorumluluk almaktır:*<br />*+: Kolaydır, az karmaşıktır, az maliyetlidir ve basit görevler için kullanışlıdır.*<br />*-:Merkezi yönetimi yoktur, güvenli ve ölçeklenebilir değildir ve performans düşüklüğü yaratır.*<br />*Serverların 7/24 açık olması ve cevap verebilir olması beklenir.*

- Switch, Router, Wireless Router, ve Firewall etc. gibi ağ cihazlarına **intermediary devices** (ara cihazlar) denir. Temelinde 2 intermediary cihaz vardır, bunlar router ve switch'tir.

-  **Switch:** Hostları **kablolu** şekilde yerel (local) networke dahil eden cihazdır. Kablosuz cihazlar ise önce **Access Point** adlı cihaza kablosuz şekilde hava aracılığıyla bağlanır, bağlantıdan sonra access point bu bağlantıyı switche kablolu şekilde aktarır.

*Access Point (Kablosuz Erişim Noktası) switch felsefesi ile çalışır.*

- **Router:** Network'ün en temel taşı bu cihazdır. Farklı networkleri birbirine bağlayan cihazdır. Ağdaki mesajların takip etmesi gereken yolu belirler.

*Foreshadowing: BGP protokolü ağ hattında kısa yolu bulmaya yarayan protokoldür.*

NIC'in neredeyse her host cihazında bulunur. NIC intermediary device'lardan router ve firewall'da bulunurken switch'de bulunmaz. Switchler bağlanmak için ethernet kartı kullanır. Yani switchlerin NIC kartı yoktur ancak NIC'ler bağlanmak için swicthleri kullanır.

- **Firewall:** Güvenlik özellikleri arttırılmış router cihazları olarak özetlenebilir.

*Burada bahsettiğimiz device olan Firewall'dır, ağdaki cihazların içersinde bulunan yazılımsal Firewall faklıdır.*

- Ağlarda iletişimin gerçekleştiği ortama **Media** ya da **Network Media** denir. Bazı media tipleri şunlardır: 

*I. **Copper Wire**, elektirik ile veri iletmi yapar, **UTP (Untwisted Shielded Pair)** kablo kullanır.* <br /> *II. **Fiber Optic**, ışıkla veri iletim yapar. Single Mode ve Multi Mode gibi alternatifleri vardır.* <br /> *III. **Wireless İletim**,hava yoluyla iletim yapar. Elektromanyetik dalgalar kullanır.*
***

### **Sınava Özel Notlar:**   
- Kamusal alanda kablo çekmek yasaktır. Yalnızca **ISP (Internet Service Provider)** kablo çekme/ kablolama hakkına sahiptir. ISP'lerin çektiği özel ağlara **leased lines** denir. Leased Lines (private line), kurumların telekominikasyon şirketleri aracılığıyla kiraladığı hususi, özel ağlardır.
-   Router farklı networkleri birbirine bağlar. Yani router'ın farklı interfaceleri farklı ağlara bakar, genelde bir interface ISP'ye diğer intrface ise yerel ağa bağlıdır. 
-   Modem dediğimiz cihazlar temelinde routerdır. Içerisinde access point, switch, router ve DHCP server bulunur.
-  Özel, fiziksel ağa bağlanma portlarına  **Interface** denir.
*Foreshadowing: Port ve Interface birbirinin yerine kullanılan terimlerdir ancak TCP/UDP protokollerindeki portlarla karıştırılmamalıdır.*
-  End device'ları networke bağlayan fiziksel porta **NIC** denir.
-  İki farklı ağı birbirine bağlanmayacaksa router alınmamalıdır.
***
## **Ağ Tipleri:** 

- LAN (Local Area Network): Yerel ağlardır.
- WAN (Wide Area Network): Uzak ağları birbirine bağlamak için kullanılır. LAN'ların ISP kullanılarak bağlanmasıyla WAN oluşur.
- Internet: Temelinde bir WAN'dır. Dünya üzerindeki WAN'ların birleşmesiyle oluşan bir ağdır. 
- Intranet: Kurum içi ağdır. Kurumun bütün içi LAN'lar WAN kullanılarak bağlanmıştır.
- Extranet: Kurum içerisindeki özel ağların diğer kurumların ağlarına bağlanmasıyla oluşturulmuş kısıtlı, kontrollü ağdır.
- MAN (Metropolitan Area Network): LAN'lardan küçük, WAN'lardan büyük. Kentlerde ya da Universitelerde bulunan hatlara verilen genel isimdir.
- WLAN (Wireless LAN).
- SAN (Storage Area Network): Sunucuların, hard disk sunucusu ile olan ağı. Ancak artık günümüzde hard diskler sunucuların içerisinde (Hyperconversion). 

Unutulmamalıdır ki her ağ internete bağı olmak zorunda değildir. Askeri hatlar, devlet kurumlarına bağlı özel ağların internete bağı yoktur.

***

## **Reliable networks:**
### 1 - Fault Tolerance 
- Ağ sistemindeki bazı routerlar ve switchlerin çökmesine rağmen sistemin sorunsuz çalışmaya devam etmesi yüksek "hata tahammüllü" ağ olduğunu gösterir.
- Hata tahammüllü yüksek sistemler. **Redundant**  olarak ifade edilir, kelime anlamı olarak yedek cihazı olan sistemler demektir.

### 2 - Scalability
- Kurulan ağın, gelecekte büyüme işleminde sorun çıkarmayacak şekilde hazırlanması demektir, kelime anlamı olarak büyütülebilirlik denilebilir.

### 3 - Quality of Service (QoS)
- Ağlarda düşük ping olmalıdır.
- Bazı durumlarda bazı cihazlara öncelik verilmelidir.
- Reliable delivery gerçekleştirilmelidir.
- Low latency olmalıdır.

Bu ve benzeri durumlar servis kalitesini belirler.

### 4 - Network Security
Ağ güvenliğinde temel 3 durum korunmalıdır, bunlar:
- Confidentialty: Ağ gizliliğinin korunması.
- Integrity: Ağ bütünlüğünün korunması.
- Availability: Ağa erişilebilirliğin korunması.

***

### **Converged Networks**
Eskiden telefon ve internet ağları ayrıydı. Günümüzde bu ağlar birleşik şekildedir ve bu durum siber güvenlikçilerin işini zorlaştırmaktadır.

***

## **İnternet Erişim Teknolojileri**
- ISP (Internet Sevice Provider): Internet Servis Sağlayıcı olarak çevrilir. 
- **Homeplug**: Bakır (copper) elektrik kablolar kullanan, evdeki priz üzerinden ağ sağlanması teknolojisidir. Kablo kalabalığını engeller. Veriyi evdeki bütün pluglara yollar.
- **WISP** (Wireless Internet Service Provider): **Rural** (kırsal), alanlarda kullanılması daha uygun olan, DSL veya kablo internetin olmadığı yerlerde kullanılan, kablolama gerektirmeyen bir bağlantı teknolojisidir, **802.11 Wireless LAN** standartını kullanır.
- Broadband **Cable**: **TV** hatlarında kullanılan coaxiel TV kablosu ile internet bağlantısının sağlanması teknolojisidir.
- Broadband **Digital Subscriber Line** (DSL): **Telefon** hatlarından aktarılan, elektiriksel yolla iletilen, yüksek hızlı çalışan bağlantı teknolojisi. Bazen "Business DSL" olarak da geçer. Bazı çeşitleri vardır, bunlar:
1 - **Asymmetrical** Digital Subscriber Line (A-DSL): Genelde daha popüler olan, evlerde kullanılan, yükleme hızı indirme hızından çok daha düşük olan cinsteki DSL aboneliğidir.
2 - **Symmetrical** Digital Subscriber Line (S-DSL): Genelde kurumlarda kullanılan hem yüksek indirme hem yüksek yükleme hızına sahip olan DSL aboneliğidir.
- Wireless WANS: Mobile Broadcast olarak da bilinir. 3G, 4G, LTE, 5G gibi teknolojileri içerir.
- Leased Lines (private line): Kurumların, telekominikasyon şirketleri aracılığıyla kiraladığı hususi, özel ağlardır.
- Metro Ethernet: Metropolitan Area Network (MAN) olarak da bilinir.
- Dail Up Telephone: Türkiyede 146 nuamralı hattın aranıp bağlanmasıyla çalışan eski bir telefon teknolojisi.
***
### Kullanıcıları İnternete Bağlanma Sırası:

1- Home User: SOHO, Teleworker
2- DSL: Cable Cellular (Hücresel veri bandı)  Satelitte Dail-Up Telephone (146 hattının aranıp bağlanma)  
3- ISP
4- Internet
### Kurumların İnternete Bağlanma Sırası:
1-Organizasyon
2-Dedicated Leased Lines: Metro Ethnernet, DSL ,Satelitte, IP-MPLS 4G
3-ISP
4-Internet
***
## Yeni Trendler:
- BYOD (Bring Your Own Device): Cihazların, kullanıcının yanında kolayca taşınabilir hale gelmesidir. Şirketlerde ve kurumsal ofislerde kişisel cihazların kullanılması teknolojisidir.
-Güvenlik riskleri artmıştır.
-Ağ yöneticilerine yeni yük binmiştir.
- Collabration: Online iş birliği aplikasyonları ve teknolojilerinin geneli collabration uygulamlarını oluşturur. Toplantıların artık online gerçekleşmesi bu trendin gelişmesinde etkili olmuştur.
- Video İletişim: Video dosya tipler günümüzde networklere yüklenen yüklerin büyük bir kısmını oluşturmaktadır. 
- Cloud Computing: Sunucu kurma ve işletmenin yüksek maliyeti olduğundan kullanıcılar sunucuları kiralama yoluna gitmektedir. (Google Drive, Gmail, AWS, etc...) 

***

## Veri Merkezleri (Data Centers)
- Yüksek hızlı sanal sunucular bulundururlar.
- SAN teknolojisini kullanarak yedekli depolama sağlarlar.
- Elektirik kesintilerine karşı yedek güç kaynakları bulundururlar, veri merkezlerindeki server cihazların 7/24 çalışması beklenir.
- Yedek veri iletişim kanalları bulundururlar, birçok ISP'ye bağlantıları vardır ve redundant bir ağ mimarisi kullanırlar.
- Fiziksel ve yazılımsal kontroller içerirler.
*Data Centerlar bakım yönüyle yüksek maliyetlidir, işletilmesi zordur.*

## Güvenlik Tehditleri
- Spyware: Gizlice veri toplayan malwaredır.
- DoS Attack: Denail of service, yani **availability**nin kesilmesidir.
- DDos: Distirbuted DoS Attack: Compromised bilgisayarlarla gerçekleştirilir.
- Zero Day Attack: İlk kez ortaya çıkmış açığın kullanılarak saldırı gerçekleştirilmesidir. Sürekli yamalama exploitleri engeller. Mavi takım zero day açıklarına çözüm üretir.
- Identity Theft: Başka bir kişi gibi davranarak dolandırıcılık yapılması (**fraud**).

*3 Temel sızma yolu vardır, E-mail, OS exploits, physical devices (USB gibi).*
*Viruslerle mücadele asla bitmez.*
## Security Solutions (Güvenlik Çözümleri)
- Antivirus.
- Firewall.
- IPS: Intrusion Preventation Systems
- VPN: Güvenli bağlantı sağlar.
- ACL: Ağ trafiğinin kontrolünü sağlar. Genelde source ve destination adreslerine bakar. TCP packet header kısmına yada UDP source ve destination portlarına bakar.

## Güvenlikle İlgili Sınav Bilgileri

- **Internal threats are far worse then external threats**. External'da kullanılan hız 2/4/8/10 Mbit hızlarındayken Internal'da bu hız 1000 Mbitlere çıkabilir.
- Firewall dışarıdan gelen birçok tehditi önler. Firewall **cihazı** iç ağda yoktur. Yazılımsal firewall'lar iç ağda bulunurlar.
- **ADSL** routerler NAT yapar. NAT varsa dışarıdan içeriye erişim yapılamaz.
*Statik IP de olsa NAT'a erişilmez.*
*Evdeki akıllı ampüle aynı hatta bağlı cihazla yapılamaz. Sebebi NAT'dır. Cihazdan servera, serverdan da ampüle bağlantı sağlanır. **Doğrudan erişim yoktur**.*








 			

	
	


