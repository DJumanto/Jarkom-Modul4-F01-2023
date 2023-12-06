# Laporan Praktikum Modul 4 Jaringan Komputer

| Kelompok | Nama | NRP |
|----------|------|-----|
| F01      |Alfa Fakhrur Rizal Zaini|5025211214|


# Topologi
![Topologi](topologi.png)
- Pengerjaan CIDR menggunakan Cisco Packet Tracer
- Pengerjaan VLSM menggunakan GNS3 Virtual Machine

# CIDR
Pembagian IP dari metode CIDR dapat dilihat melalui gambar berikut:

## Subnetting
### Pembagian IP
![Pembagian IP](pembagianIP.png)
### Tree
![Tree CIDR](TreeCIDR.png)
### Klasifikasi
![Klasifikasi](klasifikasiCIRD.png)
### Penggabungan IP
![Penggabungan 1](penggabungan.png)
![Penggabungan 2](penggabungan-1.png)
![Penggabungan 3](penggabungan-2.png)

## Routing
### How to
Proses routing dapat dilakukan dengan mengkonfigurasi :

router - bagian Routing
Server dan Client - bagian Desktop -> IP Configuration.
Sebagai contoh untuk Routing IP router Frieren ke Client Lake Korridor

#### LakeKorridor
![LakeKorridor IP](LakeKorridor.png)

Maka dari itu, kita perlu setting frieren untuk mendengarkan dari aura dan setting aura untuk melakukan nexthop ke frieren ketika ingin mengakses LakeKorridor atau client yang se-subnet dengan melakukan routing ke network id milik LakeKorridor

### Aura
![Aura IP](Aura.png)
### Frieren
![Frieren IP](Frieren.png)

Settingan tersebut dijalankan pada semua router agar client dapat diakses oleh router / client luar
