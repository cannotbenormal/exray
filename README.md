BISA SEMUA YANG DIBAWAH

TERNYATA, SETELAH INSTALL, HARUS BISA JALANIN NO.9, INSTALL CERTIFICATE NYA 
WAJIB JALAN NO.9 CARI SOLUSI DULU








- ===== STEP ====
- 0.Wajib Pointing sub/domain Cloudflare ke ip vps
- 0.1 VPS Wajib Open All Port
- 1.WAJIB D. MONKEY 9-10 (Azure Tested D-10 Buster Gen.2 1 vcpu 1 GB Ram 9.93/month(free service eligible))
- 2.sudo su
- 3.passwd root
- 4.isipw
- 5.nano /etc/ssh/sshd_config
- 6.Ubah PermitRootLogin jadi -> PermitRootLogin yes (WAJIB BIAR BISA LOGIN MAKE ROOT)
- 7.UPDATE
```
    apt-get update && apt-get upgrade -y && update-grub && sleep 2 && reboot
```
- 8.login dengan root
- 9.edit di script auto-pointing.sh dengan domain mu
```
DOMAIN=webmu.my.id
SUB_DOMAIN=jav-${sub}.webmu.my.id
NS_DOMAIN=nsa-${sub}.webmu.my.id
CF_ID=emailmu@gmail.com
CF_KEY=key_global_mu_xxxxxxxxxxxxxxxxxxxxx
```
- 10.Ganti Dengan Domain Kamu
```
cat >/root/domain <<EOF
webmu.my.id
EOF
```
- 11.Ganti Dengan Domain Kamu
```
mkdir -p /etc/xray
cat >/etc/xray/domain <<EOF
webmu.my.id
EOF
```

- 12.Tambahin CERT SSL Let's Encrypt  ~ JANGAN DULU DO, KALO ERROR BARU TAMBHAIN INI, BLOM NORMAL INI
```

curl https://get.acme.sh | sh

~/.acme.sh/acme.sh --set-default-ca --server letsencrypt
~/.acme.sh/acme.sh --register-account -m emailmu@gmail.com
~/.acme.sh/acme.sh --issue -d webmu.my.id --standalone

~/.acme.sh/acme.sh --installcert -d webmu.my.id --key-file /root/private.key --fullchain-file /root/cert.crt

```
- 13.Install Script
```
wget https://raw.githubusercontent.com/cannotbenormal/exray/main/setup.sh && chmod +x setup.sh && ./setup.sh
```
- 14.Wajib Reboot
- 15.Ketik: xmenu
- 16.Pilih 9:Perbarui Sertifikat #SKIP
- 17.Reboot dulu, baru bisa make.


nano /usr/bin/auto-pointing
nano /usr/bin/auto-pointing
nano /usr/bin/auto-pointing

























<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=SCRIPT+XRAY+MANTAP" />
</p>

# XRAY MANTAP
- ***Script XRAY Multi Port 443/80 By SL***
- ***SCRIPT UNTUK MEMBUAT SERVER VPN***

<p align='center'><a href="https://api.daily.dev/get?r=cannotbenormal"><img src="https://raw.githubusercontent.com/cannotbenormal/.github/main/kotori2.png?r=82s" width="150" alt="Hayuk"/></a></p>

<p align="center">
<img height=21 src="https://komarev.com/ghpvc/?username=cannotbenormal">
</p>
<div height='45' align="center">
<h2>Contact me: <br>
<a href="https://facebook.com/sulaiman.xl"> <img src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/facebook.svg" height='50'> </a>
<h2>Support me: <br>
<a href="https://trakteer.id/sulaiman-l/tip"> <img src="https://cdn.trakteer.id/images/embed/trbtn-red-6.png" height='50'> </a>
</h2>
</div>
#

# FITUR XRAY TLS
- TROJAN WS        : **443**
- TROJAN GRPC      : **443**
- SHADOWSOCKS WS   : **443**
- SHADOWSOCKS GRPC : **443**
- VMESS WS         : **443**
- VMESS GRPC       : **443**
- VLESS WS         : **443**
- VLESS GRPC       : **443**

# FITUR XRAY HTTP
- TROJAN WS        : **80**
- TROJAN GRPC      : **80**
- SHADOWSOCKS WS   : **80**
- SHADOWSOCKS GRPC : **80**
- VMESS WS         : **80**
- VMESS GRPC       : **80**
- VLESS WS         : **80**
- VLESS GRPC       : **80**


# OS 
- Debian 9 (HVM)
- Debian 10
* Berhasil di gunakan di vps aws dan os debian 9 hvm
* untuk vps isp yg lain saya tidak tau, dan os yg lain juga saya tidak tau wkwk

