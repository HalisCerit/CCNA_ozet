## Physical Layer (Fiziksel Katman) 

### Fiziksel Katman Amacı:
- Yerel ağda kablolu ya da kablosuz bağlantıyı sağlar. Bu iş NIC ile yapılır. Kablolu, kablosuz  ve bluetooth ile haberleşen cihazların içerisinde NIC bulunur.
*Hatırlatma: NIC'ler MAC adreslerini tutarlar.*
*Extra: GSM kartlarında NIC bulunmaz bu cihazlar IMEI aracılığıyla baz istasyonlarına bağlanır.*
- Bu katman, 6. katman PDU'su olan frame'i bitlere dönüştürür ve bu bitleri diğer cihazlara iletilmesini sağlar.
- Encapsulation'ın son adımıdır.
***
### ADSL Modemin İçeriği:
Bir ADSL modem aşağıda verilen 4 cihazın birleşmesiyle oluşmuş bir cihazdır:
- Router: Routerın bir interface'i yerel ağa bakarken diğer interface'i WAN'a bağlıdır.
- Switch: Routerın LAN'a bağlı olan interface'i switchin portuna bağlıdır.
- DHCP Sunucusu: Yerel ağda IP atamasından sorumludur, switche bağlıdır.
- Access Point: Kablosuz yerel haberleşmede kullanılan bileşendir, switche kablosuz bağlanmak isteyen cihazlar switche access point cihazı aracılığıyla bağlanır.
***
### Fiziksel Katman Standart Kurumları
- ISO
- ⚠️EIA/TIA (kablolama)
- ITU-T (kablolama)
- ANSI (ADSL)
- IEEE 

TCP/IP standartlarının tamamını IETF denetler, ancak IETF fiziksel katmanı doğrudan denetlemez.
##### *Hatırlatma: RFC dökümanları IETF tarafından yayınlanır.*

***

## Fiziksel Katman Bileşenleri
Fiziksel katman standartlarnın 3 temel alanı:
**Coding**,
**Signal Transmission**, 
**Media bileşenleri** (kablolar, connectorler)'dir.
***

## 1- Coding (Kodlama) 
- Bit akışının ağ içerisindeki diğer cihazlar tarafından tanınabilir bir formata dönüştürülmesi **kodlama** olarak adlandırılır. Farklı iletim hızları için farklı yöntemler vardır, örneğin 10 Mbit hızlar için Mancherster kodlama kullabılırken, 100 Mbit için 4B/5B kodlamalar kullanılır.
Manchester kodlamada aktarılan veriyi 5 Volt ve 0 Volt değerlerinin hareketlerini yönlerine göre oluşturur. Voltajın düşmesi 0'ı temsil ederken yükselmesi 1'i temsil eder.

## 2- Signal Transmission (Sinyalleme)
- NIC kartını kullanarak elektiriksel sinyallerin kodlama yöntemine göre üretilmesine **sinyallme** denir. Sinyalleme bakır kabloda elektirikle, fiber kabloda ışıkla, kablosuz iletimde ise dalgalarla iletim yapar.

    ### Bandwidth (Bant genişliği)
    - Saniyede iletilen bit miktarınıdır. 

    Örnek: 100 MB boyutunda olan bir dosya, indirme hızı 100 Mbps olan bir networkte kaç saniyede indirilir ?
    1 MB = 8 Mbit'tir yani dosya 800 Mbitdir. Bu durunda dosya 8 saniyede iner.

    ### Latency (Gecikme)
    - Data'nın karşıya iletime süresidir.
    *Extra: Ses iletimi 150 ping'in altındaysa gerçekleşir.*
    ### Throughput (Verim)
    - Ağın gerçekte alabilceği verimdir. Örneğin, ağın sağlayabilceği maksimum internet beklentisi 100 Mbps olsada son kullanıcının aldığı internet 50 Mbps olabilir bu duruma throughput denir. 
    ### Goodput
    - Frame'lerden bağımsız saf datanın aktarılma süresidir.

