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
