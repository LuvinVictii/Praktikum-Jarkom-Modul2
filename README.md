# Lapres
### Kelompok F09
|   Nama   |      NRP      |
|:--------:|:-------------:|
| Muhammad Daffa Harits | 5025211005 |
| Muhammad Naufal Baihaqi | 5025211103 |

## No 1
Yudhistira akan digunakan sebagai DNS Master, Werkudara sebagai DNS Slave, Arjuna merupakan Load Balancer yang terdiri dari beberapa Web Server yaitu Prabakusuma, Abimanyu, dan Wisanggeni. Buatlah topologi dengan pembagian sebagai [berikut](https://docs.google.com/spreadsheets/d/1OqwQblR_mXurPI4gEGqUe7v0LSr1yJViGVEzpMEm2e8/edit#gid=1475903193). Folder topologi dapat diakses pada drive [berikut](https://drive.google.com/drive/folders/1Ij9J1HdIW4yyPEoDqU1kAwTn_iIxg3gk)
### Konfigurasi
**Pandudewanata**
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.56.1.1
	netmask 255.255.255.0

auto eth2
iface eth2 inet static
	address 10.56.2.1
	netmask 255.255.255.0

auto eth3
iface eth3 inet static
	address 10.56.3.1
	netmask 255.255.255.0
```
**Nakula**
```
auto eth0
iface eth0 inet static
	address 10.56.1.2
	netmask 255.255.255.0
	gateway 10.56.1.1
```
**Sadewa**
```
auto eth0
iface eth0 inet static
	address 10.56.1.3
	netmask 255.255.255.0
	gateway 10.56.1.1
```
**Yudistira**
```
auto eth0
iface eth0 inet static
	address 10.56.2.2
	netmask 255.255.255.0
	gateway 10.56.2.1
```
**Werkudara**
```
auto eth0
iface eth0 inet static
	address 10.56.2.3
	netmask 255.255.255.0
	gateway 10.56.2.1
```
**Prabukusuma**
```
auto eth0
iface eth0 inet static
	address 10.56.3.2
	netmask 255.255.255.0
	gateway 10.56.3.1
```
**Abimanyu**
```
auto eth0
iface eth0 inet static
	address 10.56.3.3
	netmask 255.255.255.0
	gateway 10.56.3.1
```
**Wisanggeni**
```
auto eth0
iface eth0 inet static
	address 10.56.3.4
	netmask 255.255.255.0
	gateway 10.56.3.1
```
### Ping
1. **Pandudewanata**  
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/00da1eeb-9f15-4de8-9fe5-02ec4f76daf1)
2. **Nakula**  
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/64f1ba39-bc65-47bb-b051-17983ed335f8)
3. **Sadewa**  
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/e6c1dbfb-935d-47c8-b7a5-04ca32ae83e5)
4. **Yudistira**  
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/5c2c41e8-deef-485c-a7e4-a5227093065f)
5. **Werkudara**  
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/89d63cc2-68b2-4ca3-b880-60a236a19017)
6. **Prabukusuma**  
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/b3b30ce6-4b6c-4649-b7d7-500d20b056af)
7. **Abimanyu**  
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/c7537115-af46-4bfa-a05a-2926e822bc38)
8. **Wisanggeni**  
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/b80fd167-3566-4532-9d00-7eac9226893c)

## No 2
Buatlah website utama pada node arjuna dengan akses ke arjuna.yyy.com dengan alias www.arjuna.yyy.com dengan yyy merupakan kode kelompok.
### Ping arjuna.f09.com di Werkudara
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/b0c7c338-c0e0-4163-9f22-b8c038de53c7)
### Reverse dns
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/238ecc93-b411-43e3-a7fc-0a2a3d8c1b0e)
### Ping alias
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/544861f8-d76e-4fd2-824d-ba6bd163afa4)

## No 3
Dengan cara yang sama seperti soal nomor 2, buatlah website utama dengan akses ke abimanyu.yyy.com dan alias www.abimanyu.yyy.com.
### Ping abimanyu
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/74485afb-1a0f-47b9-88f3-644c30cef8bd)
### Reverse abimanyu
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/da08efcf-2e7c-4eca-a694-e1127d7d6ba6)
### Ping www.abimanyu.f09.com
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/a345e04d-032c-4424-94dd-07bad7d002d9)

## No 4
Kemudian, karena terdapat beberapa web yang harus di-deploy, buatlah subdomain parikesit.abimanyu.yyy.com yang diatur DNS-nya di Yudhistira dan mengarah ke Abimanyu.
### parikesit.abimanyu.yyy.com
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/231a8003-df39-4d5e-b42b-d374146f221e)

## No 5
Buat juga reverse domain untuk domain utama. (Abimanyu saja yang direverse)
### Reverse abimanyu
**(Reverse abimanyu sudah dikerjakan di no 3)**
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/efc4c0e0-7c44-4e25-96a1-6bdf1e105322)

## No 6
Agar dapat tetap dihubungi ketika DNS Server Yudhistira bermasalah, buat juga Werkudara sebagai DNS Slave untuk domain utama.
### Slave
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/46d3d8ea-0838-4253-953f-c999ff0561e2)

## No 7
Seperti yang kita tahu karena banyak sekali informasi yang harus diterima, buatlah subdomain khusus untuk perang yaitu baratayuda.abimanyu.yyy.com dengan alias www.baratayuda.abimanyu.yyy.com yang didelegasikan dari Yudhistira ke Werkudara dengan IP menuju ke Abimanyu dalam folder Baratayuda.  

![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/dac80ce6-561d-4151-94a0-7d8678b7ec32)

## No 8
Untuk informasi yang lebih spesifik mengenai Ranjapan Baratayuda, buatlah subdomain melalui Werkudara dengan akses rjp.baratayuda.abimanyu.yyy.com dengan alias www.rjp.baratayuda.abimanyu.yyy.com yang mengarah ke Abimanyu.  

![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/b6a8086d-9485-4912-abff-b0ebd1397f34)

## No 9
Arjuna merupakan suatu Load Balancer Nginx dengan tiga worker (yang juga menggunakan nginx sebagai webserver) yaitu Prabakusuma, Abimanyu, dan Wisanggeni. Lakukan deployment pada masing-masing worker.  

**Di yudhistira, arjuna diarahkan ke load balancer, kemudian tambahkan cname www**  

![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/a56573b4-9d29-4e17-a3cb-db6eafcb3a01)
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/cdb01509-3696-4638-a1aa-6bc7b156c8c3)
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/c658b270-e4aa-4883-b3b9-40d306bf2997)

## No 10
Kemudian gunakan algoritma Round Robin untuk Load Balancer pada Arjuna. Gunakan server_name pada soal nomor 1. Untuk melakukan pengecekan akses alamat web tersebut kemudian pastikan worker yang digunakan untuk menangani permintaan akan berganti ganti secara acak. Untuk webserver di masing-masing worker wajib berjalan di port 8001-8003. Contoh:
- Prabakusuma:8001
- Abimanyu:8002
- Wisanggeni:8003

**Pengerjaan :**
- Port ditambahkan 800x (x dari 1 sampai 3) di worker (/etc/nginx/sites-available/arjuna) dan load balancer (/etc/nginx/sites-available/lb-arjuna)
- Tes menggunakan lynx untuk http://10.56.3.2:8001, http://10.56.3.3:8002, dst

![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/83b24e80-d930-43b7-b654-da6344307dcc)
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/0aff293f-37f9-4a2e-a540-906a04f8f621)

## No 11
Selain menggunakan Nginx, lakukan konfigurasi Apache Web Server pada worker Abimanyu dengan web server www.abimanyu.yyy.com. Pertama dibutuhkan web server dengan DocumentRoot pada /var/www/abimanyu.yyy  

- **Stop nginx di load balancer dan abimanyu**  
  apt-get install apache2 di abimanyu

- **di yudistira :**  
  hapus baratayuda yang di bawahnya parikesit

- **di werkudara :**  
  nano /etc/bind/named.conf.option

- **di abimanyu :**  
  jalankan apache.sh

- **di nakula :**  
  ubah /etc/resolv.conf agar mengarah ke master dan slave
  test menggunakan lynx abimanyu.f09.com

![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/b44810b5-9ad5-4bd2-952d-15a2b57fecf2)

## No 12
Setelah itu ubahlah agar url www.abimanyu.yyy.com/index.php/home menjadi www.abimanyu.yyy.com/home.

**Ubah /etc/apache2/sites-available/abimanyu.f09.conf menjadi :**
```
<VirtualHost *:80>
        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/abimanyu.f09
        ServerName abimanyu.f09.com
        ServerAlias www.abimanyu.f09.com

        <Directory /var/www/abimanyu.f09>
                Options +Indexes
        </Directory>

        Alias "/home" "/var/www/abimanyu.f09/index.php/home"

        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/b0c3b01f-fe6c-43ee-9fdc-341fc4bc1547)
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/51815f9e-ca09-4497-8bcc-66563603615e)

