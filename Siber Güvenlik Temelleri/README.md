## Internet Protokolü

**IP:** Bilgisayar ve yönlendiricilerin iletişimi için ortak ağ protokolü.

## OSI Referans Modeli

![gorsel](https://upload.wikimedia.org/wikipedia/commons/thumb/5/55/OSI_HUN.gif/640px-OSI_HUN.gif)

**Uygulama** Kullanıcı etkileşimli uygulamalar: HTTP,SMTP

**Sunu** Farklı veri formatlarının birbirine dönüşümü: ASCII, MP3, JPG

**Oturum** *(Oturumun açılması, yönetilmesi ve sonlandırılması bu katmanda gerçekleşir.)* Soket açma, oturum kurma: SQL,RPC

**Taşıma** *(Bir bilgisayardan başka bir bilgisayara bağlantıyı gerçekleştirdikten sonra, bu bağlantıyı yöneten, sonlandıran ve verinin kontrolünü sağlayan mekanızmaların devreye girdiği katmandır.)* Hata ve akış kontrolü: TCP, UDP

**Ağ** *(Bu katmada, network bazında, farklı protokoller-[Dynamic Routing](https://www.geeksforgeeks.org/what-is-dynamic-routing-in-computer-network/)- devreye girerek, bir noktadan diğer noktaya en hızlı şekilde veri gönderimi sağlanır.)* Uçtan uca iletişim, sanal adresleme: IP

**Veri Bağlama** *(Fiziksel olarak hangi cihazlarla haberleşildiği)* Ortama Erişim: Ethernet, Wireless

**Fiziksel** *(1 ve 0'lardan oluşur.)* İkili iletim: Koaksiyel, UTP ve fiber kablolar

## Katmanlar Arası Haberleşme

![gorsel](https://ecomputernotes.com/images/Communication-between-the-layers-in-OSI-model.jpg)

Görselde görüldüğü üzere en üstte *Application* katmanı var. Bu katmanda, göndermek istediğimiz paketi alıyoruz.

*Presentation* Sunum katmanında, gerekiyorsa şifreleme ya da zipleme ya da format değişikliğine ihtiyacımız varsa, bu değişiklikleri sağlarız.

*Session* Koymamız gereken oturum bilgilerini yerleştiriyoruz.

*Transport* **TSP Header** bunun içerisinde;
- Paketin karşı tarafta gönderileceği **Port Numarası**
- Paketin bizden çıkacağı **PORT Numarası**
- Hangi protokolle *(TSP,UDP)* gideceği

bilgileri vardır.

*IP Katmanı* için;
- Kendi **IP Adresimizi** yerleştiriyoruz.
- Ardından göndermek istediğimiz **IP Adresini** yerleştiriyoruz.

Bu şekilde paketler yüklenir.

Nasıl ki yukardan aşağıya doğru paketleri yüklediysek, aynı şekilde aşağıdan yukarıya doğru paketler açılmaya başlanır.

## Katmanlar ve Protokoller

### TCP/IP Referans Modeli

İnternetin temeli.

4 Katmandan oluşur.
1. Uygulama
2. Taşıma
3. Ağ
4. Ağ Erişimi

![gorsel](https://www.cemaltaner.com.tr/wp-content/uploads/2018/09/b1%C5%9F10.png)
