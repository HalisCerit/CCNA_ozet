# 3- Protokoller ve Modeller
**OSI**: Data haberleşmesini standartlaştırmatası için tasarlanmış 7 katmandan oluşan protokol kümesi.
**TCP/IP**: 4 katmandan oluşan, protokol kümesidir.


## MAC Adresleri ve IP Adresleri
- MAC ve IP adreslerini cihazların aralarında haberleşme yaparken kullanırlar.
#### MAC Adresleri:
- **48 bitten** oluşurlar.
- NIC üzerinde bulunurlar, fiziksel adres olarak da geçerler, eşsizdirler.
- MAC adresleri *9C-35-5B-5F-AA-BB* tazrındadırlar.
- Ethernet Kartı üzerinde **Bured-in** adreslerdir.
- NIC'de protokoller yüklü gelir ama istenirse değiştirilebilir, bunlar TCP/IPv4 veya TCP/IPv6'dır.
*Wifi kartı da bir NIC kartıdır.*
#### IP Adresleri:
- 32 bit / 4 kısımdan oluşurlar.
- IP adresleri 192.168.1.5 tazrındadır, bölümler (0-255) aralığında olmalıdır, yani 0 yada 255 alamazlar. 
- IP adresleri MAC adreslerindeki kalıcı adreslerin tersine mantıksal adreslerdir.
- IP adresi 192.168.5.1 olan bir cihazın 192.168.5 kısmı bulunduğu "Network"ü temsil ederken, .1 kısmı yerel ağdaki "Host" numarasını gösterir.

### Hatırlatma:
*Router networkleri birbirine bağlar, router uçları farklı ağlara bakar.*
*Switch son kullnıcıları ağa dahil eder.*

## ŞEKİL 1_3_1


## İletişim Temelleri:
- Source (Kaynak).
- Destination (Hedef).
- Media (Ortam).

*Ağlar "scale" ve "complexity" olarak değişebilir, yalnızca bağlantı olması yetmez.*

### *Message Source > Transmitter > Transmission Medium > Reciver > Message Destination*

## İletişim Protokolleri:
- Tüm iletişim protokoller çerçevesinde gerçekleşir.
- Protokoller iletişimin izleyeceği kurallardır.
- Kurallar protokollere bağlıdır.

*Kurallar dizisine protokol denir.*







