## Physical Layer (Fiziksel Katman) 

### Fiziksel Katman Amacı:
- Yerel ağda ağda kablolu ya da kablosuz bağlantıyı sağlar. Bu iş NIC ile yapılır. Kablolu, kablosuz  ve bluetooth haberleşen cihazların içerisinde NIC bulunur.
*Hatırlatma: NIC'ler MAC adreslerini tutarlar.*
*Extra: GSM kartlarında NIC bulunmaz bu cihazlar IMEI aracılığıyla baz istasyonlarına bağlanır.*
- Bu katman frame denen 6. katman PDU'sunu bitlere dönüştürüp bu bitleri diğer cihazlara iletir.
- Encapsulation'ın son adımıdır.
***
### ADSL Modemin İçeriği:
Bir ADSL modem aşağıda verilen 4 cihazın birleşmesiyle oluşmuş bir cihazdır:
- Router: Routerın bir interface'i yerel ağa bakarken diğer interface'i WAN'a bağlıdır.
- Switch: Routerın LAN'a bağlı olan interface'i switchin portuna bağlıdır.
- DHCP Sunucusu: Yerel ağda IP atamasından sorumludur, switche bağlıdır.
- Access Point: Kablosuz yerel haberleşmede kullanılan componenttir.
***
### Fiziksel Katman Standart Kurumları
- ISO
- ⚠️EIA/TIA (kablolama)
- ITU-T (kablolama)
- ANSI (ADSL)
- IEEE 

TCP/IP standartlarının tamamını IETF denetler, ancak IETF fiziksel katmanı doğrudan denetlemez.
*Hatırlatma: RFC dökümanları IETF tarafından yayınlanır.*
***
### Fiziksel Katman Bileşenleri
- RJ-45 connector ethernet aletlerine bağlantı sağladığımız bileşendir. Fiziksel katman standartlarnın 3 işlevsel alanı:

**Fiziksel bileşenler** (kablolar, connectorler)
**Kodlama**
**Sinyalleme** 

### Coding (Kodlama) 
- Bit akışının ağ içerisindeki diğer cihazlar tarafından tanınabilir bir formata dönüştürülmesi **kodlama** olarak adlandırılır. Farklı iletim hızları için farklı yöntemler vardır, örneğin 10 Mbit hızlar için Mancherster kodlama, 100 Mbit için 4B/5B kodlamalar kullanılır.
Manchester kodlamada 5 Volt ve 0 Volt değerlerinin hareketlerini yönlerine göre aktarılan datayı ortaya çıkarır. Voltajın düşmesi 0'ı temsil ederken yükselmesi 1'i temsil eder.
### Signal Transmission (Sinyalleme)
- NIC kartını kullanarak elektiriksel sinyallerin kodlama yöntemine göre üretilmesine **sinyallme** denir. Sinyalleme bakır kabloda elektirikle, fiber kabloda ışıkla, kablosuz iletimde ise dalgalarla iletim yapar.

### Bandwidth (Bant genişliği)
- Saniyede iletilen bit miktarınıdır. 

Örnek: 100 MB boyutunda olan bir dosya, indirme hızı 100 Mbps olan bir networkte kaç saniyede indirilir ?
1 MB = 8 Mbit'tir yani dosya 800 Mbitdir. Bu durunda dosya 8 saniyede iner.
Latency (Gecikme): Data'nın karşıya iletime süresidir.
*Extra: Ses iletimi 150 ping'in altındaysa gerçekleşir.*
Throughput (Verim): Ağın gerçekte alabilceği verimdir. Örneğin, ağın sağlayabilceği maksimum internet beklentisi 100 Mbps olsada son kullanıcının aldığı internet 50 Mbps olabilir bu duruma throughput denir. 
Goodput: Frame'lerden bağımsız saf datanın aktarılma süresidir.
***
### Bakır Kablolama:
- Attentuation (Zayıflama): Bakır kablo kullanılan ağlarda görünen sinyal **zayıflamasıdır**, genelde bu durum 100m'den sonra oluşur. Bu durumun oluşmasının engellenmesi için kablolamalar 100 meterenin altında tutulmaktadır, bu kuralları EIA/TIA belirlemektedir. EMI (Electro Magnetic Interface) ya da RFI (Radio Frequency Interference) veri sinyallerini bozan parazitlenmelerdir.
- Bu pazaritlenmeleri engellemek adına kablo mesafe kurallarına uyulmalıdır, çapraz kablolama yapılmalıdır (twisted) ve shielded kablo kullanılmalıdır.
### Bakır Kablo Çeşitleri:
UTP (Unshielded Twisted Pair): 4x2 bükümlü kablodur.
STP (Shielded Twisted Pair): UTP kablonun korumalı halidir. 
Coaxial Cable: Koaksiyel kablo.
SFTP (Shielded Foiled Twisted Pair): UTP ve STP arasındadır. Folyolanmış bükümlü kablolaların kendi aralarında da bükümlenmesiyle oluşur. 
*Önemli: Shield kullanılan kablolarda topraklama yapılması gereklidir. SFTP'de ve STP'de topraklama yapılmalıdır.* 
### UTP-STP
İçerisinde turuncu, turuncu-beyaz, mavi, mavi-beyaz, yeşil, yeşil-beyaz, kırmızı, kırmızı-beyaz kablolardan oluşan, 305 metre olarak satılan, ucundan RJ-45 connector bağlanabilen bakır kablolardır. **Flöresan** lambalar, diğer kablolar ve  yüksek enerjili kablolar iletimi gerçkeltiren kablonun içerisindeki iletimi etkiler. Bu durumları önlemek için "kalkan" kullanılır. Bu kalkanın kullanılması durumunda topraklama gereklidir.
***Cancellation**: Kablo içerisindeki elektiriksel haraketten dolayı bir elektromanyetik dalga oluşur. Kabloların birbirine sarılarak iletim yapması (twisted olması) oluşacak elektro manyetik alanın oluşmasını engeller. Bu etkiye cancellation denmektedir.*
***Crosstalk**: İki adet twisted kablonun birbirini manyetik olarak etkilemesine crosstalk denir.*

IEEE kabloların elektiriksel özelikelerini belirler.

tablo

### Coaxial Cable
Anten kablosu olarak bilinen kablodur. Kablo TV genellikle bu kablo ile ulaştırılır. BNC, N type, F type gibi tipleri mevcutttur.


***
| T568A<br>Kablo yapısı 	| T568B<br>Kablo yapısı 	|
|:---------------------:	|:---------------------:	|
|      Yeşil-Beyaz      	|     Turuncu-Beyaz     	|
|         Yeşil         	|        Turuncu        	|
|     Turuncu-Beyaz     	|      Yeşil-Beyaz      	|
|          Mavi         	|          Mavi         	|
|       Mavi-Beyaz      	|       Mavi-Beyaz      	|
|        Turuncu        	|         Yeşil         	|
|     Kırmızı-Beyaz     	|     Kırmızı-Beyaz     	|
|        Kırmızı        	|        Kırmızı        	|



