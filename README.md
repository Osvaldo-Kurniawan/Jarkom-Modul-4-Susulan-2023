# Jarkom-Modul-4-Susulan-2023

| Name           | NRP        | Kelas     |
| ---            | ---        | ----------|
| Gabrielle Immanuel Osvaldo K. | 5025211135 | Jaringan Komputer (B) |
| Victor Gustinova | 5025211159 | Jaringan Komputer (B) |

# Gambar Topologi

<img width="667" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/934073e8-230d-4f02-991b-0c7f68c7de24">

# VLSM
## Tree VLSM
![All](https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/125529445/fed69413-e7aa-466f-9be3-3c5262759b6b)

## Pembagian IP VLSM
![image](https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/125529445/09e5e61c-4486-4870-934a-34abab2c4282)

## Config Network
Pada config ini akan diberikan ip address yang disesuaikan dengan subnet masing-masing interface. Juga dilakukan konfigurasi iptables dan nameserver agar node dapat mengakses internet.

### Aura
```
auto eth0
iface eth0 inet dhcp
up iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 10.16.0.0/19

#A9
auto eth1
iface eth1 inet static
address 10.16.24.129
netmask 255.255.255.252

#A11
auto eth2
iface eth2 inet static
address 10.16.24.133
netmask 255.255.255.252

#A1
auto eth3
iface eth3 inet static
address 10.16.24.113
netmask 255.255.255.252
```
### Denken
```
#A9
auto eth0
iface eth0 inet static
address 10.16.24.130
netmask 255.255.255.252
gateway 10.16.24.129
up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A10
auto eth1
iface eth1 inet static
address 10.16.22.1
netmask 255.255.255.0
```

### Royal Capital
```
#A10
auto eth0
iface eth0 inet static
address 10.16.22.2
netmask 255.255.255.0
gateway 10.16.22.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Wille Region
```
#A10
auto eth0
iface eth0 inet static
address 10.16.22.3
netmask 255.255.255.0
gateway 10.16.22.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Eisen
```
#A11
auto eth0
iface eth0 inet static
address 10.16.24.134
netmask 255.255.255.252
gateway 10.16.24.133
up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A13
auto eth1
iface eth1 inet static
address 10.16.24.137
netmask 255.255.255.252

#A14
auto eth2
iface eth2 inet static
address 10.16.24.141
netmask 255.255.255.252

#A17
auto eth3
iface eth3 inet static
address 10.16.24.145
netmask 255.255.255.252

#A12
auto eth4
iface eth4 inet static
address 10.16.24.105
netmask 255.255.255.248
```

### Stark
```
#A13
auto eth0
iface eth0 inet static
address 10.16.24.138
netmask 255.255.255.252
gateway 10.16.24.137
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Lugner
```
#A14
auto eth0
iface eth0 inet static
address 10.16.24.142
netmask 255.255.255.252
gateway 10.16.24.141
up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A16
auto eth1
iface eth1 inet static
address 10.16.12.1
netmask 255.255.252.0

#A15
auto eth2
iface eth2 inet static
address 10.16.23.1
netmask 255.255.255.0
```

### Turk Region
```
#A16
auto eth0
iface eth0 inet static
address 10.16.12.2
netmask 255.255.252.0
gateway 10.16.12.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf

```

### Grobe Forest
```
#A15
auto eth0
iface eth0 inet static
address 10.16.23.2
netmask 255.255.255.0
gateway 10.16.23.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Linie
```
#A17
auto eth0
iface eth0 inet static
address 10.16.24.146
netmask 255.255.255.252
gateway 10.16.24.145
up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A18
auto eth1
iface eth1 inet static
address 10.16.20.1
netmask 255.255.254.0

#A19
auto eth2
iface eth2 inet static
address 10.16.24.149
netmask 255.255.255.252
```

### Granz Channel
```
#A18
auto eth0
iface eth0 inet static
address 10.16.20.2
netmask 255.255.254.0
gateway 10.16.20.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Lawine 
```
#A19
auto eth0
iface eth0 inet static
address 10.16.24.150
netmask 255.255.255.252
gateway 10.16.24.149
up echo nameserver 192.168.122.1 > /etc/resolv.conf


#A20
auto eth1
iface eth1 inet static
address 10.16.24.1
netmask 255.255.255.192
```

### Heiter 
```
#A20
auto eth0
iface eth0 inet static
address 10.16.24.2
netmask 255.255.255.192
gateway 10.16.24.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf


