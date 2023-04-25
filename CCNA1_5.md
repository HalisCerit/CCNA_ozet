## Sayı Sistemleri
### İkili Sayı Sistemleri:
- Bilgisayarlardaki bütün işlemler ve veriler 1 ve 0'lardan oluşmaktadır.
- Mesela daha önce gördüğümüz IP adresleri 32 Bitlik dizilerden oluşmaktadır.

|    172    	|     16    	|    254    	|     1     	|
|:---------:	|:---------:	|:---------:	|:---------:	|
| 1010 1100 	| 0001 0000 	| 1111 1110 	| 0000 0001 	|

- Bu yapı 4 adet 8 bitten yani 4 byte'dan yani 4 adet **octetten** oluşmaktadır.
- Onluk sistemde sayılar "0" ile "9" arasındaki saylarla belirlenir.

| 128 	|  64 	|  32 	|  16 	|  8  	|  4  	|  2  	|  0  	|                 	|
|:---:	|:---:	|:---:	|:---:	|:---:	|:---:	|:---:	|:---:	|-----------------	|
| 2^7 	| 2^6 	| 2^5 	| 2^4 	| 2^3 	| 2^2 	| 2^1 	| 2^0 	|                 	|
|  1  	|  1  	|  1  	|  1  	|  1  	|  1  	|  1  	|  1  	| 1111 1111 = 255 	|

    Onluk Sistemden İkili Sayı Sistemnine Geçiş:
    
    192=?   
    192-128=64
    64-64=0
    1100 0000=192

### Hexadecimal Yapı Ve IPv6 Adresleme

|   0  	|   1  	|   2  	|   3  	|   4  	|   5  	|   6  	|   7  	|   8  	|   9  	|  10  	|  11  	|  12  	|  13  	|  14  	|  15  	|
|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|:----:	|
|   0  	|   1  	|   2  	|   3  	|   4  	|   5  	|   6  	|   7  	|   8  	|   9  	|   A  	|   B  	|   C  	|   D  	|   E  	|   F  	|
| 0000 	| 0001 	| 0010 	| 0011 	| 0100 	| 0101 	| 0110 	| 0111 	| 1000 	| 1001 	| 1010 	| 1011 	| 1100 	| 1101 	| 1110 	| 1111 	|
***
**Hatırlatma:**
- IPv4 32 bittir.
- MAC adresleri 48 bittir. 
- IPv6 adresleri 128 bittir. IPv6, IP adrelserinin statik yani cihazların gerçek IP adresleri olarak kullanılmasını sağlayacaktır.
***
- IPv6 adreleri "2001 0DB8 45CF A156 BBBB BBBB BBBB BBBB" şeklindedir.
- Verilen bu adreste **2001 0DB8 45CF A156** kısmı **Network** kısmmıdır.
- Verilen bu adreste **BBBB BBBB BBBB BBBB** kısmı **Host** kısmmıdır.
- Bu kısımlar 4 adet 16 bitlik yapının birleşmesiyle oluşur.
- IPv4 ve IPv6 adresleri çok uzun oldukarından DNS (Domain Names Server) hatırlanması kolay adların kullanılmasını sağlar.
 