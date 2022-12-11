# JARKOM-A01-SHIFT-4-2022
### Kelompok A01

| **No** | **Nama**              | **NRP**    |
| ------ | --------------------- | ---------- |
| 1      | Okyan Awang Ramadhana | 5025201252 |
| 2      | M Dzikri Fakhrizal    | 5025201201 |
| 3      | Fachrendy Zulfikar A  | 5025201018 |

### Soal
- Soal shift dikerjakan pada Cisco Packet Tracer dan GNS3 menggunakan metode
perhitungan CLASSLESS yang berbeda.
- Keterangan: Bila di CPT menggunakan VLSM, maka di GNS3 menggunakan CIDR
atau Sebaliknya
- Jika tidak ada pemberitahuan revisi soal dari asisten, berarti semua soal BERSIFAT BENAR
dan DAPAT DIKERJAKAN.
- Untuk di GNS3 CLOUD merupakan NAT1 jangan sampai salah agar bisa terkoneksi
internet.
- Pembagian IP menggunakan Prefix IP yang telah ditentukan pada modul pengenalan
- Pembagian IP dan routing harus SE-EFISIEN MUNGKIN.

### List

1. [VLSM](#VLSM)
2. [CIDR](#CIDR)

## VLSM

### Topologi
Buat topologi jaringan yang sesuai yaitu dengan mengatur IP Address pada setiap interface yang ada.
<img width="667" alt="Screenshot_20221126_015456" src="https://user-images.githubusercontent.com/81427127/204076456-ece05689-f9cd-4641-9525-08db09af198a.png">

### Plotting Subnetting
Kemudian buat plotting subnettingnya,
![Frame 2](https://user-images.githubusercontent.com/81427127/204076497-c1447a0e-622d-4f5a-a2a8-5b3445005841.png)

![IP](https://user-images.githubusercontent.com/81427127/204076523-f1e05ad9-1f8e-4196-9e29-1a7bf2fd1618.png)

### Tree
Setelah dilakukan pembagian subnetting, lakukan pembagian IP Address menggunakan tree pada setiap interface yang ada.
![Tabloid - 2](https://user-images.githubusercontent.com/81427127/204076578-737821ac-b2eb-45f2-b217-1a34fafbf4c2.png)

Gunakan prefix IP ```192.169.X.X```, dimulai dari 192.169.0.0/20 kemudian bagi menjadi dua bagian, lakukan cara yang sama sampai 192.169.x.x/30.

### VLSM-IP
![VLSM_IP](https://user-images.githubusercontent.com/81427127/204076679-f7d72c05-106a-42d4-8cb0-8fe97ea69a38.png)

![CPT](https://user-images.githubusercontent.com/81427127/204076756-a5d24b48-5952-4747-ad14-bbeb5c506977.png)

### Testing
Testing dari Client ke Client

<img width="423" alt="Screenshot_20221126_021008" src="https://user-images.githubusercontent.com/90445721/204094370-582ac19e-a596-4fd2-a0eb-f3fcbdc37be1.jpg">

Testing dari Router ke Router

<img width="422" alt="router - router" src="https://user-images.githubusercontent.com/90445721/204094396-f7076004-7755-45a5-8cfd-12b3e4efb6b9.png">

Testing dari Client ke Router Terdekat

<img width="422" alt="router - router" src="https://user-images.githubusercontent.com/90445721/204094663-ec8e922b-892d-426f-95ba-8c7d17648333.png">

Testing dari Client ke Server

<img width="423" alt="Screenshot_20221126_021008" src="https://user-images.githubusercontent.com/90445721/204094436-e9955470-8e03-49bd-b949-11c698cf99a2.jpg">

Testing dari Server ke Server

<img width="423" alt="Screenshot_20221126_021008" src="https://user-images.githubusercontent.com/90445721/204094454-62f7d7b0-9777-48f7-82aa-eca248e3b0b3.jpg">

## CIDR

### Topologi

![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/topologi.PNG)

### Topologi-subnet

![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/topologi-subnet.PNG)

### Langkah

#### Step-1

![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/Step/step-1.PNG)

#### Step-2
![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/Step/step-2.PNG)

#### Step-3
![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/Step/step-3.PNG)

#### Step-4
![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/Step/step-4.PNG)

#### Step-5
![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/Step/Step-5.jpg)

#### Step-6
![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/Step/Step-6.jpg)

#### Step-7
![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/Step/Step-7.jpg)

#### Step-8
![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/Step/Step-8.jpg)

#### Step-9
![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/Step/Step-9.jpg)

#### Step-10
![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/Step/Step-10.jpg)

### CIDR

![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/CIDR.PNG)

### Tree

![image](https://raw.githubusercontent.com/Chroax/Jarkom-Modul-4-B11-2022/main/image/CIDR/tree.png)

### Konfigurasi Node

- **ThePerformance**
    ```
    auto lo
    iface lo inet loopback

    auto eth0
    iface eth0 inet dhcp

    auto eth1
    iface eth1 inet static
    address 192.169.68.1
    netmask 255.255.255.252

    auto eth2
    iface eth2 inet static
    address 192.169.66.1
    netmask 255.255.255.252

    auto eth3
    iface eth3 inet static
    address 192.169.32.1
    netmask 255.255.255.252

    auto eth4
    iface eth4 inet static
    address 192.169.160.1
    netmask 255.255.255.252
    ```

- **TheMagical**
    ```
    auto lo
    iface lo inet loopback

    auto eth0
    iface eth0 inet static
    address 192.169.66.2
    netmask 255.255.255.252
    gateway 192.169.66.1

    auto eth1
    iface eth1 inet static
    address 192.169.64.1
    netmask 255.255.254.0
    ```

- **TheOrder**
    ```
    auto lo
    iface lo inet loopback

    auto eth0
    iface eth0 inet static
    address 192.169.160.2
    netmask 255.255.255.252
    gateway 192.169.160.1

    auto eth1
    iface eth1 inet static
    address 192.169.136.1
    netmask 255.255.255.252

    auto eth2
    iface eth2 inet static
    address 192.169.144.1
    netmask 255.255.255.192
    ```

- **TheMinister**
    ```
    auto lo
    iface lo inet loopback

    auto eth0
    iface eth0 inet static
    address 192.169.136.2
    netmask 255.255.255.252
    gateway 192.169.136.1

    auto eth1
    iface eth1 inet static
    address 192.169.133.1
    netmask 255.255.255.252

    auto eth2
    iface eth2 inet static
    address 192.169.128.1
    netmask 255.255.252.0
    ```

- **TheDauntless**
    ```
    auto lo
    iface lo inet loopback

    auto eth0
    iface eth0 inet static
    address 192.169.133.2
    netmask 255.255.255.252
    gateway 192.169.133.1

    auto eth1
    iface eth1 inet static
    address 192.169.132.1
    netmask 255.255.255.0
    ```

- **TheInstrument**
    ```
    auto lo
    iface lo inet loopback

    auto eth0
    iface eth0 inet static
    address 192.169.32.2
    netmask 255.255.255.252
    gateway 192.169.32.1

    auto eth1
    iface eth1 inet static
    address 192.169.17.1
    netmask 255.255.255.252

    auto eth2
    iface eth2 inet static
    address 192.169.4.1
    netmask 255.255.255.252

    auto eth3
    iface eth3 inet static
    address 192.169.8.1
    netmask 255.255.255.128
    ```

- **TheFireFist**
    ```
    auto lo
    iface lo inet loopback

    auto eth0
    iface eth0 inet static
    address 192.169.4.2
    netmask 255.255.255.252
    gateway 192.169.4.1

    auto eth1
    iface eth1 inet static
    address 192.169.2.1
    netmask 255.255.254.0

    auto eth2
    iface eth2 inet static
    address 192.169.0.1
    netmask 255.255.255.0
    ```

- **TheProfound**
    ```
    auto lo
    iface lo inet loopback

    auto eth0
    iface eth0 inet static
    address 192.169.17.2
    netmask 255.255.255.252
    gateway 192.169.17.1

    auto eth1
    iface eth1 inet static
    address 192.169.16.1
    netmask 255.255.255.128

    auto eth2
    iface eth2 inet static
    address 192.169.16.129
    netmask 255.255.255.128
    ```

- **TheQueen**
    ```
    auto lo
    iface lo inet loopback

    auto eth0
    iface eth0 inet static
    address 192.169.0.2
    netmask 255.255.255.0
    gateway 192.169.0.1

    auto eth1
    iface eth1 inet static
    address 192.169.1.1
    netmask 255.255.255.252
    ```

- **Haines**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.64.2
    netmask 255.255.254.0
    gateway 192.169.64.1
    ```

- **Corveks**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.64.3
    netmask 255.255.254.0
    gateway 192.169.64.1
    ```

- **TheBeast**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.68.2
    netmask 255.255.255.252
    gateway 192.169.68.1
    ```

- **Ashaf**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.144.2
    netmask 255.255.255.192
    gateway 192.169.144.1
    ```

- **Guidessau**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.128.2
    netmask 255.255.252.0
    gateway 192.169.128.1
    ```

- **Johan**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.132.3
    netmask 255.255.255.0
    gateway 192.169.132.1
    ```

- **Phanora**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.132.2
    netmask 255.255.255.0
    gateway 192.169.132.1
    ```

- **MattCugat**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.8.2
    netmask 255.255.255.128
    gateway 192.169.8.1
    ```

- **Helga**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.16.130
    netmask 255.255.255.128
    gateway 192.169.16.129
    ```

- **Spendrow**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.16.2
    netmask 255.255.255.128
    gateway 192.169.16.1
    ```

- **Oakleave**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.2.2
    netmask 255.255.254.0
    gateway 192.169.2.1
    ```

- **Keith**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.0.3
    netmask 255.255.255.0
    gateway 192.169.0.1
    ```

- **TheWitch**
    ```
    auto eth0
    iface eth0 inet static
    address 192.169.1.2
    netmask 255.255.255.252
    gateway 192.169.1.1
    ```
### Konfigurasi Routing

- **ThePerformance**
    ```
    route add -net 192.169.144.0 netmask 255.255.255.192 gw 192.169.160.2
    route add -net 192.169.136.0 netmask 255.255.255.252 gw 192.169.160.2
    route add -net 192.169.128.0 netmask 255.255.252.0 gw 192.169.160.2
    route add -net 192.169.133.0 netmask 255.255.255.252 gw 192.169.160.2
    route add -net 192.169.132.0 netmask 255.255.255.0 gw 192.169.160.2

    route add -net 192.169.64.0 netmask 255.255.254.0 gw 192.169.66.2

    route add -net 192.169.8.0 netmask 255.255.255.128 gw 192.169.32.2
    route add -net 192.169.17.0 netmask 255.255.255.252 gw 192.169.32.2
    route add -net 192.169.16.0 netmask 255.255.255.128 gw 192.169.32.2
    route add -net 192.169.16.128 netmask 255.255.255.128 gw 192.169.32.2
    route add -net 192.169.4.0 netmask 255.255.255.252 gw 192.169.32.2
    route add -net 192.169.2.0 netmask 255.255.254.0 gw 192.169.32.2
    route add -net 192.169.0.0 netmask 255.255.255.0 gw 192.169.32.2
    route add -net 192.169.1.0 netmask 255.255.255.252 gw 192.169.32.2

    iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.169.0.0/16
    ```

- **TheMagical**
    ```
    route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.169.66.1
    ```

- **TheOrder**
    ```
    route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.169.160.1

    route add -net 192.169.128.0 netmask 255.255.252.0 gw 192.169.136.2
    route add -net 192.169.133.0 netmask 255.255.255.252 gw 192.169.136.2
    route add -net 192.169.132.0 netmask 255.255.255.0 gw 192.169.136.2
    ```

- **TheMinister**
    ```
    route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.169.136.1

    route add -net 192.169.132.0 netmask 255.255.255.0 gw 192.169.133.2
    ```

- **TheDauntless**
    ```
    route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.169.133.1
    ```

- **TheInstrument**
    ```
    route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.169.32.1

    route add -net 192.169.16.0 netmask 255.255.255.128 gw 192.169.17.2
    route add -net 192.169.16.128 netmask 255.255.255.128 gw 192.169.17.2

    route add -net 192.169.2.0 netmask 255.255.254.0 gw 192.169.4.2
    route add -net 192.169.0.0 netmask 255.255.255.0 gw 192.169.4.2
    route add -net 192.169.1.0 netmask 255.255.255.252 gw 192.169.4.2
    ```

- **TheFireFist**
    ```
    route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.169.4.1

    route add -net 192.169.1.0 netmask 255.255.255.252 gw 192.169.0.2
    ```

- **TheProfound**
    ```
    route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.169.17.1
    ```

- **TheQueen**
    ```
    route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.169.0.1
    ```

- **All Except ThePerformance**
    ```
    echo nameserver 192.168.122.1 > /etc/resolv.conf
    ```

## Kendala
- Ketika sedang testing di CPT sering kali failed
