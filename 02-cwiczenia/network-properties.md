## Ustawianie parametrów sieci

### Zadania

0. Z wykorzystaniem dowolnych systemów operacyjnych na których potrafisz uruchomić interpreter ``python`` oraz oprogramowania virtualbox odwzoruj poniższy schemat sieci:

![alt text][network]

[network]: ./network.png "Logo Title Text 2"

1. na 1 z komputerów zainstaluj i uruchom program ``server.py`` dostępne pod adresem ``https://github.com/jkanclerz/client-server-chat``
2. na 2 z komputerów zainstaluj i uruchom program ``client.py`` dostępne pod adresem ``https://github.com/jkanclerz/client-server-chat``
3. Manipulując konfiguracją sieci na poziomie virtualbox, uruchom serwer czatu, oraz udostępnij go na wybranym porcie oraz adresie tak aby istniała możliwość połączenia przez inne osoby w obrębie pracowni
4. Zainstaluj oprogramowanie serwera HTTP ``nginx`` lub innego, skonfiguruj plik index.html wg instrukcji, sprawdź dostępność strony z wykorzystaniem dowolnego klienta protokołu ``HTTP`` z różnych konfiguracji IP
5. Posługując się programami tj: ``netstat`` lub ``lsof`` sprawdź na jakich portach zostały uruchomione serwery czatu czy HTTP

Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 10.0.15.4 | ip addr add 10.0.15.4/24 dev eth0 |
| MASKA  | /24 (255.255.255.0) | |
|   |  | |
| PC 2  |  | |
| IP - address  | 10.0.15.6 | ip addr add 10.0.15.6/24 dev eth0 |
| MASKA  | /24 (255.255.255.0 )| |

Weryfikacja połączenia

Polecenie
```
ping 10.0.15.4
```

Efekt
```
Nawiązanie połączenia pomiędzy maszynami
```

Polecenie
```
ping 10.0.15.6
```

Efekt
```
Nawiązanie połączenia pomiędzy maszynami
```

Statyczna konfiguracja parametrów połączenia
Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 192.168.10.10 | ip addr add 192.168.10.10/24 dev eth0 |
| MASKA  | 255.255.255.0 | |
|   |  | |
| PC 2  |  | |
| IP - address  | 192.168.10.11 | ip addr add 192.168.10.11/23 dev eth0 |
| MASKA  | 255.255.128.0 | |
| PC 2  |  | |
| IP - address  | 172.16.100.100 | ip addr add 172.16.100.100/16 dev eth0 |
| MASKA  | 255.255.0.0 | |

Weryfikacja połączenia

Polecenie
```
ping 192.168.10.11
```

Efekt
```
Udana próba nawiązania połęczenia 
```

Polecenie
```
ping 192.168.10.10
```

Efekt
```
Udana próba nawiązania połęczenia 
```

Polecenie
```
ping 172.16.100.100
```

Efekt
```
Nieudana próba nawiązania połęczenia 
```


Nowa statyczna konfiguracja 

-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 192.168.8.130 | ip addr add 192.168.8.130/24 dev eth0|
| MASKA  | 255.255.255.0 | |
|   |  | |
| PC 2  |  | |
| IP - address  | 192.168.8.106 | ip addr add 192.168.8.106/24 dev eth0 |
| MASKA  | 255.255.255.0 | |

Weryfikacja połączenia

Polecenie
```
ping 192.168.8.106
```

Efekt
```
Udana próba połączenia
```

Polecenie
```
ping 192.168.8.130
```

Efekt
```
Udana próba połączenia
```

### Utrwalenie konfiguracji

Dlaczego? Jak? Co? :)

Utrwalamy konfiguracje aby zachować ją po wyłączeniu maszyn. Można to zrobić poprzez modyfikację pliku z konfiguracją sieci.

### Warto wiedzieć

-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
| Lokalizacja pliku z konfiguracją sieci| etc/network/interfaces | |
| DOWN -> Wyłączenie interfejsu sieciowego|ip link set eth1 down | |
| UP -> Włączenie interfejsu sieciowego| ip link set eth1 up | |
| Sprawdzenie obecnych parametrów | vi etc/network/interfaces | |
| lista wszystkich interfejsów | ip addr show | |
| Które interfejsy jakie porty słuchają | netstat | |

