<h2>Nexus Prover</h2>

![GZba1vvasAI6YjJ](https://github.com/user-attachments/assets/b0c5bd11-e9b3-4cea-8c88-024eac7fae80)

## VPS Specification
- Min Ram 4 GB
- Recommended RAM 6 GB
- Bisa pakai Contabo Cloud VPS 1
---

## Installation
- Kalian bisa pakai CMD berikut :
```bash
curl -sSL https://raw.githubusercontent.com/0xishaq/nexus/main/nexus.sh | bash
```
- maupun command berikut untuk menjalankan script :
```bash
wget -qO - https://raw.githubusercontent.com/0xishaq/nexus/main/nexus.sh | bash
```

## Status
Buat dulu screen sebelum check status `screen -S nexus`
- Untuk mencek Prover status kalian bisa pakai :
```bash
systemctl status nexus.service
```
- Untuk check logs, pakai command berikut :
```bash
journalctl -u nexus.service -f -n 50
```
- Jika logs di terminal kalian seperti ini berarti Nexus Prover kalian berjalan normal

![Screenshot 2024-10-09 115039](https://github.com/user-attachments/assets/3d3065d8-cb88-44ca-88b8-ac072bcf9eff)

Script ini hanya bisa kalian jalankan di OS ubuntu lokal maupun vps
- jika install di vps setelah instalasi kalian tidak perlu melakukan apapun.
- tetapi jika kalian install di lokal kalian harus membuka terminal terus menerus ketika terminal di tutup kalian harus menjalankan ulang script berikut :
```bash
sudo systemctl start nexus.service
```

## Link Prover ID dengan Email
Kalian harus connect email dengan prover id kalian yang ada di web supaya data cycle kalian tersimpan caranya :
- Masuk ke https://beta.nexus.xyz/
- Kemudian klik ikon orang di pojok kiri bawah
- Masukan Email kemudian verif
- Jika sudah cek apakah sudah centang hijau di samping email
- Done

## Cara run 1 prover-d di berbagai vps
Jika kalian ingin gunakan 1 prover-id di web dengan yang di vps supaya sama dengan yang di website caranya :
- Masuk ke https://beta.nexus.xyz/
- Kemudian inspect element `ctrl`+`shift`+`i` kalau di chrome
- Masuk ke tab Application
- Selanjutnya masuk ke 'local storage' cari https://beta.nexus.xyz/
- kemudian copy prover-id kalian simpan didalam note untuk jaga-jaga
![Screenshot 2024-12-11 194601](https://github.com/user-attachments/assets/afe91f5a-59ce-4b61-b280-7c33a64dbf47)
- Selanjutnya ubah prover-id yang ada di vps dengan prover-id yang barusan di copy
```bash
cd .nexus
nano prover-id
```
jika sudah save `ctrl`+`x`+`y`+`enter` kemudian Restart nexus.service
```bash
sudo systemctl restart nexus.service
```

