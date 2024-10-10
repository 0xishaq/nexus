<h2>Nexus Prover</h2>

## VPS Specification
- Min Ram 4 GB
- Recommended RAM 6 GB
- Bisa pakai Contabo Cloud VPS 1
---

Script ini hanya bisa kalian jalankan di OS ubuntu lokal maupun vps
- jika install di vps setelah instalasi kalian tidak perlu melakukan apapun.
- tetapi jika kalian install di lokal kalian harus membuka terminal terus menerus ketika terminal di tutup kalian harus menjalankan ulang script berikut :
```bash
sudo systemctl start nexus.service
```

## Installation
- Kalian bisa pakai CMD berikut :
```bash
curl -sSL https://raw.githubusercontent.com/0xishaq/nexus-prover/main/nexus.sh | bash
```
- maupun command berikut untuk menjalankan script :
```bash
wget -qO - https://raw.githubusercontent.com/0xishaq/nexus-prover/main/nexus.sh | bash
```

## Status
- Untuk mencek Prover statur kalian bisa pakai :
```bash
systemctl status nexus.service
```
- Untuk check logs, pakai command berikut :
```bash
journalctl -u nexus.service -f -n 50
```
- You will see something like this, it means, it is fine

![Screenshot 2024-10-09 115039](https://github.com/user-attachments/assets/3d3065d8-cb88-44ca-88b8-ac072bcf9eff)