## No 13
Selain itu, pada subdomain www.parikesit.abimanyu.yyy.com, DocumentRoot disimpan pada /var/www/parikesit.abimanyu.yyy

no-13.sh :  
```
touch /etc/apache2/sites-available/parikesit.abimanyu.f09.com.conf

mkdir /var/www/parikesit.abimanyu.f09

echo '
<VirtualHost *:80>
        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/parikesit.abimanyu.f09
        ServerName parikesit.abimanyu.f09.com
        ServerAlias www.parikesit.abimanyu.f09.com

        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>' > /etc/apache2/sites-available/parikesit.abimanyu.f09.com.conf

a2ensite parikesit.abimanyu.f09.com.conf

service apache2 reload

service apache2 restart

apt-get install wget unzip


wget 'https://drive.usercontent.google.com/download?id=1LdbYntiYVF_NVNgJis1GLCLPEGyIOreS&export=download&authuser=0&confirm=t&uuid=7440274a-d695-44db-8cd9-70df5bbf7c96&at=APZUnTWw6S5Rd4s_a6CHfvUKTqQG:1696947964978' -O parikesit_abimanyu.zip

unzip -j parikesit_abimanyu.zip -d /var/www/parikesit.abimanyu.f09


rm -rf /var/www/parikesit.abimanyu.f09/parikesit_abimanyu.zip
```
**Di yudhistira :**  
ubah /etc/bind/abimanyu/abimanyu.f09.com  
-parikesit IN A diarahkan ke abimanyu  
-buat cname parikesit ( www.parikesit IN CNAME parikesit.abimanyu.f09.com. )  