#A21
auto eth1
iface eth1 inet static
address 10.16.16.1
netmask 255.255.252.0
```

### Riegel Canyon
```
#A21
auto eth0
iface eth0 inet static
address 10.16.16.2
netmask 255.255.252.0
gateway 10.16.16.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf

```

### Sein
```
#A21
auto eth0
iface eth0 inet static
address 10.16.16.3
netmask 255.255.252.0
gateway 10.16.16.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Bredt Region
```
#A20
auto eth0
iface eth0 inet static
address 10.16.24.3
netmask 255.255.255.192
gateway 10.16.24.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Richter
```
#A12
auto eth0
iface eth0 inet static
address 10.16.24.106
netmask 255.255.255.248
gateway 10.16.24.105
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Revolte  
```
#A12
auto eth0
iface eth0 inet static
address 10.16.24.107
netmask 255.255.255.248
gateway 10.16.24.105
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Frieren
```
#A1
auto eth0				
iface eth0 inet static
address 10.16.24.114
netmask 255.255.255.252
gateway 10.16.24.113
up echo nameserver 192.168.122.1 > /etc/resolv.conf


#A3
auto eth1
iface eth1 inet static
address 10.16.24.117
netmask 255.255.255.252

#A2
auto eth2
iface eth2 inet static
address 10.16.26.65
netmask 255.255.255.224
```

### Lake Korridor
```
#A2
auto eth0
iface eth0 inet static
address 10.16.26.64
netmask 255.255.255.224
gateway 10.16.26.65
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Flamme
```
#A3
auto eth0
iface eth0 inet static
address 10.16.24.118
netmask 255.255.255.252
gateway 10.16.24.117
up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A7
auto eth1
iface eth1 inet static
address 10.16.24.125
netmask 255.255.255.252

#A6
auto eth2
iface eth2 inet static
address 10.16.8.1
netmask 255.255.252.0

#A4
auto eth3
iface eth3 inet static
address 10.16.24.121
netmask 255.255.255.252
```

### Fern
```
#A4
auto eth0
iface eth0 inet static
address 10.16.24.122
netmask 255.255.255.252
gateway 10.16.24.121
up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A5
auto eth1
iface eth1 inet static
address 10.16.0.1
netmask 255.255.248.0
```

### Laub Hills
```
#A5
auto eth0
iface eth0 inet static
address 10.16.0.2
netmask 255.255.248.0
gateway 10.16.0.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Appetit Region
```
#A5
auto eth0
iface eth0 inet static
address 10.16.0.3
netmask 255.255.248.0
gateway 10.16.0.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Rohr Road
```
#A6
auto eth0
iface eth0 inet static
address 10.16.8.2
netmask 255.255.252.0
gateway 10.16.8.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Himmel
```
#A7
auto eth0
iface eth0 inet static
address 10.16.12.2
netmask 255.255.255.252
gateway 10.16.12.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A8
auto eth1
iface eth1 inet static
address 10.16.24.97
netmask 255.255.255.248
```

### Schwer Mountain
```
#A8
auto eth0
iface eth0 inet static
address 10.16.24.98
netmask 255.255.255.248
gateway 10.16.24.97
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

## Routing
Routing dilakukan pada router-router yang ada. Rute yang ditambahkan adalah rute subnet yang melewati router tersebut namun tidak terhubung secara langsung. Oleh karena itulah router yang terletak pada ujung topologi tidak dilakukan routing.

