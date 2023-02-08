<h1 align="center"><strong>Tutorial Testnet Shardeum<strong></h1>

- [Website](https://shardeum.org/id/)
- [Discord](https://discord.gg/shardeum)
- [Faucet](https://faucet-sphinx.shardeum.org/)
- [Doc offcial](https://docs.shardeum.org/node/run/validator)

## Spesifikasi Minimum

| Komponen    | Requirements minimal                          |
| ----------- | --------------------------------------------- |
| sistem      | Ubuntu 18.04 atau lebih tinggi                |
| CPU         | 4 Cores / 8 Cores                             |
| RAM         | 4+ GB / 16 GB RAM                             |
| Penyimpanan | 250 GB SSD                                    |
| Koneksi     | 20 mbps / 50 mbps upload & bandwidth download |

<h2 align="center"><strong>Setup Wallet & Faucet</strong></h2>

- disarangkan gunakan wallet baru!
- buka website [Network Endpoints](https://docs.shardeum.org/network/endpoints#sphinx-1x)
- add RPC `Sphinx 1.X` langsung **klik to connect**
- Buka website [Faucet](https://faucet-sphinx.shardeum.org/) atau Faucet di [Discord](https://discord.gg/shardeum)
- lanjut step SETUP NODE

[![Shardeum.png](https://i.postimg.cc/ydxm4Rc6/Shardeum.png)](https://postimg.cc/G808vHX6)

<h2 align="center"><strong>Setup NODE</strong></h2>

### Install & Update

```
ufw allow ssh && ufw allow 8080 && ufw allow https && ufw allow http && ufw allow 443 && ufw enable
```

```
sudo apt update && sudo apt upgrade -y
```

```
sudo apt-get install curl
```

```
sudo apt install docker.io -y
```

```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

<h2 align="center"><strong>RUN NODE</strong></h2>

```
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```

## dibagian **# GET INFO FROM USER #**

- Do you want to run the web based Dashboard? (y/n): `y`
- Set the password to access the Dashboard: `Buat password ex:art123`
- Enter the port (1025-65536) to access the web based Dashboard (default 8080): `8080 atau lansung enter`
- What base directory should the node use (defaults to ~/.shardeum): `Langsung enter`
- Tunggu hingga selesai!

[![Shardeum.png](https://i.postimg.cc/qv4dTPxR/Shardeum.png)](https://postimg.cc/GH7fPSNw)

## Next open shell app NODE

```
$HOME/.shardeum/shell.sh
```

### Start Cli

```
operator-cli gui start
```

### Check status

```
pm2 list
```

[![Screenshot-2023-02-06-202600.png](https://i.postimg.cc/2SjmNpCw/Screenshot-2023-02-06-202600.png)](https://postimg.cc/PP701Rpp)

<h2 align="center"><strong> Start Validator & STAKE</strong></h2>

- Buka di browser `https://IP-VPS:8080`
- jika browser situs tidak aman, klik PROCEED TO THE SITE
- masukan Password yang di buat tadi
- ke bagia **Maintenance** & Klik **Start Node**

[![Shardeum.png](https://i.postimg.cc/RVYFdV7t/Shardeum.png)](https://postimg.cc/qz84MrZB)

### Start Validator

operator-cli start

### Check status

```
pm2 list
```

[![Screenshot-2023-02-06-203347.png](https://i.postimg.cc/23Nzp329/Screenshot-2023-02-06-203347.png)](https://postimg.cc/FkGt3Ft0)

- silahkan lanjutkan stake 10 SHM di dashboard validator
- Connect wallet
- Klik Add Stake & Klik Stake

[![Shardeum.png](https://i.postimg.cc/k414Hx6n/Shardeum.png)](https://postimg.cc/7GzwGJnc)

Stake Wallet Address [wallet connected]
Nominee Public Key [filled in automatically while validator is running]
Stake amount (SHM) [empty and is in units ether not wei]

<h2 align="center"><strong>Perintah-perintah Berguna</strong></h2>

### Start operator
```
operator-cli start
```
### Storp operator
```
operator-cli stop
```
### Check Status operator
```
operator-cli status
```
### Check list operator
```
pm2 list
```
### Delete operator
```
pm2 delete [id]
```
### Art-Team INFO

noted: **art team** here does not have any specific goals or intentions, they only collect data and share it with everyone.

untuk INFO Testnet lainya Silahkan join Discord 👇

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/ArtSy5team)
[![Discord](https://img.shields.io/badge/discord-7289d9?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/EAKEdZU6c8)
[![Github](https://img.shields.io/badge/GitHub-171515?style=for-the-badge&logo=GitHub&logoColor=white)](https://github.com/Art-Sy5team)
[![trakteer](https://img.shields.io/badge/trakteer.id-e31e1e?style=for-the-badge&logo=ko-fi&logoColor=white)](https://trakteer.id/Art-Sy5team/tip)
