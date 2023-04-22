## Data Link Katmanı
- Data Link katmanı denilince akla gelen ilk protokol kuşkusuz **Ethernet** protokolüdür. Ancak Data Link katmanında bulunan tek protokol ethernet protokolü değildir. Wireless LAN, PPP ve HDLC gibi protokoller data link katmanında bulunan diğer protokollerdir.
- Bu protokollerden bazıları MAC adresi kullanırken bazıları kullanmaz:


| **MAC adresi kullanan Protokoller** 	| **Başlık bilgileri bulundurmalarına rağmen <br>MAC adreslerini kullanmayan WAN teknolojileri** 	|
|:-----------------------------------:	|:----------------------------------------------------------------------------------------------:	|
|        Wireless LAN protokolü       	|                                  PPP (Point-to-Point-Protocol)                                 	|
|          Ethernet protokolü         	|                              HDLC (High-Level-Data-Link-Control)                              	|

- PPP (Point-to-Point-Protocol): İki cihaz arasında güvenli ve kesintisiz iletişimi için kullanılan bir protokoldür.
- HDLC (High-Level-Data-Link-Control): WAN'larda noktadan noktaya aktarmalarda hata kontrolü için kullanılan bir protokoldür.
- **Data Link karmanının temel görevi aynı katman üzerinde iletişim sağlamaktır.**
- MAC adreslerini kullnarak hangi NIC'den hangi NIC'e gidileceğini belirleriz, bu işlemi IP adresleri kullanarak yapamayız IPv4 adresleri günümüzde sanal adreslerdir.
- Data Link katmanı pakette **frame** yapısını oluşturur pakete (header) başlık ve kuyruk (trailer) bilgisi eklenir.
- Fiziksel katmana geçiş kontrolü MAC (Media Access Control), ağdaki trafiği kontrol ederek paketlerin çarpışmasını (collision) engeller. Ethernet'te **IEEE 802.3 CSMA/CD** algoritması kullanılırken, WLAN'da **802.11 CSMA/CA** algoritması kullanılır.
- Katman 2'den katman 1'e frame PDU'su bir anda geçemez, MAC (Media Access Control) gibi geçiş kontrol protokolü vardır.

<img src="./Diagrams/1_6_1.png" alt="image" width="35%" height="35%">

- LLC Sublayer (Logical Link Layer): Encapsulation  sırasında PDU'nun layer 2'den layer 3'e geçerken üst katmandaki IP'yi kontrol eder.
- MAC Sublayer (Media Access Control): Decapsulation sırasında layer 2'den layer 1'e geçişi kontrol eder, ayrıca:
    - Framing yapısını tasarlar.
    - MAC ile geçiş kontrolü yapar.
    - Ethernet Protokolü hem 1 hem 2 katmanda çalışır.

<img src="./Diagrams/1_6_2.png" alt="image" width="50%" height="50%">

***

<img src="./Diagrams/1_6_3.png" alt="image" width="50%" height="50%">

- Ağlar arasında hangi protokoller varsa başlık bilgisi ona göre değiştirilir.
- Paket 1.110 IP adresli cihazımızdan R1'e ulaşınca Data Link paketi atılır, frame'in başına ve sonuna  PPP kısımları eklenir.
- Paket R2'ye ulaşınca PPP başlık ve kuyruk bilgisi atılır, yerlerine HDLC bilgisi eklenir.
- Paketin R3'e ulaşmasıyla HDLC bilgileri header ve trailerdan silinir. Kaynak MAC adrsine R2 routerının MAC adrsi yazılır, hedef MAC adresinen ise Server'ın MAC adresi yazılır. 
- Unutulmamalıdır ki bu ağ yapısında wireless cihazların bulunması durumunda kullanılan protokollerde de değişiklik görülecektir.
- İkinci katman protokolleri sürekli değişebilir.

### Data Link Katmanı Standart Kurumları

- 1. ve 2. katmanda gözlenen IEEE data haberleşme satndartları **IEEE 802.3 Ethernet** ve **IEEE 802.11 WLAN (Wireless LAN)**.
- ITU (International Telecommunications Union)
- ISO (International Organization of Standartization)
- ANSI (American National Standarts Instıtue) ADSL cihazlarının standartlarını belirler.

*Hatırlatma: L3, L4, L5, L6 ve L7 standartlarını IETF RFC elemanları ile standartlaştırır.*

***
### Topolojiler
Topolojiler ağların haritasıdır, bu haritalarla ağlarda oluşan problemlerin çözümü sağlanır. Topolojiler 2'ye ayrılabilir, **fziksel topolojiler** ve **logical (mantıksal) topolojiler**. Fiziksel topolojiler cihazların birbirine nasıl bağlandığı ve fiziksel bağlantıların gösterildiği ağ haritasıdır. Mantıksal topolojiler ise ağdaki IP adres planlamaları, VLAN gibi ağ yöntemleri ile ilgilidir.

<img src="./Diagrams/1_6_4.png" alt="image" width="50%" height="50%">

Mantıksal Topolojiler de içinde 2'ye ayrılabilir:
- WAN Topolojiler. Bu topoloji PPP, HDLC ve artık kullanılamyan Frame Relay gibi protokollerin kullanıldığı ağlarda kullanılır.
- LAN Topolojiler.

### WAN Topolojiler: 
- **Point-To-Point**
   P2P (Point-To-Point) topolojisi, iki nokta arasında kalıcı bağlantının sağlandığı, doğrudan karşı tarafa iletimin gerçekleştiği ve nodeların aktardığı medyayı diğer hostlarla paylaşmadığı topoloji türüdür. (CCNA 3'de detaylı işlencektir).
   
<img src="./Diagrams/1_6_5.png" alt="image" width="35%" height="35%">

***

- **Hub And Spoke**
   Merkez ve merkezi çevreleyen şubeler tarzında bir yapısı vardır. Ancak bu topolojide merkezin ölmesi durumunda tüm ağ çöker. Bu topoloji Frame Relay yapısında kullanılan bir topolodir.

<img src="./Diagrams/1_6_6.png" alt="image" width="35%" height="35%">

***

- **Mesh Topoloji**
   Bu ağ topolojisinde bütün nodelar birbirine bağlıdır, bu sebeple en güvenilir topolojidir denilebilir. Ancak her node'u bağlamak için ISP ye para verilmesi gerekldir, bu da maliyetleri çok yükseltir.

<img src="./Diagrams/1_6_7.png" alt="image" width="35%" height="35%">

***




