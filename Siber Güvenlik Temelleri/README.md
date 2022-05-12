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

*Her katman çalışmak için bir alt katmanın servisine ihtiyaç duyar.*

**Switch** Sadece lokal ağ üzerinde, aynı ağda bulunan cihazların, birbiriyle haberleşmesi için konumlandırılır.

**Router** IP'yi anlayabilecek cihazlar.

### Katman 7 - Uygulama Katmanı

Uygulamanın iş mantığı ve işlevselliği bu katmadandır. Kullanıcıların ağ üzerinden hizmetlerle etkileşim kurmak için kullandıkları şeydir. Çoğu geliştirici, *Uygulama Katmanında* uygulamalar oluşturur.

- HTTP - Web uygulamalarına erişmemizi sağlar.
- FTP - Kullanıcıların dosya aktarmasına izin verir.
- SNMP - Ağ cihazı yapılandırmalarını okumak ve güncellemek için protokol.

### Katman 6 - Sunum Katmanı

Tipik olarak görünmeyen bir katmandır. Verileri uyarlamaktan, dönüştürmekten ve çevirmekten sorumludur.

Bu katman, uygulamanın ve altındaki katmanların birbirini anlayabilmesini sağlamak içindir.

- Metin ve verileri temsil etmek için kullanılan *Kodlama Şemaları*, örneğin ASCII ve UTF
- Hizmetler için şifreleme, örneğin SSL ve TSL
- Sıkıştırma, örneğin birçok HTTP uygulamasında gösterilen GZip.

### Katman 5 - Oturum Katmanı

Bu katmanın sorumluluğu, uygulama ile aşağıdaki katmanlar arasındaki bağlantıları yönetmektir. Oturumlar olarak da adlandırılan bağlantıların kurulmasını, sürdürülmesini ve sonlandırılmasını içerir.

Yaygın protokoller:
- SOCKS - Bir proxy sunucusu aracılığıyla paket göndermek için bir protokol.
- NetBIOS - Oturumlar oluşturmak ve adları çözmek için eski bir Windows protokolü.
- SIP - VOIP ieltişimlerine katılmak için kullanılan protokoldür.

### Katman 4 - Taşıma Katmanı

Uygulamaların ağ üzerinde temsil edilmesini sağlayan katman.

Bu katmandaki bilinen uygulamalar:

- TCP - Birçok uygulama için kullanılır, kararlılık sağlar, herhangi bir zamanda ne kadar veri gönderilebileceğinin kontrolü, güvenilirlik ve daha fazlası.
- UDP - Birçok hizmet için hafif ve hızlı protokol kullanımı.
- QUIC - Daha hızlı bağlantılar için tasarlanmış bir protokol be HTTP protokolünün 2. sürümüyle beraberdir.

### Katman 3 - Ağ Katmanı

Paketleri yönlendiriciler aracılığıyla ağlar arasında yönlendiren katmandır.

Bu katmanda aşağıdaki protokoller bulunur:

- IP - İnternete erişirken kullanılır. IP sürüm 4 ve 6 olmak üzere iki versiyondan gelir.
- ICMP - Ağ cihazları ve ağ operatörleri tarafından, ağ bağlantılarını teşhis etmek veya cihazların hata koşullarını gönderip bunlara yanıt vermesi ve daha fazlası için kullanılır.
- IPSec - İki ağ cihazı arasında şifreli ve güvenli bağlantılara izin verir.

### Katman 2 - Bağlantı Katmanı

Bağlantı ağları, adından da anlaşılacağı gibi, ağ düğümlerinin bağlı olduğu fiziksel bağlantılar aracılığıyla paket göndermek için tasarlanmış protokollerden oluşur. 

Bu katmandaki protokoller şunları içerir:

- Ethernet - Fiziksel bir kablo kullanarak ağlara bağlanırken çoğu işletim sistemi tarafından kullanılan bir protokol.
- Wi-Fi - Radyo sinyalleri aracılığıyla ağlara erişmek için, IEEE 802.11.xx adlı bir protokol ailesi kullanılır.
- NDP - IP sürüm 6(IPv6), IPv6 aracılığıyla iletişim kurmak için gereken bilgileri toplamak için bağlantı katmanında bu protokol kullanılır.

### Katman 1 - Fiziksel Katman

Fiziksel katman, bitlerin ve baytların fiziksel bir ortam arasında aktarılmasına izin veren sinyali temsil eder. Elektrik sinyalleri veya örneğin fiber kullanılarak bir kablo üzerinden radyo veya sinyaller aracılığıyla aktarılabilir.

Fiziksel katman protokollerinin örnekleri şunları içerir:

- CAN Bus - Mikrodenetleyicilerde ve diğer cihazlarda, bilgisayar içermeyen diğer benzer cihazlarla iletişim kurmak için kullanılır. Genellikle ICS'de kullanılır.
- Ethernet Fiziksel Katman - Ethernet tarafından, saniyede birçok gigabayt trafik hızına kadar sinyal göndermek için fiziksel katmanda kullanılır.
- Bluetooth Fiziksel Katman - Bluetooth'un ayrıca radyo sinyallerinin nasıl gönderileceği ve alınacağı konusunda kendi özellikleri vardır.
