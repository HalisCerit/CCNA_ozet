# **1-GEÇMİŞTEN GÜNÜMÜZE İNTERNET**
|“Fixed” Computing   |Bring Your Own Device   |Internet Of Things   |Internet Of Everything   |
|---|---|---|---|
|Eskiden cihazlara kullanıcının fiziksel olarak gitmesi gerekirdir.”Sabit” bilgisayarlar vardı.   |Cihazların kullanıcının yanında kolayca taşınabilir hale gelmesidir. Şirketlerde ve kurumsal ofislerde kişisel cihazların kullanılması teknolojisidir. <br />**-Güvenlik riskleri artmıştır.** <br />**-Ağ yöneticilerine yeni yük binmiştir** </span>|Age of devices olarak bilinen teknolojik gelişmedir. Fiziksel objelerin, toplu olarak ve internet yoluyla iletişimini gerçekleştirme teknolojisidir.	   |İnsanların, işlemlerin, dataların ve cisimlerin dâhil olduğu birçok nesnenin internet aracılıyla iletişim kurması teknolojisi.   |

### **İnternetin Temel Gelişim Aşamaları**

- HTTP (Hypertext-Transport-Protocol) 
-  WEB 2.0   
-  I.O.T.

### **Local Area Networks-LAN (Yerel Alan Ağları)**
-	İki ya da daha fazla cihazın haberleştiği ortama **Network** denir.
- 	Aynı coğrafyada/bölgede bulunan ağlara **LAN** adı verilir. "Same location" olarak ifade edilir.
### **Çeşitli Boyutlu Ağlar:**
- SOHO (Small Home Office) ağları
- Şirket ağları
- Global ağlar

## **Ağ Bileşenleri: Client-Server İlişkisi | Host Kavramı | Intermediary Devices | Network Media**

- 	Ağda bulunan bütün son kullanıcı cihazlarını **host** olarak ifade edilir. Namı diğer **end devices’tır**. IP üzerinden iletişim yapan bazı cihazlar: pcler, ağa bağlı yazıcılar, VOIP’ler, telefonlar vb. End devicelar **NIC (Network Interface Card)** ile networke bağlanırlar. NIC’in diğer bir adı da **Ethernet Card**’dır.


*Neredeyse her cihazda NIC yani Ethernet kartı bulunur, NIC'ler bazen anakartın içerisine gömülü olarak bulunabilir.*

- **Server** dediğimiz aslında bir host cihazdır, ancak içerisinde diğer hostların kullanacağı hizmetleri bulundurduğu için bu ismi almıştır. **Client** ise serverdan hizmeti ağ yoluyla isteyen cihazlara denir. 

*Server bir cihaz değildir, işlemdir.*

- Cihazların server işlemini yapmak için özel bir server bilgisayarı olma zorunluluğu yoktur, günlük kullanımdaki host/end user cihazları da server işlemlerini kısıtlı kapasitede olsa yapabilir. Bu duruma **Peer-to-Peer (P2P)** denir. Cihaz **hem server hemde client** olarak davranır. Torent bağlanrılarında kullanılan teknoloji P2P'dır. Ayrıca kripto para benzeri teknolıjilerde de P2P'den yararlanılır.

*Ancak Peer-to-Peer sorumluluk almaktır:*<br />*+: Kolaydır, az karmaşıktır, az maliyetlidir ve basit görevler için kullanışlıdır.*<br />*-:Merkezi yönetimi yoktur, güvenli ve ölçeklenebilir değildir ve performans düşüklüğü yaratır.*<br />*Serverların 7/24 açık olması ve cevap verebilir olması beklenir.*

- Firewall, Switch, Router, Wireless Router, ve Firewall etc. gibi ağ cihazlarına **intermediary devices** denir. 2 adet temel cihaz vardır: Bunlar router ve switch'tir.

-  **Switch:** Hostları kablolu şekilde local networke dahil eden cihazdır. 

*Access Point (Kablosuz Erişim Noktası) switch felsefesi ile çalışır.*

