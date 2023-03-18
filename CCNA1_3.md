# 3- Protokoller ve Modeller
**OSI**: Data haberleşmesini standartlaştırmatası için tasarlanmış 7 katmandan oluşan protokol kümesi.
**TCP/IP**: 4 katmandan oluşan, protokol kümesidir.


## MAC Adresleri ve IP Adresleri
- MAC ve IP adreslerini cihazların aralarında haberleşme yaparken kullanırlar.
#### MAC Adresleri:
- **48 bitten** oluşurlar.
- NIC üzerinde bulunurlar, fiziksel adres olarak da geçerler, eşsizdirler.
- MAC adresleri *9C-35-5B-5F-AA-BB* tazrındadırlar.
- Ethernet Kartı üzerinde **Bured-in adres**lerdir.
- NIC'de protokoller yüklü gelir ama istenirse değiştirilebilir, bunlar TCP/IPv4 veya TCP/IPv6'dır.
*Wifi kartı da bir NIC kartıdır.*
#### IP Adresleri:
- 32 bit / 4 kısımdan oluşurlar.
- IP adresleri 192.168.1.5 tazrındadır, bölümler (0-255) aralığında olmalıdır, yani 0 yada 255 alamazlar. 
- IP adresleri MAC adreslerindeki kalıcı adreslerin tersine mantıksal adreslerdir.
- IP adresi 192.168.5.1 olan bir cihazın 192.168.5 kısmına "Network kısmı olarak ifade edilirken, .1 ise yerel ağdaki "Host" kısmıdır.

### Hatırlatma:
*Router networkleri birbirine bağlar, router uçları farklı ağlara bakar.*
*Switch son kullnıcıları ağa dahil eder.*

## ---------------ŞEKİL 1_3_1-------------------


## İletişim Temelleri:
- Source (Kaynak).
- Destination (Hedef).
- Media (Ortam).

*Ağlar "scale" ve "complexity" olarak değişebilir, yalnızca bağlantı olması yetmez.*

*Message Source > Transmitter > Transmission Medium > Reciver > Message Destination*

## İletişim Protokolleri:
- Tüm iletişim protokoller çerçevesinde gerçekleşir.
- Protokoller iletişimin izleyeceği kurallardır.
- Kurallar protokollere bağlıdır.

*Kurallar dizisine protokol denir.*

5 temel protokol vardır, bunlar:

### 1- Encoding:

- Fiziksel ortamda mesajın iletime uygun hale getirilme işlemidir.
- Kodun yorumlanması için çözülmesine, yani, bu işin tersine **decoding** denir.
- Hostlar arası kodlama ortama uygun olmalıdır.
- Ağ üzerinden yollanan mesajlar bitlere dönüştürülür.
- Bitler ışık, ses veya elektriksel darbe modeline dönüştürülür, hedef (destination) bunu çözümler.

### 2- Formatting and Encapsulation:

- Bir mesajın gönderilirken belli bir formatta ya da yapıda olması gerekmektedir.
- Bu format mesajın türüne ve mesaj iletmek için kullanan kaynaklara bağlıdır.

*Data'nın içerisinde version, traffic class, flow control, payload lenght etc. olması bir formatlamdır.*

### 3- Message Size:

- 500 MB'lık bir dosyayı istersek tek parça halinde gönderebiliriz, ancak iletim sırasında bir sorun sonucu yalnızca bir bit bile yanlış aktarılırsa bütün veri kullanılmaz olur. Bu ölçeklendirilebilir ve kullanışlı değildir. 
- Datayı küçük parçalar halinde yollamak istersek bu parçaların doğru aktarılması için bir takım kontrol bilgileri gerekmektedir. Adres bilgisi burada devreye girer.

### 4- Message Timing:

- Akış kontrolü iletim hızının yönetimini sağlar.
- Ağdaki cihazların birbirinden yanıt almaması durumunda ne kadar bekleyeceklerini "connection timeout" yoluyla belirlenir.
- Flow control dataların çarpışmamasını, yani collision oluşmaması sağlar.
- Collision durumu ağda iletilerin çarpışmasdır.

### 5- Message Delivery Options:
- **Unicast:** Bir cihazın, tek bir cihazla iletişimdir. (One-to-One)
- **Multidcast:** Bir cihazın birden çok cihaza yaptığı iletişimdir. Multicast MAC adresiyle çalışır, iletiyle ilgilnen cihazlar paketi alır. (One-to-Many)
- **Broadcast:** Bir cihazın ağdaki her kullanıcıya iletim yapmasıdır.

*Anycast IPv6'da vardır.*

## Ağ Protokollerine Genel Bakış

### 1- Ağ İletişim Protokolleri: 

İki ya da daha fazla cihazın bir veya birden çok ağ üzerinden iletişim kurmasını sağlarlar, bu protokollerden bazıları:

- Ethernet: MAC'lerin kullanıldığı yerel iletişim protokolüdür. 

- IP: Adresleme protokolüdürç 

- TCP: Düzenli ve eksiksiz iletim yapılmasını sağlayan protokoldür.

- HTTP:Web sayfalarının görüntülenmesinde kullanılan protokoldür.






