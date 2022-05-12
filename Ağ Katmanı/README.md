# IP - The Internet Protocol

IP, yalnızca fiziksel bağlantılar üzerinden değil, aynı zamanda yönlendirici ağları arasında da ağlar arasında iletişim kurmak için kullanılır. Kullanılan adresleme şeması ya IPv4 ya da IPv6'dır.

**Ağ maskesi(Netmask)** , bir ağın ne kadar büyük olduğunu ve ağ içinde hangi paketin yönlendirildiğini ve hangi paketin ağ dışına yönlendirileceğini belirler.

Bazı örnerkler aşağıdaki tablodaki gibidir;

| IP Adresi|     Slash Notation     |    Netmask  |
| ------------- | ------------- | ------------- |
| 10.0.0.1 | /8 - Example: 10.0.0.1/8  | 255.0.0.0              |
| 172.16.1.1  | /12 - Example: 172.16.1.1/12 | 255.240.0.0              |
| 192.168.0.1 | /16 - Example: 192.168.0.1/16 | 255.255.0.0|
| 192.168.0.1 | /24 - Example: 192.168.0.1/24 | 255.255.255.0 |

Yukarıdaki tabloda IP adresleri yalnızca dahili organizasyonel kullanım için ayrılmıştır. Internet üzerinden yönlendirilmemeleri gerekir. Bu tür IP adreslerine genel olarak **RFC1918** adresleri denir.

# Farklı Ağlar

RFC1918 içindeki farklı ağlara ve ağların ne kadar büyük olduğuna bir göz atalım:

- 10.0.0.0/8 - 16 milyondan fazla IP adresi
- 172.16.0.0/12 - Yaklaşık 1 milyon IP adresi
- 192.168.0.0/16 - 65534 IP adresi

IP segmentleri ayrıca daha küçük ve daha ayrıntılı ağlara bölünebilir.

Her ağın, ağdaki her ana bilgisayara trafik yayınlamak için ayrılmış bir adresi vardır, buna **yayın adresi** denir. Yayın verileri, yalnızca tek bir ana bilgisayara veri göndermek yerine ağdaki herkese veri göndermek anlamına gelir.
