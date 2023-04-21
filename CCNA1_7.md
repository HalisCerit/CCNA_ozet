## Network Katmanı
- Data Link katamanında type kısmıyla belirtilen katman **network katmanı**dır.
***
#### Hatırlatma:
Örnek olması için bir ağda bulunan X cihazının:
IPv4 adresi: 192.168.5.1,
Subnet Maskesi: 255.255.255.0,
Default Gateway Adresı:192.168.5.5'dır.


1- Bu cihazın Subnet maskesi 255.255.2555.0 olduğundan IPv4 adresinde bulunan ilk 3 octeti (192.168.5) cihazın **network** kısmını, son octet  kısmı ise **host** ifade etmektedir.
2- Bu cihazın aynı ağdaki başka cihazlarla IPv4 adresini kullnarak iletişim kurmak istemesi durmunda ARP protokolü MAC adreslerının bulunmasını sağlar.
3- ARP (Adres Resolution Protocol): 2. katmanda cihazların IPv4 adreslerini kullanarak MAC ağdaki diğer cihazların IPv4 adreslerini öğredikleri protocoldür.
4- Switchler erişilebilir ağlarda bulunan cihazların MAC adreslerini **MAC Adres Tablo**larında tutarlar.
5- Cihazlar arasında iletilen paketler routerlara ulaştıktan sonra iletim **Router Tablosu**nda bulunan satırlara bakılarak yönlendirme işlemi yapılır.
6- Switchler asla IP adresi tutmazlar.
7- Routerın asıl görevi **networkleri bağlamaktır.**
***
OSI TABLOSU RESMI
***

- Network katmnında temel anlamda **4 işlem** vardır. Bunlar:

1- Adresleme
2- Encapsulation
3- Routing 
 3.1- Best Path Selection: Paketin routing tablosuna bakılarak yönlendirilmesidir.
3.2- Packet Switching: Paketin seçilen bu yoldan iletilmesidir.
4- Decapsultaion
###### *Extra: Routing Table'da 850.000 satır bulunmaktadır.*
***
Network Layer Characteristics
- Bu şekilde Router tablosu şı şekilde oluşmaktadır.
1- 10.0.0.5 IP adresli hostun ağa bağlanmasıyla 

***
IP Kapsülleme:
- Transport katmanındaki encapsulation segment headerın datanın önüne eklenmesiyle oluşmaktadır.Bu katmandaki PDU **segment** olarak adlandırılmaktadır.
-  Network katmanındaki encapsulation IP hederın segmentin başına gelmesiyle oluşur, bu katmandaki PDU **packet** olarak adlandırılmaktadır.
- Packeti oluşturan IPv4 bilgisi 32 bitken IPv6 bilgisi 128 bittir.
- IP adresleri kaynaktan hedefe gidene kadar değişmez. Ancak günümüzde NAT kullanıldığından dolayı verilen sahte IP sunucuya ulaşana kadar diyebiliriz. Yine de IP adresleri yol boyunca değişmez demek yanlış bir tanımlama olmayacaktır.
***
IP özellikleri IP'nin en düşük yüke sahip olacağı şekilde tasarlanmıştır. Bu  özellikler şu şekilde tanımlanabilir:
- Connectionless (Bağlantısız)
- Best Effort (En İyi Çaba)
- Media Indiependent (Medyadam Bağımsız)
***
### 1-Connectionless 

















