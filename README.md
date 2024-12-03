- **Nama**: Aryasatya Alaauddin
- **NRP**: 5027231082

# Network Layer dan Konsep Terkait

## 1. **Network Layer**
Lapisan ketiga pada model OSI bertanggung jawab untuk:
- **Routing**: Menentukan jalur terbaik untuk pengiriman paket data.
- **Forwarding**: Mengirimkan paket ke jaringan yang sesuai.
- **Fragmentasi & Reassembly**: Memecah paket besar menjadi bagian kecil agar sesuai dengan MTU.
- **Pengalamatan Logis**: Menggunakan alamat IP untuk identifikasi perangkat.

---

## 2. **Protokol Penting**
- **IPv4 & IPv6**: Format pengalamatan dengan 32-bit (IPv4) atau 128-bit (IPv6).
- **ARP**: Menghubungkan alamat IP dengan MAC Address.
- **ICMP**: Protokol untuk diagnosa jaringan (contoh: `ping`).
- **OSPF**: Protokol routing berbasis link-state.

---

## 3. **Routing**
### **Algoritma Routing**
- **Distance Vector**: Menggunakan tabel jarak antar node (contoh: RIP).
- **Link State**: Router membangun peta topologi jaringan (contoh: OSPF).

### **Jenis Routing**
- **Static Routing**: Jalur tetap, manual. Stabil tapi tidak fleksibel.
- **Dynamic Routing**: Jalur adaptif berdasarkan perubahan jaringan. Lebih kompleks.

### **Protokol Routing**
- **RIP**: Menggunakan hop count. Sederhana, cocok untuk jaringan kecil.
- **OSPF**: Optimal untuk jaringan besar, berbasis link-state.
- **BGP**: Digunakan untuk routing antar jaringan besar di internet.

---

## 4. **NAT (Network Address Translation)**
### **Jenis NAT**
1. **Static NAT**: Satu IP privat dipetakan ke satu IP publik.
2. **Dynamic NAT**: IP publik dialokasikan dari pool secara dinamis.
3. **PAT (Port Address Translation)**: Banyak perangkat menggunakan satu IP publik dengan nomor port berbeda.

### **Keuntungan NAT**
- Privasi: Menyembunyikan alamat IP internal.
- Keamanan: Mengurangi paparan perangkat internal ke internet.
- Efisiensi: Menghemat penggunaan alamat IP publik.

---

## 5. **IP Addressing**
### **IPv4**
- Format 32-bit, terdiri dari 4 oktet (contoh: `192.168.1.1`).
- **Network ID**: Mengidentifikasi jaringan.
- **Host ID**: Mengidentifikasi perangkat di jaringan.

### **IPv6**
- Format 128-bit, mendukung ruang alamat lebih besar.

### **Subnetting**
Teknik membagi jaringan besar menjadi subnet kecil untuk efisiensi IP dan kemudahan pengelolaan.

#### **Jenis Subnetting**
1. **Classful Subnetting**: Berdasarkan kelas IP tradisional (A, B, C). Sederhana tapi kurang fleksibel.
2. **Classless Subnetting (CIDR)**: Tidak terikat kelas, lebih efisien.
3. **VLSM (Variable Length Subnet Mask)**: Mengoptimalkan alokasi IP untuk kebutuhan jaringan.

---

## 6. **Subnetting - Contoh**
Blok IP: `192.168.1.0/24`
### Pembagian:
- **Subnet 1**: `192.168.1.0/26` (62 host)
- **Subnet 2**: `192.168.1.64/27` (30 host)
- **Subnet 3**: `192.168.1.96/28` (14 host)

---

## 7. **ICMP (Internet Control Message Protocol)**
Protokol untuk komunikasi pesan kesalahan dan diagnosa jaringan:
- **Echo Request/Reply**: Tes konektivitas (contoh: `ping`).
- **Destination Unreachable**: Paket tidak dapat mencapai tujuan.
- **Time Exceeded**: Waktu hidup paket (TTL) habis.

---

## 8. **Tips Implementasi Subnetting**
- Prioritaskan subnet terbesar.
- Pantau tabel routing secara berkala.
- Gunakan CIDR atau VLSM untuk efisiensi.