![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/4e426649-2c46-44f9-b4ba-ba507bb8a74c)

## No 14
Pada subdomain tersebut folder /public hanya dapat melakukan directory listing sedangkan pada folder /secret tidak dapat diakses (403 Forbidden).

buat folder secret dan tambahkan pada /etc/apache2/sites-available/parikesit.abimanyu.f09.com.conf
di bawah alias
```
	<Directory /var/www/parikesit.abimanyu.f09/public>
                Options +Indexes
        </Directory>

        <Directory /var/www/parikesit.abimanyu.f09/secret>
               Options -Indexes
        </Directory>
```
atau bisa langsung dicek karena sudah dibash di soal 13  
```
lynx www.parikesit.abimanyu.f09.com/public  
lynx www.parikesit.abimanyu.f09.com/secret  
```
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/5f6026c1-2745-41fc-906a-2da24e84ee18)
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/adea0c16-88a2-4e01-a654-5c2fc675ba58)

## No 15
Buatlah kustomisasi halaman error pada folder /error untuk mengganti error kode pada Apache. Error kode yang perlu diganti adalah 404 Not Found dan 403 Forbidden.

tambahkan  
```
ErrorDocument 404 /error/404.html  
ErrorDocument 403 /error/403.html  
```  
kemudian cek
```
lynx www.parikesit.abimanyu.f09.com/woooyyyyy  
```
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/ccbae3b9-a3b4-4b12-8244-7296dd53b7a3)

## No 16
Buatlah suatu konfigurasi virtual host agar file asset www.parikesit.abimanyu.yyy.com/public/js menjadi www.parikesit.abimanyu.yyy.com/js  
  
tambahkan  
```
Alias "/js" "/var/www/parikesit.abimanyu.f09/public/js"  
```
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/59634fa0-5edc-42a2-9456-e44b180c97e6)

## No 17
Agar aman, buatlah konfigurasi agar www.rjp.baratayuda.abimanyu.yyy.com hanya dapat diakses melalui port 14000 dan 14400.