# Syarat && Bahan Untuk Menggunakan Script Ini
- Wajib Punya VPS
- Wajib Punya Akun Cloudflare
- Wajib Punya Domain Punya Kamu Sendiri
- ***Jika semua syarat dan Bahan sudah terpenuhi ,silahkan di coba script ini***

# Settingan Di Cloudflare
1. Buat VPS Baru
2. Pointing Dulu Domain Kamu, Kalo sudah pernah di pointing
   - Pergi ke dash.cloudflare.com,lalu pilih domain punya kamu, di tab TLS/SSL lalu pilih Overview, di tab TLS/SSL Harus pilih yang FULL
   - FULL (Encrypts end-to-end, using a self signed certificate on the server)✅
   ![settinggambar1](https://raw.githubusercontent.com/cannotbenormal/exray/main/img/settingambar1.jpg)
   ![settinggambar2](https://raw.githubusercontent.com/cannotbenormal/exray/main/img/settingambar2.jpg)
   ![settinggambar3](https://raw.githubusercontent.com/cannotbenormal/exray/main/img/settingambar3.jpg)
   - Lalu pilih Edge Certificates disini kamu harus matikan Always Use HTTPS (Harus Mati/OFF)❌
   ![settinggambar4](https://raw.githubusercontent.com/cannotbenormal/exray/main/img/settingambar4.jpg)
   - Buka tab Network di cloudflare kamu aktifkan WebSocket nya ✅
   ![settinggambar5](https://raw.githubusercontent.com/cannotbenormal/exray/main/img/settingambar5.jpg)
   ![settinggambar6](https://raw.githubusercontent.com/cannotbenormal/exray/main/img/settingambar6.jpg)
3. Setting Di Cloudflare Selesai
# Cara Install Script Nya
- Login ke VPS kamu ( wajib pake user ***root***)
1. MASUK KE VPS LALU KETIK

<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=sudo+su" />
</p>


```
sudo su
```

2. Update Dulu VPS NYA

<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=apt-get+update" />
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=apt-get+upgrade+-y" />
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=update-grub+&&+reboot" />
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=reboot" />
</p>

```
apt-get update && apt-get upgrade -y && update-grub && sleep 2 && reboot
```
- Otomatis Akan Reboot/ Hidupkan Ulang
3. Login Lagi Ke VPS NYA
4. Masukan Nama Domain Kamu, domain harus aktif
- contoh nama domain punya aku,silahkan ganti dengan punya kamu
```
cat >/root/domain <<EOF
mantapxsl.my.id
EOF
```
- ganti mantapxsl.my.id menjadi nama domain punya kamu
```
mkdir -p /etc/xray
cat >/etc/xray/domain <<EOF
mantapxsl.my.id
EOF
```

5. Salin kode di bawah ini dan paste kan ke dalam vps punya kamu
- maka proses install akan berjalan, jangan keluar dari vps
- jika keluar dari vps saat lagi proses install,maka akan gagal
```
wget https://raw.githubusercontent.com/cannotbenormal/exray/main/setup.sh && chmod +x setup.sh && ./setup.sh
```
6. jika sudah selesai,lalu ketik xmenu untuk menampilkan menu
<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=xmenu" />
</p>

```
xmenu
```
7. DONE / SELESAI

# Info Perbaiki / FIX
- ***NOTE***
- jika xray dan nginx mengalami error !
- ketik
```
certv2ray
```
lalu ketik
```
restart-xray
```

# INFO KODE SCRIPT
- xmenu (untuk menampilkan menu
- updatedll (untuk update sc)
- restart-xray (hidupkan ulang xray)
- certv2ray (Perbarui Sertifikat / Update Certificate)

# Contoh Cara Pointing Domain ke Cloudflare
- Link:
```
https://youtu.be/Pwfvwy5Ghcw
```
# Cara Pointing Subdomain Secara Otomatis Di Cloudflare Menggunakan Script
- edit dulu script auto-pointing nya
```
nano /usr/bin/auto-pointing
```
- contoh punya aku
- tinggal ubah saja yg mantapxsl.my.id menjadi domain punya kamu
```
DOMAIN=mantapxsl.my.id
SUB_DOMAIN=onichan-${sub}.mantapxsl.my.id
NS_DOMAIN=zerosl-${sub}.mantapxsl.my.id
CF_ID=slinfinity69@gmail.com
CF_KEY=dd2c5e0313f122b3c1833471d469b1025f492
```
- Lalu ubah juga CF_ID= isi dengan alamat email cloudflare kamu
- CF_KEY= isi dengan YOUR API KEY (GLOBAL API KEY)

# Cara Mendapatkan API KEY CLOUDFLARE
- Link
https://dash.cloudflare.com/profile/api-tokens
- API Keys ,Global API Key, Klik View, Masukan Password kamu, lalu klik View
- nanti muncul Your API Key ,lalu tinggal di salin/copy


