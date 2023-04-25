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

- LLC Sublayer Türkçe'siyle LLC alt katmanı, Data Link katmanından Network katmanına geçişi kontrol eder. Üstteki katmanda kullanılan protokol IPv4 mü IPv6 mı bu bilgiyi tanımlar.
- LLC'nin de bulunduğu ethernet frame yapısı, frame'in oluşma sıraısyla beraber şu şekilde gösterilebilir:

<img src="./Diagrams/1_7_1.png" alt="image" width="55%" height="55%">

- MAC sublayer medyaya erişimden ve veriyi kapsüllemeden sorumludur. 
- IEEE 802.3 Ethernet protokolünde ethernet frame'in yapısını temel anlamda 3'e ayırmıştır:    
    - Ethernet Addressing: MAC adresi içermesi.
    - Frame datası.
    - Ethernet Hata Tespiti: FCS içermesi.
     
### Ethernet II Frame Yapısı

<img src="./Diagrams/1_7_2.png" alt="image" width="70%" height="70%">
kjsahkfjh