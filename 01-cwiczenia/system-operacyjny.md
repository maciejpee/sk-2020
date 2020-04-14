## System operacyjny w środowisku sieciowym

### Zadania


1. Z wykorzystaniem maszyny wirtualnej, zainstaluj SO oraz wypisz parametry konfiguracji IP tj:
   * Adres
   * Maska
   * Adres bramy
   * DNS 1
   * DNS 2
    
    Powyższe parametry uzyskaj na wszystkich z wymienionych systemów

   * [Linux Alpine](https://alpinelinux.org/)
   * [Linux Debian](https://www.debian.org/)
   * [Linux CentOS](https://www.centos.org/)
   * Windows 

2. Sprawdź oraz przygotuj charakterystykę dla przykładowego urządzenia w Twojej sieci domowej
   * Adres
   * Maska
   * Adres bramy
   * DNS 1
   * DNS 2
  
    Przygotuj dokumentację graficzną Twojej sieci domowej, uwzględnij adresy i urządzenia

3. Zarejestruj konto w CISCO Academy celem pobrania Packet tracer
   https://www.netacad.com/courses/packet-tracer

4. Dlaczego umiejętnosci z zakresu sieci komputerowych mogą mi się przydać? :)


### Charakterystyka systemu operacyjnego

| Charakterystyka           | wartość               | komentarzu                |
| -------------             |:-------------:        | -----:                    |
| nazwa                     | linux                 | centos 7                  |
| cfg interfejsów           | centos 7 | /etc/sysconfig/network-scripts         |
| program (parametry sieci) | niewiem               |                           |
| Nazwa                     | Apine                 |                           |
| Parametry IP              | $ ip all              |show all ip configuration  |
| routing table             | $ ip route show       | default jest gateway -em  |
| DNS config                | $ cat /etc/resolv.conf| DNS                      |

### Konfiguracja połączenia sieciowego Alpine

| Parametr      | wartość       | komentarzu |
| ------------- |:-------------:| -----:|
| Adres IP      | 10.0.2.15     | przydzielony przez DHCP |
| Maska podsieci| 10.0.2.15/24  | Notacja cidr | 
| Brama         | 10.0.2.2      | #wg ip groupe show |
| DNS 1         | 10.10.0.8     |  |
| DNS 2         | 10.10.04      |  |

### Konfiguracja połączenia sieciowego CentOS

| Parametr      | wartość       | komentarzu |
| ------------- |:-------------:| -----:|
| Adres IP      | 127.0.0.1     | przydzielony przez DHCP |
| Maska podsieci| 127.0.0.1/8   | Notacja cidr | 
| Brama         | 10.0.2.2      | #wg ip groupe show |
| DNS 1         | 10.10.0.8     |  |
| DNS 2         | 10.10.04      |  |


## Charakterystyka mojego komputera w sieci domowej

| Parametr      | wartość       | komentarzu |
| ------------- |:-------------:| -----:|
| Adres IP      | 10.71.119.83  |  |
| Maska podsieci| 225.225.240.0 |  | 
| Brama         | 10.71.112.1   |  |
| DNS 1         | 217.113.224.135     |  |
| DNS 2         | 217.113.224.134      |  |

### Schemat sieci

aby załączyć obrazek 

```markdown
![alt schemat](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)![alt schemat](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)

![alt schemat](images/my-network-schema.png)
```

![my network](network.png)

