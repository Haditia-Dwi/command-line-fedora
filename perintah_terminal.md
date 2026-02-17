# 🐧 Fedora Personal Cheat Sheet
![Fedora Version](https://img.shields.io/badge/OS-Fedora_41-blue?style=flat-square&logo=fedora)
![Status](https://img.shields.io/badge/Status-Learning-green?style=flat-square)

Dokumentasi pribadi untuk command penting di Fedora Workstation.

---

## 🚀 Perintah-Perintah penting

Perintah-perintah yang dapat digunakan untuk mengetahui versi os.

### Operation System Versions
Lakukan ini untuk mengetahui versi OS.
Simple
```bash
cat /etc/fedora-release
```
Detail
```bash
cat /etc/fedora-release
```
Cek versi dan kernel
```bash
hostnamectl
```
Untuk menampilkan visualisasi
```bash
sudo dnf install fastfetch
fastfetch
```
---
### Desktop Environment
lalu ada perintah untuk mempercantik tampilan desktop
```bash
sudo dnf install gnome-tweaks gnome-extensions-app
```

```bash
flatpak install flathub com.mattjakeman.ExtensionManager
```
---
### Shortcut Configuration
fedora mempunyai fitur yang memungkinkan membuka aplikasi lewat shortcut keyboard dengan mengkonfigurasi nama gnome-software

ada dua cara yang bisa digunakan yaitu melihat dari 'flathub' ataupun '.desktop'

```bash
ls /usr/share/applications/
```
```bash
cat /usr/share/applications/firefox.desktop | grep Exec
```
terminal akan menampilkan output berupa 'Exec=firefox %u' yang mana bisa dicopy untuk dikonfigurasi menjadi shortcut di settings

jika ingin melihat menggunakan flathub maka perintahnya sebagai berikut
```bash
flatpack list
```
---
### Shell Configuration
kita juga bisa meng-kustomisasi terminal dengan kombinasi zsh dan starship untuk kebutuhan informatif dan produktifitas

1. penginstallan zsh
```bash
sudo dnf install zsh
```
2. Install starship
```bash
curl -sS https://starship.rs/install.sh | sh
```
3. jadikan Zsh sebagai default
```bash
chsh -s $(which zsh)
```
4. masukkan starship kedalam Zsh
```bash
echo 'eval "$(starship init zsh)"' >> ~/.zshrc
```
5. ubah dari bash ke zsh dengan menekan perintah berikut lalu enter
```bash
zsh
```
---
### cara untuk kustomisasi fedora
ada beberapa cara untuk meng-kustomisasi fedora diantaranya
1. mendownload tweaks untuk mengkonfigurasi tema, ikon, dan tampilan desktop serta mendownload Extensions App untuk mematikan/menghidupkan ekstensi
```bash
sudo dnf install gnome-tweaks gnome-extensions-app
```
2. mendownload Extension Manager untuk mendownload ekstensi desktop yang terkadang error jika mendownload lewat browser
```bash
flatpak install flathub com.mattjakeman.ExtensionManager
```
3. tempat untuk mendownload tema. kamu bisa mendownload ribuan tema gratis yang dikustomisasi lewat situs Gnome-look.org

setelah melakukan langkah ketiga diatas maka langkah selanjutnya membuat file untuk menyimpan hasil downloadan dari situs komunitas

1. buat direktori baru yang tersembunyi
```bash
mkdir -p ~/.themes ~/.icons
```
2. ekstrak file yang telah didownload CUT lalu pindahkan ke direktori tersembuyi yang telah dibuat dengan menekan CTRL + H

3. pindah ke software Tweaks ==> Appearance lalu atur pada bagian 
   1. Legacy Applications
   2. Icons
   3. Shell