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
| Nazwa                     | Alpine Linux              |                           |
| Parametry IP              | $ ip all              |show all eth interfaces (ip configuration)  |
| routing table             | $ ip route show       | what is gateway?! default jest gatewayem  |
| DNS config                | $ cat /etc/resolv.conf| which DNS  were set                   |

### Konfiguracja połączenia sieciowego 

| Parametr      | wartość       | komentarzu |
| ------------- |:-------------:| -----:|
| Adres IP      | 10.0.2.15     | przydzielony przez DHCP |
| Maska podsieci| 10.0.2.15/24  | Notacja cidr 255.255.255.0 | 
| Brama         | 10.0.2.2      | default from route table|
| DNS 1         | 10.10.4.204     | cat /etc/resolv.conf |
| DNS 2         | 1.1.1.1      | nslookup uek.krakow.pl |


## Charakterystyka mojego komputera w sieci domowej

| Parametr      | wartość       | komentarzu |
| ------------- |:-------------:| -----:|
| Adres IP      | 192.168.8.130  | ipconfig |
| Maska podsieci| 225.225.255.0 | ipconfig | 
| Brama         | 192.168.8.1   | ipconfig |
| DNS 1         | 192.168.8.1    | ipconfig /all |


### Schemat sieci

<mxfile host="app.diagrams.net" modified="2020-04-18T23:05:10.013Z" agent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.163 Safari/537.36" etag="7aSc9Sys2Q5CODTBZE4t" version="12.9.2" type="github"><diagram name="Page-1" id="c37626ed-c26b-45fb-9056-f9ebc6bb27b6">3VhNd6IwFP01LOshBKwu1X7MotPTMy7amV0KETIGwsRQcX79JJAImGrbczpFdaG++xJC7n3XZ3DgLC1vOcqT7yzC1PHcqHTgleN5lx6Q7wrYaMCHNRBzEtUQaIA5+Ys16Gq0IBFedQYKxqggeRcMWZbhUHQwxDlbd4ctGO2umqMYW8A8RNRGH0kkEo0C120S3zCJE730KNCJZxQuY86KTK/neHBRvep0isy19PhVgiK2bkHw2oEzzpiov6XlDFNFraGtnnezJ7u9b44z8Z4J9zRYjJeT+SR8eAyiVXb79Atc6Ku8IFpoPn6wQmDueEOU5g6cZs8r9SFjKleZPqtMLCqk2pTYGCIrKrBazJXpdUIEnucoVNm1rByJJSKlMgLb2S+YC1zu3Q/YsiSLD7MUC76RQ/QEaIjVhQehjtctGc2YpKXgUGNIV068vXTDnvyiCfwAmWr+Dik4ksWmQ8ZFwmKWIXrdoNMubc2YO8ZyTdZvLMRGOwcVgnWpxCURT2r6INDRz1bmqtRXroKNCbJoorwjw4xluEZuiNpula/3oW7+sDhyr6zgIT5EivY04jEWb1WiLTbHFAny0r2Pz1fOssE8RVzkiSLn9KwA/N6tAHu1QssIjS16twI8BStAywpXxRLxJToBHwSXR9cS/ONpCe6x+MA/BR/4H2oJR9YAAq/3wgcWKV9Y+MD5SAOQ+31qB61ZKmymVVEPhglOwTCBZZiHWe/GGB1bQxhaLIGxNwDD0WA0AObuWoTJrYsuKyvB2RLPGGW8Kb2FrLsdCFESZzIMJVXyQAenikgiD74TnUhJFFW2e02GrlCfoMT2QG2kALYU/itKeP9LidEhJVz75+tslID+zmnhlWbxpUqMDyoxPGMldtu227MSxpN7pLCfb5yNFMH4yH6egN1PzYlrweSe2jIM/xTMJC5W1Z+jiRwARnnZJM0p7W5yb/9/dY3MkqUbdWipV5JBvdieA97ZyA/e8QTlk+SXYfPQt8q1HqzD638=</diagram></mxfile>


aby załączyć obrazek 

```markdown
![alt schemat](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)![alt schemat](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)

![alt schemat](images/my-network-schema.png)
```

![my network](network.png)

