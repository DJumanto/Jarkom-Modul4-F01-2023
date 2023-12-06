# Laporan Praktikum Modul 4 Jaringan Komputer

| Kelompok | Nama | NRP |
|----------|------|-----|
| F01      |Alfa Fakhrur Rizal Zaini|5025211214|


# Topologi
![Topologi](/img/topologi.png)
- Pengerjaan CIDR menggunakan Cisco Packet Tracer
- Pengerjaan VLSM menggunakan GNS3 Virtual Machine

# CIDR
Pembagian IP dari metode CIDR dapat dilihat melalui gambar berikut:

## Subnetting
### Pembagian IP
![Pembagian IP](/img/pembagianIP.png)
### Tree
![Tree CIDR](/img/TreeCIDR.png)
### Klasifikasi
![Klasifikasi](/img/klasifikasiCIRD.png)
### Penggabungan IP
![Penggabungan 1](/img/penggabungan.png)
![Penggabungan 2](/img/penggabungan-1.png)
![Penggabungan 3](/img/penggabungan-2.png)

## Routing
### How to
Proses routing dapat dilakukan dengan mengkonfigurasi :

router - bagian Routing
Server dan Client - bagian Desktop -> IP Configuration.
Sebagai contoh untuk Routing IP router Frieren ke Client Lake Korridor

#### LakeKorridor
![LakeKorridor IP](/img/LakeKorridor.png)

Maka dari itu, kita perlu setting frieren untuk mendengarkan dari aura dan setting aura untuk melakukan nexthop ke frieren ketika ingin mengakses LakeKorridor atau client yang se-subnet dengan melakukan routing ke network id milik LakeKorridor

### Aura
![Aura IP](/img/Aura.png)
### Frieren
![Frieren IP](/img/Frieren.png)

Settingan tersebut dijalankan pada semua router agar client dapat diakses oleh router / client luar

# VLSM

Berikut merupakan kalkulasi IP range untuk tiap subnet yang didapatkan dari hasil tree:

| Subnet Name | Route                                     | Hosts Needed | Network Address | Slash | Mask              | IP Range                         | Broadcast         |
|-------------|-------------------------------------------|--------------|------------------|-------|-------------------|----------------------------------|-------------------|
| A1          | Fern-Switch4-AppetitRegion-Switch4-LaubHills | 1023         | 10.52.0.0        | /21   | 255.255.248.0     | 10.52.0.1 - 10.52.7.254          | 10.52.7.255       |
| A2          | Flamme                                    | 2            | 10.52.24.112     | /30   | 255.255.255.252   | 10.52.24.113 - 10.52.24.114      | 10.52.24.115      |
| A3          | Flamme-Switch5-RohrRoad                    | 1001         | 10.52.8.0        | /22   | 255.255.252.0     | 10.52.8.1 - 10.52.11.254         | 10.52.11.255      |
| A4          | Flamme-Himmel                              | 2            | 10.52.24.116     | /30   | 255.255.255.252   | 10.52.24.117 - 10.52.24.118      | 10.52.24.119      |
| A5          | Flamme-Frieren                             | 2            | 10.52.24.120     | /30   | 255.255.255.252   | 10.52.24.121 - 10.52.24.122      | 10.52.24.123      |
| A6          | Himmel-Switch6-SchwerMountains             | 6            | 10.52.24.96      | /29   | 255.255.255.248   | 10.52.24.97 - 10.52.24.102       | 10.52.24.103      |
| A7          | Fieren-Aura                                | 2            | 10.52.24.124     | /30   | 255.255.255.252   | 10.52.24.125 - 10.52.24.126      | 10.52.24.127      |
| A8          | Aura-Eisen                                 | 2            | 10.52.24.128     | /30   | 255.255.255.252   | 10.52.24.129 - 10.52.24.130      | 10.52.24.131      |
| A9          | Aura-Denken                                | 2            | 10.52.24.132     | /30   | 255.255.255.252   | 10.52.24.133 - 10.52.24.134      | 10.52.24.135      |
| A10         | Eisen-Switch1-Rictcher-Switch1-Revolte      | 3            | 10.52.24.104     | /29   | 255.255.255.248   | 10.52.24.105 - 10.52.24.110      | 10.52.24.111      |
| A11         | Eisen-Lugner                               | 2            | 10.52.24.136     | /30   | 255.255.255.252   | 10.52.24.137 - 10.52.24.138      | 10.52.24.139      |
| A12         | Eisen-Linie                                | 2            | 10.52.24.140     | /30   | 255.255.255.252   | 10.52.24.141 - 10.52.24.142      | 10.52.24.143      |
| A13         | Eisen-Switch0-Stark                        | 2            | 10.52.24.144     | /30   | 255.255.255.252   | 10.52.24.145 - 10.52.24.146      | 10.52.24.147      |
| A14         | Linie-Lawine                               | 2            | 10.52.24.148     | /30   | 255.255.255.252   | 10.52.24.149 - 10.52.24.150      | 10.52.24.151      |
| A15         | Linie-Switch11-GranzChannel                | 255          | 10.52.20.0       | /23   | 255.255.254.0     | 10.52.20.1 - 10.52.21.254        | 10.52.21.255      |
| A16         | Lawine-Switch7-BredtRegion-Switch7-Heiter | 31           | 10.52.24.0       | /26   | 255.255.255.192   | 10.52.24.1 - 10.52.24.62         | 10.52.24.63       |
| A17         | Heiter-Switch8-RiegelCanyon-Switch8-Sein  | 512          | 10.52.16.0       | /22   | 255.255.252.0     | 10.52.16.1 - 10.52.19.254        | 10.52.19.255      |
| A18         | Denken-Switch2-WilleRegion-Switch2-RoyalCapital | 127      | 10.52.23.0       | /24   | 255.255.255.0     | 10.52.23.1 - 10.52.23.254        | 10.52.23.255      |
| A19         | Lugner-Switch10-TurkRegion                 | 1001         | 10.52.12.0       | /22   | 255.255.252.0     | 10.52.12.1 - 10.52.15.254        | 10.52.15.255      |
| A20         | Lugner-Switch9-GrobeForest                 | 251          | 10.52.22.0       | /24   | 255.255.255.0     | 10.52.22.1 - 10.52.22.254        | 10.52.22.255      |
| A21         | Frieren-Switch3-LakeKorridor               | 25           | 10.52.24.64      | /27   | 255.255.255.224   | 10.52.24.65 - 10.52.24.94 | 10.52.24.95