Jalankan bash no-17 yg isinya :
```
touch /etc/apache2/sites-available/rjp.baratayuda.abimanyu.f09.com.conf

mkdir /var/www/rjp.baratayuda.abimanyu.f09

echo '
<VirtualHost *:14000 *:14400>
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/rjp.baratayuda.abimanyu.f09
    ServerName www.rjp.baratayuda.abimanyu.f09.com
    ServerAlias rjp.baratayuda.abimanyu.f09.com

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>'> /etc/apache2/sites-available/rjp.baratayuda.abimanyu.f09.com.conf


echo '
Listen 80
Listen 14000
Listen 14400

<IfModule ssl_module>
        Listen 443
</IfModule>

<IfModule mod_gnutls.c>
        Listen 443
</IfModule>' > /etc/apache2/ports.conf
a2ensite rjp.baratayuda.abimanyu.f09.com.conf

service apache2 reload

service apache2 restart

apt-get install wget unzip

wget 'https://drive.usercontent.google.com/download?id=1pPSP7yIR05JhSFG67RVzgkb-VcW9vQO6&export=download&authuser=0&confirm=t&uuid=c039943d-843b-47b9-8910-4b46edf58596&at=APZUnTWSNiEJdlQx1mlaCEI-F6-B:1696957565777' -O rjp_baratayuda.zip

unzip -j rjp_baratayuda.zip -d ./

mv rjp.baratayuda.abimanyu.yyy.com

rm -rf /var/www/rjp.baratayuda.abimanyu.f09/rjp_baratayuda_abimanyu.zip
```

di wekudara :  
arahkan rjp ke abimanyu  
  
di yudhistira :  
arahkan ns1 ke abimanyu  
  
test di client  
```
lynx rjp.baratayuda.abimanyu.f09.com:14400  
```
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/1442a33a-78b4-4045-9707-a6f9814b654f)

## No 18

Untuk mengaksesnya buatlah autentikasi username berupa “Wayang” dan password “baratayudayyy” dengan yyy merupakan kode kelompok. Letakkan DocumentRoot pada /var/www/rjp.baratayuda.abimanyu.yyy.

**Add user**  

- **Tertolak**  
  ![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/00aaf4fe-3511-41f7-83f5-b0186e91544a)
- **Inputkan username : Wayang**  
  ![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/893d54da-5fe3-4570-bc77-b3dd2c369bee)
- **Masukkan password**  
  ![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/6f7f6fb4-b6f4-42e2-b056-f90f3d9358ba)
- **Terbuka**  
  ![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/980e73e1-290e-4512-9e7b-feec253ddee9)  

klik di abimanyu :
```
htpasswd -b -c /etc/apache2/.htpasswd Wayang baratayudaf09
```

lalu tambahkan di /etc/apache2/sites-available/rjp.baratayuda.abimanyu.f09.com.conf  
```
<Directory "/var/www/rjp.baratayuda.abimanyu.f09">
                AuthType Basic
                AuthName "Restricted Content"
                AuthUserFile /etc/apache2/.htpasswd
                Require valid-user
        </Directory>
```
lalu test di  
  
lynx rjp.baratayuda.abimanyu.f09.com:14400  
nanti tidak bisa masuk, tunggu bentar lalu masukkan:  
username : Wayang  
pass : baratayudaf09  

## No 19
Buatlah agar setiap kali mengakses IP dari Abimanyu akan secara otomatis dialihkan ke www.abimanyu.yyy.com (alias)  
  
tambahkan dibawah serveralias www.abimanyu.f09.com di /etc/apache2/sites-available/abimanyu.f09.com.conf  
  
ServerAlias 10.56.3.3  
  
lalu test di client  
lynx 10.56.3.3  
![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/e48f974f-a26b-4ce4-8733-9df4a5c421f5)  

## No 20
Karena website www.parikesit.abimanyu.yyy.com semakin banyak pengunjung dan banyak gambar gambar random, maka ubahlah request gambar yang memiliki substring “abimanyu” akan diarahkan menuju abimanyu.png

di abimanyu :
```
nano /var/www/parikesit.abimanyu.f09/.htaccess
```
lalu isi nanonya dengan : 
```
RewriteEngine On
RewriteCond %{REQUEST_URI} !^/public/images/abimanyu.png
RewriteCond %{REQUEST_URI} abimanyu
RewriteRule \.(jpg|jpeg|png)$ /public/images/abimanyu.png [L]
```
lalu, ubah conf parikesitnya :
```
nano /etc/apache2/sites-available/parikesit.abimanyu.f09.com.conf
```
tambahkan ini :
```
<Directory /var/www/parikesit.abimanyu.f09>
                Options +FollowSymLinks -Multiviews
                AllowOverride All
        </Directory>
```

lalu jalankan :
a2enmod rewrite

lalu apache restart

lalu test di client dengan :
lynx parikesit.abimanyu.f09.com/abimanyu.jpg

- Klik D:  
  ![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/2ad63c2c-08d8-4bf0-96dc-31b83dec1a56)

- Hasil:  
  ![image](https://github.com/LuvinVictii/Praktikum-Jarkom-Modul2/assets/78089862/6f2373a2-a9ba-44f1-91c8-e4c620ee8350)
