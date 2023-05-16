## 7-Ethernet Anahtarlandırma
- Ethernet günümüzde en yaygın kullanılan LAN teknolojisidr.
- Ethernet çok esnek bir protokoldür, ister hub cihazlarında half duplex olsun ister switch cihazlarında full duplex olsun uyumlu ve sıkıntısız çalışır.
- Ethernet 1. ve 2. katmanda çalışan bir protokolüdür.
- Ethernet framing yapısını oluşturur.
- Ethernet MAC methodu olarak CSMA/CD kullanır.
- Ethernet protokolü kablolar, fiber, UTP, STP, sinyalleşme, konnektörler ve  data iletim hızları gibi bir çok konuyu denetler.

<img src="./Diagrams/1_6_20.png" alt="image" width="45%" height="45%">

Daha detaylı inceleyecek olursak:

<img src="./Diagrams/1_6_1.png" alt="image" width="45%" height="45%">

- LLC Sublayer, LLC alt katmanı, Data Link katmanından Network katmanına geçişi kontrol eder. Üstteki katmanda kullanılan protokol IPv4 mü IPv6 mı bu bilgiyi tanımlar.
- LLC'nin de bulunduğu ethernet frame yapısı, frame'in oluşma sıraısyla beraber şu şekilde gösterilebilir:

<img src="./Diagrams/1_7_1.png" alt="image" width="55%" height="55%">

- MAC sublayer medyaya erişimden ve veriyi kapsüllemeden sorumludur. 
- IEEE 802.3 Ethernet protokolünde ethernet frame'in yapısını temel anlamda 3'e ayırmıştır:    
    - Ethernet Addressing: MAC adresi içermesi.
    - Frame datası.
    - Ethernet Hata Tespiti: FCS içermesi.
     
### Ethernet II Frame Yapısı

<img src="./Diagrams/1_7_2.png" alt="image" width="70%" height="70%">

- Ethernet çerçevelerinde LLC sublayer kısmının yerine Type kullanılır, bu durum LLC'nin kullanılmadığını göstermez .
- **Minumum frame boyutu 6+6+2+46+4=64** byte'tır. Bu hesaplamada Preamble veya SFD dahil edilmez çünkü bu frame yapıları artık günümüzde kullanım dışı olmuşlardır.
- **Maximum frame boyutu 6+6+2+1500+4=1518** byte'tır. 
- 64 bytetan küçük paketler çöpe atılır, bu durumda pakete **collision frame** ya da **runt frame**. Buradaki fikir bir paket 64'ten küçük gelmişse o paket kesinlikle collision'a uğraşmıştır mantığıdır.
- Benzer bir durum paketin 1518'den büyük gelmesi durumunda yaşanır. 1518 byte'tan büyük paketler **jumbo** ya da **baby giant fragmnet** olarak adlandırılır ve çöpe atılır. Jumbo özelliğinin açılması durumunda büyük paketler de kabul edilir hale gelir.

### MAC Adresleri ve Hexadecimallik
- MAC adresleri 48 bitlik adreslerdir
- 12 adet hexadecimallerden oluşurlar.
- Fiziksel adresler şu şekillerde bulunabilir:
    - 1C-5A-81-65-5C-0F
    - 1C:5A:81:65:5C:0F
    - 1C5A.8165.5C0F
- Standart bir laptopun üzerinde 3 veya daha fazla NIC kartı bulunabilir.
<img src="./Diagrams/1_7_3.png" alt="image" width="25%" height="25%">
- Bu adresleri **IEEE** sağlar. MAC adreslerini mantığı şı şekildedir:
<img src="./Diagrams/1_7_4.png" alt="image" width="25%" height="25%">
- MAC adresleri değiştirilemeyen , burned-in, adreslerdir olarak ifade etsekte bazı cihazlar üzerindeki MAC adreslerini değiştirmek mümkündür.
- Kali Linux'da MAC adresleri değiştirilebilir, bu değiştirme için MAC changer kullanılır.
- OUI lookup gibi sitelerden cihazların MAC adreslerine bakarak üretici markalarını bulmak ve cihazların seri numaralarını görmek mümkündür.
- 3000$ gibi bir parayla 16 milyon MAC adresi alınabilir. Benzer şekilde gizli MAC adreslerini de almak mümkündür.