### Aura
```sh
#A3
route add -net 10.16.24.116 netmask 255.255.255.252 gw 10.16.24.114
#A4
route add -net 10.16.24.120 netmask 255.255.255.252 gw 10.16.24.114
#A5
route add -net 10.16.0.0 netmask 255.255.248.0 gw 10.16.24.114
#A6
route add -net 10.16.8.0 netmask 255.255.252.0 gw 10.16.24.114
#A7
route add -net 10.16.24.124 netmask 255.255.255.252 gw 10.16.24.114
#A8
route add -net 10.16.24.96 netmask 255.255.255.248 gw 10.16.24.114
#A2
route add -net 10.16.26.64 netmask 255.255.255.224 gw 10.16.24.114

#A10
route add -net 10.16.22.0 netmask 255.255.255.0 gw 10.16.24.130

#A12
route add -net 10.16.24.104 netmask 255.255.255.248 gw 10.16.24.134
#A13
route add -net 10.16.24.136 netmask 255.255.255.252 gw 10.16.24.134
#A14
route add -net 10.16.24.140 netmask 255.255.255.252 gw 10.16.24.134
#A16
route add -net 10.16.12.0 netmask 255.255.252.0 gw 10.16.24.134
#A15
route add -net 10.16.23.0 netmask 255.255.255.0 gw 10.16.24.134
#A17
route add -net 10.16.24.144 netmask 255.255.255.252 gw 10.16.24.134
#A18
route add -net 10.16.20.0 netmask 255.255.254.0 gw 10.16.24.134
#A19
route add -net 10.16.24.148 netmask 255.255.255.252 gw 10.16.24.134
#A20
route add -net 10.16.24.0 netmask 255.255.255.192 gw 10.16.24.134
#A21
route add -net 10.16.16.0 netmask 255.255.252.0 gw 10.16.24.134
```

### Eisen
```sh
#A16
route add -net 10.16.12.0 netmask 255.255.252.0 gw 10.16.24.142
#A15
route add -net 10.16.23.0 netmask 255.255.255.0 gw 10.16.24.142

#A19
route add -net 10.16.24.148 netmask 255.255.255.252 gw 10.16.24.146
#A18
route add -net 10.16.20.0 netmask 255.255.254.0 gw 10.16.24.146
#A20
route add -net 10.16.24.0 netmask 255.255.255.192 gw 10.16.24.146
#A21
route add -net 10.16.16.0 netmask 255.255.252.0 gw 10.16.24.146
```

### Flamme
```sh
#A5
route add -net 10.16.0.0 netmask 255.255.248.0 gw 10.16.24.122
#A8
route add -net 10.16.24.96 netmask 255.255.255.248 gw 10.16.24.125
```

### Frieren
```sh
#A4
route add -net 10.16.24.120 netmask 255.255.255.252 gw 10.16.24.118
#A5
route add -net 10.16.0.0 netmask 255.255.248.0 gw gw 10.16.24.122
#A6
route add -net 10.16.8.0 netmask 255.255.252.0 gw 10.16.24.118
#A7
route add -net 10.16.24.124 netmask 255.255.255.252 gw 10.16.24.118
#A8
route add -net 10.16.24.96 netmask 255.255.255.248 gw 10.16.24.118
```

### Lawine
```sh
#A21
route add -net 10.16.16.0 netmask 255.255.252.0 gw 10.16.24.2
```

### Linie
```sh
#A20
route add -net 10.16.24.0 netmask 255.255.255.192 gw 10.16.24.150
#A21
route add -net 10.16.16.0 netmask 255.255.252.0 gw 10.16.24.150
```

# CIDR

## Penggabungan IP untuk menemukan netmask tertinggi:

<img width="873" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/2c899f22-38e1-425a-854b-c37f5b255fe8">


<img width="872" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/634a3d4d-32ce-4dbe-bede-47568555c73d">


<img width="869" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/5c12491e-c579-4214-afd7-20b3759e7886">


<img width="868" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/d617b5a1-d164-4925-85b6-8c521f83c574">


<img width="865" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/12a22d4d-882f-49c2-a522-ae2c75ab0fd4">


<img width="872" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/890454f8-4f68-430a-b305-12d0a9020496">


<img width="873" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/8cf353f3-49e9-4bbd-9a06-9e49be9c5b5b">


<img width="871" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/9d9ce88a-54ca-458d-9c90-13d72dbe1c79">


<img width="866" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/d5bf52e2-34d1-4536-952c-4e191e4ca617">


<img width="872" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/8f77a123-ecb3-4945-97da-5883d48d0728">


<img width="873" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/42a01146-a81e-44ed-8b29-c752829e05df">


Netmask paling rendah adalah /14

## Tree CIDR

<img width="614" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/f02ffbb3-65cc-4316-bc83-2f4210aaf3fe">


## Pembagian IP berdasarkan tree CIDR

<img width="542" alt="image" src="https://github.com/Osvaldo-Kurniawan/Jarkom-Modul-4-Susulan-2023/assets/108170210/f01cae07-1e65-4f9c-9c3c-8918dd430fd4">