## 3- Media Bileşenleri
### **Bakır Kablolalar:**
Bakır Kablo Çeşitleri:
- Coaxial Cable: Koaksiyel kablo.
- UTP (Unshielded Twisted Pair): İçi bükümlü dışı korunasız bakır kablodur.
- STP (Shielded Twisted Pair): UTP kablonun korumalı halidir. 
- SFTP (Shielded Foiled Twisted Pair): STP kablonun daha korumalı halidir. Folyolanmış bükümlü kablolaların kendi aralarında da bükümlenmesiyle oluşur.
*Önemli: Shield kullanılan kablolarda topraklama yapılması gereklidir. SFTP'de ve STP'de topraklama yapılmalıdır.* 
- Bakır kablolama düşük üretim maliyeti, yaygınlık ve güvenilirliği nedeniyle en yaygın olarak kullanılan kablo türüdür.
- Bakır kablo kullanılan ağlarda görünen sinyal zayıflamasına **Attentuation (Zayıflama)** denir. Genelde bu durum 100m'den sonra oluşur. Attentuation durumunun oluşmasının engellenmesi için kablolamalar 100 meterenin altında tutulmaktadır, bu kuralları TIA/EIA belirlemektedir.Bununla birlikte **flöresan lambalar**, E.M.I. (Electro Magnetic Interface) ya da R.F.I. (Radio Frequency Interference), bakır kabloda iletimi bozan parazitlenmelere sebep olurlar. Bu pazaritlenmeleri engellemek adına kablolarda mesafe kurallarına uyulmalıdır, çapraz kablolama yapılmalıdır (**twisted**) ve shielded kablo kullanılmalıdır.
- İletim sırasında kablo içerisindeki elektiriksel hareketten kaynaklı elektromanyetik dalgalar oluşur.Bu etkiyi azaltmak için kablonun içerisindeki bakır teller birbirine sarılır (**twisted** hale getirilir) bu sayede elektromanyetik dalga oluşması azaltılır.
- Bu etkiye **cancellation** denmektedir.
    UTP (Unshielded Twisted Pair)-STP (Shielded Twisted Pair) Kabloların içerisinde sırasıyla:
    - Turuncu,
    - Turuncu-beyaz,
    - Mavi,
    - Mavi-beyaz,
    - Yeşil,
    - Yeşil-beyaz,
    - Kahve rengi, 
    - Kahve rengi-beyaz kabloları bulunur. 
- UTP ve STP 305 metre olarak satılan, ucundan RJ-45 connector bağlanabilen bakır kablolardır. Bu kablolar **Flöresan** lambalar, diğer kablolar ve  yüksek enerjili kablolar tarafından etkilmemek için"kalkan" kullanılır. **Bu kalkanın kullanılması durumunda topraklama gereklidir**.

Önemli terimler: 

- ***Attentuation**: Bakır kablo kullanan ağlarda gözlemlenen sinyal zayıflamasıdır.*

- ***Cancellation**: Kablo içerisindeki elektiriksel haraketten dolayı bir elektromanyetik dalga oluşur. Kabloların birbirine sarılarak iletim yapması (twisted olması) oluşacak elektro manyetik alanın oluşmasını engeller. Bu etkiye cancellation denmektedir.*

- ***Crosstalk**: İki adet twisted kablonun birbirini manyetik olarak etkilemesine crosstalk denir.*

IEEE kabloların elektiriksel özelikelerini belirlerken EIA/TIA kablosal özellikleri belirler. 
TIA/EIA-568 şu unsurları standartlaştırır:
- Kablo Tipleri
- Kablo Uzunlukları
- Könektörler
- Kablo Sonlardırma
- Test Yöntemleri

IEEE ise UTP kabloları performansa göre derecelendirir:
- CAT3 (Katagori 3)
- CAT5 ve 5e
- CAT6 ve 6e

### Coaxial Cable Özelikleri
- Anten kablosu olarak bilinen kablodur. 
- Kablo TV genellikle bu kablo ile ulaştırılır. 
- BNC, N type, F type gibi tipleri mevcutttur.


### UTP Cable Özellikleri
- Temelinde korumasız ancak bükümlü bakır kablodur.
- UTP standartlarını TIA/EIA belirler.
- Bazı UTP tipi kabloların özellikleri şunlardır:

| Twisted Pair <br> Medium (TIA) 	|    Speed          	|          Bandwidth     	|
|:-------------------------:	|:------------:	|:-------------:	|
|            cat5           	|  10/100 Mbps 	|    100 MHz    	|
|           cat5e           	|   1000 Mbps  	|    100 MHz    	|
|            cat6           	|   1000 Mbps  	|    250 MHz    	|
|        **_cat6a_**        	| **_10Gbps_** 	| **_500 MHz_** 	|
|            cat7           	|    10Gbps    	|    600 MHz    	|
|            cat8           	|   25/40Gbps  	|    2000 MHz   	|