### MAC Adres Tipleri
- Tek noktadan tek nokataya yayın yapmaya **Unicast** denir
- Aynı ağda birlikte bulunan,  IPv4 adreslerini bilinen cihazın bir diğer cihaza ping atmasına **Address Resolution Protocol/ARP** denir. ARP yerel ağda MAC adreslerinin öğrenilmesini sağlayan protokoleldir birisidir.
- IPv6 da ARP protokolü yerine aynı işlemi yapan **Neighbour Discovery/ND**  protokolü vardır.
- Ağda bulunan bütün cihazlara koşulsuz şartsız paket yollanmasına **broadcast**  denir. 
- **Broadcast** bütün cihazlara paket yollamayı MAC hedefine **FF-FF-FF-FF-FF-FF** adresini yazarak gerçekleştirir.
- İçerisinde ara cihaz bakımından yalnızca Hub olan ağlarda MAC adreslerinin pek işe yaradığını söyleyemeyiz. Bunun sebebi hublar sürekli broadcast yapar, paketler tüm cihazlara sürekli ilerilir, her cihaz gelen her broadcasti okumak zorunda kalır. Cihazlar sürekli gelen paketlerin MAC adreslerine bakıp bana mı gelmiş diye kontrol etmek zorunda kalır.


<img src="./Diagrams/1_7_5.png" alt="image" width="68%" height="68%">
<img src="./Diagrams/1_7_6.png" alt="image" width="55%" height="55%">

- Bir cihazdan birden çok cihaza paket gönderilmesine ise **Multicast** denir.
- IPv4'te multicast gerçekleştirmek için hedef MAC adresine **01-00-SE** yazılır ve IPv4 destination adresi **224-239**'la bitirilirken, IPv6'da destination MAC adresi 33-33 olarak değiştirilirken, IPv6 destination kısmına FF00 yazılır.
- Multicast ağ içerisine broadcast gibi dağıtılır , paketin gelidği port hariç paket her porta iletilir. Ancak yalnızca multicasti dinlemek isteyen cihazlarlar multicast'e erişebilir. 
- If a switch receives a frame with the destination MAC address 01:00:5E:00:00:D9 switch forwards it out all ports except the ingress port.


### Switchler Nasıl Çalışır?
**MAC Adresi Tablosu**
- Hub sinyali kuvvetlendirip iletimi diğer tüm portlara iletir. 10 Mbps hızla 1. katmanda çalışır maksimum 4 hub ard arad bağlanabilir ve yalnızca bir cihaz paket alabilir ya da gönderebilir, çünkü hublar half dublex cihazlardır.
- Switch 2. katmanda çalışan bir ara cihazdır. Temel işlevi MAC adresleme tablosunu tutmaktır. Verilere yönlendirme yapar. Hub cihazlarına göre switch cihazları devrim niteliğindedir, paket gönderme paket alma portları birbirinden farklıdır. Aynı anda aynı porttan  1Gbps alıp verebilir. Bu çalışmaya full duplex çalışma denir.
- OSI modelini hatırlayacaksak:
    - L7 Application,
    - L6 Presentation,
    - L5 Session katmanlarında PDU ismi **Data**dır.
    - L4 Transport katmanında dataya source port, destination port ve sequence numarasının eklenemesiyle **segment** oluşur.
    - L3 Network katmanında segemente source ve destination IP eklenmesiyle oluşan PDU'ya **IP packeti** denir.
    - L2 Data Link katmanında pakete frame header ve trailer eklenmesiyle **ethernet frame** oluşur.
    - L1 Pyhsical katmanda ise veriler **bitlere** dönüştürülür ve aktarılır. 1011010101110101010...
- Şimdi bir cihazın sırasıyla ağada nasıl davranış sergilediğine bakalım bakalım:
<img src="./Diagrams/1_7_7.png" alt="image" width="35%" height="35%">



