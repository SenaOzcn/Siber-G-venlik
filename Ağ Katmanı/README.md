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