- **Router:** Network'ün en temel taşı bu cihazdır bu olmadan hiç bir cihaz çalışmaz. Farklı networkleri birbirine bağlayan cihazdır. Ağdaki mesajların takip etmesi gereken yolu belirler.

- **Firewall:** Güvenlik özellikleri arttırılmış routerlar olarak özetlenebilir.

- Ağlarda iletişimin gerçekleştiği ortama **Media** ya da **Network Media** denir. Bazı media tipleri şunlardır: <br /> *I. **Copper Wire**, elektirik ile veri iletmi yapar, **UTP (Untwisted Shielded Pair)** kablo kullanır.* <br /> *II. **Fiber Optic**, ışıkla veri iletim yapar. Single Mode ve Multi Mode gibi alternatifleri vardır.* <br /> *III. **Wireless İletim**,hava yoluyla iletim yapar. Elektromanyetik dalgalar kullanır.*

## **Sınava Özel Notlar:**
   
- ###  Kamusal alanda kablo çekmek yasaktır. Yalnızca **ISP (Internet Service Provider)** kablo çekme/ kablolama hakkına sahiptir.

- ###  Router farklı networkleri birbirine bağlar.

- ###  Modem dediğimiz cihazlar temelinde routerdır.

- ### Routerların genelde bir yüzü ISP'ye bir yüzü ise LAN a bağlanır.

- ### Özel, fiziksel ağa bağlanma portlarına  **Interaface** denir.

- ### End device'ları networke bağlayan fiziksel porta **NIC** denir.

- ### İki farklı ağı birbirine bağlamayacaksan router alınmamlıdır.

## **Ağ Tipleri:** 
- Internet: Worldwide connection of networks. 

- LAN (Local Area Network): Yerel ağ.

- WAN (Wide Area Network): Uzak ağları birbirine bağlamak için kullanılır. LAN'ların ISP kullanılarak bağlanmasıyla WAN oluşur.

- Intranet: Kurum içi ağdır. Kurumun bütün içi LAN'lar WAN kullanılarak bağlanmıştır.

- Extranet: Kurum içerisindeki özel ağların diğer kurumların ağlarına bağlanmasıyla oluşturulmuş kısıtlı, kontrollü ağdır.

- MAN (Metropolitan Area Network): LAN'lardan küçük, WAN'lardan büyük. Kentlerde ya da Universitelerde bulunan hatlara verilen genel isimdir.

- WLAN (Wireless LAN).

- SAN (Storage Area Network): Sunucuların, hard disk sunucusu ile olan ağı. Ancak artık günümüzde hard diskler sunucuların içerisinde (Hyperconversion). 


Unutulmamalıdır ki her ağ internete bağı olmak zorunda değildir. Askeri hatlar, devlet kurumlarına bağlı özel ağların internete bağı yoktur.

## **Reliable networks:**
### 1 - Fault Tolerance 
- Router ve Switchler çökse bile sistemin çalışmaya devam etmesi.
- **Redundant** sistemler (yedek cihazı olan sistemler).
### 2 - Scalability
- Ağın yarın büyümeyede sorun çıkarmyacak şekilde hazırlanması.
### 3 - Quality of Service (QoS)
- Düşük ping.
- Bazı durumlarda bazı cihazlara öncelik verilmesi.
- Reliable delivery.
- Low latency.
### 4 - Network Security
- Confidentialty: Ağ gizliliğinin korunması.
- Integrity: Ağ bütünlüğünün korunması.
- Availability: Ağa erişilebilirliğin korunması.

## **Converged Networks**
Eskiden telefon ve internet ağları ayrıydı. Günümüzde bu ağlar birleşik şekildedir ve bu durum siber güvenlikçilerin işini zorlaştırmaktadır.

## **İnternet Erişim Tekknolojileri**
- ISP: Internet Sevice Provider. 

- **Homeplug**: Bakır (copper) elektrik kablolar kullanan, evdeki priz üzerinden ağ sağlanması teknolsidir. Kablo kalabalığını engeller. Veriyi evdeki bütün pluglara yollar.