- IEEE 802.3 (Ethernet Standartı), 1. katmanda hızlar, kablo tipleri, kodalamayı denetlerken 2. katmanda MAC adresini denetler.
- IEEE 803.3 Standartını da dahil ederek UTP kabloların bazı özelliklerini şu şekilde gösterebiliriz: 

|    Standart    	|   Speed (IEEE)  	|    Reach   	| Twisted Pair Medium (TIA) 	| Cable Construction 	| Date of Standart 	|
|:--------------:	|:---------------:	|:----------:	|:-------------------------:	|:------------------:	|:----------------:	|
|     802.3i     	|     10BASE-T    	|    100M    	|            CAT3           	|       UTP STP      	|       1990       	|
|     802.3u     	|    100BASE-T    	|    100M    	|            CAT5           	|       UTP STP      	|       1995       	|
|     802.3ab    	|    1000BASE-T   	|    100M    	|           CAT5e           	|       UTP STP      	|       1999       	|
| **_802.3.an_** 	| **_10GBASE-T_** 	| **_100M_** 	|        **_CAT6a_**        	|    **_UTP STP_**   	|    **_2006_**    	|
|     802.3bq    	|    25GBASE-T    	|     30M    	|            CAT8           	|         STP        	|       2016       	|
|     802.3bq    	|     40BASE-T    	|     30M    	|            CAT8           	|         STP        	|       2016       	|

***Foreshadowing: 802.15 Wifi standartıdır.***
- CAT6a günümüzde en popüler UTP kablo standartıdır. 
- UTP kabloların isimlendirme standartı şu şekildedir:

|      **10**      	|      **BASE**      	|      **T**      	|
|:----------------:	|:------------------:	|:---------------:	|
| Bağlantı<br>Hızı 	| Paralel Değil de <br> Tek Data İletim 	| Twisted<br>Pair 	|

- 1000BASE-T, 100BASE-T ve 10BASE-T'yi çalıştırır. Bu kablolar backwards compatible tasarlanmıştır.
- Switch üzerinde 24 x 1000BASET yazıyorsa 24 portlu CAT5e, CAT5 ve CAT3'ü çalıştıran bir cihaz olduğunu gösterir.
- UTP ve STP kablolamalar RJ-45 Connector ile sonlandırılır.

### UTP Kablolarda Kablolama 

**Cross Kablolama:**
- Aynı tipte cihazların birbirleriyle konuşması için cross kablolama kullanılır.

<img src="./Diagrams/1_4_1.png" alt="image" width="70%" height="70%">

**Straight Kablolama:**
- Farklı cihazları birbirlerine bağlarken bu yöntem kullanılır. Örneğin bir bilgisayar ile switch yada switch ile router birbirlerine bağlanırken straight kablolama kullanılır. 
- Switch crosslmayı içerisinde yapar bu sayede günlük hayatta straigth kablolama kullanılır.

<img src="./Diagrams/1_4_2.png" alt="image" width="70%" height="70%">

***
**T568A ve T568B RJ-45 Sonlandırma Standartları:** 
- İki sonlandırma standartı arasındaki fark tellerin sırasıdır.
- T568B genelde Birleşik Devletlerde popüler olan bir standartdır, T568A ise Avrupa ve Pasifik kıtalarında daha yaygın kullanılmaktadır.  
- 10Mbps ve 100Mbps haberleşmede 4 adet tel kullanılır. 
- İnternet ilk çıktığı zamanlar yalnızca 4 tel kullanılıyrodu daha sonra 1000Mbps'e geçilince 8 telin de 8'i kullanılır hale gelmiştir.

<img src="./Diagrams/1_4_3.png" alt="image" width="40%" height="40%">

**T568A ve T568B Standartlarıyla Straight ve Cross Kablolama:**

<img src="./Diagrams/1_4_4.png" alt="image" width="90%" height="90%">

- Son 10-15 yıldır cihazlar arasında straight kablolama kullanılmaktadır. Bu **AUTO-MDIX** teknolojisi sayesinde mümkün olmuştur. AUTO-MDIX cihazları otomatik crosslar.

### Extra: Rollover Cable
- Rollover Cable (Konsol Kablosu) İlk configirasyon yapmada kullanılan DB9 seri portlu connector kullanan bir kablo çeşitidir.
- Bir ucu RJ-45 iken diğer ucu DB9 portundadır.
- Hızı 9.6 Kbps kadardır.

***

Data kablolaması