Untuk hasil yang lebih jelas bisa dilihat di link berikut: [Link Pembagian IP](https://docs.google.com/spreadsheets/d/1hKPOa9vIqyH7hGPm7Qu1_Xl4GXmpv-j-4dbjJ8qOlTQ/edit#gid=671499381)

Berikut merupakan script yang digunakan untuk melakukan routing:

- Aura
```sh
auto eth1
iface eth1 inet static
	address 10.52.24.133
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.52.24.125
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.52.24.129
	netmask 255.255.255.252

#Denken
up route add -net 10.52.22.0 netmask 255.255.255.0 gw 10.52.24.134

#Fieren
up route add -net 10.52.24.112 netmask 255.255.255.252 gw 10.52.24.126
up route add -net 10.52.24.116 netmask 255.255.255.252 gw 10.52.24.126
up route add -net 10.52.8.0 netmask 255.255.252.0 gw 10.52.24.126
up route add -net 10.52.24.96 netmask 255.255.255.248 gw 10.52.24.126
up route add -net 10.52.0.0 netmask 255.255.248.0 gw 10.52.24.126
up route add -net 10.52.24.120 netmask 255.255.255.252 gw 10.52.24.126

#Eisen
up route add -net 10.52.24.144 netmask 255.255.255.252 gw 10.52.24.130
up route add -net 10.52.24.104 netmask 255.255.255.248 gw 10.52.24.130
up route add -net 10.52.24.136 netmask 255.255.255.252 gw 10.52.24.130
up route add -net 10.52.24.140 netmask 255.255.255.252 gw 10.52.24.130
up route add -net 10.52.16.0 netmask 255.255.252.0 gw 10.52.24.130
up route add -net 10.52.23.0 netmask 255.255.255.0 gw 10.52.24.130
up route add -net 10.52.20.0 netmask 255.255.254.0 gw 10.52.24.130
up route add -net 10.52.24.148 netmask 255.255.255.252 gw 10.52.24.130
up route add -net 10.52.24.0 netmask 255.255.255.192 gw 10.52.24.130
up route add -net 10.52.12.0 netmask 255.255.252.0 gw 10.52.24.130
```

- Frieren
```sh
auto eth0
iface eth0 inet static
	address 10.52.24.126
	netmask 255.255.255.252
	gateway 10.52.24.125

auto eth1
iface eth1 inet static
	address 10.52.24.66
	netmask 255.255.255.224
#	gateway 192.168.1.1

Static config for eth2
auto eth2
iface eth2 inet static
	address 10.52.24.122
	netmask 255.255.255.252
#	gateway 192.168.2.1
#	up echo nameserver 192.168.2.1 > /etc/resolv.conf

up route add -net 10.52.24.112 netmask 255.255.255.252 gw 10.52.24.121
up route add -net 10.52.24.116 netmask 255.255.255.252 gw 10.52.24.121
up route add -net 10.52.8.0 netmask 255.255.252.0 gw 10.52.24.121
up route add -net 10.52.24.96 netmask 255.255.255.248 gw 10.52.24.121
up route add -net 10.52.0.0 netmask 255.255.248.0 gw 10.52.24.121
```
- Denken
```sh
auto eth0
iface eth0 inet static
	address 10.52.24.134
	netmask 255.255.255.252
	gateway 10.52.24.133
#	up echo nameserver 192.168.0.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 10.52.22.1
        netmask 255.255.255.0
#	gateway 192.168.1.1
#	up echo nameserver 192.168.1.1 > /etc/resolv.conf
```

- Himmel
```sh
auto eth0
iface eth0 inet static
	address 10.52.24.118
	netmask 255.255.255.252
	gateway 10.52.24.117
#	up echo nameserver 192.168.0.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 10.52.24.97
	netmask 255.255.255.248
#	gateway 192.168.1.1
#	up echo nameserver 192.168.1.1 > /etc/resolv.conf
```

- Flamme
```sh
auto eth0
iface eth0 inet static
	address 10.52.24.121
	netmask 255.255.255.252
	gateway 10.52.24.122

auto eth1
iface eth1 inet static
	address 10.52.24.114
	netmask 255.255.255.252
#	gateway 192.168.1.1

auto eth2
iface eth2 inet static
	address 10.52.8.1
	netmask 255.255.252.0
#	gateway 192.168.2.1

auto eth3
iface eth3 inet static
	address 10.52.24.117
	netmask 255.255.255.252
#	gateway 192.168.3.1

up route add -net 10.52.0.0 netmask 255.255.248.0 gw 10.52.24.113
up route add -net 10.52.24.96 netmask 255.255.255.248 gw 10.52.24.118
```

- Eisen
```sh
auto eth0
iface eth0 inet static
	address 10.52.24.130
	netmask 255.255.255.252
	gateway 10.52.24.129

auto eth1
iface eth1 inet static
	address 10.52.24.105
	netmask 255.255.255.248

auto eth2
iface eth2 inet static
	address 10.52.24.137
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.52.24.145
	netmask 255.255.255.252

auto eth4
iface eth4 inet static
	address 10.52.24.141
	netmask 255.255.255.252

#Eisen-TurkRegion
up route add -net 10.52.16.0 netmask 255.255.252.0 gw 10.52.24.138

#Eisen-GrobeForest
up route add -net 10.52.23.0 netmask 255.255.255.0 gw 10.52.24.138

#LinieGranzChannel
up route add -net 10.52.20.0 netmask 255.255.254.0 gw 10.52.24.142

#LinieLawine
up route add -net 10.52.24.148 netmask 255.255.255.252 gw 10.52.24.142

#LawineBredtRegion
up route add -net 10.52.24.0 netmask 255.255.255.192 gw 10.52.24.142

#HeiterSeinRiegel
up route add -net 10.52.12.0 netmask 255.255.252.0 gw 10.52.24.142
```

- Lugner
```sh
auto eth0
iface eth0 inet static
	address 10.52.24.138
	netmask 255.255.255.252
	gateway 10.52.24.137

auto eth1
iface eth1 inet static
	address 10.52.16.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 10.52.23.1
	netmask 255.255.255.0
```

- Linie
```sh
auto eth0
iface eth0 inet static
	address 10.52.24.142
	netmask 255.255.255.252
	gateway 10.52.24.141

auto eth1
iface eth1 inet static
	address 10.52.24.149
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.52.20.1
	netmask 255.255.254.0

up route add -net 10.52.12.0 netmask 255.255.252.0 gw 10.52.24.150
up route add -net 10.52.24.0 netmask 255.255.255.192 gw 10.52.24.150
```

- Heiter
```sh
auto eth0
iface eth0 inet static
	address 10.52.24.2
	netmask 255.255.255.192
	gateway 10.52.24.1

auto eth1
iface eth1 inet static
	address 10.52.12.1
	netmask 255.255.252.0
```

- Lawine
```sh
auto eth0
iface eth0 inet static
	address 10.52.24.138
	netmask 255.255.255.252
	gateway 10.52.24.137

auto eth1
iface eth1 inet static
	address 10.52.16.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 10.52.23.1
	netmask 255.255.255.0
```

- Fern
```sh
auto eth0
iface eth0 inet static
	address 10.52.24.113
	netmask 255.255.255.252
	gateway 10.52.24.114
#	up echo nameserver 192.168.0.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 10.52.0.1
	netmask 255.255.248.0
#	gateway 192.168.1.1
#	up echo nameserver 192.168.1.1 > /etc/resolv.conf
```

Contoh Hasil pengujian ping dari   ``TurkRegion`` ke ``SchwerMountain``:

![Test Result VLSM](/img/testresult.png)

Sekian Laporan Resmi dari Kami

![Animated Gif](https://media.tenor.com/mdOPy_Efn9cAAAAC/spongebob-bye-bye.gif)