- **WISP** (Wireless Internet Service Provider): **Rural** (kırsal), alanlarda kullanılması daha uygun olan, DSL veya kablo internetin olmadığı yerlerde kullanılan, kablolama gerektirmeyen bir bağlantı teknolojisidir, 802.11 Wireless LAN standartını kullanır.

- Broadband **Cable**: **TV** hatlarında kullanılan coaxiel kablo ile bağlantının gerçekleştirilmesi.

- Broadband **Digital Subscriber Line** (DSL): **Telefon** hatlarından aktarılan, elektiriksel yolla iletilen, yüksek hızlı çalışan bağlantı teknolojisi. Bazen "Business DSL" olarak da geçer. 2 çeşidi vardır:
<br /> 1 - **Asymmetrical** Digital Subscriber Line (A-DSL): Genelde daha popüler olan, evlerde kullanılan, yükleme hızı indirme hızı çok daha düşük olan cinsteki DSL.
2 - **Symmetrical** Digital Subscriber Line (S-DSL): Genelde kurumlarda kullanılan hem yüksek indirme hem yüksek yükleme hızına sahip olan DSL. 

- Wireless WANS: Mobile Broadcast olarak da bilinir. 3G, 4G, LTE, 5G gibi teknolojileri içerir.

- Leased Lines (private line): Hususi kiralnmış özel ağ.

- Metro Ethernet: Metropolitan Area Network (MAN) olarak da bilinir.

- Dail Up Telephone: Türkiyede 146 nuamralı hattın aranıp bağlanmasıyla çalışan eski bir telefon teknolojisi.

### Kullanıcıları İnternete Bağlamanması:

|Home User          |DSL     |ISP   |Internet   |
|-------|-----------|--------|--------------------|
| SOHO <br /> Teleworker |Cable <br /> Cellular (Hücresel veri bandı) <br /> Satelitte <br /> Dail-Up Telephone (146 hattının aranıp bağlanma)   | -   |  - |

### Kurumların İnternete Bağlanamsı

| Organizasyon	|Dedicated Leased Lines       	|ISP   	|Internet  	|
|---	|---	|---	|---	|
|  - 	| Metro Ethnernet <br /> DSL <br /> Satelitte <br /> IP-MPLS 4G  	|   	-|   -	|

## Yeni Trendler:
- BYDO: Bring Your Own Device
- Collabration: Online iş birliği applikasyonları ve teknolojileri. Toplantıların artık online gerçekleşmesi bu trendin gelişmesinde etkili olmuştur.
- Video İletişim: Günümüzde networklere yüklenen ağır yüklerden bir tanesi video dosya tipleridir. Network
- Cloud Computing: Sunucu kurma ve işletmenin yüksek maliyeti olduğundan kullanıcılar sunucuları kiralama yoluna gitmektedir. (Google Drive, Gmail, AWS, etc...) 

## Veri Merkezleri (Data Centers)
- Yüksek hızlı sanal sunucular bulundururlar.
- SAN teknolojisini kullanarak yedekli depolama sağlarlar.
- Elektirik kesintilerine karşı yedek güç kaynakları bulundururlar, veri merkezlerindeki server cihazların 7/24 çalışması beklenir.
- Yedek veri iletişim kanalları bulundururlar, birçok ISP'ye bağlantıları vardır ve redundant bir ağ mimarisi kullanırlar.
- Fiziksel ve yazılımsal kontroller içerirler.
### *Data Centerlar bakım yönüyle yüksek maliyetlidir, işletilmesi zordur.*

## Güvenlik Tehditleri
- Spyware: Gizlice veri toplayan malwaredır.
- DoS Attack: Denail of service, yani **availability**nin kesilmesidir.
- DDos: Distirbuted DoS attack. Compromised bilgisayarlarla gerçekleştirilir.
- Zero Day Attack: İlk kez ortaya çıkmış açığın kullanılarak saldırılası. Sürekli yamalama exploitleri engeller. Mavi takım zero day açıklarına çözüm üretir.
- Identity Theft: Using personal information for **fraud**.
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








 			

	
	


