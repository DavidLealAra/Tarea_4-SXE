# Tarea_4-SXE

# 1. Utiliza la imagen de Ubuntu , tag 22 y apoyandote en esta guía sigue sus instrucciones para instalar LAMP en dicho contenedor.

Primero de todo creamos el contenedor de esta manera:
```bash
sudo docker run -d --name dam_lamp -p 8000:80 -it ubuntu:22.04
```
Salida:

57590e1292d30f2f0f8fd4faf4e347998486b71eff63cce368ad64c4e15c3e27

Y nos metemos dentro:
```bash
sudo docker exec -it dam-lamp sh
```
Sin salida.

Ahora siguiendo el metodo 2 de la guia ponemos los siguientes comandos:

Actualizas:
```bash
apt update
```
<details>
<summary>Salida:</summary>
<br>


Get:1 http://archive.ubuntu.com/ubuntu jammy InRelease [270 kB]


Get:2 http://security.ubuntu.com/ubuntu jammy-security InRelease [129 kB]           


Get:3 http://archive.ubuntu.com/ubuntu jammy-updates InRelease [128 kB]             


Get:4 http://archive.ubuntu.com/ubuntu jammy-backports InRelease [127 kB]


Get:5 http://archive.ubuntu.com/ubuntu jammy/main amd64 Packages [1792 kB]


Get:6 http://archive.ubuntu.com/ubuntu jammy/universe amd64 Packages [17.5 MB]


Get:7 http://security.ubuntu.com/ubuntu jammy-security/main amd64 Packages [2377 kB]


Get:8 http://archive.ubuntu.com/ubuntu jammy/restricted amd64 Packages [164 kB]


Get:9 http://archive.ubuntu.com/ubuntu jammy/multiverse amd64 Packages [266 kB]         


Get:10 http://archive.ubuntu.com/ubuntu jammy-updates/universe amd64 Packages [1451 kB]  


Get:11 http://archive.ubuntu.com/ubuntu jammy-updates/multiverse amd64 Packages [51.8 kB]  


Get:12 http://archive.ubuntu.com/ubuntu jammy-updates/restricted amd64 Packages [3283 kB]   


Get:13 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 Packages [2654 kB]        


Get:14 http://archive.ubuntu.com/ubuntu jammy-backports/main amd64 Packages [81.4 kB]      


Get:15 http://archive.ubuntu.com/ubuntu jammy-backports/universe amd64 Packages [33.7 kB]    


Get:16 http://security.ubuntu.com/ubuntu jammy-security/multiverse amd64 Packages [44.7 kB]  


Get:17 http://security.ubuntu.com/ubuntu jammy-security/restricted amd64 Packages [3205 kB]


Get:18 http://security.ubuntu.com/ubuntu jammy-security/universe amd64 Packages [1162 kB]


Fetched 34.7 MB in 3s (12.3 MB/s)                           


Reading package lists... Done


Building dependency tree... Done


Reading state information... Done


All packages are up to date.
</details>

Instalas el Lamp server:
```bash
apt install -y lamp-server^
```
<details>
<summary>Salida:</summary>
<br>

  
Reading package lists... Done


Building dependency tree... Done


Reading state information... Done


Note, selecting 'libevent-pthreads-2.1-7' for task 'lamp-server'


Note, selecting 'libperl5.34' for task 'lamp-server'


Note, selecting 'libcurl4' for task 'lamp-server'


Note, selecting 'libtimedate-perl' for task 'lamp-server'


Note, selecting 'libhtml-tagset-perl' for task 'lamp-server'


Note, selecting 'libgdbm-compat4' for task 'lamp-server'


Note, selecting 'libssh-4' for task 'lamp-server'


Note, selecting 'ssl-cert' for task 'lamp-server'


Note, selecting 'libfcgi-perl' for task 'lamp-server'


Note, selecting 'perl' for task 'lamp-server'


Note, selecting 'libldap-common' for task 'lamp-server'


Note, selecting 'libaio1' for task 'lamp-server'


Note, selecting 'libaprutil1-dbd-sqlite3' for task 'lamp-server'


Note, selecting 'mysql-server-8.0' for task 'lamp-server'


Note, selecting 'libapr1' for task 'lamp-server'


Note, selecting 'libsasl2-modules' for task 'lamp-server'


Note, selecting 'mysql-client-8.0' for task 'lamp-server'


Note, selecting 'libsasl2-2' for task 'lamp-server'


Note, selecting 'mysql-common' for task 'lamp-server'


Note, selecting 'libapache2-mod-php' for task 'lamp-server'


Note, selecting 'php-common' for task 'lamp-server'


Note, selecting 'php8.1-opcache' for task 'lamp-server'


Note, selecting 'liblua5.3-0' for task 'lamp-server'


Note, selecting 'libencode-locale-perl' for task 'lamp-server'


Note, selecting 'librtmp1' for task 'lamp-server'


Note, selecting 'php8.1-mysql' for task 'lamp-server'


Note, selecting 'libapache2-mod-php8.1' for task 'lamp-server'


Note, selecting 'bzip2' for task 'lamp-server'


Note, selecting 'liblwp-mediatypes-perl' for task 'lamp-server'


Note, selecting 'libsasl2-modules-db' for task 'lamp-server'


Note, selecting 'libprotobuf-lite23' for task 'lamp-server'


Note, selecting 'libldap-2.5-0' for task 'lamp-server'


Note, selecting 'apache2-data' for task 'lamp-server'


Note, selecting 'libhtml-template-perl' for task 'lamp-server'


Note, selecting 'apache2-bin' for task 'lamp-server'


Note, selecting 'liburi-perl' for task 'lamp-server'


Note, selecting 'libfcgi0ldbl' for task 'lamp-server'


Note, selecting 'libsodium23' for task 'lamp-server'


Note, selecting 'libio-html-perl' for task 'lamp-server'


Note, selecting 'mecab-ipadic-utf8' for task 'lamp-server'


Note, selecting 'mecab-ipadic' for task 'lamp-server'


Note, selecting 'mailcap' for task 'lamp-server'


Note, selecting 'php8.1-common' for task 'lamp-server'


Note, selecting 'php8.1-readline' for task 'lamp-server'


Note, selecting 'libaprutil1' for task 'lamp-server'


Note, selecting 'libhttp-date-perl' for task 'lamp-server'


Note, selecting 'libmecab2' for task 'lamp-server'


Note, selecting 'php-mysql' for task 'lamp-server'


Note, selecting 'libhtml-parser-perl' for task 'lamp-server'


Note, selecting 'libcgi-fast-perl' for task 'lamp-server'


Note, selecting 'mysql-server' for task 'lamp-server'


Note, selecting 'mysql-server-core-8.0' for task 'lamp-server'


Note, selecting 'apache2-utils' for task 'lamp-server'


Note, selecting 'libbrotli1' for task 'lamp-server'


Note, selecting 'mime-support' for task 'lamp-server'


Note, selecting 'mecab-utils' for task 'lamp-server'


Note, selecting 'libevent-core-2.1-7' for task 'lamp-server'


Note, selecting 'apache2' for task 'lamp-server'


Note, selecting 'libclone-perl' for task 'lamp-server'


Note, selecting 'php8.1-cli' for task 'lamp-server'


Note, selecting 'mysql-client-core-8.0' for task 'lamp-server'


Note, selecting 'libhttp-message-perl' for task 'lamp-server'


Note, selecting 'libfcgi-bin' for task 'lamp-server'


Note, selecting 'perl-modules-5.34' for task 'lamp-server'


Note, selecting 'libcgi-pm-perl' for task 'lamp-server'


Note, selecting 'libaprutil1-ldap' for task 'lamp-server'


The following additional packages will be installed:


  ca-certificates file libargon2-1 libbsd0 libedit2 libexpat1 libgdbm6 libicu70 libjansson4
  libmagic-mgc libmagic1 libmd0 libnghttp2-14 libnuma1 libpsl5 libsqlite3-0 libxml2
  media-types netbase openssl psmisc publicsuffix tzdata ucf xz-utils

  
Suggested packages:

  
  apache2-doc apache2-suexec-pristine | apache2-suexec-custom www-browser ufw bzip2-doc
  php-pear gdbm-l10n libdata-dump-perl libipc-sharedcache-perl libsasl2-modules-gssapi-mit
  | libsasl2-modules-gssapi-heimdal libsasl2-modules-ldap libsasl2-modules-otp
  libsasl2-modules-sql libbusiness-isbn-perl libwww-perl mailx tinyca perl-doc
  libterm-readline-gnu-perl | libterm-readline-perl-perl make libtap-harness-archive-perl


The following NEW packages will be installed:


  apache2 apache2-bin apache2-data apache2-utils bzip2 ca-certificates file libaio1  
  libapache2-mod-php libapache2-mod-php8.1 libapr1 libaprutil1 libaprutil1-dbd-sqlite3
  libaprutil1-ldap libargon2-1 libbrotli1 libbsd0 libcgi-fast-perl libcgi-pm-perl
  libclone-perl libcurl4 libedit2 libencode-locale-perl libevent-core-2.1-7
  libevent-pthreads-2.1-7 libexpat1 libfcgi-bin libfcgi-perl libfcgi0ldbl libgdbm-compat4
  libgdbm6 libhtml-parser-perl libhtml-tagset-perl libhtml-template-perl libhttp-date-perl
  libhttp-message-perl libicu70 libio-html-perl libjansson4 libldap-2.5-0 libldap-common
  liblua5.3-0 liblwp-mediatypes-perl libmagic-mgc libmagic1 libmd0 libmecab2 libnghttp2-14
  libnuma1 libperl5.34 libprotobuf-lite23 libpsl5 librtmp1 libsasl2-2 libsasl2-modules
  libsasl2-modules-db libsodium23 libsqlite3-0 libssh-4 libtimedate-perl liburi-perl libxml2
  mailcap mecab-ipadic mecab-ipadic-utf8 mecab-utils media-types mime-support mysql-client-8.0
  mysql-client-core-8.0 mysql-common mysql-server mysql-server-8.0 mysql-server-core-8.0
  netbase openssl perl perl-modules-5.34 php-common php-mysql php8.1-cli php8.1-common
  php8.1-mysql php8.1-opcache php8.1-readline psmisc publicsuffix ssl-cert tzdata ucf xz-utils


0 upgraded, 91 newly installed, 0 to remove and 0 not upgraded.


Need to get 61.5 MB of archives.


After this operation, 382 MB of additional disk space will be used.


Get:1 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 perl-modules-5.34 all 5.34.0-3ubuntu1.3 [2976 kB]


Get:2 http://archive.ubuntu.com/ubuntu jammy/main amd64 libgdbm6 amd64 1.23-1 [33.9 kB]


Get:3 http://archive.ubuntu.com/ubuntu jammy/main amd64 libgdbm-compat4 amd64 1.23-1 [6606 B]


Get:4 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libperl5.34 amd64 5.34.0-3ubuntu1.3 [4820 kB]


Get:5 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 perl amd64 5.34.0-3ubuntu1.3 [232 kB]


Get:6 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libapr1 amd64 1.7.0-8ubuntu0.22.04.2 [108 kB]


Get:7 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libexpat1 amd64 2.4.7-1ubuntu0.4 [91.2 kB]


Get:8 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libaprutil1 amd64 1.6.1-5ubuntu4.22.04.2 [92.8 kB]


Get:9 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libsqlite3-0 amd64 3.37.2-2ubuntu0.3 [641 kB]


Get:10 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libaprutil1-dbd-sqlite3 amd64 1.6.1-5ubuntu4.22.04.2 [11.3 kB]


Get:11 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libsasl2-modules-db amd64 2.1.27+dfsg2-3ubuntu1.2 [20.5 kB]


Get:12 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libsasl2-2 amd64 2.1.27+dfsg2-3ubuntu1.2 [53.8 kB]


Get:13 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libldap-2.5-0 amd64 2.5.18+dfsg-0ubuntu0.22.04.2 [183 kB]


Get:14 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libaprutil1-ldap amd64 1.6.1-5ubuntu4.22.04.2 [9170 B]


Get:15 http://archive.ubuntu.com/ubuntu jammy/main amd64 libbrotli1 amd64 1.0.9-2build6 [315 kB]


Get:16 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libnghttp2-14 amd64 1.43.0-1ubuntu0.2 [76.9 kB]


Get:17 http://archive.ubuntu.com/ubuntu jammy/main amd64 libpsl5 amd64 0.21.0-1.2build2 [58.4 kB]


Get:18 http://archive.ubuntu.com/ubuntu jammy/main amd64 librtmp1 amd64 2.4+20151223.gitfa8646d.1-2build4 [58.2 kB]


Get:19 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libssh-4 amd64 0.9.6-2ubuntu0.22.04.3 [186 kB]


Get:20 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libcurl4 amd64 7.81.0-1ubuntu1.18 [289 kB]


Get:21 http://archive.ubuntu.com/ubuntu jammy/main amd64 libjansson4 amd64 2.13.1-1.1build3 [32.4 kB]


Get:22 http://archive.ubuntu.com/ubuntu jammy/main amd64 liblua5.3-0 amd64 5.3.6-1build1 [140 kB]


Get:23 http://archive.ubuntu.com/ubuntu jammy/main amd64 libicu70 amd64 70.1-2 [10.6 MB]


Get:24 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libxml2 amd64 2.9.13+dfsg-1ubuntu0.4 [763 kB]


Get:25 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 apache2-bin amd64 2.4.52-1ubuntu4.12 [1348 kB]


Get:26 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 apache2-data all 2.4.52-1ubuntu4.12 [165 kB]


Get:27 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 apache2-utils amd64 2.4.52-1ubuntu4.12 [89.1 kB]


Get:28 http://archive.ubuntu.com/ubuntu jammy/main amd64 media-types all 7.0.0 [25.5 kB]


Get:29 http://archive.ubuntu.com/ubuntu jammy/main amd64 mailcap all 3.70+nmu1ubuntu1 [23.8 kB]


Get:30 http://archive.ubuntu.com/ubuntu jammy/main amd64 mime-support all 3.66 [3696 B]


Get:31 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 apache2 amd64 2.4.52-1ubuntu4.12 [97.9 kB]


Get:32 http://archive.ubuntu.com/ubuntu jammy/main amd64 mysql-common all 5.8+1.0.8 [7212 B]


Get:33 http://archive.ubuntu.com/ubuntu jammy/main amd64 libmd0 amd64 1.0.4-1build1 [23.0 kB]


Get:34 http://archive.ubuntu.com/ubuntu jammy/main amd64 libbsd0 amd64 0.11.5-1 [44.8 kB]


Get:35 http://archive.ubuntu.com/ubuntu jammy/main amd64 libedit2 amd64 3.1-20210910-1build1 [96.8 kB]


Get:36 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 mysql-client-core-8.0 amd64 8.0.39-0ubuntu0.22.04.1 
[2762 kB]


Get:37 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 mysql-client-8.0 amd64 8.0.39-0ubuntu0.22.04.1 [22.7 kB]


Get:38 http://archive.ubuntu.com/ubuntu jammy/main amd64 libaio1 amd64 0.3.112-13build1 [7176 B]


Get:39 http://archive.ubuntu.com/ubuntu jammy/main amd64 libevent-core-2.1-7 amd64 2.1.12-stable-1build3 [93.9 kB]


Get:40 http://archive.ubuntu.com/ubuntu jammy/main amd64 libevent-pthreads-2.1-7 amd64 2.1.12-stable-1build3 [7642 B]


Get:41 http://archive.ubuntu.com/ubuntu jammy/main amd64 libmecab2 amd64 0.996-14build9 [199 kB]


Get:42 http://archive.ubuntu.com/ubuntu jammy/main amd64 libnuma1 amd64 2.0.14-3ubuntu2 [22.5 kB]


Get:43 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libprotobuf-lite23 amd64 3.12.4-1ubuntu7.22.04.1 
[209 kB]


Get:44 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 mysql-server-core-8.0 amd64 8.0.39-0ubuntu0.22.04.1 
[17.6 MB]


Get:45 http://archive.ubuntu.com/ubuntu jammy/main amd64 psmisc amd64 23.4-2build3 [119 kB]


Get:46 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 mysql-server-8.0 amd64 8.0.39-0ubuntu0.22.04.1 [1437 kB]


Get:47 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 openssl amd64 3.0.2-0ubuntu1.18 [1184 kB]


Get:48 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 ca-certificates all 20240203~22.04.1 [162 kB]


Get:49 http://archive.ubuntu.com/ubuntu jammy/main amd64 libargon2-1 amd64 0~20171227-0.3 [19.5 kB]


Get:50 http://archive.ubuntu.com/ubuntu jammy/main amd64 netbase all 6.3 [12.9 kB]


Get:51 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 tzdata all 2024a-0ubuntu0.22.04.1 [349 kB]


Get:52 http://archive.ubuntu.com/ubuntu jammy/main amd64 ucf all 3.0043 [56.1 kB]


Get:53 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libmagic-mgc amd64 1:5.41-3ubuntu0.1 [257 kB]


Get:54 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libmagic1 amd64 1:5.41-3ubuntu0.1 [87.2 kB]


Get:55 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 file amd64 1:5.41-3ubuntu0.1 [21.5 kB]


Get:56 http://archive.ubuntu.com/ubuntu jammy/main amd64 publicsuffix all 20211207.1025-1 [129 kB]


Get:57 http://archive.ubuntu.com/ubuntu jammy/main amd64 xz-utils amd64 5.2.5-2ubuntu1 [84.8 kB]


Get:58 http://archive.ubuntu.com/ubuntu jammy/main amd64 bzip2 amd64 1.0.8-5build1 [34.8 kB]


Get:59 http://archive.ubuntu.com/ubuntu jammy/main amd64 php-common all 2:92ubuntu1 [12.4 kB]


Get:60 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 php8.1-common amd64 8.1.2-1ubuntu2.19 [1127 kB]


Get:61 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 php8.1-opcache amd64 8.1.2-1ubuntu2.19 [365 kB]


Get:62 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 php8.1-readline amd64 8.1.2-1ubuntu2.19 [13.6 kB]


Get:63 http://archive.ubuntu.com/ubuntu jammy/main amd64 libsodium23 amd64 1.0.18-1build2 [164 kB]


Get:64 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 php8.1-cli amd64 8.1.2-1ubuntu2.19 [1833 kB]


Get:65 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libapache2-mod-php8.1 amd64 8.1.2-1ubuntu2.19 [1765 
kB]


Get:66 http://archive.ubuntu.com/ubuntu jammy/main amd64 libapache2-mod-php all 2:8.1+92ubuntu1 [2898 B]


Get:67 http://archive.ubuntu.com/ubuntu jammy/main amd64 libhtml-tagset-perl all 3.20-4 [12.5 kB]


Get:68 http://archive.ubuntu.com/ubuntu jammy/main amd64 liburi-perl all 5.10-1 [78.8 kB]


Get:69 http://archive.ubuntu.com/ubuntu jammy/main amd64 libhtml-parser-perl amd64 3.76-1build2 [88.4 kB]


Get:70 http://archive.ubuntu.com/ubuntu jammy/main amd64 libcgi-pm-perl all 4.54-1 [188 kB]


Get:71 http://archive.ubuntu.com/ubuntu jammy/main amd64 libfcgi0ldbl amd64 2.4.2-2build2 [28.0 kB]


Get:72 http://archive.ubuntu.com/ubuntu jammy/main amd64 libfcgi-perl amd64 0.82+ds-1build1 [22.8 kB]


Get:73 http://archive.ubuntu.com/ubuntu jammy/main amd64 libcgi-fast-perl all 1:2.15-1 [10.5 kB]


Get:74 http://archive.ubuntu.com/ubuntu jammy/main amd64 libclone-perl amd64 0.45-1build3 [11.0 kB]


Get:75 http://archive.ubuntu.com/ubuntu jammy/main amd64 libencode-locale-perl all 1.05-1.1 [11.8 kB]


Get:76 http://archive.ubuntu.com/ubuntu jammy/main amd64 libfcgi-bin amd64 2.4.2-2build2 [11.2 kB]


Get:77 http://archive.ubuntu.com/ubuntu jammy/main amd64 libhtml-template-perl all 2.97-1.1 [59.1 kB]


Get:78 http://archive.ubuntu.com/ubuntu jammy/main amd64 libtimedate-perl all 2.3300-2 [34.0 kB]


Get:79 http://archive.ubuntu.com/ubuntu jammy/main amd64 libhttp-date-perl all 6.05-1 [9920 B]


Get:80 http://archive.ubuntu.com/ubuntu jammy/main amd64 libio-html-perl all 1.004-2 [15.4 kB]


Get:81 http://archive.ubuntu.com/ubuntu jammy/main amd64 liblwp-mediatypes-perl all 6.04-1 [19.5 kB]


Get:82 http://archive.ubuntu.com/ubuntu jammy/main amd64 libhttp-message-perl all 6.36-1 [76.8 kB]


Get:83 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libldap-common all 2.5.18+dfsg-0ubuntu0.22.04.2 [15.9 kB]


Get:84 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 libsasl2-modules amd64 2.1.27+dfsg2-3ubuntu1.2 
[68.8 kB]


Get:85 http://archive.ubuntu.com/ubuntu jammy/main amd64 mecab-utils amd64 0.996-14build9 [4850 B]


Get:86 http://archive.ubuntu.com/ubuntu jammy/main amd64 mecab-ipadic all 2.7.0-20070801+main-3 [6718 kB]


Get:87 http://archive.ubuntu.com/ubuntu jammy/main amd64 mecab-ipadic-utf8 all 2.7.0-20070801+main-3 [4384 B]


Get:88 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 mysql-server all 8.0.39-0ubuntu0.22.04.1 [9468 B]


Get:89 http://archive.ubuntu.com/ubuntu jammy-updates/main amd64 php8.1-mysql amd64 8.1.2-1ubuntu2.19 [130 kB]


Get:90 http://archive.ubuntu.com/ubuntu jammy/main amd64 php-mysql all 2:8.1+92ubuntu1 [1834 B]


Get:91 http://archive.ubuntu.com/ubuntu jammy/main amd64 ssl-cert all 1.1.2 [17.4 kB]


Fetched 61.5 MB in 6s (10.6 MB/s)    


debconf: delaying package configuration, since apt-utils is not installed


Selecting previously unselected package perl-modules-5.34.
(Reading database ... 4393 files and directories currently installed.)


Preparing to unpack .../00-perl-modules-5.34_5.34.0-3ubuntu1.3_all.deb ...


Unpacking perl-modules-5.34 (5.34.0-3ubuntu1.3) ...


Selecting previously unselected package libgdbm6:amd64.


Preparing to unpack .../01-libgdbm6_1.23-1_amd64.deb ...


Unpacking libgdbm6:amd64 (1.23-1) ...


Selecting previously unselected package libgdbm-compat4:amd64.


Preparing to unpack .../02-libgdbm-compat4_1.23-1_amd64.deb ...


Unpacking libgdbm-compat4:amd64 (1.23-1) ...


Selecting previously unselected package libperl5.34:amd64.


Preparing to unpack .../03-libperl5.34_5.34.0-3ubuntu1.3_amd64.deb ...


Unpacking libperl5.34:amd64 (5.34.0-3ubuntu1.3) ...


Selecting previously unselected package perl.


Preparing to unpack .../04-perl_5.34.0-3ubuntu1.3_amd64.deb ...


Unpacking perl (5.34.0-3ubuntu1.3) ...


Selecting previously unselected package libapr1:amd64.


Preparing to unpack .../05-libapr1_1.7.0-8ubuntu0.22.04.2_amd64.deb ...


Unpacking libapr1:amd64 (1.7.0-8ubuntu0.22.04.2) ...


Selecting previously unselected package libexpat1:amd64.


Preparing to unpack .../06-libexpat1_2.4.7-1ubuntu0.4_amd64.deb ...


Unpacking libexpat1:amd64 (2.4.7-1ubuntu0.4) ...


Selecting previously unselected package libaprutil1:amd64.


Preparing to unpack .../07-libaprutil1_1.6.1-5ubuntu4.22.04.2_amd64.deb ...


Unpacking libaprutil1:amd64 (1.6.1-5ubuntu4.22.04.2) ...


Selecting previously unselected package libsqlite3-0:amd64.


Preparing to unpack .../08-libsqlite3-0_3.37.2-2ubuntu0.3_amd64.deb ...


Unpacking libsqlite3-0:amd64 (3.37.2-2ubuntu0.3) ...


Selecting previously unselected package libaprutil1-dbd-sqlite3:amd64.


Preparing to unpack .../09-libaprutil1-dbd-sqlite3_1.6.1-5ubuntu4.22.04.2_amd64.deb ...


Unpacking libaprutil1-dbd-sqlite3:amd64 (1.6.1-5ubuntu4.22.04.2) ...


Selecting previously unselected package libsasl2-modules-db:amd64.


Preparing to unpack .../10-libsasl2-modules-db_2.1.27+dfsg2-3ubuntu1.2_amd64.deb ...


Unpacking libsasl2-modules-db:amd64 (2.1.27+dfsg2-3ubuntu1.2) ...


Selecting previously unselected package libsasl2-2:amd64.


Preparing to unpack .../11-libsasl2-2_2.1.27+dfsg2-3ubuntu1.2_amd64.deb ...


Unpacking libsasl2-2:amd64 (2.1.27+dfsg2-3ubuntu1.2) ...


Selecting previously unselected package libldap-2.5-0:amd64.


Preparing to unpack .../12-libldap-2.5-0_2.5.18+dfsg-0ubuntu0.22.04.2_amd64.deb ...


Unpacking libldap-2.5-0:amd64 (2.5.18+dfsg-0ubuntu0.22.04.2) ...


Selecting previously unselected package libaprutil1-ldap:amd64.


Preparing to unpack .../13-libaprutil1-ldap_1.6.1-5ubuntu4.22.04.2_amd64.deb ...


Unpacking libaprutil1-ldap:amd64 (1.6.1-5ubuntu4.22.04.2) ...


Selecting previously unselected package libbrotli1:amd64.


Preparing to unpack .../14-libbrotli1_1.0.9-2build6_amd64.deb ...


Unpacking libbrotli1:amd64 (1.0.9-2build6) ...


Selecting previously unselected package libnghttp2-14:amd64.


Preparing to unpack .../15-libnghttp2-14_1.43.0-1ubuntu0.2_amd64.deb ...


Unpacking libnghttp2-14:amd64 (1.43.0-1ubuntu0.2) ...


Selecting previously unselected package libpsl5:amd64.


Preparing to unpack .../16-libpsl5_0.21.0-1.2build2_amd64.deb ...


Unpacking libpsl5:amd64 (0.21.0-1.2build2) ...


Selecting previously unselected package librtmp1:amd64.


Preparing to unpack .../17-librtmp1_2.4+20151223.gitfa8646d.1-2build4_amd64.deb ...


Unpacking librtmp1:amd64 (2.4+20151223.gitfa8646d.1-2build4) ...


Selecting previously unselected package libssh-4:amd64.


Preparing to unpack .../18-libssh-4_0.9.6-2ubuntu0.22.04.3_amd64.deb ...


Unpacking libssh-4:amd64 (0.9.6-2ubuntu0.22.04.3) ...


Selecting previously unselected package libcurl4:amd64.


Preparing to unpack .../19-libcurl4_7.81.0-1ubuntu1.18_amd64.deb ...


Unpacking libcurl4:amd64 (7.81.0-1ubuntu1.18) ...


Selecting previously unselected package libjansson4:amd64.


Preparing to unpack .../20-libjansson4_2.13.1-1.1build3_amd64.deb ...


Unpacking libjansson4:amd64 (2.13.1-1.1build3) ...


Selecting previously unselected package liblua5.3-0:amd64.


Preparing to unpack .../21-liblua5.3-0_5.3.6-1build1_amd64.deb ...


Unpacking liblua5.3-0:amd64 (5.3.6-1build1) ...

Selecting previously unselected package libicu70:amd64.


Preparing to unpack .../22-libicu70_70.1-2_amd64.deb ...


Unpacking libicu70:amd64 (70.1-2) ...


Selecting previously unselected package libxml2:amd64.


Preparing to unpack .../23-libxml2_2.9.13+dfsg-1ubuntu0.4_amd64.deb ...


Unpacking libxml2:amd64 (2.9.13+dfsg-1ubuntu0.4) ...


Selecting previously unselected package apache2-bin.


Preparing to unpack .../24-apache2-bin_2.4.52-1ubuntu4.12_amd64.deb ...


Unpacking apache2-bin (2.4.52-1ubuntu4.12) ...


Selecting previously unselected package apache2-data.


Preparing to unpack .../25-apache2-data_2.4.52-1ubuntu4.12_all.deb ...


Unpacking apache2-data (2.4.52-1ubuntu4.12) ...


Selecting previously unselected package apache2-utils.


Preparing to unpack .../26-apache2-utils_2.4.52-1ubuntu4.12_amd64.deb ...


Unpacking apache2-utils (2.4.52-1ubuntu4.12) ...


Selecting previously unselected package media-types.


Preparing to unpack .../27-media-types_7.0.0_all.deb ...


Unpacking media-types (7.0.0) ...


Selecting previously unselected package mailcap.


Preparing to unpack .../28-mailcap_3.70+nmu1ubuntu1_all.deb ...


Unpacking mailcap (3.70+nmu1ubuntu1) ...


Selecting previously unselected package mime-support.


Preparing to unpack .../29-mime-support_3.66_all.deb ...


Unpacking mime-support (3.66) ...


Selecting previously unselected package apache2.


Preparing to unpack .../30-apache2_2.4.52-1ubuntu4.12_amd64.deb ...


Unpacking apache2 (2.4.52-1ubuntu4.12) ...


Selecting previously unselected package mysql-common.


Preparing to unpack .../31-mysql-common_5.8+1.0.8_all.deb ...


Unpacking mysql-common (5.8+1.0.8) ...


Selecting previously unselected package libmd0:amd64.


Preparing to unpack .../32-libmd0_1.0.4-1build1_amd64.deb ...


Unpacking libmd0:amd64 (1.0.4-1build1) ...


Selecting previously unselected package libbsd0:amd64.


Preparing to unpack .../33-libbsd0_0.11.5-1_amd64.deb ...


Unpacking libbsd0:amd64 (0.11.5-1) ...


Selecting previously unselected package libedit2:amd64.


Preparing to unpack .../34-libedit2_3.1-20210910-1build1_amd64.deb ...


Unpacking libedit2:amd64 (3.1-20210910-1build1) ...


Selecting previously unselected package mysql-client-core-8.0.


Preparing to unpack .../35-mysql-client-core-8.0_8.0.39-0ubuntu0.22.04.1_amd64.deb ...


Unpacking mysql-client-core-8.0 (8.0.39-0ubuntu0.22.04.1) ...


Selecting previously unselected package mysql-client-8.0.


Preparing to unpack .../36-mysql-client-8.0_8.0.39-0ubuntu0.22.04.1_amd64.deb ...


Unpacking mysql-client-8.0 (8.0.39-0ubuntu0.22.04.1) ...


Selecting previously unselected package libaio1:amd64.


Preparing to unpack .../37-libaio1_0.3.112-13build1_amd64.deb ...


Unpacking libaio1:amd64 (0.3.112-13build1) ...


Selecting previously unselected package libevent-core-2.1-7:amd64.


Preparing to unpack .../38-libevent-core-2.1-7_2.1.12-stable-1build3_amd64.deb ...


Unpacking libevent-core-2.1-7:amd64 (2.1.12-stable-1build3) ...


Selecting previously unselected package libevent-pthreads-2.1-7:amd64.


Preparing to unpack .../39-libevent-pthreads-2.1-7_2.1.12-stable-1build3_amd64.deb ...


Unpacking libevent-pthreads-2.1-7:amd64 (2.1.12-stable-1build3) ...


Selecting previously unselected package libmecab2:amd64.


Preparing to unpack .../40-libmecab2_0.996-14build9_amd64.deb ...


Unpacking libmecab2:amd64 (0.996-14build9) ...


Selecting previously unselected package libnuma1:amd64.


Preparing to unpack .../41-libnuma1_2.0.14-3ubuntu2_amd64.deb ...


Unpacking libnuma1:amd64 (2.0.14-3ubuntu2) ...


Selecting previously unselected package libprotobuf-lite23:amd64.


Preparing to unpack .../42-libprotobuf-lite23_3.12.4-1ubuntu7.22.04.1_amd64.deb ...


Unpacking libprotobuf-lite23:amd64 (3.12.4-1ubuntu7.22.04.1) ...


Selecting previously unselected package mysql-server-core-8.0.


Preparing to unpack .../43-mysql-server-core-8.0_8.0.39-0ubuntu0.22.04.1_amd64.deb ...


Unpacking mysql-server-core-8.0 (8.0.39-0ubuntu0.22.04.1) ...


Selecting previously unselected package psmisc.


Preparing to unpack .../44-psmisc_23.4-2build3_amd64.deb ...


Unpacking psmisc (23.4-2build3) ...


Setting up mysql-common (5.8+1.0.8) ...


update-alternatives: using /etc/mysql/my.cnf.fallback to provide /etc/mysql/my.cnf (my.cnf) in a
uto mode


Selecting previously unselected package mysql-server-8.0.


(Reading database ... 7535 files and directories currently installed.)


Preparing to unpack .../00-mysql-server-8.0_8.0.39-0ubuntu0.22.04.1_amd64.deb ...


debconf: unable to initialize frontend: Dialog


debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use


d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)


debconf: falling back to frontend: Readline


Unpacking mysql-server-8.0 (8.0.39-0ubuntu0.22.04.1) ...


Selecting previously unselected package openssl.


Preparing to unpack .../01-openssl_3.0.2-0ubuntu1.18_amd64.deb ...


Unpacking openssl (3.0.2-0ubuntu1.18) ...


Selecting previously unselected package ca-certificates.


Preparing to unpack .../02-ca-certificates_20240203~22.04.1_all.deb ...


Unpacking ca-certificates (20240203~22.04.1) ...


Selecting previously unselected package libargon2-1:amd64.


Preparing to unpack .../03-libargon2-1_0~20171227-0.3_amd64.deb ...


Unpacking libargon2-1:amd64 (0~20171227-0.3) ...


Selecting previously unselected package netbase.


Preparing to unpack .../04-netbase_6.3_all.deb ...


Unpacking netbase (6.3) ...


Selecting previously unselected package tzdata.


Preparing to unpack .../05-tzdata_2024a-0ubuntu0.22.04.1_all.deb ...


Unpacking tzdata (2024a-0ubuntu0.22.04.1) ...


Selecting previously unselected package ucf.


Preparing to unpack .../06-ucf_3.0043_all.deb ...


Moving old data out of the way


Unpacking ucf (3.0043) ...


Selecting previously unselected package libmagic-mgc.


Preparing to unpack .../07-libmagic-mgc_1%3a5.41-3ubuntu0.1_amd64.deb ...


Unpacking libmagic-mgc (1:5.41-3ubuntu0.1) ...


Selecting previously unselected package libmagic1:amd64.


Preparing to unpack .../08-libmagic1_1%3a5.41-3ubuntu0.1_amd64.deb ...


Unpacking libmagic1:amd64 (1:5.41-3ubuntu0.1) ...


Selecting previously unselected package file.


Preparing to unpack .../09-file_1%3a5.41-3ubuntu0.1_amd64.deb ...


Unpacking file (1:5.41-3ubuntu0.1) ...


Selecting previously unselected package publicsuffix.


Preparing to unpack .../10-publicsuffix_20211207.1025-1_all.deb ...


Unpacking publicsuffix (20211207.1025-1) ...


Selecting previously unselected package xz-utils.


Preparing to unpack .../11-xz-utils_5.2.5-2ubuntu1_amd64.deb ...


Unpacking xz-utils (5.2.5-2ubuntu1) ...


Selecting previously unselected package bzip2.


Preparing to unpack .../12-bzip2_1.0.8-5build1_amd64.deb ...


Unpacking bzip2 (1.0.8-5build1) ...


Selecting previously unselected package php-common.


Preparing to unpack .../13-php-common_2%3a92ubuntu1_all.deb ...


Unpacking php-common (2:92ubuntu1) ...


Selecting previously unselected package php8.1-common.


Preparing to unpack .../14-php8.1-common_8.1.2-1ubuntu2.19_amd64.deb ...


Unpacking php8.1-common (8.1.2-1ubuntu2.19) ...


Selecting previously unselected package php8.1-opcache.


Preparing to unpack .../15-php8.1-opcache_8.1.2-1ubuntu2.19_amd64.deb ...


Unpacking php8.1-opcache (8.1.2-1ubuntu2.19) ...


Selecting previously unselected package php8.1-readline.


Preparing to unpack .../16-php8.1-readline_8.1.2-1ubuntu2.19_amd64.deb ...


Unpacking php8.1-readline (8.1.2-1ubuntu2.19) ...


Selecting previously unselected package libsodium23:amd64.


Preparing to unpack .../17-libsodium23_1.0.18-1build2_amd64.deb ...


Unpacking libsodium23:amd64 (1.0.18-1build2) ...


Selecting previously unselected package php8.1-cli.


Preparing to unpack .../18-php8.1-cli_8.1.2-1ubuntu2.19_amd64.deb ...


Unpacking php8.1-cli (8.1.2-1ubuntu2.19) ...


Selecting previously unselected package libapache2-mod-php8.1.


Preparing to unpack .../19-libapache2-mod-php8.1_8.1.2-1ubuntu2.19_amd64.deb ...


Unpacking libapache2-mod-php8.1 (8.1.2-1ubuntu2.19) ...


Selecting previously unselected package libapache2-mod-php.


Preparing to unpack .../20-libapache2-mod-php_2%3a8.1+92ubuntu1_all.deb ...


Unpacking libapache2-mod-php (2:8.1+92ubuntu1) ...


Selecting previously unselected package libhtml-tagset-perl.


Preparing to unpack .../21-libhtml-tagset-perl_3.20-4_all.deb ...


Unpacking libhtml-tagset-perl (3.20-4) ...


Selecting previously unselected package liburi-perl.


Preparing to unpack .../22-liburi-perl_5.10-1_all.deb ...


Unpacking liburi-perl (5.10-1) ...


Selecting previously unselected package libhtml-parser-perl:amd64.


Preparing to unpack .../23-libhtml-parser-perl_3.76-1build2_amd64.deb ...


Unpacking libhtml-parser-perl:amd64 (3.76-1build2) ...


Selecting previously unselected package libcgi-pm-perl.


Preparing to unpack .../24-libcgi-pm-perl_4.54-1_all.deb ...


Unpacking libcgi-pm-perl (4.54-1) ...


Selecting previously unselected package libfcgi0ldbl:amd64.


Preparing to unpack .../25-libfcgi0ldbl_2.4.2-2build2_amd64.deb ...


Unpacking libfcgi0ldbl:amd64 (2.4.2-2build2) ...


Selecting previously unselected package libfcgi-perl:amd64.


Preparing to unpack .../26-libfcgi-perl_0.82+ds-1build1_amd64.deb ...


Unpacking libfcgi-perl:amd64 (0.82+ds-1build1) ...


Selecting previously unselected package libcgi-fast-perl.


Preparing to unpack .../27-libcgi-fast-perl_1%3a2.15-1_all.deb ...


Unpacking libcgi-fast-perl (1:2.15-1) ...


Selecting previously unselected package libclone-perl.


Preparing to unpack .../28-libclone-perl_0.45-1build3_amd64.deb ...


Unpacking libclone-perl (0.45-1build3) ...


Selecting previously unselected package libencode-locale-perl.


Preparing to unpack .../29-libencode-locale-perl_1.05-1.1_all.deb ...


Unpacking libencode-locale-perl (1.05-1.1) ...


Selecting previously unselected package libfcgi-bin.


Preparing to unpack .../30-libfcgi-bin_2.4.2-2build2_amd64.deb ...


Unpacking libfcgi-bin (2.4.2-2build2) ...


Selecting previously unselected package libhtml-template-perl.


Preparing to unpack .../31-libhtml-template-perl_2.97-1.1_all.deb ...


Unpacking libhtml-template-perl (2.97-1.1) ...


Selecting previously unselected package libtimedate-perl.


Preparing to unpack .../32-libtimedate-perl_2.3300-2_all.deb ...


Unpacking libtimedate-perl (2.3300-2) ...


Selecting previously unselected package libhttp-date-perl.


Preparing to unpack .../33-libhttp-date-perl_6.05-1_all.deb ...


Unpacking libhttp-date-perl (6.05-1) ...


Selecting previously unselected package libio-html-perl.


Preparing to unpack .../34-libio-html-perl_1.004-2_all.deb ...


Unpacking libio-html-perl (1.004-2) ...


Selecting previously unselected package liblwp-mediatypes-perl.


Preparing to unpack .../35-liblwp-mediatypes-perl_6.04-1_all.deb ...


Unpacking liblwp-mediatypes-perl (6.04-1) ...


Selecting previously unselected package libhttp-message-perl.


Preparing to unpack .../36-libhttp-message-perl_6.36-1_all.deb ...


Unpacking libhttp-message-perl (6.36-1) ...


Selecting previously unselected package libldap-common.


Preparing to unpack .../37-libldap-common_2.5.18+dfsg-0ubuntu0.22.04.2_all.deb ...


Unpacking libldap-common (2.5.18+dfsg-0ubuntu0.22.04.2) ...


Selecting previously unselected package libsasl2-modules:amd64.


Preparing to unpack .../38-libsasl2-modules_2.1.27+dfsg2-3ubuntu1.2_amd64.deb ...


Unpacking libsasl2-modules:amd64 (2.1.27+dfsg2-3ubuntu1.2) ...


Selecting previously unselected package mecab-utils.


Preparing to unpack .../39-mecab-utils_0.996-14build9_amd64.deb ...


Unpacking mecab-utils (0.996-14build9) ...


Selecting previously unselected package mecab-ipadic.


Preparing to unpack .../40-mecab-ipadic_2.7.0-20070801+main-3_all.deb ...


Unpacking mecab-ipadic (2.7.0-20070801+main-3) ...


Selecting previously unselected package mecab-ipadic-utf8.


Preparing to unpack .../41-mecab-ipadic-utf8_2.7.0-20070801+main-3_all.deb ...


Unpacking mecab-ipadic-utf8 (2.7.0-20070801+main-3) ...


Selecting previously unselected package mysql-server.


Preparing to unpack .../42-mysql-server_8.0.39-0ubuntu0.22.04.1_all.deb ...


Unpacking mysql-server (8.0.39-0ubuntu0.22.04.1) ...


Selecting previously unselected package php8.1-mysql.


Preparing to unpack .../43-php8.1-mysql_8.1.2-1ubuntu2.19_amd64.deb ...


Unpacking php8.1-mysql (8.1.2-1ubuntu2.19) ...


Selecting previously unselected package php-mysql.


Preparing to unpack .../44-php-mysql_2%3a8.1+92ubuntu1_all.deb ...


Unpacking php-mysql (2:8.1+92ubuntu1) ...


Selecting previously unselected package ssl-cert.


Preparing to unpack .../45-ssl-cert_1.1.2_all.deb ...


Unpacking ssl-cert (1.1.2) ...


Setting up libexpat1:amd64 (2.4.7-1ubuntu0.4) ...


Setting up media-types (7.0.0) ...


Setting up libmecab2:amd64 (0.996-14build9) ...


Setting up libpsl5:amd64 (0.21.0-1.2build2) ...


Setting up libsodium23:amd64 (1.0.18-1build2) ...


Setting up libfcgi0ldbl:amd64 (2.4.2-2build2) ...


Setting up libmagic-mgc (1:5.41-3ubuntu0.1) ...


Setting up psmisc (23.4-2build3) ...


Setting up libargon2-1:amd64 (0~20171227-0.3) ...


Setting up libbrotli1:amd64 (1.0.9-2build6) ...


Setting up libsqlite3-0:amd64 (3.37.2-2ubuntu0.3) ...


Setting up libsasl2-modules:amd64 (2.1.27+dfsg2-3ubuntu1.2) ...


Setting up libfcgi-bin (2.4.2-2build2) ...


Setting up libnghttp2-14:amd64 (1.43.0-1ubuntu0.2) ...


Setting up libmagic1:amd64 (1:5.41-3ubuntu0.1) ...


Setting up libapr1:amd64 (1.7.0-8ubuntu0.22.04.2) ...


Setting up file (1:5.41-3ubuntu0.1) ...


Setting up perl-modules-5.34 (5.34.0-3ubuntu1.3) ...


Setting up bzip2 (1.0.8-5build1) ...


Setting up libldap-common (2.5.18+dfsg-0ubuntu0.22.04.2) ...


Setting up libjansson4:amd64 (2.13.1-1.1build3) ...


Setting up libsasl2-modules-db:amd64 (2.1.27+dfsg2-3ubuntu1.2) ...


Setting up tzdata (2024a-0ubuntu0.22.04.1) ...


debconf: unable to initialize frontend: Dialog


debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use


d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)


debconf: falling back to frontend: Readline


Configuring tzdata
- - - - - - - - - - - - -  - - - - -

Please select the geographic area in which you live. Subsequent configuration questions will
narrow this down by presenting a list of cities, representing the time zones in which they are
located.


  1. Africa   3. Antarctica  5. Arctic  7. Atlantic  9. Indian    11. US
  2. America  4. Australia   6. Asia    8. Europe    10. Pacific  12. Etc


Geographic area: 8



Please select the city or region corresponding to your time zone.


  1. Amsterdam   14. Copenhagen   27. London      40. Riga        53. Ulyanovsk
  2. Andorra     15. Dublin       28. Luxembourg  41. Rome        54. Uzhgorod
  3. Astrakhan   16. Gibraltar    29. Madrid      42. Samara      55. Vaduz
  4. Athens      17. Guernsey     30. Malta       43. San_Marino  56. Vatican
  5. Belfast     18. Helsinki     31. Mariehamn   44. Sarajevo    57. Vienna
  6. Belgrade    19. Isle_of_Man  32. Minsk       45. Saratov     58. Vilnius
  7. Berlin      20. Istanbul     33. Monaco      46. Simferopol  59. Volgograd
  8. Bratislava  21. Jersey       34. Moscow      47. Skopje      60. Warsaw
  9. Brussels    22. Kaliningrad  35. Nicosia     48. Sofia       61. Zagreb
  10. Bucharest  23. Kirov        36. Oslo        49. Stockholm   62. Zaporozhye
  11. Budapest   24. Kyiv         37. Paris       50. Tallinn     63. Zurich
  12. Busingen   25. Lisbon       38. Podgorica   51. Tirane
  13. Chisinau   26. Ljubljana    39. Prague      52. Tiraspol


Time zone: 29


Current default time zone: 'Europe/Madrid'


Local time is now:      Fri Oct 25 19:45:32 CEST 2024.


Universal Time is now:  Fri Oct 25 17:45:32 UTC 2024.


Run 'dpkg-reconfigure tzdata' if you wish to change it.




Setting up libprotobuf-lite23:amd64 (3.12.4-1ubuntu7.22.04.1) ...


Setting up librtmp1:amd64 (2.4+20151223.gitfa8646d.1-2build4) ...


Setting up xz-utils (5.2.5-2ubuntu1) ...


update-alternatives: using /usr/bin/xz to provide /usr/bin/lzma (lzma) in auto mode


update-alternatives: warning: skip creation of /usr/share/man/man1/lzma.1.gz because associated 


file /usr/share/man/man1/xz.1.gz (of link group lzma) doesn't exist


update-alternatives: warning: skip creation of /usr/share/man/man1/unlzma.1.gz because associate


d file /usr/share/man/man1/unxz.1.gz (of link group lzma) doesn't exist


update-alternatives: warning: skip creation of /usr/share/man/man1/lzcat.1.gz because associated

 
 file /usr/share/man/man1/xzcat.1.gz (of link group lzma) doesn't exist


update-alternatives: warning: skip creation of /usr/share/man/man1/lzmore.1.gz because associate


d file /usr/share/man/man1/xzmore.1.gz (of link group lzma) doesn't exist


update-alternatives: warning: skip creation of /usr/share/man/man1/lzless.1.gz because associate


d file /usr/share/man/man1/xzless.1.gz (of link group lzma) doesn't exist


update-alternatives: warning: skip creation of /usr/share/man/man1/lzdiff.1.gz because associate


d file /usr/share/man/man1/xzdiff.1.gz (of link group lzma) doesn't exist


update-alternatives: warning: skip creation of /usr/share/man/man1/lzcmp.1.gz because associated

 
 file /usr/share/man/man1/xzcmp.1.gz (of link group lzma) doesn't exist


update-alternatives: warning: skip creation of /usr/share/man/man1/lzgrep.1.gz because associate


d file /usr/share/man/man1/xzgrep.1.gz (of link group lzma) doesn't exist


update-alternatives: warning: skip creation of /usr/share/man/man1/lzegrep.1.gz because associat


ed file /usr/share/man/man1/xzegrep.1.gz (of link group lzma) doesn't exist


update-alternatives: warning: skip creation of /usr/share/man/man1/lzfgrep.1.gz because associat


ed file /usr/share/man/man1/xzfgrep.1.gz (of link group lzma) doesn't exist


Setting up mecab-utils (0.996-14build9) ...


Setting up libevent-core-2.1-7:amd64 (2.1.12-stable-1build3) ...


Setting up ucf (3.0043) ...


debconf: unable to initialize frontend: Dialog


debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use


d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)


debconf: falling back to frontend: Readline


Setting up libsasl2-2:amd64 (2.1.27+dfsg2-3ubuntu1.2) ...


Setting up libssh-4:amd64 (0.9.6-2ubuntu0.22.04.3) ...


Setting up libnuma1:amd64 (2.0.14-3ubuntu2) ...


Setting up libmd0:amd64 (1.0.4-1build1) ...


Setting up liblua5.3-0:amd64 (5.3.6-1build1) ...


Setting up netbase (6.3) ...


Setting up apache2-data (2.4.52-1ubuntu4.12) ...


Setting up libaio1:amd64 (0.3.112-13build1) ...


Setting up openssl (3.0.2-0ubuntu1.18) ...


Setting up libbsd0:amd64 (0.11.5-1) ...


Setting up publicsuffix (20211207.1025-1) ...


Setting up libgdbm6:amd64 (1.23-1) ...


Setting up libicu70:amd64 (70.1-2) ...


Setting up libevent-pthreads-2.1-7:amd64 (2.1.12-stable-1build3) ...


Setting up libaprutil1:amd64 (1.6.1-5ubuntu4.22.04.2) ...


Setting up php-common (2:92ubuntu1) ...


Setting up mecab-ipadic (2.7.0-20070801+main-3) ...


Compiling IPA dictionary for Mecab.  This takes long time...


reading /usr/share/mecab/dic/ipadic/unk.def ... 40


emitting double-array: 100% |###########################################| 


/usr/share/mecab/dic/ipadic/model.def is not found. skipped.


reading /usr/share/mecab/dic/ipadic/Adnominal.csv ... 135


reading /usr/share/mecab/dic/ipadic/Noun.place.csv ... 72999


reading /usr/share/mecab/dic/ipadic/Noun.demonst.csv ... 120


reading /usr/share/mecab/dic/ipadic/Noun.number.csv ... 42


reading /usr/share/mecab/dic/ipadic/Noun.others.csv ... 151


reading /usr/share/mecab/dic/ipadic/Symbol.csv ... 208


reading /usr/share/mecab/dic/ipadic/Noun.adverbal.csv ... 795


reading /usr/share/mecab/dic/ipadic/Postp-col.csv ... 91


reading /usr/share/mecab/dic/ipadic/Conjunction.csv ... 171


reading /usr/share/mecab/dic/ipadic/Prefix.csv ... 221


reading /usr/share/mecab/dic/ipadic/Adverb.csv ... 3032


reading /usr/share/mecab/dic/ipadic/Noun.org.csv ... 16668


reading /usr/share/mecab/dic/ipadic/Others.csv ... 2


reading /usr/share/mecab/dic/ipadic/Adj.csv ... 27210


reading /usr/share/mecab/dic/ipadic/Auxil.csv ... 199


reading /usr/share/mecab/dic/ipadic/Noun.verbal.csv ... 12146


reading /usr/share/mecab/dic/ipadic/Interjection.csv ... 252


reading /usr/share/mecab/dic/ipadic/Filler.csv ... 19


reading /usr/share/mecab/dic/ipadic/Noun.name.csv ... 34202


reading /usr/share/mecab/dic/ipadic/Noun.adjv.csv ... 3328


reading /usr/share/mecab/dic/ipadic/Noun.nai.csv ... 42


reading /usr/share/mecab/dic/ipadic/Postp.csv ... 146


reading /usr/share/mecab/dic/ipadic/Noun.csv ... 60477


reading /usr/share/mecab/dic/ipadic/Verb.csv ... 130750


reading /usr/share/mecab/dic/ipadic/Suffix.csv ... 1393


reading /usr/share/mecab/dic/ipadic/Noun.proper.csv ... 27328


emitting double-array: 100% |###########################################| 


reading /usr/share/mecab/dic/ipadic/matrix.def ... 1316x1316


emitting matrix      : 100% |###########################################| 




done!


update-alternatives: using /var/lib/mecab/dic/ipadic to provide /var/lib/mecab/dic/debian (mecab
-dictionary) in auto mode


Setting up php8.1-common (8.1.2-1ubuntu2.19) ...


debconf: unable to initialize frontend: Dialog


debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use


d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)


debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/calendar.ini with new version


debconf: unable to initialize frontend: Dialog


debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use


d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)


debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/ctype.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline





Creating config file /etc/php/8.1/mods-available/exif.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/fileinfo.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/ffi.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/ftp.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/gettext.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/iconv.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/pdo.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/phar.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/posix.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/shmop.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/sockets.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/sysvmsg.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/sysvsem.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/sysvshm.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/tokenizer.ini with new version
Setting up libedit2:amd64 (3.1-20210910-1build1) ...
Setting up libaprutil1-dbd-sqlite3:amd64 (1.6.1-5ubuntu4.22.04.2) ...
Setting up libldap-2.5-0:amd64 (2.5.18+dfsg-0ubuntu0.22.04.2) ...
Setting up ca-certificates (20240203~22.04.1) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline
Updating certificates in /etc/ssl/certs...
146 added, 0 removed; done.
Setting up php8.1-mysql (8.1.2-1ubuntu2.19) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/mysqlnd.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/mysqli.ini with new version
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/pdo_mysql.ini with new version
Setting up ssl-cert (1.1.2) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline
Setting up mysql-server-core-8.0 (8.0.39-0ubuntu0.22.04.1) ...
Setting up libgdbm-compat4:amd64 (1.23-1) ...
Setting up mecab-ipadic-utf8 (2.7.0-20070801+main-3) ...
Compiling IPA dictionary for Mecab.  This takes long time...
reading /usr/share/mecab/dic/ipadic/unk.def ... 40
emitting double-array: 100% |###########################################| 
/usr/share/mecab/dic/ipadic/model.def is not found. skipped.
reading /usr/share/mecab/dic/ipadic/Adnominal.csv ... 135
reading /usr/share/mecab/dic/ipadic/Noun.place.csv ... 72999
reading /usr/share/mecab/dic/ipadic/Noun.demonst.csv ... 120
reading /usr/share/mecab/dic/ipadic/Noun.number.csv ... 42
reading /usr/share/mecab/dic/ipadic/Noun.others.csv ... 151
reading /usr/share/mecab/dic/ipadic/Symbol.csv ... 208
reading /usr/share/mecab/dic/ipadic/Noun.adverbal.csv ... 795
reading /usr/share/mecab/dic/ipadic/Postp-col.csv ... 91
reading /usr/share/mecab/dic/ipadic/Conjunction.csv ... 171
reading /usr/share/mecab/dic/ipadic/Prefix.csv ... 221
reading /usr/share/mecab/dic/ipadic/Adverb.csv ... 3032
reading /usr/share/mecab/dic/ipadic/Noun.org.csv ... 16668
reading /usr/share/mecab/dic/ipadic/Others.csv ... 2
reading /usr/share/mecab/dic/ipadic/Adj.csv ... 27210
reading /usr/share/mecab/dic/ipadic/Auxil.csv ... 199
reading /usr/share/mecab/dic/ipadic/Noun.verbal.csv ... 12146
reading /usr/share/mecab/dic/ipadic/Interjection.csv ... 252
reading /usr/share/mecab/dic/ipadic/Filler.csv ... 19
reading /usr/share/mecab/dic/ipadic/Noun.name.csv ... 34202
reading /usr/share/mecab/dic/ipadic/Noun.adjv.csv ... 3328
reading /usr/share/mecab/dic/ipadic/Noun.nai.csv ... 42
reading /usr/share/mecab/dic/ipadic/Postp.csv ... 146
reading /usr/share/mecab/dic/ipadic/Noun.csv ... 60477
reading /usr/share/mecab/dic/ipadic/Verb.csv ... 130750
reading /usr/share/mecab/dic/ipadic/Suffix.csv ... 1393
reading /usr/share/mecab/dic/ipadic/Noun.proper.csv ... 27328
emitting double-array: 100% |###########################################| 
reading /usr/share/mecab/dic/ipadic/matrix.def ... 1316x1316
emitting matrix      : 100% |###########################################| 




done!


update-alternatives: using /var/lib/mecab/dic/ipadic-utf8 to provide /var/lib/mecab/dic/debian (
mecab-dictionary) in auto mode


Setting up libcurl4:amd64 (7.81.0-1ubuntu1.18) ...


Setting up php8.1-readline (8.1.2-1ubuntu2.19) ...


debconf: unable to initialize frontend: Dialog


debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use


d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)


debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/readline.ini with new version
Setting up libxml2:amd64 (2.9.13+dfsg-1ubuntu0.4) ...
Setting up php8.1-opcache (8.1.2-1ubuntu2.19) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/mods-available/opcache.ini with new version
Setting up apache2-utils (2.4.52-1ubuntu4.12) ...
Setting up mysql-client-core-8.0 (8.0.39-0ubuntu0.22.04.1) ...
Setting up libperl5.34:amd64 (5.34.0-3ubuntu1.3) ...
Setting up php-mysql (2:8.1+92ubuntu1) ...
Setting up libaprutil1-ldap:amd64 (1.6.1-5ubuntu4.22.04.2) ...
Setting up perl (5.34.0-3ubuntu1.3) ...
Setting up libio-html-perl (1.004-2) ...
Setting up libtimedate-perl (2.3300-2) ...
Setting up mysql-client-8.0 (8.0.39-0ubuntu0.22.04.1) ...
Setting up libfcgi-perl:amd64 (0.82+ds-1build1) ...
Setting up mailcap (3.70+nmu1ubuntu1) ...
Setting up liburi-perl (5.10-1) ...
Setting up mysql-server-8.0 (8.0.39-0ubuntu0.22.04.1) ...


debconf: unable to initialize frontend: Dialog


debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use


d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)


debconf: falling back to frontend: Readline


invoke-rc.d: could not determine current runlevel


invoke-rc.d: policy-rc.d denied execution of stop.
update-alternatives: using /etc/mysql/mysql.cnf to provide /etc/mysql/my.cnf (my.cnf) in auto mo
de


Renaming removed key_buffer and myisam-recover options (if present)


Cannot stat file /proc/217/fd/0: Permission denied


Cannot stat file /proc/217/fd/1: Permission denied


Cannot stat file /proc/217/fd/2: Permission denied


Cannot stat file /proc/217/fd/3: Permission denied


Cannot stat file /proc/217/fd/4: Permission denied


Cannot stat file /proc/217/fd/5: Permission denied


Cannot stat file /proc/217/fd/6: Permission denied


Cannot stat file /proc/217/fd/7: Permission denied


Cannot stat file /proc/217/fd/8: Permission denied


Cannot stat file /proc/217/fd/9: Permission denied


Cannot stat file /proc/217/fd/10: Permission denied


Cannot stat file /proc/217/fd/11: Permission denied


Cannot stat file /proc/217/fd/12: Permission denied


Cannot stat file /proc/217/fd/13: Permission denied


Cannot stat file /proc/217/fd/14: Permission denied


Cannot stat file /proc/217/fd/15: Permission denied


Cannot stat file /proc/217/fd/16: Permission denied


Cannot stat file /proc/217/fd/17: Permission denied


Cannot stat file /proc/217/fd/18: Permission denied


Cannot stat file /proc/217/fd/19: Permission denied


Cannot stat file /proc/217/fd/20: Permission denied


Cannot stat file /proc/217/fd/21: Permission denied


Cannot stat file /proc/217/fd/22: Permission denied


Cannot stat file /proc/217/fd/23: Permission denied


Cannot stat file /proc/217/fd/24: Permission denied


Cannot stat file /proc/217/fd/25: Permission denied


mysqld will log errors to /var/log/mysql/error.log


mysqld is running as pid 8383


invoke-rc.d: could not determine current runlevel


invoke-rc.d: policy-rc.d denied execution of start.


Setting up libhttp-date-perl (6.05-1) ...


Setting up mime-support (3.66) ...


Setting up libclone-perl (0.45-1build3) ...


Setting up libhtml-tagset-perl (3.20-4) ...


Setting up liblwp-mediatypes-perl (6.04-1) ...


Setting up libencode-locale-perl (1.05-1.1) ...


Setting up apache2-bin (2.4.52-1ubuntu4.12) ...


Setting up php8.1-cli (8.1.2-1ubuntu2.19) ...


update-alternatives: using /usr/bin/php8.1 to provide /usr/bin/php (php) in auto mode


update-alternatives: warning: skip creation of /usr/share/man/man1/php.1.gz because associated f


ile /usr/share/man/man1/php8.1.1.gz (of link group php) doesn't exist


update-alternatives: using /usr/bin/phar8.1 to provide /usr/bin/phar (phar) in auto mode


update-alternatives: warning: skip creation of /usr/share/man/man1/phar.1.gz because associated 


file /usr/share/man/man1/phar8.1.1.gz (of link group phar) doesn't exist


update-alternatives: using /usr/bin/phar.phar8.1 to provide /usr/bin/phar.phar (phar.phar) in au
to mode


update-alternatives: warning: skip creation of /usr/share/man/man1/phar.phar.1.gz because associ


ated file /usr/share/man/man1/phar.phar8.1.1.gz (of link group phar.phar) doesn't exist


debconf: unable to initialize frontend: Dialog


debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use


d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)


debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/cli/php.ini with new version
Setting up libhtml-parser-perl:amd64 (3.76-1build2) ...
Setting up libapache2-mod-php8.1 (8.1.2-1ubuntu2.19) ...
Package apache2 is not configured yet. Will defer actions by package libapache2-mod-php8.1.
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be use
d. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline




Creating config file /etc/php/8.1/apache2/php.ini with new version
No module matches 
Setting up libhttp-message-perl (6.36-1) ...
Setting up mysql-server (8.0.39-0ubuntu0.22.04.1) ...
Setting up apache2 (2.4.52-1ubuntu4.12) ...


Enabling module mpm_event.


Enabling module authz_core.


Enabling module authz_host.


Enabling module authn_core.


Enabling module auth_basic.


Enabling module access_compat.


Enabling module authn_file.


Enabling module authz_user.


Enabling module alias.


Enabling module dir.


Enabling module autoindex.


Enabling module env.


Enabling module mime.


Enabling module negotiation.


Enabling module setenvif.


Enabling module filter.


Enabling module deflate.


Enabling module status.


Enabling module reqtimeout.


Enabling conf charset.


Enabling conf localized-error-pages.


Enabling conf other-vhosts-access-log.


Enabling conf security.


Enabling conf serve-cgi-bin.


Enabling site 000-default.


info: Switch to mpm prefork for package libapache2-mod-php8.1


Module mpm_event disabled.


Enabling module mpm_prefork.


info: Executing deferred 'a2enmod php8.1' for package libapache2-mod-php8.1


Enabling module php8.1.


invoke-rc.d: could not determine current runlevel


invoke-rc.d: policy-rc.d denied execution of start.


Setting up libcgi-pm-perl (4.54-1) ...


Setting up libhtml-template-perl (2.97-1.1) ...


Setting up libapache2-mod-php (2:8.1+92ubuntu1) ...


Setting up libcgi-fast-perl (1:2.15-1) ...


Processing triggers for libc-bin (2.35-0ubuntu3.8) ...


Processing triggers for ca-certificates (20240203~22.04.1) ...


Updating certificates in /etc/ssl/certs...


0 added, 0 removed; done.


Running hooks in /etc/ca-certificates/update.d...


done.


Processing triggers for php8.1-cli (8.1.2-1ubuntu2.19) ...


Processing triggers for libapache2-mod-php8.1 (8.1.2-1ubuntu2.19) ...
</details>

Iniciar MySql:
```bash
service mysql start
```
Salida:

Starting MySQL database server mysqld  

Asegurar la instalacion de MySQL:
```bash
mysql_secure_installation
```
<details>
<summary>Salida:</summary>
<br>


Securing the MySQL server deployment.

Connecting to MySQL using a blank password.

VALIDATE PASSWORD COMPONENT can be used to test passwords
and improve security. It checks the strength of password
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD component?

Press y|Y for Yes, any other key for No: Y

There are three levels of password validation policy:

LOW    Length >= 8
MEDIUM Length >= 8, numeric, mixed case, and special characters
STRONG Length >= 8, numeric, mixed case, special characters and dictionary                  file

Please enter 0 = LOW, 1 = MEDIUM and 2 = STRONG: 2

Skipping password set for root as authentication with auth_socket is used by default.
If you would like to use password authentication instead, this can be done with the "ALTER_USER" command.
See https://dev.mysql.com/doc/refman/8.0/en/alter-user.html#alter-user-password-management for more information.

By default, a MySQL installation has an anonymous user,
allowing anyone to log into MySQL without having to have
a user account created for them. This is intended only for
testing, and to make the installation go a bit smoother.
You should remove them before moving into a production
environment.

Remove anonymous users? (Press y|Y for Yes, any other key for No) : Y
Success.


Normally, root should only be allowed to connect from
'localhost'. This ensures that someone cannot guess at
the root password from the network.

Disallow root login remotely? (Press y|Y for Yes, any other key for No) : Y
Success.

By default, MySQL comes with a database named 'test' that
anyone can access. This is also intended only for testing,
and should be removed before moving into a production
environment.


Remove test database and access to it? (Press y|Y for Yes, any other key for No) : Y
 - Dropping test database...
Success.

 - Removing privileges on test database...
Success.

Reloading the privilege tables will ensure that all changes
made so far will take effect immediately.

Reload privilege tables now? (Press y|Y for Yes, any other key for No) : Y
Success.

All done! 
</details>

Iniciar MySQL:
```bash
mysql -u root -p
```
Salida:

Enter password: (darle a enter ya que no hay contraseña)

Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 12
Server version: 8.0.39-0ubuntu0.22.04.1 (Ubuntu)

Copyright (c) 2000, 2024, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

Ya en MySQL poner los siguientes comandos:
```bash
use mysql;
```
Salida:

Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
```bash
update user set plugin='mysql_native_password' where user='root';
```
Salida:

Query OK, 1 row affected (0.00 sec)
Rows matched: 1  Changed: 1  Warnings: 0
```bash
flush privileges;
```
Salida:

Query OK, 0 rows affected (0.01 sec)
```bash
quit;
```
Salida:

Bye

Iniciamos Apache2:
```bash
service apache2 start
```
Salida:

Starting Apache httpd web server apache2 

Para probar el PHP, colocaremos un archivo PHP en la raíz del documento por defecto de Apache:
```bash
echo "<?php phpinfo(); ?>" | tee /var/www/html/info.php
```
Comprobacion:

![SXEtarea4](SXEtarea4.PNG)

# 2. Utiliza esta guía para instalar wordpress en el contenedor.

Cree el directorio de instalación y descargue el archivo de WordPress.org:
```bash
mkdir -p /srv/www
chown www-data: /srv/www
curl -O https://wordpress.org/latest.tar.gz
tar -zxvf latest.tar.gz -C /srv/www
```
<details>
<summary>Salida:</summary>
<br>

  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 23.4M  100 23.4M    0     0  4921k      0  0:00:04  0:00:04 --:--:-- 5525k
 wordpress/
wordpress/xmlrpc.php
wordpress/wp-blog-header.php
wordpress/readme.html
wordpress/wp-signup.php
wordpress/index.php
wordpress/wp-cron.php
wordpress/wp-config-sample.php
wordpress/wp-login.php
wordpress/wp-settings.php
wordpress/license.txt
wordpress/wp-content/
wordpress/wp-content/themes/
wordpress/wp-content/themes/twentytwentythree/
wordpress/wp-content/themes/twentytwentythree/theme.json
wordpress/wp-content/themes/twentytwentythree/parts/
wordpress/wp-content/themes/twentytwentythree/parts/footer.html
wordpress/wp-content/themes/twentytwentythree/parts/comments.html
wordpress/wp-content/themes/twentytwentythree/parts/header.html
wordpress/wp-content/themes/twentytwentythree/parts/post-meta.html
wordpress/wp-content/themes/twentytwentythree/patterns/
wordpress/wp-content/themes/twentytwentythree/patterns/hidden-404.php
wordpress/wp-content/themes/twentytwentythree/patterns/post-meta.php
wordpress/wp-content/themes/twentytwentythree/patterns/hidden-no-results.php
wordpress/wp-content/themes/twentytwentythree/patterns/call-to-action.php
wordpress/wp-content/themes/twentytwentythree/patterns/footer-default.php
wordpress/wp-content/themes/twentytwentythree/patterns/hidden-comments.php
wordpress/wp-content/themes/twentytwentythree/styles/
wordpress/wp-content/themes/twentytwentythree/styles/sherbet.json
wordpress/wp-content/themes/twentytwentythree/styles/grapes.json
wordpress/wp-content/themes/twentytwentythree/styles/canary.json
wordpress/wp-content/themes/twentytwentythree/styles/electric.json
wordpress/wp-content/themes/twentytwentythree/styles/pitch.json
wordpress/wp-content/themes/twentytwentythree/styles/block-out.json
wordpress/wp-content/themes/twentytwentythree/styles/whisper.json
wordpress/wp-content/themes/twentytwentythree/styles/marigold.json
wordpress/wp-content/themes/twentytwentythree/styles/aubergine.json
wordpress/wp-content/themes/twentytwentythree/styles/pilgrimage.json
wordpress/wp-content/themes/twentytwentythree/assets/
wordpress/wp-content/themes/twentytwentythree/assets/fonts/
wordpress/wp-content/themes/twentytwentythree/assets/fonts/source-serif-pro/
wordpress/wp-content/themes/twentytwentythree/assets/fonts/source-serif-pro/SourceSerif4Variable-Roman.ttf.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/source-serif-pro/SourceSerif4Variable-Italic.otf.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/source-serif-pro/SourceSerif4Variable-Italic.ttf.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/source-serif-pro/SourceSerif4Variable-Roman.otf.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/source-serif-pro/LICENSE.md
wordpress/wp-content/themes/twentytwentythree/assets/fonts/ibm-plex-mono/
wordpress/wp-content/themes/twentytwentythree/assets/fonts/ibm-plex-mono/IBMPlexMono-Italic.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/ibm-plex-mono/IBMPlexMono-Regular.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/ibm-plex-mono/OFL.txt
wordpress/wp-content/themes/twentytwentythree/assets/fonts/ibm-plex-mono/IBMPlexMono-Light.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/ibm-plex-mono/IBMPlexMono-Bold.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/inter/
wordpress/wp-content/themes/twentytwentythree/assets/fonts/inter/LICENSE.txt
wordpress/wp-content/themes/twentytwentythree/assets/fonts/inter/Inter-VariableFont_slnt,wght.ttf
wordpress/wp-content/themes/twentytwentythree/assets/fonts/dm-sans/
wordpress/wp-content/themes/twentytwentythree/assets/fonts/dm-sans/DMSans-Regular-Italic.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/dm-sans/DMSans-Bold.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/dm-sans/LICENSE.txt
wordpress/wp-content/themes/twentytwentythree/assets/fonts/dm-sans/DMSans-Bold-Italic.woff2
wordpress/wp-content/themes/twentytwentythree/assets/fonts/dm-sans/DMSans-Regular.woff2
wordpress/wp-content/themes/twentytwentythree/screenshot.png
wordpress/wp-content/themes/twentytwentythree/readme.txt
wordpress/wp-content/themes/twentytwentythree/templates/
wordpress/wp-content/themes/twentytwentythree/templates/blank.html
wordpress/wp-content/themes/twentytwentythree/templates/page.html
wordpress/wp-content/themes/twentytwentythree/templates/index.html
wordpress/wp-content/themes/twentytwentythree/templates/blog-alternative.html
wordpress/wp-content/themes/twentytwentythree/templates/archive.html
wordpress/wp-content/themes/twentytwentythree/templates/search.html
wordpress/wp-content/themes/twentytwentythree/templates/single.html
wordpress/wp-content/themes/twentytwentythree/templates/404.html
wordpress/wp-content/themes/twentytwentythree/templates/home.html
wordpress/wp-content/themes/twentytwentythree/style.css
wordpress/wp-content/themes/twentytwentytwo/
wordpress/wp-content/themes/twentytwentytwo/theme.json
wordpress/wp-content/themes/twentytwentytwo/inc/
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/hidden-404.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-text-only-with-tagline-black-background.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-layout-two-columns.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-wide-image-intro-buttons.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-logo-navigation-social-black-background.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/query-simple-blog.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-social-copyright.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-logo-navigation-offset-tagline.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-navigation.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/query-large-titles.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-sidebar-blog-posts.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/query-image-grid.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/query-grid.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-about-media-left.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-small-dark.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-with-tagline.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-sidebar-poster.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-featured-posts.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-query-title-citation.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-list-events.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-subscribe.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-image-with-caption.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-sidebar-grid-posts.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-about-links.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-centered-logo.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-video-header-details.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-text-only-salmon-background.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-title-navigation-social.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-dark.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-text-only-green-background.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-default.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-video-trailer.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-query-images-title-citation.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-about-links-dark.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/hidden-bird.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-layout-image-and-text.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-large-dark.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-about-large-image-and-buttons.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-pricing-table.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-about-media-right.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-layered-images-with-duotone.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-logo-navigation-gray-background.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-title-tagline-social.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-centered-title-navigation-social.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-divider-dark.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-about-simple-dark.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/query-default.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-two-images-text.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/query-text-grid.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-stacked.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-about-title-logo.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-default.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-about-solid-color.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/query-irregular-grid.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-blog.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-large-list-names.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-title-and-button.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/hidden-heading-and-bird.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-centered-logo-black-background.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-navigation-copyright.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-image-background-overlay.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-sidebar-blog-posts-right.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/general-divider-light.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/footer-logo.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/page-layout-image-text-and-video.php
wordpress/wp-content/themes/twentytwentytwo/inc/patterns/header-image-background.php
wordpress/wp-content/themes/twentytwentytwo/inc/block-patterns.php
wordpress/wp-content/themes/twentytwentytwo/parts/
wordpress/wp-content/themes/twentytwentytwo/parts/header-small-dark.html
wordpress/wp-content/themes/twentytwentytwo/parts/header-large-dark.html
wordpress/wp-content/themes/twentytwentytwo/parts/footer.html
wordpress/wp-content/themes/twentytwentytwo/parts/header.html
wordpress/wp-content/themes/twentytwentytwo/styles/
wordpress/wp-content/themes/twentytwentytwo/styles/swiss.json
wordpress/wp-content/themes/twentytwentytwo/styles/blue.json
wordpress/wp-content/themes/twentytwentytwo/styles/pink.json
wordpress/wp-content/themes/twentytwentytwo/assets/
wordpress/wp-content/themes/twentytwentytwo/assets/images/
wordpress/wp-content/themes/twentytwentytwo/assets/images/divider-white.png
wordpress/wp-content/themes/twentytwentytwo/assets/images/flight-path-on-gray-a.jpg
wordpress/wp-content/themes/twentytwentytwo/assets/images/bird-on-gray.jpg
wordpress/wp-content/themes/twentytwentytwo/assets/images/flight-path-on-transparent-d.png
wordpress/wp-content/themes/twentytwentytwo/assets/images/icon-bird.jpg
wordpress/wp-content/themes/twentytwentytwo/assets/images/flight-path-on-gray-c.jpg
wordpress/wp-content/themes/twentytwentytwo/assets/images/flight-path-on-transparent-b.png
wordpress/wp-content/themes/twentytwentytwo/assets/images/flight-path-on-transparent-a.png
wordpress/wp-content/themes/twentytwentytwo/assets/images/bird-on-green.jpg
wordpress/wp-content/themes/twentytwentytwo/assets/images/flight-path-on-gray-b.jpg
wordpress/wp-content/themes/twentytwentytwo/assets/images/bird-on-salmon.jpg
wordpress/wp-content/themes/twentytwentytwo/assets/images/flight-path-on-salmon.jpg
wordpress/wp-content/themes/twentytwentytwo/assets/images/divider-black.png
wordpress/wp-content/themes/twentytwentytwo/assets/images/ducks.jpg
wordpress/wp-content/themes/twentytwentytwo/assets/images/icon-binoculars.png
wordpress/wp-content/themes/twentytwentytwo/assets/images/flight-path-on-transparent-c.png
wordpress/wp-content/themes/twentytwentytwo/assets/images/bird-on-black.jpg
wordpress/wp-content/themes/twentytwentytwo/assets/videos/
wordpress/wp-content/themes/twentytwentytwo/assets/videos/birds.mp4
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/SourceSerif4Variable-Roman.ttf.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/SourceSerif4Variable-Italic.otf.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/SourceSerif4Variable-Italic.ttf.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/source-serif-pro/
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/source-serif-pro/SourceSerif4Variable-Roman.ttf.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/source-serif-pro/SourceSerif4Variable-Italic.otf.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/source-serif-pro/SourceSerif4Variable-Italic.ttf.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/source-serif-pro/SourceSerif4Variable-Roman.otf.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/source-serif-pro/LICENSE.md
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/ibm-plex/
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/ibm-plex/IBMPlexSans-ExtraLightItalic.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/ibm-plex/IBMPlexSans-LightItalic.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/ibm-plex/IBMPlexSans-Light.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/ibm-plex/IBMPlexMono-BoldItalic.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/ibm-plex/IBMPlexMono-TextItalic.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/ibm-plex/IBMPlexMono-Text.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/ibm-plex/LICENSE.txt
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/ibm-plex/IBMPlexMono-Bold.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/ibm-plex/IBMPlexSans-ExtraLight.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/SourceSerif4Variable-Roman.otf.woff2
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/inter/
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/inter/Inter.ttf
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/inter/LICENSE.txt
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/dm-sans/
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/dm-sans/DMSans-BoldItalic.ttf
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/dm-sans/DMSans-Bold.ttf
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/dm-sans/DMSans-Italic.ttf
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/dm-sans/DMSans-Regular.ttf
wordpress/wp-content/themes/twentytwentytwo/assets/fonts/dm-sans/LICENSE.txt
wordpress/wp-content/themes/twentytwentytwo/screenshot.png
wordpress/wp-content/themes/twentytwentytwo/index.php
wordpress/wp-content/themes/twentytwentytwo/functions.php
wordpress/wp-content/themes/twentytwentytwo/readme.txt
wordpress/wp-content/themes/twentytwentytwo/templates/
wordpress/wp-content/themes/twentytwentytwo/templates/blank.html
wordpress/wp-content/themes/twentytwentytwo/templates/page-no-separators.html
wordpress/wp-content/themes/twentytwentytwo/templates/page.html
wordpress/wp-content/themes/twentytwentytwo/templates/index.html
wordpress/wp-content/themes/twentytwentytwo/templates/single-no-separators.html
wordpress/wp-content/themes/twentytwentytwo/templates/archive.html
wordpress/wp-content/themes/twentytwentytwo/templates/search.html
wordpress/wp-content/themes/twentytwentytwo/templates/page-large-header.html
wordpress/wp-content/themes/twentytwentytwo/templates/single.html
wordpress/wp-content/themes/twentytwentytwo/templates/404.html
wordpress/wp-content/themes/twentytwentytwo/templates/home.html
wordpress/wp-content/themes/twentytwentytwo/style.css
wordpress/wp-content/themes/index.php
wordpress/wp-content/themes/twentytwentyfour/
wordpress/wp-content/themes/twentytwentyfour/theme.json
wordpress/wp-content/themes/twentytwentyfour/parts/
wordpress/wp-content/themes/twentytwentyfour/parts/sidebar.html
wordpress/wp-content/themes/twentytwentyfour/parts/footer.html
wordpress/wp-content/themes/twentytwentyfour/parts/header.html
wordpress/wp-content/themes/twentytwentyfour/parts/post-meta.html
wordpress/wp-content/themes/twentytwentyfour/patterns/
wordpress/wp-content/themes/twentytwentyfour/patterns/cta-pricing.php
wordpress/wp-content/themes/twentytwentyfour/patterns/page-home-portfolio-gallery.php
wordpress/wp-content/themes/twentytwentyfour/patterns/template-home-blogging.php
wordpress/wp-content/themes/twentytwentyfour/patterns/template-home-portfolio.php
wordpress/wp-content/themes/twentytwentyfour/patterns/hidden-404.php
wordpress/wp-content/themes/twentytwentyfour/patterns/posts-1-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/footer.php
wordpress/wp-content/themes/twentytwentyfour/patterns/template-search-blogging.php
wordpress/wp-content/themes/twentytwentyfour/patterns/template-search-portfolio.php
wordpress/wp-content/themes/twentytwentyfour/patterns/gallery-project-layout.php
wordpress/wp-content/themes/twentytwentyfour/patterns/hidden-post-navigation.php
wordpress/wp-content/themes/twentytwentyfour/patterns/team-4-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/text-centered-statement-small.php
wordpress/wp-content/themes/twentytwentyfour/patterns/page-home-business.php
wordpress/wp-content/themes/twentytwentyfour/patterns/banner-project-description.php
wordpress/wp-content/themes/twentytwentyfour/patterns/text-centered-statement.php
wordpress/wp-content/themes/twentytwentyfour/patterns/template-index-blogging.php
wordpress/wp-content/themes/twentytwentyfour/patterns/posts-images-only-offset-4-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/page-home-blogging.php
wordpress/wp-content/themes/twentytwentyfour/patterns/hidden-search.php
wordpress/wp-content/themes/twentytwentyfour/patterns/template-archive-blogging.php
wordpress/wp-content/themes/twentytwentyfour/patterns/banner-hero.php
wordpress/wp-content/themes/twentytwentyfour/patterns/gallery-offset-images-grid-3-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/text-project-details.php
wordpress/wp-content/themes/twentytwentyfour/patterns/hidden-no-results.php
wordpress/wp-content/themes/twentytwentyfour/patterns/gallery-full-screen-image.php
wordpress/wp-content/themes/twentytwentyfour/patterns/posts-list.php
wordpress/wp-content/themes/twentytwentyfour/patterns/text-title-left-image-right.php
wordpress/wp-content/themes/twentytwentyfour/patterns/page-portfolio-overview.php
wordpress/wp-content/themes/twentytwentyfour/patterns/template-home-business.php
wordpress/wp-content/themes/twentytwentyfour/patterns/page-home-portfolio.php
wordpress/wp-content/themes/twentytwentyfour/patterns/page-newsletter-landing.php
wordpress/wp-content/themes/twentytwentyfour/patterns/hidden-post-meta.php
wordpress/wp-content/themes/twentytwentyfour/patterns/posts-grid-2-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/cta-subscribe-centered.php
wordpress/wp-content/themes/twentytwentyfour/patterns/page-rsvp-landing.php
wordpress/wp-content/themes/twentytwentyfour/patterns/cta-services-image-left.php
wordpress/wp-content/themes/twentytwentyfour/patterns/template-archive-portfolio.php
wordpress/wp-content/themes/twentytwentyfour/patterns/cta-content-image-on-right.php
wordpress/wp-content/themes/twentytwentyfour/patterns/gallery-offset-images-grid-4-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/footer-colophon-3-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/text-alternating-images.php
wordpress/wp-content/themes/twentytwentyfour/patterns/hidden-comments.php
wordpress/wp-content/themes/twentytwentyfour/patterns/footer-centered-logo-nav.php
wordpress/wp-content/themes/twentytwentyfour/patterns/text-feature-grid-3-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/posts-3-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/hidden-portfolio-hero.php
wordpress/wp-content/themes/twentytwentyfour/patterns/cta-rsvp.php
wordpress/wp-content/themes/twentytwentyfour/patterns/template-index-portfolio.php
wordpress/wp-content/themes/twentytwentyfour/patterns/testimonial-centered.php
wordpress/wp-content/themes/twentytwentyfour/patterns/template-single-portfolio.php
wordpress/wp-content/themes/twentytwentyfour/patterns/gallery-offset-images-grid-2-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/hidden-sidebar.php
wordpress/wp-content/themes/twentytwentyfour/patterns/posts-images-only-3-col.php
wordpress/wp-content/themes/twentytwentyfour/patterns/page-about-business.php
wordpress/wp-content/themes/twentytwentyfour/patterns/text-faq.php
wordpress/wp-content/themes/twentytwentyfour/styles/
wordpress/wp-content/themes/twentytwentyfour/styles/rust.json
wordpress/wp-content/themes/twentytwentyfour/styles/maelstrom.json
wordpress/wp-content/themes/twentytwentyfour/styles/onyx.json
wordpress/wp-content/themes/twentytwentyfour/styles/fossil.json
wordpress/wp-content/themes/twentytwentyfour/styles/ice.json
wordpress/wp-content/themes/twentytwentyfour/styles/mint.json
wordpress/wp-content/themes/twentytwentyfour/styles/ember.json
wordpress/wp-content/themes/twentytwentyfour/assets/
wordpress/wp-content/themes/twentytwentyfour/assets/images/
wordpress/wp-content/themes/twentytwentyfour/assets/images/windows.webp
wordpress/wp-content/themes/twentytwentyfour/assets/images/museum.webp
wordpress/wp-content/themes/twentytwentyfour/assets/images/art-gallery.webp
wordpress/wp-content/themes/twentytwentyfour/assets/images/abstract-geometric-art.webp
wordpress/wp-content/themes/twentytwentyfour/assets/images/green-staircase.webp
wordpress/wp-content/themes/twentytwentyfour/assets/images/icon-message.webp
wordpress/wp-content/themes/twentytwentyfour/assets/images/building-exterior.webp
wordpress/wp-content/themes/twentytwentyfour/assets/images/tourist-and-building.webp
wordpress/wp-content/themes/twentytwentyfour/assets/images/hotel-facade.webp
wordpress/wp-content/themes/twentytwentyfour/assets/images/angular-roof.webp
wordpress/wp-content/themes/twentytwentyfour/assets/css/
wordpress/wp-content/themes/twentytwentyfour/assets/css/button-outline.css
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/instrument-sans/
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/instrument-sans/InstrumentSans-VariableFont_wdth,wght.woff2
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/instrument-sans/InstrumentSans-Italic-VariableFont_wdth,wght.woff2
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/instrument-sans/OFL.txt
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/jost/
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/jost/Jost-Italic-VariableFont_wght.woff2
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/jost/OFL.txt
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/jost/Jost-VariableFont_wght.woff2
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/cardo/
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/cardo/cardo_normal_400.woff2
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/cardo/LICENSE.txt
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/cardo/cardo_italic_400.woff2
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/cardo/cardo_normal_700.woff2
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/inter/
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/inter/LICENSE.txt
wordpress/wp-content/themes/twentytwentyfour/assets/fonts/inter/Inter-VariableFont_slnt,wght.woff2
wordpress/wp-content/themes/twentytwentyfour/screenshot.png
wordpress/wp-content/themes/twentytwentyfour/functions.php
wordpress/wp-content/themes/twentytwentyfour/readme.txt
wordpress/wp-content/themes/twentytwentyfour/templates/
wordpress/wp-content/themes/twentytwentyfour/templates/page.html
wordpress/wp-content/themes/twentytwentyfour/templates/index.html
wordpress/wp-content/themes/twentytwentyfour/templates/single-with-sidebar.html
wordpress/wp-content/themes/twentytwentyfour/templates/page-wide.html
wordpress/wp-content/themes/twentytwentyfour/templates/page-with-sidebar.html
wordpress/wp-content/themes/twentytwentyfour/templates/archive.html
wordpress/wp-content/themes/twentytwentyfour/templates/page-no-title.html
wordpress/wp-content/themes/twentytwentyfour/templates/search.html
wordpress/wp-content/themes/twentytwentyfour/templates/single.html
wordpress/wp-content/themes/twentytwentyfour/templates/404.html
wordpress/wp-content/themes/twentytwentyfour/templates/home.html
wordpress/wp-content/themes/twentytwentyfour/style.css
wordpress/wp-content/index.php
wordpress/wp-content/plugins/
wordpress/wp-content/plugins/akismet/
wordpress/wp-content/plugins/akismet/akismet.php
wordpress/wp-content/plugins/akismet/.htaccess
wordpress/wp-content/plugins/akismet/class.akismet-admin.php
wordpress/wp-content/plugins/akismet/class.akismet-cli.php
wordpress/wp-content/plugins/akismet/class.akismet-widget.php
wordpress/wp-content/plugins/akismet/class.akismet.php
wordpress/wp-content/plugins/akismet/views/
wordpress/wp-content/plugins/akismet/views/title.php
wordpress/wp-content/plugins/akismet/views/connect-jp.php
wordpress/wp-content/plugins/akismet/views/notice.php
wordpress/wp-content/plugins/akismet/views/config.php
wordpress/wp-content/plugins/akismet/views/stats.php
wordpress/wp-content/plugins/akismet/views/logo.php
wordpress/wp-content/plugins/akismet/views/activate.php
wordpress/wp-content/plugins/akismet/views/get.php
wordpress/wp-content/plugins/akismet/views/setup.php
wordpress/wp-content/plugins/akismet/views/predefined.php
wordpress/wp-content/plugins/akismet/views/enter.php
wordpress/wp-content/plugins/akismet/views/start.php
wordpress/wp-content/plugins/akismet/_inc/
wordpress/wp-content/plugins/akismet/_inc/rtl/
wordpress/wp-content/plugins/akismet/_inc/rtl/akismet-rtl.css
wordpress/wp-content/plugins/akismet/_inc/rtl/akismet-admin-rtl.css
wordpress/wp-content/plugins/akismet/_inc/akismet.css
wordpress/wp-content/plugins/akismet/_inc/img/
wordpress/wp-content/plugins/akismet/_inc/img/akismet-refresh-logo@2x.png
wordpress/wp-content/plugins/akismet/_inc/img/akismet-refresh-logo.svg
wordpress/wp-content/plugins/akismet/_inc/img/arrow-left.svg
wordpress/wp-content/plugins/akismet/_inc/img/logo-full-2x.png
wordpress/wp-content/plugins/akismet/_inc/img/logo-a-2x.png
wordpress/wp-content/plugins/akismet/_inc/img/icon-external.svg
wordpress/wp-content/plugins/akismet/_inc/fonts/
wordpress/wp-content/plugins/akismet/_inc/fonts/inter.css
wordpress/wp-content/plugins/akismet/_inc/akismet-admin.css
wordpress/wp-content/plugins/akismet/_inc/akismet-frontend.js
wordpress/wp-content/plugins/akismet/_inc/akismet-admin.js
wordpress/wp-content/plugins/akismet/_inc/akismet.js
wordpress/wp-content/plugins/akismet/changelog.txt
wordpress/wp-content/plugins/akismet/wrapper.php
wordpress/wp-content/plugins/akismet/index.php
wordpress/wp-content/plugins/akismet/LICENSE.txt
wordpress/wp-content/plugins/akismet/class.akismet-rest-api.php
wordpress/wp-content/plugins/akismet/readme.txt
wordpress/wp-content/plugins/index.php
wordpress/wp-content/plugins/hello.php
wordpress/wp-mail.php
wordpress/wp-links-opml.php
wordpress/wp-load.php
wordpress/wp-includes/
wordpress/wp-includes/class-wp-styles.php
wordpress/wp-includes/class-wp-user-query.php
wordpress/wp-includes/l10n.php
wordpress/wp-includes/date.php
wordpress/wp-includes/php-compat/
wordpress/wp-includes/php-compat/readonly.php
wordpress/wp-includes/class-wp-oembed.php
wordpress/wp-includes/images/
wordpress/wp-includes/images/w-logo-blue-white-bg.png
wordpress/wp-includes/images/blank.gif
wordpress/wp-includes/images/down_arrow.gif
wordpress/wp-includes/images/spinner.gif
wordpress/wp-includes/images/media/
wordpress/wp-includes/images/media/document.svg
wordpress/wp-includes/images/media/interactive.png
wordpress/wp-includes/images/media/text.svg
wordpress/wp-includes/images/media/video.svg
wordpress/wp-includes/images/media/default.png
wordpress/wp-includes/images/media/code.svg
wordpress/wp-includes/images/media/code.png
wordpress/wp-includes/images/media/audio.png
wordpress/wp-includes/images/media/text.png
wordpress/wp-includes/images/media/default.svg
wordpress/wp-includes/images/media/interactive.svg
wordpress/wp-includes/images/media/archive.png
wordpress/wp-includes/images/media/video.png
wordpress/wp-includes/images/media/spreadsheet.png
wordpress/wp-includes/images/media/audio.svg
wordpress/wp-includes/images/media/document.png
wordpress/wp-includes/images/media/archive.svg
wordpress/wp-includes/images/media/spreadsheet.svg
wordpress/wp-includes/images/uploader-icons.png
wordpress/wp-includes/images/xit-2x.gif
wordpress/wp-includes/images/w-logo-blue.png
wordpress/wp-includes/images/wpicons-2x.png
wordpress/wp-includes/images/admin-bar-sprite-2x.png
wordpress/wp-includes/images/rss-2x.png
wordpress/wp-includes/images/spinner-2x.gif
wordpress/wp-includes/images/wpicons.png
wordpress/wp-includes/images/icon-pointer-flag.png
wordpress/wp-includes/images/down_arrow-2x.gif
wordpress/wp-includes/images/arrow-pointer-blue-2x.png
wordpress/wp-includes/images/rss.png
wordpress/wp-includes/images/toggle-arrow-2x.png
wordpress/wp-includes/images/xit.gif
wordpress/wp-includes/images/smilies/
wordpress/wp-includes/images/smilies/icon_rolleyes.gif
wordpress/wp-includes/images/smilies/icon_razz.gif
wordpress/wp-includes/images/smilies/icon_question.gif
wordpress/wp-includes/images/smilies/rolleyes.png
wordpress/wp-includes/images/smilies/icon_surprised.gif
wordpress/wp-includes/images/smilies/icon_exclaim.gif
wordpress/wp-includes/images/smilies/icon_lol.gif
wordpress/wp-includes/images/smilies/icon_eek.gif
wordpress/wp-includes/images/smilies/icon_neutral.gif
wordpress/wp-includes/images/smilies/icon_confused.gif
wordpress/wp-includes/images/smilies/icon_sad.gif
wordpress/wp-includes/images/smilies/icon_mad.gif
wordpress/wp-includes/images/smilies/icon_mrgreen.gif
wordpress/wp-includes/images/smilies/mrgreen.png
wordpress/wp-includes/images/smilies/frownie.png
wordpress/wp-includes/images/smilies/icon_wink.gif
wordpress/wp-includes/images/smilies/icon_redface.gif
wordpress/wp-includes/images/smilies/icon_idea.gif
wordpress/wp-includes/images/smilies/icon_twisted.gif
wordpress/wp-includes/images/smilies/icon_biggrin.gif
wordpress/wp-includes/images/smilies/icon_evil.gif
wordpress/wp-includes/images/smilies/simple-smile.png
wordpress/wp-includes/images/smilies/icon_cry.gif
wordpress/wp-includes/images/smilies/icon_cool.gif
wordpress/wp-includes/images/smilies/icon_arrow.gif
wordpress/wp-includes/images/smilies/icon_smile.gif
wordpress/wp-includes/images/wpspin-2x.gif
wordpress/wp-includes/images/wpspin.gif
wordpress/wp-includes/images/uploader-icons-2x.png
wordpress/wp-includes/images/crystal/
wordpress/wp-includes/images/crystal/interactive.png
wordpress/wp-includes/images/crystal/default.png
wordpress/wp-includes/images/crystal/code.png
wordpress/wp-includes/images/crystal/audio.png
wordpress/wp-includes/images/crystal/text.png
wordpress/wp-includes/images/crystal/archive.png
wordpress/wp-includes/images/crystal/video.png
wordpress/wp-includes/images/crystal/spreadsheet.png
wordpress/wp-includes/images/crystal/license.txt
wordpress/wp-includes/images/crystal/document.png
wordpress/wp-includes/images/icon-pointer-flag-2x.png
wordpress/wp-includes/images/admin-bar-sprite.png
wordpress/wp-includes/images/toggle-arrow.png
wordpress/wp-includes/images/arrow-pointer-blue.png
wordpress/wp-includes/locale.php
wordpress/wp-includes/class-wp-dependencies.php
wordpress/wp-includes/class-wp-feed-cache-transient.php
wordpress/wp-includes/class-wp-recovery-mode-email-service.php
wordpress/wp-includes/block-supports/
wordpress/wp-includes/block-supports/position.php
wordpress/wp-includes/block-supports/background.php
wordpress/wp-includes/block-supports/custom-classname.php
wordpress/wp-includes/block-supports/border.php
wordpress/wp-includes/block-supports/spacing.php
wordpress/wp-includes/block-supports/align.php
wordpress/wp-includes/block-supports/generated-classname.php
wordpress/wp-includes/block-supports/typography.php
wordpress/wp-includes/block-supports/elements.php
wordpress/wp-includes/block-supports/duotone.php
wordpress/wp-includes/block-supports/shadow.php
wordpress/wp-includes/block-supports/settings.php
wordpress/wp-includes/block-supports/block-style-variations.php
wordpress/wp-includes/block-supports/colors.php
wordpress/wp-includes/block-supports/utils.php
wordpress/wp-includes/block-supports/dimensions.php
wordpress/wp-includes/block-supports/layout.php
wordpress/wp-includes/class-wp-comment-query.php
wordpress/wp-includes/theme-compat/
wordpress/wp-includes/theme-compat/footer.php
wordpress/wp-includes/theme-compat/sidebar.php
wordpress/wp-includes/theme-compat/footer-embed.php
wordpress/wp-includes/theme-compat/embed.php
wordpress/wp-includes/theme-compat/header-embed.php
wordpress/wp-includes/theme-compat/header.php
wordpress/wp-includes/theme-compat/embed-content.php
wordpress/wp-includes/theme-compat/comments.php
wordpress/wp-includes/theme-compat/embed-404.php
wordpress/wp-includes/class-wp-customize-control.php
wordpress/wp-includes/SimplePie/
wordpress/wp-includes/SimplePie/Parser.php
wordpress/wp-includes/SimplePie/Sanitize.php
wordpress/wp-includes/SimplePie/Core.php
wordpress/wp-includes/SimplePie/Decode/
wordpress/wp-includes/SimplePie/Decode/HTML/
wordpress/wp-includes/SimplePie/Decode/HTML/Entities.php
wordpress/wp-includes/SimplePie/Category.php
wordpress/wp-includes/SimplePie/gzdecode.php
wordpress/wp-includes/SimplePie/Locator.php
wordpress/wp-includes/SimplePie/Parse/
wordpress/wp-includes/SimplePie/Parse/Date.php
wordpress/wp-includes/SimplePie/Author.php
wordpress/wp-includes/SimplePie/Cache.php
wordpress/wp-includes/SimplePie/IRI.php
wordpress/wp-includes/SimplePie/Credit.php
wordpress/wp-includes/SimplePie/Content/
wordpress/wp-includes/SimplePie/Content/Type/
wordpress/wp-includes/SimplePie/Content/Type/Sniffer.php
wordpress/wp-includes/SimplePie/Restriction.php
wordpress/wp-includes/SimplePie/Item.php
wordpress/wp-includes/SimplePie/XML/
wordpress/wp-includes/SimplePie/XML/Declaration/
wordpress/wp-includes/SimplePie/XML/Declaration/Parser.php
wordpress/wp-includes/SimplePie/Cache/
wordpress/wp-includes/SimplePie/Cache/Base.php
wordpress/wp-includes/SimplePie/Cache/Memcached.php
wordpress/wp-includes/SimplePie/Cache/MySQL.php
wordpress/wp-includes/SimplePie/Cache/Memcache.php
wordpress/wp-includes/SimplePie/Cache/Redis.php
wordpress/wp-includes/SimplePie/Cache/DB.php
wordpress/wp-includes/SimplePie/Cache/File.php
wordpress/wp-includes/SimplePie/Source.php
wordpress/wp-includes/SimplePie/Registry.php
wordpress/wp-includes/SimplePie/Rating.php
wordpress/wp-includes/SimplePie/Copyright.php
wordpress/wp-includes/SimplePie/Exception.php
wordpress/wp-includes/SimplePie/Misc.php
wordpress/wp-includes/SimplePie/Caption.php
wordpress/wp-includes/SimplePie/Net/
wordpress/wp-includes/SimplePie/Net/IPv6.php
wordpress/wp-includes/SimplePie/File.php
wordpress/wp-includes/SimplePie/HTTP/
wordpress/wp-includes/SimplePie/HTTP/Parser.php
wordpress/wp-includes/SimplePie/Enclosure.php
wordpress/wp-includes/media-template.php
wordpress/wp-includes/cache.php
wordpress/wp-includes/class-wp-widget.php
wordpress/wp-includes/compat.php
wordpress/wp-includes/default-filters.php
wordpress/wp-includes/Requests/
wordpress/wp-includes/Requests/src/
wordpress/wp-includes/Requests/src/Transport/
wordpress/wp-includes/Requests/src/Transport/Fsockopen.php
wordpress/wp-includes/Requests/src/Transport/Curl.php
wordpress/wp-includes/Requests/src/Cookie/
wordpress/wp-includes/Requests/src/Cookie/Jar.php
wordpress/wp-includes/Requests/src/Requests.php
wordpress/wp-includes/Requests/src/Auth.php
wordpress/wp-includes/Requests/src/Port.php
wordpress/wp-includes/Requests/src/HookManager.php
wordpress/wp-includes/Requests/src/Exception/
wordpress/wp-includes/Requests/src/Exception/Transport/
wordpress/wp-includes/Requests/src/Exception/Transport/Curl.php
wordpress/wp-includes/Requests/src/Exception/ArgumentCount.php
wordpress/wp-includes/Requests/src/Exception/Transport.php
wordpress/wp-includes/Requests/src/Exception/Http.php
wordpress/wp-includes/Requests/src/Exception/InvalidArgument.php
wordpress/wp-includes/Requests/src/Exception/Http/
wordpress/wp-includes/Requests/src/Exception/Http/Status304.php
wordpress/wp-includes/Requests/src/Exception/Http/Status403.php
wordpress/wp-includes/Requests/src/Exception/Http/Status306.php
wordpress/wp-includes/Requests/src/Exception/Http/Status401.php
wordpress/wp-includes/Requests/src/Exception/Http/Status402.php
wordpress/wp-includes/Requests/src/Exception/Http/Status417.php
wordpress/wp-includes/Requests/src/Exception/Http/Status505.php
wordpress/wp-includes/Requests/src/Exception/Http/Status418.php
wordpress/wp-includes/Requests/src/Exception/Http/Status414.php
wordpress/wp-includes/Requests/src/Exception/Http/Status504.php
wordpress/wp-includes/Requests/src/Exception/Http/Status413.php
wordpress/wp-includes/Requests/src/Exception/Http/Status429.php
wordpress/wp-includes/Requests/src/Exception/Http/Status503.php
wordpress/wp-includes/Requests/src/Exception/Http/Status415.php
wordpress/wp-includes/Requests/src/Exception/Http/Status502.php
wordpress/wp-includes/Requests/src/Exception/Http/Status416.php
wordpress/wp-includes/Requests/src/Exception/Http/Status305.php
wordpress/wp-includes/Requests/src/Exception/Http/Status408.php
wordpress/wp-includes/Requests/src/Exception/Http/Status511.php
wordpress/wp-includes/Requests/src/Exception/Http/Status407.php
wordpress/wp-includes/Requests/src/Exception/Http/Status411.php
wordpress/wp-includes/Requests/src/Exception/Http/Status410.php
wordpress/wp-includes/Requests/src/Exception/Http/Status431.php
wordpress/wp-includes/Requests/src/Exception/Http/Status409.php
wordpress/wp-includes/Requests/src/Exception/Http/Status428.php
wordpress/wp-includes/Requests/src/Exception/Http/Status405.php
wordpress/wp-includes/Requests/src/Exception/Http/Status501.php
wordpress/wp-includes/Requests/src/Exception/Http/Status406.php
wordpress/wp-includes/Requests/src/Exception/Http/Status404.php
wordpress/wp-includes/Requests/src/Exception/Http/Status400.php
wordpress/wp-includes/Requests/src/Exception/Http/Status412.php
wordpress/wp-includes/Requests/src/Exception/Http/Status500.php
wordpress/wp-includes/Requests/src/Exception/Http/StatusUnknown.php
wordpress/wp-includes/Requests/src/Autoload.php
wordpress/wp-includes/Requests/src/Response.php
wordpress/wp-includes/Requests/src/Utility/
wordpress/wp-includes/Requests/src/Utility/InputValidator.php
wordpress/wp-includes/Requests/src/Utility/CaseInsensitiveDictionary.php
wordpress/wp-includes/Requests/src/Utility/FilteredIterator.php
wordpress/wp-includes/Requests/src/Response/
wordpress/wp-includes/Requests/src/Response/Headers.php
wordpress/wp-includes/Requests/src/Cookie.php
wordpress/wp-includes/Requests/src/Auth/
wordpress/wp-includes/Requests/src/Auth/Basic.php
wordpress/wp-includes/Requests/src/Proxy.php
wordpress/wp-includes/Requests/src/Iri.php
wordpress/wp-includes/Requests/src/Ipv6.php
wordpress/wp-includes/Requests/src/Transport.php
wordpress/wp-includes/Requests/src/Session.php
wordpress/wp-includes/Requests/src/Capability.php
wordpress/wp-includes/Requests/src/Hooks.php
wordpress/wp-includes/Requests/src/Proxy/
wordpress/wp-includes/Requests/src/Proxy/Http.php
wordpress/wp-includes/Requests/src/Ssl.php
wordpress/wp-includes/Requests/src/Exception.php
wordpress/wp-includes/Requests/src/IdnaEncoder.php
wordpress/wp-includes/Requests/library/
wordpress/wp-includes/Requests/library/Requests.php
wordpress/wp-includes/embed.php
wordpress/wp-includes/block-template.php
wordpress/wp-includes/class-wp-fatal-error-handler.php
wordpress/wp-includes/theme.json
wordpress/wp-includes/css/
wordpress/wp-includes/css/admin-bar.min.css
wordpress/wp-includes/css/editor.min.css
wordpress/wp-includes/css/admin-bar-rtl.min.css
wordpress/wp-includes/css/media-views.min.css
wordpress/wp-includes/css/classic-themes.css
wordpress/wp-includes/css/customize-preview.css
wordpress/wp-includes/css/classic-themes.min.css
wordpress/wp-includes/css/admin-bar-rtl.css
wordpress/wp-includes/css/editor.css
wordpress/wp-includes/css/wp-embed-template.min.css
wordpress/wp-includes/css/wp-pointer.css
wordpress/wp-includes/css/customize-preview-rtl.css
wordpress/wp-includes/css/wp-pointer-rtl.css
wordpress/wp-includes/css/jquery-ui-dialog-rtl.min.css
wordpress/wp-includes/css/dist/
wordpress/wp-includes/css/dist/preferences/
wordpress/wp-includes/css/dist/preferences/style-rtl.min.css
wordpress/wp-includes/css/dist/preferences/style.min.css
wordpress/wp-includes/css/dist/preferences/style-rtl.css
wordpress/wp-includes/css/dist/preferences/style.css
wordpress/wp-includes/css/dist/edit-widgets/
wordpress/wp-includes/css/dist/edit-widgets/style-rtl.min.css
wordpress/wp-includes/css/dist/edit-widgets/style.min.css
wordpress/wp-includes/css/dist/edit-widgets/style-rtl.css
wordpress/wp-includes/css/dist/edit-widgets/style.css
wordpress/wp-includes/css/dist/patterns/
wordpress/wp-includes/css/dist/patterns/style-rtl.min.css
wordpress/wp-includes/css/dist/patterns/style.min.css
wordpress/wp-includes/css/dist/patterns/style-rtl.css
wordpress/wp-includes/css/dist/patterns/style.css
wordpress/wp-includes/css/dist/block-directory/
wordpress/wp-includes/css/dist/block-directory/style-rtl.min.css
wordpress/wp-includes/css/dist/block-directory/style.min.css
wordpress/wp-includes/css/dist/block-directory/style-rtl.css
wordpress/wp-includes/css/dist/block-directory/style.css
wordpress/wp-includes/css/dist/edit-site/
wordpress/wp-includes/css/dist/edit-site/style-rtl.min.css
wordpress/wp-includes/css/dist/edit-site/style.min.css
wordpress/wp-includes/css/dist/edit-site/style-rtl.css
wordpress/wp-includes/css/dist/edit-site/style.css
wordpress/wp-includes/css/dist/block-library/
wordpress/wp-includes/css/dist/block-library/classic-rtl.css
wordpress/wp-includes/css/dist/block-library/editor.min.css
wordpress/wp-includes/css/dist/block-library/elements-rtl.css
wordpress/wp-includes/css/dist/block-library/reset-rtl.css
wordpress/wp-includes/css/dist/block-library/style-rtl.min.css
wordpress/wp-includes/css/dist/block-library/theme.css
wordpress/wp-includes/css/dist/block-library/theme-rtl.min.css
wordpress/wp-includes/css/dist/block-library/editor-elements-rtl.css
wordpress/wp-includes/css/dist/block-library/common-rtl.min.css
wordpress/wp-includes/css/dist/block-library/elements-rtl.min.css
wordpress/wp-includes/css/dist/block-library/editor.css
wordpress/wp-includes/css/dist/block-library/classic-rtl.min.css
wordpress/wp-includes/css/dist/block-library/editor-elements.min.css
wordpress/wp-includes/css/dist/block-library/reset-rtl.min.css
wordpress/wp-includes/css/dist/block-library/common.css
wordpress/wp-includes/css/dist/block-library/theme.min.css
wordpress/wp-includes/css/dist/block-library/elements.min.css
wordpress/wp-includes/css/dist/block-library/style.min.css
wordpress/wp-includes/css/dist/block-library/theme-rtl.css
wordpress/wp-includes/css/dist/block-library/classic.css
wordpress/wp-includes/css/dist/block-library/editor-rtl.css
wordpress/wp-includes/css/dist/block-library/editor-rtl.min.css
wordpress/wp-includes/css/dist/block-library/style-rtl.css
wordpress/wp-includes/css/dist/block-library/classic.min.css
wordpress/wp-includes/css/dist/block-library/common.min.css
wordpress/wp-includes/css/dist/block-library/reset.min.css
wordpress/wp-includes/css/dist/block-library/elements.css
wordpress/wp-includes/css/dist/block-library/reset.css
wordpress/wp-includes/css/dist/block-library/editor-elements.css
wordpress/wp-includes/css/dist/block-library/editor-elements-rtl.min.css
wordpress/wp-includes/css/dist/block-library/common-rtl.css
wordpress/wp-includes/css/dist/block-library/style.css
wordpress/wp-includes/css/dist/format-library/
wordpress/wp-includes/css/dist/format-library/style-rtl.min.css
wordpress/wp-includes/css/dist/format-library/style.min.css
wordpress/wp-includes/css/dist/format-library/style-rtl.css
wordpress/wp-includes/css/dist/format-library/style.css
wordpress/wp-includes/css/dist/edit-post/
wordpress/wp-includes/css/dist/edit-post/classic-rtl.css
wordpress/wp-includes/css/dist/edit-post/style-rtl.min.css
wordpress/wp-includes/css/dist/edit-post/classic-rtl.min.css
wordpress/wp-includes/css/dist/edit-post/style.min.css
wordpress/wp-includes/css/dist/edit-post/classic.css
wordpress/wp-includes/css/dist/edit-post/style-rtl.css
wordpress/wp-includes/css/dist/edit-post/classic.min.css
wordpress/wp-includes/css/dist/edit-post/style.css
wordpress/wp-includes/css/dist/widgets/
wordpress/wp-includes/css/dist/widgets/style-rtl.min.css
wordpress/wp-includes/css/dist/widgets/style.min.css
wordpress/wp-includes/css/dist/widgets/style-rtl.css
wordpress/wp-includes/css/dist/widgets/style.css
wordpress/wp-includes/css/dist/commands/
wordpress/wp-includes/css/dist/commands/style-rtl.min.css
wordpress/wp-includes/css/dist/commands/style.min.css
wordpress/wp-includes/css/dist/commands/style-rtl.css
wordpress/wp-includes/css/dist/commands/style.css
wordpress/wp-includes/css/dist/customize-widgets/
wordpress/wp-includes/css/dist/customize-widgets/style-rtl.min.css
wordpress/wp-includes/css/dist/customize-widgets/style.min.css
wordpress/wp-includes/css/dist/customize-widgets/style-rtl.css
wordpress/wp-includes/css/dist/customize-widgets/style.css
wordpress/wp-includes/css/dist/reusable-blocks/
wordpress/wp-includes/css/dist/reusable-blocks/style-rtl.min.css
wordpress/wp-includes/css/dist/reusable-blocks/style.min.css
wordpress/wp-includes/css/dist/reusable-blocks/style-rtl.css
wordpress/wp-includes/css/dist/reusable-blocks/style.css
wordpress/wp-includes/css/dist/editor/
wordpress/wp-includes/css/dist/editor/style-rtl.min.css
wordpress/wp-includes/css/dist/editor/style.min.css
wordpress/wp-includes/css/dist/editor/style-rtl.css
wordpress/wp-includes/css/dist/editor/style.css
wordpress/wp-includes/css/dist/nux/
wordpress/wp-includes/css/dist/nux/style-rtl.min.css
wordpress/wp-includes/css/dist/nux/style.min.css
wordpress/wp-includes/css/dist/nux/style-rtl.css
wordpress/wp-includes/css/dist/nux/style.css
wordpress/wp-includes/css/dist/list-reusable-blocks/
wordpress/wp-includes/css/dist/list-reusable-blocks/style-rtl.min.css
wordpress/wp-includes/css/dist/list-reusable-blocks/style.min.css
wordpress/wp-includes/css/dist/list-reusable-blocks/style-rtl.css
wordpress/wp-includes/css/dist/list-reusable-blocks/style.css
wordpress/wp-includes/css/dist/components/
wordpress/wp-includes/css/dist/components/style-rtl.min.css
wordpress/wp-includes/css/dist/components/style.min.css
wordpress/wp-includes/css/dist/components/style-rtl.css
wordpress/wp-includes/css/dist/components/style.css
wordpress/wp-includes/css/dist/block-editor/
wordpress/wp-includes/css/dist/block-editor/content.min.css
wordpress/wp-includes/css/dist/block-editor/style-rtl.min.css
wordpress/wp-includes/css/dist/block-editor/default-editor-styles-rtl.css
wordpress/wp-includes/css/dist/block-editor/default-editor-styles-rtl.min.css
wordpress/wp-includes/css/dist/block-editor/content.css
wordpress/wp-includes/css/dist/block-editor/content-rtl.min.css
wordpress/wp-includes/css/dist/block-editor/default-editor-styles.min.css
wordpress/wp-includes/css/dist/block-editor/default-editor-styles.css
wordpress/wp-includes/css/dist/block-editor/style.min.css
wordpress/wp-includes/css/dist/block-editor/content-rtl.css
wordpress/wp-includes/css/dist/block-editor/style-rtl.css
wordpress/wp-includes/css/dist/block-editor/style.css
wordpress/wp-includes/css/media-views-rtl.css
wordpress/wp-includes/css/customize-preview-rtl.min.css
wordpress/wp-includes/css/jquery-ui-dialog.css
wordpress/wp-includes/css/admin-bar.css
wordpress/wp-includes/css/media-views-rtl.min.css
wordpress/wp-includes/css/jquery-ui-dialog.min.css
wordpress/wp-includes/css/wp-pointer-rtl.min.css
wordpress/wp-includes/css/buttons-rtl.css
wordpress/wp-includes/css/buttons.css
wordpress/wp-includes/css/wp-embed-template-ie.css
wordpress/wp-includes/css/wp-embed-template-ie.min.css
wordpress/wp-includes/css/media-views.css
wordpress/wp-includes/css/jquery-ui-dialog-rtl.css
wordpress/wp-includes/css/dashicons.css
wordpress/wp-includes/css/editor-rtl.css
wordpress/wp-includes/css/wp-auth-check-rtl.min.css
wordpress/wp-includes/css/editor-rtl.min.css
wordpress/wp-includes/css/customize-preview.min.css
wordpress/wp-includes/css/buttons-rtl.min.css
wordpress/wp-includes/css/wp-pointer.min.css
wordpress/wp-includes/css/wp-auth-check.min.css
wordpress/wp-includes/css/wp-auth-check.css
wordpress/wp-includes/css/wp-auth-check-rtl.css
wordpress/wp-includes/css/wp-embed-template.css
wordpress/wp-includes/css/buttons.min.css
wordpress/wp-includes/css/dashicons.min.css
wordpress/wp-includes/theme-templates.php
wordpress/wp-includes/class-wp-http-curl.php
wordpress/wp-includes/class-wp-duotone.php
wordpress/wp-includes/class-smtp.php
wordpress/wp-includes/class-simplepie.php
wordpress/wp-includes/class-wpdb.php
wordpress/wp-includes/class-wp-role.php
wordpress/wp-includes/feed.php
wordpress/wp-includes/class-wp-simplepie-file.php
wordpress/wp-includes/class-wp-theme.php
wordpress/wp-includes/class-wp-theme-json.php
wordpress/wp-includes/class-walker-page.php
wordpress/wp-includes/class-wp-paused-extensions-storage.php
wordpress/wp-includes/class-wp-block-editor-context.php
wordpress/wp-includes/ms-default-filters.php
wordpress/wp-includes/class-wp-theme-json-data.php
wordpress/wp-includes/class-wp-http-requests-hooks.php
wordpress/wp-includes/ms-files.php
wordpress/wp-includes/class-wp-block-pattern-categories-registry.php
wordpress/wp-includes/class-snoopy.php
wordpress/wp-includes/class-wp-http.php
wordpress/wp-includes/class-wp-post.php
wordpress/wp-includes/class-http.php
wordpress/wp-includes/media.php
wordpress/wp-includes/script-loader.php
wordpress/wp-includes/class-pop3.php
wordpress/wp-includes/category.php
wordpress/wp-includes/class-wp-recovery-mode-link-service.php
wordpress/wp-includes/class-wp-customize-widgets.php
wordpress/wp-includes/block-i18n.json
wordpress/wp-includes/block-template-utils.php
wordpress/wp-includes/Text/
wordpress/wp-includes/Text/Diff/
wordpress/wp-includes/Text/Diff/Renderer/
wordpress/wp-includes/Text/Diff/Renderer/inline.php
wordpress/wp-includes/Text/Diff/Renderer.php
wordpress/wp-includes/Text/Diff/Engine/
wordpress/wp-includes/Text/Diff/Engine/native.php
wordpress/wp-includes/Text/Diff/Engine/string.php
wordpress/wp-includes/Text/Diff/Engine/xdiff.php
wordpress/wp-includes/Text/Diff/Engine/shell.php
wordpress/wp-includes/Text/Diff.php
wordpress/wp-includes/ms-deprecated.php
wordpress/wp-includes/class-phpass.php
wordpress/wp-includes/class-avif-info.php
wordpress/wp-includes/class-wp-editor.php
wordpress/wp-includes/class-wp-navigation-fallback.php
wordpress/wp-includes/meta.php
wordpress/wp-includes/assets/
wordpress/wp-includes/assets/script-loader-packages.php
wordpress/wp-includes/assets/script-loader-react-refresh-entry.php
wordpress/wp-includes/assets/script-loader-packages.min.php
wordpress/wp-includes/assets/script-loader-react-refresh-runtime.min.php
wordpress/wp-includes/assets/script-loader-react-refresh-entry.min.php
wordpress/wp-includes/assets/script-loader-react-refresh-runtime.php
wordpress/wp-includes/taxonomy.php
wordpress/wp-includes/rest-api.php
wordpress/wp-includes/class-wp-widget-factory.php
wordpress/wp-includes/nav-menu.php
wordpress/wp-includes/class-wp-http-response.php
wordpress/wp-includes/class-wp-tax-query.php
wordpress/wp-includes/class-wp-http-ixr-client.php
wordpress/wp-includes/shortcodes.php
wordpress/wp-includes/user.php
wordpress/wp-includes/class-wp-image-editor-gd.php
wordpress/wp-includes/class-walker-nav-menu.php
wordpress/wp-includes/class-wp-simplepie-sanitize-kses.php
wordpress/wp-includes/ms-functions.php
wordpress/wp-includes/class-wp-customize-section.php
wordpress/wp-includes/class-wp-block-bindings-registry.php
wordpress/wp-includes/class-wp-matchesmapregex.php
wordpress/wp-includes/class-wp-recovery-mode-cookie-service.php
wordpress/wp-includes/revision.php
wordpress/wp-includes/functions.wp-styles.php
wordpress/wp-includes/class-wp-customize-manager.php
wordpress/wp-includes/class-walker-category.php
wordpress/wp-includes/class-requests.php
wordpress/wp-includes/query.php
wordpress/wp-includes/ms-blogs.php
wordpress/wp-includes/class-wp-network.php
wordpress/wp-includes/cache-compat.php
wordpress/wp-includes/html-api/
wordpress/wp-includes/html-api/class-wp-html-text-replacement.php
wordpress/wp-includes/html-api/class-wp-html-processor-state.php
wordpress/wp-includes/html-api/class-wp-html-token.php
wordpress/wp-includes/html-api/class-wp-html-attribute-token.php
wordpress/wp-includes/html-api/class-wp-html-span.php
wordpress/wp-includes/html-api/class-wp-html-unsupported-exception.php
wordpress/wp-includes/html-api/class-wp-html-open-elements.php
wordpress/wp-includes/html-api/class-wp-html-processor.php
wordpress/wp-includes/html-api/class-wp-html-stack-event.php
wordpress/wp-includes/html-api/html5-named-character-references.php
wordpress/wp-includes/html-api/class-wp-html-active-formatting-elements.php
wordpress/wp-includes/html-api/class-wp-html-tag-processor.php
wordpress/wp-includes/html-api/class-wp-html-decoder.php
wordpress/wp-includes/cron.php
wordpress/wp-includes/blocks.php
wordpress/wp-includes/class-wp-block-bindings-source.php
wordpress/wp-includes/ms-site.php
wordpress/wp-includes/feed-rss.php
wordpress/wp-includes/rewrite.php
wordpress/wp-includes/certificates/
wordpress/wp-includes/certificates/ca-bundle.crt
wordpress/wp-includes/class-wp-roles.php
wordpress/wp-includes/embed-template.php
wordpress/wp-includes/rss.php
wordpress/wp-includes/canonical.php
wordpress/wp-includes/class-wp-site.php
wordpress/wp-includes/class-wp-comment.php
wordpress/wp-includes/kses.php
wordpress/wp-includes/ms-settings.php
wordpress/wp-includes/class-wp-term-query.php
wordpress/wp-includes/category-template.php
wordpress/wp-includes/ID3/
wordpress/wp-includes/ID3/module.tag.lyrics3.php
wordpress/wp-includes/ID3/module.audio.dts.php
wordpress/wp-includes/ID3/module.tag.id3v1.php
wordpress/wp-includes/ID3/module.audio.flac.php
wordpress/wp-includes/ID3/module.audio.mp3.php
wordpress/wp-includes/ID3/module.audio-video.matroska.php
wordpress/wp-includes/ID3/module.audio-video.quicktime.php
wordpress/wp-includes/ID3/module.tag.apetag.php
wordpress/wp-includes/ID3/getid3.lib.php
wordpress/wp-includes/ID3/module.audio.ac3.php
wordpress/wp-includes/ID3/getid3.php
wordpress/wp-includes/ID3/license.txt
wordpress/wp-includes/ID3/module.audio-video.flv.php
wordpress/wp-includes/ID3/readme.txt
wordpress/wp-includes/ID3/module.tag.id3v2.php
wordpress/wp-includes/ID3/module.audio.ogg.php
wordpress/wp-includes/ID3/module.audio-video.riff.php
wordpress/wp-includes/ID3/module.audio-video.asf.php
wordpress/wp-includes/class-walker-page-dropdown.php
wordpress/wp-includes/class-wp-block-supports.php
wordpress/wp-includes/class-wp-customize-panel.php
wordpress/wp-includes/class-wp-locale.php
wordpress/wp-includes/class-wp-user-meta-session-tokens.php
wordpress/wp-includes/class-wp-block-parser-block.php
wordpress/wp-includes/class-wp-http-requests-response.php
wordpress/wp-includes/template-loader.php
wordpress/wp-includes/interactivity-api/
wordpress/wp-includes/interactivity-api/class-wp-interactivity-api.php
wordpress/wp-includes/interactivity-api/class-wp-interactivity-api-directives-processor.php
wordpress/wp-includes/interactivity-api/interactivity-api.php
wordpress/wp-includes/class-wp-site-query.php
wordpress/wp-includes/style-engine.php
wordpress/wp-includes/rss-functions.php
wordpress/wp-includes/vars.php
wordpress/wp-includes/feed-rss2.php
wordpress/wp-includes/sitemaps.php
wordpress/wp-includes/general-template.php
wordpress/wp-includes/class-wp-block-template.php
wordpress/wp-includes/script-modules.php
wordpress/wp-includes/default-constants.php
wordpress/wp-includes/blocks/
wordpress/wp-includes/blocks/latest-comments.php
wordpress/wp-includes/blocks/post-content.php
wordpress/wp-includes/blocks/navigation-link.php
wordpress/wp-includes/blocks/navigation/
wordpress/wp-includes/blocks/navigation/editor.min.css
wordpress/wp-includes/blocks/navigation/style-rtl.min.css
wordpress/wp-includes/blocks/navigation/block.json
wordpress/wp-includes/blocks/navigation/editor.css
wordpress/wp-includes/blocks/navigation/view-modal.min.asset.php
wordpress/wp-includes/blocks/navigation/view.min.asset.php
wordpress/wp-includes/blocks/navigation/view.js
wordpress/wp-includes/blocks/navigation/style.min.css
wordpress/wp-includes/blocks/navigation/editor-rtl.css
wordpress/wp-includes/blocks/navigation/view.asset.php
wordpress/wp-includes/blocks/navigation/view-modal.asset.php
wordpress/wp-includes/blocks/navigation/editor-rtl.min.css
wordpress/wp-includes/blocks/navigation/view.min.js
wordpress/wp-includes/blocks/navigation/style-rtl.css
wordpress/wp-includes/blocks/navigation/style.css
wordpress/wp-includes/blocks/post-content/
wordpress/wp-includes/blocks/post-content/editor.min.css
wordpress/wp-includes/blocks/post-content/block.json
wordpress/wp-includes/blocks/post-content/editor.css
wordpress/wp-includes/blocks/post-content/editor-rtl.css
wordpress/wp-includes/blocks/post-content/editor-rtl.min.css
wordpress/wp-includes/blocks/comments/
wordpress/wp-includes/blocks/comments/editor.min.css
wordpress/wp-includes/blocks/comments/style-rtl.min.css
wordpress/wp-includes/blocks/comments/block.json
wordpress/wp-includes/blocks/comments/editor.css
wordpress/wp-includes/blocks/comments/style.min.css
wordpress/wp-includes/blocks/comments/editor-rtl.css
wordpress/wp-includes/blocks/comments/editor-rtl.min.css
wordpress/wp-includes/blocks/comments/style-rtl.css
wordpress/wp-includes/blocks/comments/style.css
wordpress/wp-includes/blocks/calendar.php
wordpress/wp-includes/blocks/site-tagline.php
wordpress/wp-includes/blocks/loginout.php
wordpress/wp-includes/blocks/query-pagination-numbers/
wordpress/wp-includes/blocks/query-pagination-numbers/editor.min.css
wordpress/wp-includes/blocks/query-pagination-numbers/block.json
wordpress/wp-includes/blocks/query-pagination-numbers/editor.css
wordpress/wp-includes/blocks/query-pagination-numbers/editor-rtl.css
wordpress/wp-includes/blocks/query-pagination-numbers/editor-rtl.min.css
wordpress/wp-includes/blocks/gallery/
wordpress/wp-includes/blocks/gallery/editor.min.css
wordpress/wp-includes/blocks/gallery/style-rtl.min.css
wordpress/wp-includes/blocks/gallery/theme.css
wordpress/wp-includes/blocks/gallery/block.json
wordpress/wp-includes/blocks/gallery/theme-rtl.min.css
wordpress/wp-includes/blocks/gallery/editor.css
wordpress/wp-includes/blocks/gallery/theme.min.css
wordpress/wp-includes/blocks/gallery/style.min.css
wordpress/wp-includes/blocks/gallery/theme-rtl.css
wordpress/wp-includes/blocks/gallery/editor-rtl.css
wordpress/wp-includes/blocks/gallery/editor-rtl.min.css
wordpress/wp-includes/blocks/gallery/style-rtl.css
wordpress/wp-includes/blocks/gallery/style.css
wordpress/wp-includes/blocks/list.php
wordpress/wp-includes/blocks/shortcode/
wordpress/wp-includes/blocks/shortcode/editor.min.css
wordpress/wp-includes/blocks/shortcode/block.json
wordpress/wp-includes/blocks/shortcode/editor.css
wordpress/wp-includes/blocks/shortcode/editor-rtl.css
wordpress/wp-includes/blocks/shortcode/editor-rtl.min.css
wordpress/wp-includes/blocks/calendar/
wordpress/wp-includes/blocks/calendar/style-rtl.min.css
wordpress/wp-includes/blocks/calendar/block.json
wordpress/wp-includes/blocks/calendar/style.min.css
wordpress/wp-includes/blocks/calendar/style-rtl.css
wordpress/wp-includes/blocks/calendar/style.css
wordpress/wp-includes/blocks/comment-content/
wordpress/wp-includes/blocks/comment-content/style-rtl.min.css
wordpress/wp-includes/blocks/comment-content/block.json
wordpress/wp-includes/blocks/comment-content/style.min.css
wordpress/wp-includes/blocks/comment-content/style-rtl.css
wordpress/wp-includes/blocks/comment-content/style.css
wordpress/wp-includes/blocks/details/
wordpress/wp-includes/blocks/details/editor.min.css
wordpress/wp-includes/blocks/details/style-rtl.min.css
wordpress/wp-includes/blocks/details/block.json
wordpress/wp-includes/blocks/details/editor.css
wordpress/wp-includes/blocks/details/style.min.css
wordpress/wp-includes/blocks/details/editor-rtl.css
wordpress/wp-includes/blocks/details/editor-rtl.min.css
wordpress/wp-includes/blocks/details/style-rtl.css
wordpress/wp-includes/blocks/details/style.css
wordpress/wp-includes/blocks/template-part/
wordpress/wp-includes/blocks/template-part/editor.min.css
wordpress/wp-includes/blocks/template-part/theme.css
wordpress/wp-includes/blocks/template-part/block.json
wordpress/wp-includes/blocks/template-part/theme-rtl.min.css
wordpress/wp-includes/blocks/template-part/editor.css
wordpress/wp-includes/blocks/template-part/theme.min.css
wordpress/wp-includes/blocks/template-part/theme-rtl.css
wordpress/wp-includes/blocks/template-part/editor-rtl.css
wordpress/wp-includes/blocks/template-part/editor-rtl.min.css
wordpress/wp-includes/blocks/button.php
wordpress/wp-includes/blocks/comments-pagination-next.php
wordpress/wp-includes/blocks/post-title.php
wordpress/wp-includes/blocks/post-navigation-link/
wordpress/wp-includes/blocks/post-navigation-link/style-rtl.min.css
wordpress/wp-includes/blocks/post-navigation-link/block.json
wordpress/wp-includes/blocks/post-navigation-link/style.min.css
wordpress/wp-includes/blocks/post-navigation-link/style-rtl.css
wordpress/wp-includes/blocks/post-navigation-link/style.css
wordpress/wp-includes/blocks/require-dynamic-blocks.php
wordpress/wp-includes/blocks/columns/
wordpress/wp-includes/blocks/columns/editor.min.css
wordpress/wp-includes/blocks/columns/style-rtl.min.css
wordpress/wp-includes/blocks/columns/block.json
wordpress/wp-includes/blocks/columns/editor.css
wordpress/wp-includes/blocks/columns/style.min.css
wordpress/wp-includes/blocks/columns/editor-rtl.css
wordpress/wp-includes/blocks/columns/editor-rtl.min.css
wordpress/wp-includes/blocks/columns/style-rtl.css
wordpress/wp-includes/blocks/columns/style.css
wordpress/wp-includes/blocks/shortcode.php
wordpress/wp-includes/blocks/comment-reply-link/
wordpress/wp-includes/blocks/comment-reply-link/block.json
wordpress/wp-includes/blocks/post-author-name/
wordpress/wp-includes/blocks/post-author-name/block.json
wordpress/wp-includes/blocks/site-title.php
wordpress/wp-includes/blocks/term-description/
wordpress/wp-includes/blocks/term-description/style-rtl.min.css
wordpress/wp-includes/blocks/term-description/block.json
wordpress/wp-includes/blocks/term-description/style.min.css
wordpress/wp-includes/blocks/term-description/style-rtl.css
wordpress/wp-includes/blocks/term-description/style.css
wordpress/wp-includes/blocks/code/
wordpress/wp-includes/blocks/code/editor.min.css
wordpress/wp-includes/blocks/code/style-rtl.min.css
wordpress/wp-includes/blocks/code/theme.css
wordpress/wp-includes/blocks/code/block.json
wordpress/wp-includes/blocks/code/theme-rtl.min.css
wordpress/wp-includes/blocks/code/editor.css
wordpress/wp-includes/blocks/code/theme.min.css
wordpress/wp-includes/blocks/code/style.min.css
wordpress/wp-includes/blocks/code/theme-rtl.css
wordpress/wp-includes/blocks/code/editor-rtl.css
wordpress/wp-includes/blocks/code/editor-rtl.min.css
wordpress/wp-includes/blocks/code/style-rtl.css
wordpress/wp-includes/blocks/code/style.css
wordpress/wp-includes/blocks/comment-date.php
wordpress/wp-includes/blocks/footnotes/
wordpress/wp-includes/blocks/footnotes/style-rtl.min.css
wordpress/wp-includes/blocks/footnotes/block.json
wordpress/wp-includes/blocks/footnotes/style.min.css
wordpress/wp-includes/blocks/footnotes/style-rtl.css
wordpress/wp-includes/blocks/footnotes/style.css
wordpress/wp-includes/blocks/comments-pagination.php
wordpress/wp-includes/blocks/loginout/
wordpress/wp-includes/blocks/loginout/block.json
wordpress/wp-includes/blocks/avatar/
wordpress/wp-includes/blocks/avatar/editor.min.css
wordpress/wp-includes/blocks/avatar/style-rtl.min.css
wordpress/wp-includes/blocks/avatar/block.json
wordpress/wp-includes/blocks/avatar/editor.css
wordpress/wp-includes/blocks/avatar/style.min.css
wordpress/wp-includes/blocks/avatar/editor-rtl.css
wordpress/wp-includes/blocks/avatar/editor-rtl.min.css
wordpress/wp-includes/blocks/avatar/style-rtl.css
wordpress/wp-includes/blocks/avatar/style.css
wordpress/wp-includes/blocks/button/
wordpress/wp-includes/blocks/button/editor.min.css
wordpress/wp-includes/blocks/button/style-rtl.min.css
wordpress/wp-includes/blocks/button/block.json
wordpress/wp-includes/blocks/button/editor.css
wordpress/wp-includes/blocks/button/style.min.css
wordpress/wp-includes/blocks/button/editor-rtl.css
wordpress/wp-includes/blocks/button/editor-rtl.min.css
wordpress/wp-includes/blocks/button/style-rtl.css
wordpress/wp-includes/blocks/button/style.css
wordpress/wp-includes/blocks/comments-title/
wordpress/wp-includes/blocks/comments-title/editor.min.css
wordpress/wp-includes/blocks/comments-title/block.json
wordpress/wp-includes/blocks/comments-title/editor.css
wordpress/wp-includes/blocks/comments-title/editor-rtl.css
wordpress/wp-includes/blocks/comments-title/editor-rtl.min.css
wordpress/wp-includes/blocks/image.php
wordpress/wp-includes/blocks/widget-group.php
wordpress/wp-includes/blocks/comments-pagination-numbers.php
wordpress/wp-includes/blocks/post-author.php
wordpress/wp-includes/blocks/post-author-biography/
wordpress/wp-includes/blocks/post-author-biography/block.json
wordpress/wp-includes/blocks/categories/
wordpress/wp-includes/blocks/categories/editor.min.css
wordpress/wp-includes/blocks/categories/style-rtl.min.css
wordpress/wp-includes/blocks/categories/block.json
wordpress/wp-includes/blocks/categories/editor.css
wordpress/wp-includes/blocks/categories/style.min.css
wordpress/wp-includes/blocks/categories/editor-rtl.css
wordpress/wp-includes/blocks/categories/editor-rtl.min.css
wordpress/wp-includes/blocks/categories/style-rtl.css
wordpress/wp-includes/blocks/categories/style.css
wordpress/wp-includes/blocks/social-link/
wordpress/wp-includes/blocks/social-link/editor.min.css
wordpress/wp-includes/blocks/social-link/block.json
wordpress/wp-includes/blocks/social-link/editor.css
wordpress/wp-includes/blocks/social-link/editor-rtl.css
wordpress/wp-includes/blocks/social-link/editor-rtl.min.css
wordpress/wp-includes/blocks/separator/
wordpress/wp-includes/blocks/separator/editor.min.css
wordpress/wp-includes/blocks/separator/style-rtl.min.css
wordpress/wp-includes/blocks/separator/theme.css
wordpress/wp-includes/blocks/separator/block.json
wordpress/wp-includes/blocks/separator/theme-rtl.min.css
wordpress/wp-includes/blocks/separator/editor.css
wordpress/wp-includes/blocks/separator/theme.min.css
wordpress/wp-includes/blocks/separator/style.min.css
wordpress/wp-includes/blocks/separator/theme-rtl.css
wordpress/wp-includes/blocks/separator/editor-rtl.css
wordpress/wp-includes/blocks/separator/editor-rtl.min.css
wordpress/wp-includes/blocks/separator/style-rtl.css
wordpress/wp-includes/blocks/separator/style.css
wordpress/wp-includes/blocks/html/
wordpress/wp-includes/blocks/html/editor.min.css
wordpress/wp-includes/blocks/html/block.json
wordpress/wp-includes/blocks/html/editor.css
wordpress/wp-includes/blocks/html/editor-rtl.css
wordpress/wp-includes/blocks/html/editor-rtl.min.css
wordpress/wp-includes/blocks/page-list/
wordpress/wp-includes/blocks/page-list/editor.min.css
wordpress/wp-includes/blocks/page-list/style-rtl.min.css
wordpress/wp-includes/blocks/page-list/block.json
wordpress/wp-includes/blocks/page-list/editor.css
wordpress/wp-includes/blocks/page-list/style.min.css
wordpress/wp-includes/blocks/page-list/editor-rtl.css
wordpress/wp-includes/blocks/page-list/editor-rtl.min.css
wordpress/wp-includes/blocks/page-list/style-rtl.css
wordpress/wp-includes/blocks/page-list/style.css
wordpress/wp-includes/blocks/home-link/
wordpress/wp-includes/blocks/home-link/block.json
wordpress/wp-includes/blocks/pattern/
wordpress/wp-includes/blocks/pattern/block.json
wordpress/wp-includes/blocks/social-link.php
wordpress/wp-includes/blocks/require-static-blocks.php
wordpress/wp-includes/blocks/query-pagination-previous/
wordpress/wp-includes/blocks/query-pagination-previous/block.json
wordpress/wp-includes/blocks/widget-group/
wordpress/wp-includes/blocks/widget-group/block.json
wordpress/wp-includes/blocks/freeform/
wordpress/wp-includes/blocks/freeform/editor.min.css
wordpress/wp-includes/blocks/freeform/block.json
wordpress/wp-includes/blocks/freeform/editor.css
wordpress/wp-includes/blocks/freeform/editor-rtl.css
wordpress/wp-includes/blocks/freeform/editor-rtl.min.css
wordpress/wp-includes/blocks/audio/
wordpress/wp-includes/blocks/audio/editor.min.css
wordpress/wp-includes/blocks/audio/style-rtl.min.css
wordpress/wp-includes/blocks/audio/theme.css
wordpress/wp-includes/blocks/audio/block.json
wordpress/wp-includes/blocks/audio/theme-rtl.min.css
wordpress/wp-includes/blocks/audio/editor.css
wordpress/wp-includes/blocks/audio/theme.min.css
wordpress/wp-includes/blocks/audio/style.min.css
wordpress/wp-includes/blocks/audio/theme-rtl.css
wordpress/wp-includes/blocks/audio/editor-rtl.css
wordpress/wp-includes/blocks/audio/editor-rtl.min.css
wordpress/wp-includes/blocks/audio/style-rtl.css
wordpress/wp-includes/blocks/audio/style.css
wordpress/wp-includes/blocks/query/
wordpress/wp-includes/blocks/query/editor.min.css
wordpress/wp-includes/blocks/query/block.json
wordpress/wp-includes/blocks/query/editor.css
wordpress/wp-includes/blocks/query/view.min.asset.php
wordpress/wp-includes/blocks/query/view.js
wordpress/wp-includes/blocks/query/editor-rtl.css
wordpress/wp-includes/blocks/query/view.asset.php
wordpress/wp-includes/blocks/query/editor-rtl.min.css
wordpress/wp-includes/blocks/query/view.min.js
wordpress/wp-includes/blocks/blocks-json.php
wordpress/wp-includes/blocks/home-link.php
wordpress/wp-includes/blocks/post-excerpt.php
wordpress/wp-includes/blocks/post-author-name.php
wordpress/wp-includes/blocks/site-tagline/
wordpress/wp-includes/blocks/site-tagline/editor.min.css
wordpress/wp-includes/blocks/site-tagline/block.json
wordpress/wp-includes/blocks/site-tagline/editor.css
wordpress/wp-includes/blocks/site-tagline/editor-rtl.css
wordpress/wp-includes/blocks/site-tagline/editor-rtl.min.css
wordpress/wp-includes/blocks/verse/
wordpress/wp-includes/blocks/verse/style-rtl.min.css
wordpress/wp-includes/blocks/verse/block.json
wordpress/wp-includes/blocks/verse/style.min.css
wordpress/wp-includes/blocks/verse/style-rtl.css
wordpress/wp-includes/blocks/verse/style.css
wordpress/wp-includes/blocks/site-logo/
wordpress/wp-includes/blocks/site-logo/editor.min.css
wordpress/wp-includes/blocks/site-logo/style-rtl.min.css
wordpress/wp-includes/blocks/site-logo/block.json
wordpress/wp-includes/blocks/site-logo/editor.css
wordpress/wp-includes/blocks/site-logo/style.min.css
wordpress/wp-includes/blocks/site-logo/editor-rtl.css
wordpress/wp-includes/blocks/site-logo/editor-rtl.min.css
wordpress/wp-includes/blocks/site-logo/style-rtl.css
wordpress/wp-includes/blocks/site-logo/style.css
wordpress/wp-includes/blocks/query.php
wordpress/wp-includes/blocks/site-title/
wordpress/wp-includes/blocks/site-title/editor.min.css
wordpress/wp-includes/blocks/site-title/style-rtl.min.css
wordpress/wp-includes/blocks/site-title/block.json
wordpress/wp-includes/blocks/site-title/editor.css
wordpress/wp-includes/blocks/site-title/style.min.css
wordpress/wp-includes/blocks/site-title/editor-rtl.css
wordpress/wp-includes/blocks/site-title/editor-rtl.min.css
wordpress/wp-includes/blocks/site-title/style-rtl.css
wordpress/wp-includes/blocks/site-title/style.css
wordpress/wp-includes/blocks/page-list.php
wordpress/wp-includes/blocks/search.php
wordpress/wp-includes/blocks/query-no-results/
wordpress/wp-includes/blocks/query-no-results/block.json
wordpress/wp-includes/blocks/heading/
wordpress/wp-includes/blocks/heading/style-rtl.min.css
wordpress/wp-includes/blocks/heading/block.json
wordpress/wp-includes/blocks/heading/style.min.css
wordpress/wp-includes/blocks/heading/style-rtl.css
wordpress/wp-includes/blocks/heading/style.css
wordpress/wp-includes/blocks/block.php
wordpress/wp-includes/blocks/pullquote/
wordpress/wp-includes/blocks/pullquote/editor.min.css
wordpress/wp-includes/blocks/pullquote/style-rtl.min.css
wordpress/wp-includes/blocks/pullquote/theme.css
wordpress/wp-includes/blocks/pullquote/block.json
wordpress/wp-includes/blocks/pullquote/theme-rtl.min.css
wordpress/wp-includes/blocks/pullquote/editor.css
wordpress/wp-includes/blocks/pullquote/theme.min.css
wordpress/wp-includes/blocks/pullquote/style.min.css
wordpress/wp-includes/blocks/pullquote/theme-rtl.css
wordpress/wp-includes/blocks/pullquote/editor-rtl.css
wordpress/wp-includes/blocks/pullquote/editor-rtl.min.css
wordpress/wp-includes/blocks/pullquote/style-rtl.css
wordpress/wp-includes/blocks/pullquote/style.css
wordpress/wp-includes/blocks/buttons/
wordpress/wp-includes/blocks/buttons/editor.min.css
wordpress/wp-includes/blocks/buttons/style-rtl.min.css
wordpress/wp-includes/blocks/buttons/block.json
wordpress/wp-includes/blocks/buttons/editor.css
wordpress/wp-includes/blocks/buttons/style.min.css
wordpress/wp-includes/blocks/buttons/editor-rtl.css
wordpress/wp-includes/blocks/buttons/editor-rtl.min.css
wordpress/wp-includes/blocks/buttons/style-rtl.css
wordpress/wp-includes/blocks/buttons/style.css
wordpress/wp-includes/blocks/post-featured-image.php
wordpress/wp-includes/blocks/post-terms.php
wordpress/wp-includes/blocks/rss.php
wordpress/wp-includes/blocks/nextpage/
wordpress/wp-includes/blocks/nextpage/editor.min.css
wordpress/wp-includes/blocks/nextpage/block.json
wordpress/wp-includes/blocks/nextpage/editor.css
wordpress/wp-includes/blocks/nextpage/editor-rtl.css
wordpress/wp-includes/blocks/nextpage/editor-rtl.min.css
wordpress/wp-includes/blocks/paragraph/
wordpress/wp-includes/blocks/paragraph/editor.min.css
wordpress/wp-includes/blocks/paragraph/style-rtl.min.css
wordpress/wp-includes/blocks/paragraph/block.json
wordpress/wp-includes/blocks/paragraph/editor.css
wordpress/wp-includes/blocks/paragraph/style.min.css
wordpress/wp-includes/blocks/paragraph/editor-rtl.css
wordpress/wp-includes/blocks/paragraph/editor-rtl.min.css
wordpress/wp-includes/blocks/paragraph/style-rtl.css
wordpress/wp-includes/blocks/paragraph/style.css
wordpress/wp-includes/blocks/media-text.php
wordpress/wp-includes/blocks/footnotes.php
wordpress/wp-includes/blocks/navigation-submenu/
wordpress/wp-includes/blocks/navigation-submenu/editor.min.css
wordpress/wp-includes/blocks/navigation-submenu/block.json
wordpress/wp-includes/blocks/navigation-submenu/editor.css
wordpress/wp-includes/blocks/navigation-submenu/editor-rtl.css
wordpress/wp-includes/blocks/navigation-submenu/editor-rtl.min.css
wordpress/wp-includes/blocks/archives/
wordpress/wp-includes/blocks/archives/editor.min.css
wordpress/wp-includes/blocks/archives/style-rtl.min.css
wordpress/wp-includes/blocks/archives/block.json
wordpress/wp-includes/blocks/archives/editor.css
wordpress/wp-includes/blocks/archives/style.min.css
wordpress/wp-includes/blocks/archives/editor-rtl.css
wordpress/wp-includes/blocks/archives/editor-rtl.min.css
wordpress/wp-includes/blocks/archives/style-rtl.css
wordpress/wp-includes/blocks/archives/style.css
wordpress/wp-includes/blocks/post-template/
wordpress/wp-includes/blocks/post-template/editor.min.css
wordpress/wp-includes/blocks/post-template/style-rtl.min.css
wordpress/wp-includes/blocks/post-template/block.json
wordpress/wp-includes/blocks/post-template/editor.css
wordpress/wp-includes/blocks/post-template/style.min.css
wordpress/wp-includes/blocks/post-template/editor-rtl.css
wordpress/wp-includes/blocks/post-template/editor-rtl.min.css
wordpress/wp-includes/blocks/post-template/style-rtl.css
wordpress/wp-includes/blocks/post-template/style.css
wordpress/wp-includes/blocks/query-pagination/
wordpress/wp-includes/blocks/query-pagination/editor.min.css
wordpress/wp-includes/blocks/query-pagination/style-rtl.min.css
wordpress/wp-includes/blocks/query-pagination/block.json
wordpress/wp-includes/blocks/query-pagination/editor.css
wordpress/wp-includes/blocks/query-pagination/style.min.css
wordpress/wp-includes/blocks/query-pagination/editor-rtl.css
wordpress/wp-includes/blocks/query-pagination/editor-rtl.min.css
wordpress/wp-includes/blocks/query-pagination/style-rtl.css
wordpress/wp-includes/blocks/query-pagination/style.css
wordpress/wp-includes/blocks/post-comments-form.php
wordpress/wp-includes/blocks/embed/
wordpress/wp-includes/blocks/embed/editor.min.css
wordpress/wp-includes/blocks/embed/style-rtl.min.css
wordpress/wp-includes/blocks/embed/theme.css
wordpress/wp-includes/blocks/embed/block.json
wordpress/wp-includes/blocks/embed/theme-rtl.min.css
wordpress/wp-includes/blocks/embed/editor.css
wordpress/wp-includes/blocks/embed/theme.min.css
wordpress/wp-includes/blocks/embed/style.min.css
wordpress/wp-includes/blocks/embed/theme-rtl.css
wordpress/wp-includes/blocks/embed/editor-rtl.css
wordpress/wp-includes/blocks/embed/editor-rtl.min.css
wordpress/wp-includes/blocks/embed/style-rtl.css
wordpress/wp-includes/blocks/embed/style.css
wordpress/wp-includes/blocks/archives.php
wordpress/wp-includes/blocks/navigation-submenu.php
wordpress/wp-includes/blocks/block/
wordpress/wp-includes/blocks/block/block.json
wordpress/wp-includes/blocks/post-featured-image/
wordpress/wp-includes/blocks/post-featured-image/editor.min.css
wordpress/wp-includes/blocks/post-featured-image/style-rtl.min.css
wordpress/wp-includes/blocks/post-featured-image/block.json
wordpress/wp-includes/blocks/post-featured-image/editor.css
wordpress/wp-includes/blocks/post-featured-image/style.min.css
wordpress/wp-includes/blocks/post-featured-image/editor-rtl.css
wordpress/wp-includes/blocks/post-featured-image/editor-rtl.min.css
wordpress/wp-includes/blocks/post-featured-image/style-rtl.css
wordpress/wp-includes/blocks/post-featured-image/style.css
wordpress/wp-includes/blocks/comment-content.php
wordpress/wp-includes/blocks/media-text/
wordpress/wp-includes/blocks/media-text/editor.min.css
wordpress/wp-includes/blocks/media-text/style-rtl.min.css
wordpress/wp-includes/blocks/media-text/block.json
wordpress/wp-includes/blocks/media-text/editor.css
wordpress/wp-includes/blocks/media-text/style.min.css
wordpress/wp-includes/blocks/media-text/editor-rtl.css
wordpress/wp-includes/blocks/media-text/editor-rtl.min.css
wordpress/wp-includes/blocks/media-text/style-rtl.css
wordpress/wp-includes/blocks/media-text/style.css
wordpress/wp-includes/blocks/page-list-item/
wordpress/wp-includes/blocks/page-list-item/block.json
wordpress/wp-includes/blocks/column/
wordpress/wp-includes/blocks/column/block.json
wordpress/wp-includes/blocks/categories.php
wordpress/wp-includes/blocks/comment-edit-link/
wordpress/wp-includes/blocks/comment-edit-link/block.json
wordpress/wp-includes/blocks/rss/
wordpress/wp-includes/blocks/rss/editor.min.css
wordpress/wp-includes/blocks/rss/style-rtl.min.css
wordpress/wp-includes/blocks/rss/block.json
wordpress/wp-includes/blocks/rss/editor.css
wordpress/wp-includes/blocks/rss/style.min.css
wordpress/wp-includes/blocks/rss/editor-rtl.css
wordpress/wp-includes/blocks/rss/editor-rtl.min.css
wordpress/wp-includes/blocks/rss/style-rtl.css
wordpress/wp-includes/blocks/rss/style.css
wordpress/wp-includes/blocks/comments-pagination/
wordpress/wp-includes/blocks/comments-pagination/editor.min.css
wordpress/wp-includes/blocks/comments-pagination/style-rtl.min.css
wordpress/wp-includes/blocks/comments-pagination/block.json
wordpress/wp-includes/blocks/comments-pagination/editor.css
wordpress/wp-includes/blocks/comments-pagination/style.min.css
wordpress/wp-includes/blocks/comments-pagination/editor-rtl.css
wordpress/wp-includes/blocks/comments-pagination/editor-rtl.min.css
wordpress/wp-includes/blocks/comments-pagination/style-rtl.css
wordpress/wp-includes/blocks/comments-pagination/style.css
wordpress/wp-includes/blocks/comment-date/
wordpress/wp-includes/blocks/comment-date/block.json
wordpress/wp-includes/blocks/query-title/
wordpress/wp-includes/blocks/query-title/style-rtl.min.css
wordpress/wp-includes/blocks/query-title/block.json
wordpress/wp-includes/blocks/query-title/style.min.css
wordpress/wp-includes/blocks/query-title/style-rtl.css
wordpress/wp-includes/blocks/query-title/style.css
wordpress/wp-includes/blocks/comments-pagination-previous.php
wordpress/wp-includes/blocks/post-navigation-link.php
wordpress/wp-includes/blocks/quote/
wordpress/wp-includes/blocks/quote/style-rtl.min.css
wordpress/wp-includes/blocks/quote/theme.css
wordpress/wp-includes/blocks/quote/block.json
wordpress/wp-includes/blocks/quote/theme-rtl.min.css
wordpress/wp-includes/blocks/quote/theme.min.css
wordpress/wp-includes/blocks/quote/style.min.css
wordpress/wp-includes/blocks/quote/theme-rtl.css
wordpress/wp-includes/blocks/quote/style-rtl.css
wordpress/wp-includes/blocks/quote/style.css
wordpress/wp-includes/blocks/more/
wordpress/wp-includes/blocks/more/editor.min.css
wordpress/wp-includes/blocks/more/block.json
wordpress/wp-includes/blocks/more/editor.css
wordpress/wp-includes/blocks/more/editor-rtl.css
wordpress/wp-includes/blocks/more/editor-rtl.min.css
wordpress/wp-includes/blocks/read-more/
wordpress/wp-includes/blocks/read-more/style-rtl.min.css
wordpress/wp-includes/blocks/read-more/block.json
wordpress/wp-includes/blocks/read-more/style.min.css
wordpress/wp-includes/blocks/read-more/style-rtl.css
wordpress/wp-includes/blocks/read-more/style.css
wordpress/wp-includes/blocks/query-no-results.php
wordpress/wp-includes/blocks/post-date/
wordpress/wp-includes/blocks/post-date/style-rtl.min.css
wordpress/wp-includes/blocks/post-date/block.json
wordpress/wp-includes/blocks/post-date/style.min.css
wordpress/wp-includes/blocks/post-date/style-rtl.css
wordpress/wp-includes/blocks/post-date/style.css
wordpress/wp-includes/blocks/query-pagination-numbers.php
wordpress/wp-includes/blocks/tag-cloud/
wordpress/wp-includes/blocks/tag-cloud/style-rtl.min.css
wordpress/wp-includes/blocks/tag-cloud/block.json
wordpress/wp-includes/blocks/tag-cloud/style.min.css
wordpress/wp-includes/blocks/tag-cloud/style-rtl.css
wordpress/wp-includes/blocks/tag-cloud/style.css
wordpress/wp-includes/blocks/legacy-widget.php
wordpress/wp-includes/blocks/comment-edit-link.php
wordpress/wp-includes/blocks/missing/
wordpress/wp-includes/blocks/missing/block.json
wordpress/wp-includes/blocks/post-title/
wordpress/wp-includes/blocks/post-title/style-rtl.min.css
wordpress/wp-includes/blocks/post-title/block.json
wordpress/wp-includes/blocks/post-title/style.min.css
wordpress/wp-includes/blocks/post-title/style-rtl.css
wordpress/wp-includes/blocks/post-title/style.css
wordpress/wp-includes/blocks/index.php
wordpress/wp-includes/blocks/social-links/
wordpress/wp-includes/blocks/social-links/editor.min.css
wordpress/wp-includes/blocks/social-links/style-rtl.min.css
wordpress/wp-includes/blocks/social-links/block.json
wordpress/wp-includes/blocks/social-links/editor.css
wordpress/wp-includes/blocks/social-links/style.min.css
wordpress/wp-includes/blocks/social-links/editor-rtl.css
wordpress/wp-includes/blocks/social-links/editor-rtl.min.css
wordpress/wp-includes/blocks/social-links/style-rtl.css
wordpress/wp-includes/blocks/social-links/style.css
wordpress/wp-includes/blocks/page-list-item.php
wordpress/wp-includes/blocks/gallery.php
wordpress/wp-includes/blocks/query-pagination-next.php
wordpress/wp-includes/blocks/post-excerpt/
wordpress/wp-includes/blocks/post-excerpt/editor.min.css
wordpress/wp-includes/blocks/post-excerpt/style-rtl.min.css
wordpress/wp-includes/blocks/post-excerpt/block.json
wordpress/wp-includes/blocks/post-excerpt/editor.css
wordpress/wp-includes/blocks/post-excerpt/style.min.css
wordpress/wp-includes/blocks/post-excerpt/editor-rtl.css
wordpress/wp-includes/blocks/post-excerpt/editor-rtl.min.css
wordpress/wp-includes/blocks/post-excerpt/style-rtl.css
wordpress/wp-includes/blocks/post-excerpt/style.css
wordpress/wp-includes/blocks/preformatted/
wordpress/wp-includes/blocks/preformatted/style-rtl.min.css
wordpress/wp-includes/blocks/preformatted/block.json
wordpress/wp-includes/blocks/preformatted/style.min.css
wordpress/wp-includes/blocks/preformatted/style-rtl.css
wordpress/wp-includes/blocks/preformatted/style.css
wordpress/wp-includes/blocks/latest-posts.php
wordpress/wp-includes/blocks/latest-comments/
wordpress/wp-includes/blocks/latest-comments/style-rtl.min.css
wordpress/wp-includes/blocks/latest-comments/block.json
wordpress/wp-includes/blocks/latest-comments/style.min.css
wordpress/wp-includes/blocks/latest-comments/style-rtl.css
wordpress/wp-includes/blocks/latest-comments/style.css
wordpress/wp-includes/blocks/comments-pagination-previous/
wordpress/wp-includes/blocks/comments-pagination-previous/block.json
wordpress/wp-includes/blocks/comment-author-name.php
wordpress/wp-includes/blocks/comments-pagination-next/
wordpress/wp-includes/blocks/comments-pagination-next/block.json
wordpress/wp-includes/blocks/read-more.php
wordpress/wp-includes/blocks/cover.php
wordpress/wp-includes/blocks/search/
wordpress/wp-includes/blocks/search/editor.min.css
wordpress/wp-includes/blocks/search/style-rtl.min.css
wordpress/wp-includes/blocks/search/theme.css
wordpress/wp-includes/blocks/search/block.json
wordpress/wp-includes/blocks/search/theme-rtl.min.css
wordpress/wp-includes/blocks/search/editor.css
wordpress/wp-includes/blocks/search/view.min.asset.php
wordpress/wp-includes/blocks/search/view.js
wordpress/wp-includes/blocks/search/theme.min.css
wordpress/wp-includes/blocks/search/style.min.css
wordpress/wp-includes/blocks/search/theme-rtl.css
wordpress/wp-includes/blocks/search/editor-rtl.css
wordpress/wp-includes/blocks/search/view.asset.php
wordpress/wp-includes/blocks/search/editor-rtl.min.css
wordpress/wp-includes/blocks/search/view.min.js
wordpress/wp-includes/blocks/search/style-rtl.css
wordpress/wp-includes/blocks/search/style.css
wordpress/wp-includes/blocks/query-pagination-previous.php
wordpress/wp-includes/blocks/list-item/
wordpress/wp-includes/blocks/list-item/block.json
wordpress/wp-includes/blocks/navigation-link/
wordpress/wp-includes/blocks/navigation-link/editor.min.css
wordpress/wp-includes/blocks/navigation-link/style-rtl.min.css
wordpress/wp-includes/blocks/navigation-link/block.json
wordpress/wp-includes/blocks/navigation-link/editor.css
wordpress/wp-includes/blocks/navigation-link/style.min.css
wordpress/wp-includes/blocks/navigation-link/editor-rtl.css
wordpress/wp-includes/blocks/navigation-link/editor-rtl.min.css
wordpress/wp-includes/blocks/navigation-link/style-rtl.css
wordpress/wp-includes/blocks/navigation-link/style.css
wordpress/wp-includes/blocks/latest-posts/
wordpress/wp-includes/blocks/latest-posts/editor.min.css
wordpress/wp-includes/blocks/latest-posts/style-rtl.min.css
wordpress/wp-includes/blocks/latest-posts/block.json
wordpress/wp-includes/blocks/latest-posts/editor.css
wordpress/wp-includes/blocks/latest-posts/style.min.css
wordpress/wp-includes/blocks/latest-posts/editor-rtl.css
wordpress/wp-includes/blocks/latest-posts/editor-rtl.min.css
wordpress/wp-includes/blocks/latest-posts/style-rtl.css
wordpress/wp-includes/blocks/latest-posts/style.css
wordpress/wp-includes/blocks/template-part.php
wordpress/wp-includes/blocks/post-comments-form/
wordpress/wp-includes/blocks/post-comments-form/editor.min.css
wordpress/wp-includes/blocks/post-comments-form/style-rtl.min.css
wordpress/wp-includes/blocks/post-comments-form/block.json
wordpress/wp-includes/blocks/post-comments-form/editor.css
wordpress/wp-includes/blocks/post-comments-form/style.min.css
wordpress/wp-includes/blocks/post-comments-form/editor-rtl.css
wordpress/wp-includes/blocks/post-comments-form/editor-rtl.min.css
wordpress/wp-includes/blocks/post-comments-form/style-rtl.css
wordpress/wp-includes/blocks/post-comments-form/style.css
wordpress/wp-includes/blocks/post-author-biography.php
wordpress/wp-includes/blocks/term-description.php
wordpress/wp-includes/blocks/group/
wordpress/wp-includes/blocks/group/editor.min.css
wordpress/wp-includes/blocks/group/style-rtl.min.css
wordpress/wp-includes/blocks/group/theme.css
wordpress/wp-includes/blocks/group/block.json
wordpress/wp-includes/blocks/group/theme-rtl.min.css
wordpress/wp-includes/blocks/group/editor.css
wordpress/wp-includes/blocks/group/theme.min.css
wordpress/wp-includes/blocks/group/style.min.css
wordpress/wp-includes/blocks/group/theme-rtl.css
wordpress/wp-includes/blocks/group/editor-rtl.css
wordpress/wp-includes/blocks/group/editor-rtl.min.css
wordpress/wp-includes/blocks/group/style-rtl.css
wordpress/wp-includes/blocks/group/style.css
wordpress/wp-includes/blocks/post-terms/
wordpress/wp-includes/blocks/post-terms/style-rtl.min.css
wordpress/wp-includes/blocks/post-terms/block.json
wordpress/wp-includes/blocks/post-terms/style.min.css
wordpress/wp-includes/blocks/post-terms/style-rtl.css
wordpress/wp-includes/blocks/post-terms/style.css
wordpress/wp-includes/blocks/pattern.php
wordpress/wp-includes/blocks/heading.php
wordpress/wp-includes/blocks/avatar.php
wordpress/wp-includes/blocks/table/
wordpress/wp-includes/blocks/table/editor.min.css
wordpress/wp-includes/blocks/table/style-rtl.min.css
wordpress/wp-includes/blocks/table/theme.css
wordpress/wp-includes/blocks/table/block.json
wordpress/wp-includes/blocks/table/theme-rtl.min.css
wordpress/wp-includes/blocks/table/editor.css
wordpress/wp-includes/blocks/table/theme.min.css
wordpress/wp-includes/blocks/table/style.min.css
wordpress/wp-includes/blocks/table/theme-rtl.css
wordpress/wp-includes/blocks/table/editor-rtl.css
wordpress/wp-includes/blocks/table/editor-rtl.min.css
wordpress/wp-includes/blocks/table/style-rtl.css
wordpress/wp-includes/blocks/table/style.css
wordpress/wp-includes/blocks/comments.php
wordpress/wp-includes/blocks/list/
wordpress/wp-includes/blocks/list/style-rtl.min.css
wordpress/wp-includes/blocks/list/block.json
wordpress/wp-includes/blocks/list/style.min.css
wordpress/wp-includes/blocks/list/style-rtl.css
wordpress/wp-includes/blocks/list/style.css
wordpress/wp-includes/blocks/comment-author-name/
wordpress/wp-includes/blocks/comment-author-name/block.json
wordpress/wp-includes/blocks/file.php
wordpress/wp-includes/blocks/comments-pagination-numbers/
wordpress/wp-includes/blocks/comments-pagination-numbers/editor.min.css
wordpress/wp-includes/blocks/comments-pagination-numbers/block.json
wordpress/wp-includes/blocks/comments-pagination-numbers/editor.css
wordpress/wp-includes/blocks/comments-pagination-numbers/editor-rtl.css
wordpress/wp-includes/blocks/comments-pagination-numbers/editor-rtl.min.css
wordpress/wp-includes/blocks/comment-template.php
wordpress/wp-includes/blocks/query-pagination-next/
wordpress/wp-includes/blocks/query-pagination-next/block.json
wordpress/wp-includes/blocks/file/
wordpress/wp-includes/blocks/file/editor.min.css
wordpress/wp-includes/blocks/file/style-rtl.min.css
wordpress/wp-includes/blocks/file/block.json
wordpress/wp-includes/blocks/file/editor.css
wordpress/wp-includes/blocks/file/view.min.asset.php
wordpress/wp-includes/blocks/file/view.js
wordpress/wp-includes/blocks/file/style.min.css
wordpress/wp-includes/blocks/file/editor-rtl.css
wordpress/wp-includes/blocks/file/view.asset.php
wordpress/wp-includes/blocks/file/editor-rtl.min.css
wordpress/wp-includes/blocks/file/view.min.js
wordpress/wp-includes/blocks/file/style-rtl.css
wordpress/wp-includes/blocks/file/style.css
wordpress/wp-includes/blocks/image/
wordpress/wp-includes/blocks/image/editor.min.css
wordpress/wp-includes/blocks/image/style-rtl.min.css
wordpress/wp-includes/blocks/image/theme.css
wordpress/wp-includes/blocks/image/block.json
wordpress/wp-includes/blocks/image/theme-rtl.min.css
wordpress/wp-includes/blocks/image/editor.css
wordpress/wp-includes/blocks/image/view.min.asset.php
wordpress/wp-includes/blocks/image/view.js
wordpress/wp-includes/blocks/image/theme.min.css
wordpress/wp-includes/blocks/image/style.min.css
wordpress/wp-includes/blocks/image/theme-rtl.css
wordpress/wp-includes/blocks/image/editor-rtl.css
wordpress/wp-includes/blocks/image/view.asset.php
wordpress/wp-includes/blocks/image/editor-rtl.min.css
wordpress/wp-includes/blocks/image/view.min.js
wordpress/wp-includes/blocks/image/style-rtl.css
wordpress/wp-includes/blocks/image/style.css
wordpress/wp-includes/blocks/navigation.php
wordpress/wp-includes/blocks/query-title.php
wordpress/wp-includes/blocks/comments-title.php
wordpress/wp-includes/blocks/query-pagination.php
wordpress/wp-includes/blocks/text-columns/
wordpress/wp-includes/blocks/text-columns/editor.min.css
wordpress/wp-includes/blocks/text-columns/style-rtl.min.css
wordpress/wp-includes/blocks/text-columns/block.json
wordpress/wp-includes/blocks/text-columns/editor.css
wordpress/wp-includes/blocks/text-columns/style.min.css
wordpress/wp-includes/blocks/text-columns/editor-rtl.css
wordpress/wp-includes/blocks/text-columns/editor-rtl.min.css
wordpress/wp-includes/blocks/text-columns/style-rtl.css
wordpress/wp-includes/blocks/text-columns/style.css
wordpress/wp-includes/blocks/comment-template/
wordpress/wp-includes/blocks/comment-template/style-rtl.min.css
wordpress/wp-includes/blocks/comment-template/block.json
wordpress/wp-includes/blocks/comment-template/style.min.css
wordpress/wp-includes/blocks/comment-template/style-rtl.css
wordpress/wp-includes/blocks/comment-template/style.css
wordpress/wp-includes/blocks/video/
wordpress/wp-includes/blocks/video/editor.min.css
wordpress/wp-includes/blocks/video/style-rtl.min.css
wordpress/wp-includes/blocks/video/theme.css
wordpress/wp-includes/blocks/video/block.json
wordpress/wp-includes/blocks/video/theme-rtl.min.css
wordpress/wp-includes/blocks/video/editor.css
wordpress/wp-includes/blocks/video/theme.min.css
wordpress/wp-includes/blocks/video/style.min.css
wordpress/wp-includes/blocks/video/theme-rtl.css
wordpress/wp-includes/blocks/video/editor-rtl.css
wordpress/wp-includes/blocks/video/editor-rtl.min.css
wordpress/wp-includes/blocks/video/style-rtl.css
wordpress/wp-includes/blocks/video/style.css
wordpress/wp-includes/blocks/cover/
wordpress/wp-includes/blocks/cover/editor.min.css
wordpress/wp-includes/blocks/cover/style-rtl.min.css
wordpress/wp-includes/blocks/cover/block.json
wordpress/wp-includes/blocks/cover/editor.css
wordpress/wp-includes/blocks/cover/style.min.css
wordpress/wp-includes/blocks/cover/editor-rtl.css
wordpress/wp-includes/blocks/cover/editor-rtl.min.css
wordpress/wp-includes/blocks/cover/style-rtl.css
wordpress/wp-includes/blocks/cover/style.css
wordpress/wp-includes/blocks/post-template.php
wordpress/wp-includes/blocks/post-date.php
wordpress/wp-includes/blocks/post-author/
wordpress/wp-includes/blocks/post-author/style-rtl.min.css
wordpress/wp-includes/blocks/post-author/block.json
wordpress/wp-includes/blocks/post-author/style.min.css
wordpress/wp-includes/blocks/post-author/style-rtl.css
wordpress/wp-includes/blocks/post-author/style.css
wordpress/wp-includes/blocks/comment-reply-link.php
wordpress/wp-includes/blocks/tag-cloud.php
wordpress/wp-includes/blocks/site-logo.php
wordpress/wp-includes/blocks/legacy-widget/
wordpress/wp-includes/blocks/legacy-widget/block.json
wordpress/wp-includes/blocks/spacer/
wordpress/wp-includes/blocks/spacer/editor.min.css
wordpress/wp-includes/blocks/spacer/style-rtl.min.css
wordpress/wp-includes/blocks/spacer/block.json
wordpress/wp-includes/blocks/spacer/editor.css
wordpress/wp-includes/blocks/spacer/style.min.css
wordpress/wp-includes/blocks/spacer/editor-rtl.css
wordpress/wp-includes/blocks/spacer/editor-rtl.min.css
wordpress/wp-includes/blocks/spacer/style-rtl.css
wordpress/wp-includes/blocks/spacer/style.css
wordpress/wp-includes/class-wp-block-parser.php
wordpress/wp-includes/class-wp-plugin-dependencies.php
wordpress/wp-includes/pomo/
wordpress/wp-includes/pomo/translations.php
wordpress/wp-includes/pomo/plural-forms.php
wordpress/wp-includes/pomo/streams.php
wordpress/wp-includes/pomo/entry.php
wordpress/wp-includes/pomo/mo.php
wordpress/wp-includes/pomo/po.php
wordpress/wp-includes/customize/
wordpress/wp-includes/customize/class-wp-customize-nav-menu-section.php
wordpress/wp-includes/customize/class-wp-customize-upload-control.php
wordpress/wp-includes/customize/class-wp-customize-nav-menu-item-setting.php
wordpress/wp-includes/customize/class-wp-customize-nav-menu-item-control.php
wordpress/wp-includes/customize/class-wp-customize-selective-refresh.php
wordpress/wp-includes/customize/class-wp-customize-code-editor-control.php
wordpress/wp-includes/customize/class-wp-customize-header-image-control.php
wordpress/wp-includes/customize/class-wp-customize-themes-panel.php
wordpress/wp-includes/customize/class-wp-customize-filter-setting.php
wordpress/wp-includes/customize/class-wp-widget-area-customize-control.php
wordpress/wp-includes/customize/class-wp-customize-background-position-control.php
wordpress/wp-includes/customize/class-wp-customize-new-menu-control.php
wordpress/wp-includes/customize/class-wp-customize-nav-menus-panel.php
wordpress/wp-includes/customize/class-wp-customize-themes-section.php
wordpress/wp-includes/customize/class-wp-customize-background-image-control.php
wordpress/wp-includes/customize/class-wp-customize-site-icon-control.php
wordpress/wp-includes/customize/class-wp-customize-nav-menu-auto-add-control.php
wordpress/wp-includes/customize/class-wp-customize-background-image-setting.php
wordpress/wp-includes/customize/class-wp-customize-image-control.php
wordpress/wp-includes/customize/class-wp-customize-nav-menu-location-control.php
wordpress/wp-includes/customize/class-wp-customize-date-time-control.php
wordpress/wp-includes/customize/class-wp-customize-color-control.php
wordpress/wp-includes/customize/class-wp-sidebar-block-editor-control.php
wordpress/wp-includes/customize/class-wp-customize-custom-css-setting.php
wordpress/wp-includes/customize/class-wp-customize-header-image-setting.php
wordpress/wp-includes/customize/class-wp-customize-partial.php
wordpress/wp-includes/customize/class-wp-customize-nav-menu-locations-control.php
wordpress/wp-includes/customize/class-wp-customize-theme-control.php
wordpress/wp-includes/customize/class-wp-customize-new-menu-section.php
wordpress/wp-includes/customize/class-wp-customize-nav-menu-name-control.php
wordpress/wp-includes/customize/class-wp-customize-sidebar-section.php
wordpress/wp-includes/customize/class-wp-customize-nav-menu-control.php
wordpress/wp-includes/customize/class-wp-customize-cropped-image-control.php
wordpress/wp-includes/customize/class-wp-customize-media-control.php
wordpress/wp-includes/customize/class-wp-customize-nav-menu-setting.php
wordpress/wp-includes/customize/class-wp-widget-form-customize-control.php
wordpress/wp-includes/widgets/
wordpress/wp-includes/widgets/class-wp-widget-pages.php
wordpress/wp-includes/widgets/class-wp-widget-media-image.php
wordpress/wp-includes/widgets/class-wp-widget-search.php
wordpress/wp-includes/widgets/class-wp-widget-tag-cloud.php
wordpress/wp-includes/widgets/class-wp-widget-recent-comments.php
wordpress/wp-includes/widgets/class-wp-widget-media.php
wordpress/wp-includes/widgets/class-wp-widget-archives.php
wordpress/wp-includes/widgets/class-wp-widget-block.php
wordpress/wp-includes/widgets/class-wp-widget-custom-html.php
wordpress/wp-includes/widgets/class-wp-nav-menu-widget.php
wordpress/wp-includes/widgets/class-wp-widget-recent-posts.php
wordpress/wp-includes/widgets/class-wp-widget-links.php
wordpress/wp-includes/widgets/class-wp-widget-media-audio.php
wordpress/wp-includes/widgets/class-wp-widget-rss.php
wordpress/wp-includes/widgets/class-wp-widget-meta.php
wordpress/wp-includes/widgets/class-wp-widget-categories.php
wordpress/wp-includes/widgets/class-wp-widget-media-video.php
wordpress/wp-includes/widgets/class-wp-widget-calendar.php
wordpress/wp-includes/widgets/class-wp-widget-media-gallery.php
wordpress/wp-includes/widgets/class-wp-widget-text.php
wordpress/wp-includes/class-wp-image-editor.php
wordpress/wp-includes/deprecated.php
wordpress/wp-includes/class-wp-http-cookie.php
wordpress/wp-includes/class-wp-block-list.php
wordpress/wp-includes/feed-rss2-comments.php
wordpress/wp-includes/class-wp-date-query.php
wordpress/wp-includes/class-wp-oembed-controller.php
wordpress/wp-includes/class-walker-comment.php
wordpress/wp-includes/class-feed.php
wordpress/wp-includes/block-patterns.php
wordpress/wp-includes/class-wp-list-util.php
wordpress/wp-includes/class-wp-recovery-mode.php
wordpress/wp-includes/plugin.php
wordpress/wp-includes/class-walker-category-dropdown.php
wordpress/wp-includes/link-template.php
wordpress/wp-includes/comment.php
wordpress/wp-includes/class-wp-network-query.php
wordpress/wp-includes/https-detection.php
wordpress/wp-includes/registration.php
wordpress/wp-includes/PHPMailer/
wordpress/wp-includes/PHPMailer/SMTP.php
wordpress/wp-includes/PHPMailer/PHPMailer.php
wordpress/wp-includes/PHPMailer/Exception.php
wordpress/wp-includes/default-widgets.php
wordpress/wp-includes/class-oembed.php
wordpress/wp-includes/post-thumbnail-template.php
wordpress/wp-includes/capabilities.php
wordpress/wp-includes/class-wp-text-diff-renderer-inline.php
wordpress/wp-includes/l10n/
wordpress/wp-includes/l10n/class-wp-translations.php
wordpress/wp-includes/l10n/class-wp-translation-file.php
wordpress/wp-includes/l10n/class-wp-translation-controller.php
wordpress/wp-includes/l10n/class-wp-translation-file-php.php
wordpress/wp-includes/l10n/class-wp-translation-file-mo.php
wordpress/wp-includes/version.php
wordpress/wp-includes/update.php
wordpress/wp-includes/class.wp-styles.php
wordpress/wp-includes/class-wp-error.php
wordpress/wp-includes/block-bindings.php
wordpress/wp-includes/class-wp-post-type.php
wordpress/wp-includes/class-wp-meta-query.php
wordpress/wp-includes/class-wp-feed-cache.php
wordpress/wp-includes/fonts/
wordpress/wp-includes/fonts/dashicons.eot
wordpress/wp-includes/fonts/dashicons.woff
wordpress/wp-includes/fonts/class-wp-font-library.php
wordpress/wp-includes/fonts/class-wp-font-face-resolver.php
wordpress/wp-includes/fonts/class-wp-font-face.php
wordpress/wp-includes/fonts/class-wp-font-collection.php
wordpress/wp-includes/fonts/dashicons.woff2
wordpress/wp-includes/fonts/dashicons.ttf
wordpress/wp-includes/fonts/class-wp-font-utils.php
wordpress/wp-includes/fonts/dashicons.svg
wordpress/wp-includes/class-wp-taxonomy.php
wordpress/wp-includes/http.php
wordpress/wp-includes/atomlib.php
wordpress/wp-includes/class-wp-customize-nav-menus.php
wordpress/wp-includes/functions.php
wordpress/wp-includes/class-wp-term.php
wordpress/wp-includes/author-template.php
wordpress/wp-includes/pluggable.php
wordpress/wp-includes/class-wp-recovery-mode-key-service.php
wordpress/wp-includes/class.wp-scripts.php
wordpress/wp-includes/class-wp-user-request.php
wordpress/wp-includes/class-wp-theme-json-resolver.php
wordpress/wp-includes/error-protection.php
wordpress/wp-includes/class-json.php
wordpress/wp-includes/class-wp-user.php
wordpress/wp-includes/class-wp-block-type.php
wordpress/wp-includes/class-wp-ajax-response.php
wordpress/wp-includes/class-wp-textdomain-registry.php
wordpress/wp-includes/sodium_compat/
wordpress/wp-includes/sodium_compat/src/
wordpress/wp-includes/sodium_compat/src/Core32/
wordpress/wp-includes/sodium_compat/src/Core32/Int32.php
wordpress/wp-includes/sodium_compat/src/Core32/SipHash.php
wordpress/wp-includes/sodium_compat/src/Core32/Ed25519.php
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519.php
wordpress/wp-includes/sodium_compat/src/Core32/SecretStream/
wordpress/wp-includes/sodium_compat/src/Core32/SecretStream/State.php
wordpress/wp-includes/sodium_compat/src/Core32/XChaCha20.php
wordpress/wp-includes/sodium_compat/src/Core32/Poly1305/
wordpress/wp-includes/sodium_compat/src/Core32/Poly1305/State.php
wordpress/wp-includes/sodium_compat/src/Core32/ChaCha20.php
wordpress/wp-includes/sodium_compat/src/Core32/Salsa20.php
wordpress/wp-includes/sodium_compat/src/Core32/Int64.php
wordpress/wp-includes/sodium_compat/src/Core32/ChaCha20/
wordpress/wp-includes/sodium_compat/src/Core32/ChaCha20/IetfCtx.php
wordpress/wp-includes/sodium_compat/src/Core32/ChaCha20/Ctx.php
wordpress/wp-includes/sodium_compat/src/Core32/XSalsa20.php
wordpress/wp-includes/sodium_compat/src/Core32/Poly1305.php
wordpress/wp-includes/sodium_compat/src/Core32/HChaCha20.php
wordpress/wp-includes/sodium_compat/src/Core32/Util.php
wordpress/wp-includes/sodium_compat/src/Core32/HSalsa20.php
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519/
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519/H.php
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519/Fe.php
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519/README.md
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519/Ge/
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519/Ge/P2.php
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519/Ge/Cached.php
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519/Ge/P3.php
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519/Ge/Precomp.php
wordpress/wp-includes/sodium_compat/src/Core32/Curve25519/Ge/P1p1.php
wordpress/wp-includes/sodium_compat/src/Core32/X25519.php
wordpress/wp-includes/sodium_compat/src/Core32/BLAKE2b.php
wordpress/wp-includes/sodium_compat/src/PHP52/
wordpress/wp-includes/sodium_compat/src/PHP52/SplFixedArray.php
wordpress/wp-includes/sodium_compat/src/Crypto.php
wordpress/wp-includes/sodium_compat/src/Compat.php
wordpress/wp-includes/sodium_compat/src/Core/
wordpress/wp-includes/sodium_compat/src/Core/Base64/
wordpress/wp-includes/sodium_compat/src/Core/Base64/Original.php
wordpress/wp-includes/sodium_compat/src/Core/Base64/Common.php
wordpress/wp-includes/sodium_compat/src/Core/Base64/UrlSafe.php
wordpress/wp-includes/sodium_compat/src/Core/SipHash.php
wordpress/wp-includes/sodium_compat/src/Core/Ed25519.php
wordpress/wp-includes/sodium_compat/src/Core/Ristretto255.php
wordpress/wp-includes/sodium_compat/src/Core/Curve25519.php
wordpress/wp-includes/sodium_compat/src/Core/SecretStream/
wordpress/wp-includes/sodium_compat/src/Core/SecretStream/State.php
wordpress/wp-includes/sodium_compat/src/Core/XChaCha20.php
wordpress/wp-includes/sodium_compat/src/Core/Poly1305/
wordpress/wp-includes/sodium_compat/src/Core/Poly1305/State.php
wordpress/wp-includes/sodium_compat/src/Core/ChaCha20.php
wordpress/wp-includes/sodium_compat/src/Core/Salsa20.php
wordpress/wp-includes/sodium_compat/src/Core/ChaCha20/
wordpress/wp-includes/sodium_compat/src/Core/ChaCha20/IetfCtx.php
wordpress/wp-includes/sodium_compat/src/Core/ChaCha20/Ctx.php
wordpress/wp-includes/sodium_compat/src/Core/XSalsa20.php
wordpress/wp-includes/sodium_compat/src/Core/Poly1305.php
wordpress/wp-includes/sodium_compat/src/Core/HChaCha20.php
wordpress/wp-includes/sodium_compat/src/Core/Util.php
wordpress/wp-includes/sodium_compat/src/Core/HSalsa20.php
wordpress/wp-includes/sodium_compat/src/Core/Curve25519/
wordpress/wp-includes/sodium_compat/src/Core/Curve25519/H.php
wordpress/wp-includes/sodium_compat/src/Core/Curve25519/Fe.php
wordpress/wp-includes/sodium_compat/src/Core/Curve25519/README.md
wordpress/wp-includes/sodium_compat/src/Core/Curve25519/Ge/
wordpress/wp-includes/sodium_compat/src/Core/Curve25519/Ge/P2.php
wordpress/wp-includes/sodium_compat/src/Core/Curve25519/Ge/Cached.php
wordpress/wp-includes/sodium_compat/src/Core/Curve25519/Ge/P3.php
wordpress/wp-includes/sodium_compat/src/Core/Curve25519/Ge/Precomp.php
wordpress/wp-includes/sodium_compat/src/Core/Curve25519/Ge/P1p1.php
wordpress/wp-includes/sodium_compat/src/Core/X25519.php
wordpress/wp-includes/sodium_compat/src/Core/BLAKE2b.php
wordpress/wp-includes/sodium_compat/src/SodiumException.php
wordpress/wp-includes/sodium_compat/src/Crypto32.php
wordpress/wp-includes/sodium_compat/src/File.php
wordpress/wp-includes/sodium_compat/autoload-php7.php
wordpress/wp-includes/sodium_compat/composer.json
wordpress/wp-includes/sodium_compat/namespaced/
wordpress/wp-includes/sodium_compat/namespaced/Crypto.php
wordpress/wp-includes/sodium_compat/namespaced/Compat.php
wordpress/wp-includes/sodium_compat/namespaced/Core/
wordpress/wp-includes/sodium_compat/namespaced/Core/SipHash.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Xsalsa20.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Ed25519.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Curve25519.php
wordpress/wp-includes/sodium_compat/namespaced/Core/XChaCha20.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Poly1305/
wordpress/wp-includes/sodium_compat/namespaced/Core/Poly1305/State.php
wordpress/wp-includes/sodium_compat/namespaced/Core/ChaCha20.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Salsa20.php
wordpress/wp-includes/sodium_compat/namespaced/Core/ChaCha20/
wordpress/wp-includes/sodium_compat/namespaced/Core/ChaCha20/IetfCtx.php
wordpress/wp-includes/sodium_compat/namespaced/Core/ChaCha20/Ctx.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Poly1305.php
wordpress/wp-includes/sodium_compat/namespaced/Core/HChaCha20.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Util.php
wordpress/wp-includes/sodium_compat/namespaced/Core/HSalsa20.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Curve25519/
wordpress/wp-includes/sodium_compat/namespaced/Core/Curve25519/H.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Curve25519/Fe.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Curve25519/Ge/
wordpress/wp-includes/sodium_compat/namespaced/Core/Curve25519/Ge/P2.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Curve25519/Ge/Cached.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Curve25519/Ge/P3.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Curve25519/Ge/Precomp.php
wordpress/wp-includes/sodium_compat/namespaced/Core/Curve25519/Ge/P1p1.php
wordpress/wp-includes/sodium_compat/namespaced/Core/X25519.php
wordpress/wp-includes/sodium_compat/namespaced/Core/BLAKE2b.php
wordpress/wp-includes/sodium_compat/namespaced/File.php
wordpress/wp-includes/sodium_compat/lib/
wordpress/wp-includes/sodium_compat/lib/namespaced.php
wordpress/wp-includes/sodium_compat/lib/constants.php
wordpress/wp-includes/sodium_compat/lib/php72compat.php
wordpress/wp-includes/sodium_compat/lib/php72compat_const.php
wordpress/wp-includes/sodium_compat/lib/sodium_compat.php
wordpress/wp-includes/sodium_compat/lib/ristretto255.php
wordpress/wp-includes/sodium_compat/lib/stream-xchacha20.php
wordpress/wp-includes/sodium_compat/LICENSE
wordpress/wp-includes/sodium_compat/autoload.php
wordpress/wp-includes/robots-template.php
wordpress/wp-includes/sitemaps/
wordpress/wp-includes/sitemaps/class-wp-sitemaps-renderer.php
wordpress/wp-includes/sitemaps/class-wp-sitemaps-provider.php
wordpress/wp-includes/sitemaps/class-wp-sitemaps-index.php
wordpress/wp-includes/sitemaps/class-wp-sitemaps-stylesheet.php
wordpress/wp-includes/sitemaps/providers/
wordpress/wp-includes/sitemaps/providers/class-wp-sitemaps-taxonomies.php
wordpress/wp-includes/sitemaps/providers/class-wp-sitemaps-posts.php
wordpress/wp-includes/sitemaps/providers/class-wp-sitemaps-users.php
wordpress/wp-includes/sitemaps/class-wp-sitemaps-registry.php
wordpress/wp-includes/sitemaps/class-wp-sitemaps.php
wordpress/wp-includes/session.php
wordpress/wp-includes/rest-api/
wordpress/wp-includes/rest-api/endpoints/
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-font-faces-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-block-patterns-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-application-passwords-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-widget-types-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-pattern-directory-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-navigation-fallback-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-block-types-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-themes-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-font-families-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-widgets-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-templates-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-search-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-url-details-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-attachments-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-users-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-template-autosaves-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-global-styles-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-sidebars-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-block-pattern-categories-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-block-renderer-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-posts-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-comments-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-menu-items-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-menu-locations-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-post-types-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-autosaves-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-edit-site-export-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-terms-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-plugins-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-font-collections-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-site-health-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-blocks-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-post-statuses-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-settings-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-revisions-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-block-directory-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-menus-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-taxonomies-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-template-revisions-controller.php
wordpress/wp-includes/rest-api/endpoints/class-wp-rest-global-styles-revisions-controller.php
wordpress/wp-includes/rest-api/class-wp-rest-response.php
wordpress/wp-includes/rest-api/class-wp-rest-server.php
wordpress/wp-includes/rest-api/search/
wordpress/wp-includes/rest-api/search/class-wp-rest-post-search-handler.php
wordpress/wp-includes/rest-api/search/class-wp-rest-post-format-search-handler.php
wordpress/wp-includes/rest-api/search/class-wp-rest-term-search-handler.php
wordpress/wp-includes/rest-api/search/class-wp-rest-search-handler.php
wordpress/wp-includes/rest-api/fields/
wordpress/wp-includes/rest-api/fields/class-wp-rest-post-meta-fields.php
wordpress/wp-includes/rest-api/fields/class-wp-rest-meta-fields.php
wordpress/wp-includes/rest-api/fields/class-wp-rest-term-meta-fields.php
wordpress/wp-includes/rest-api/fields/class-wp-rest-user-meta-fields.php
wordpress/wp-includes/rest-api/fields/class-wp-rest-comment-meta-fields.php
wordpress/wp-includes/rest-api/class-wp-rest-request.php
wordpress/wp-includes/class-wp-classic-to-block-menu-converter.php
wordpress/wp-includes/class-wp-admin-bar.php
wordpress/wp-includes/class-wp-script-modules.php
wordpress/wp-includes/block-editor.php
wordpress/wp-includes/class-wp-hook.php
wordpress/wp-includes/class-wp-block-patterns-registry.php
wordpress/wp-includes/https-migration.php
wordpress/wp-includes/post.php
wordpress/wp-includes/class-wp-object-cache.php
wordpress/wp-includes/class-wp-walker.php
wordpress/wp-includes/class-wp-rewrite.php
wordpress/wp-includes/ms-network.php
wordpress/wp-includes/class-wp-customize-setting.php
wordpress/wp-includes/IXR/
wordpress/wp-includes/IXR/class-IXR-server.php
wordpress/wp-includes/IXR/class-IXR-message.php
wordpress/wp-includes/IXR/class-IXR-value.php
wordpress/wp-includes/IXR/class-IXR-introspectionserver.php
wordpress/wp-includes/IXR/class-IXR-client.php
wordpress/wp-includes/IXR/class-IXR-clientmulticall.php
wordpress/wp-includes/IXR/class-IXR-base64.php
wordpress/wp-includes/IXR/class-IXR-date.php
wordpress/wp-includes/IXR/class-IXR-request.php
wordpress/wp-includes/IXR/class-IXR-error.php
wordpress/wp-includes/class-wp-block.php
wordpress/wp-includes/class-wp-query.php
wordpress/wp-includes/class-wp-scripts.php
wordpress/wp-includes/block-patterns/
wordpress/wp-includes/block-patterns/query-offset-posts.php
wordpress/wp-includes/block-patterns/query-large-title-posts.php
wordpress/wp-includes/block-patterns/social-links-shared-background-color.php
wordpress/wp-includes/block-patterns/query-grid-posts.php
wordpress/wp-includes/block-patterns/query-medium-posts.php
wordpress/wp-includes/block-patterns/query-standard-posts.php
wordpress/wp-includes/block-patterns/query-small-posts.php
wordpress/wp-includes/class-wp.php
wordpress/wp-includes/spl-autoload-compat.php
wordpress/wp-includes/registration-functions.php
wordpress/wp-includes/class-wp-application-passwords.php
wordpress/wp-includes/global-styles-and-settings.php
wordpress/wp-includes/feed-rdf.php
wordpress/wp-includes/load.php
wordpress/wp-includes/bookmark.php
wordpress/wp-includes/class-wp-token-map.php
wordpress/wp-includes/comment-template.php
wordpress/wp-includes/class-wp-block-styles-registry.php
wordpress/wp-includes/theme-i18n.json
wordpress/wp-includes/fonts.php
wordpress/wp-includes/admin-bar.php
wordpress/wp-includes/ms-load.php
wordpress/wp-includes/class.wp-dependencies.php
wordpress/wp-includes/class-wp-theme-json-schema.php
wordpress/wp-includes/class-wp-http-proxy.php
wordpress/wp-includes/class-wp-block-parser-frame.php
wordpress/wp-includes/block-bindings/
wordpress/wp-includes/block-bindings/post-meta.php
wordpress/wp-includes/block-bindings/pattern-overrides.php
wordpress/wp-includes/class-wp-dependency.php
wordpress/wp-includes/js/
wordpress/wp-includes/js/utils.js
wordpress/wp-includes/js/customize-preview.min.js
wordpress/wp-includes/js/customize-preview-nav-menus.js
wordpress/wp-includes/js/autosave.js
wordpress/wp-includes/js/customize-selective-refresh.js
wordpress/wp-includes/js/customize-preview-widgets.js
wordpress/wp-includes/js/hoverIntent.min.js
wordpress/wp-includes/js/media-grid.js
wordpress/wp-includes/js/comment-reply.js
wordpress/wp-includes/js/customize-loader.js
wordpress/wp-includes/js/wp-sanitize.js
wordpress/wp-includes/js/wp-emoji.js
wordpress/wp-includes/js/swfobject.js
wordpress/wp-includes/js/wp-sanitize.min.js
wordpress/wp-includes/js/wp-emoji-loader.js
wordpress/wp-includes/js/media-audiovideo.js
wordpress/wp-includes/js/zxcvbn-async.js
wordpress/wp-includes/js/colorpicker.min.js
wordpress/wp-includes/js/hoverintent-js.min.js
wordpress/wp-includes/js/backbone.js
wordpress/wp-includes/js/json2.js
wordpress/wp-includes/js/media-editor.js
wordpress/wp-includes/js/customize-preview-widgets.min.js
wordpress/wp-includes/js/media-grid.min.js
wordpress/wp-includes/js/wplink.js
wordpress/wp-includes/js/customize-views.min.js
wordpress/wp-includes/js/underscore.min.js
wordpress/wp-includes/js/wp-embed-template.js
wordpress/wp-includes/js/wp-backbone.js
wordpress/wp-includes/js/utils.min.js
wordpress/wp-includes/js/customize-preview-nav-menus.min.js
wordpress/wp-includes/js/media-models.js
wordpress/wp-includes/js/wp-embed.js
wordpress/wp-includes/js/comment-reply.min.js
wordpress/wp-includes/js/wp-util.min.js
wordpress/wp-includes/js/tw-sack.min.js
wordpress/wp-includes/js/heartbeat.js
wordpress/wp-includes/js/media-views.js
wordpress/wp-includes/js/dist/
wordpress/wp-includes/js/dist/annotations.min.js
wordpress/wp-includes/js/dist/core-data.js
wordpress/wp-includes/js/dist/list-reusable-blocks.js
wordpress/wp-includes/js/dist/dom.min.js
wordpress/wp-includes/js/dist/block-directory.js
wordpress/wp-includes/js/dist/edit-widgets.js
wordpress/wp-includes/js/dist/core-commands.js
wordpress/wp-includes/js/dist/keyboard-shortcuts.js
wordpress/wp-includes/js/dist/patterns.js
wordpress/wp-includes/js/dist/url.min.js
wordpress/wp-includes/js/dist/components.js
wordpress/wp-includes/js/dist/edit-site.min.js
wordpress/wp-includes/js/dist/wordcount.js
wordpress/wp-includes/js/dist/vendor/
wordpress/wp-includes/js/dist/vendor/wp-polyfill-object-fit.min.js
wordpress/wp-includes/js/dist/vendor/regenerator-runtime.min.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-object-fit.js
wordpress/wp-includes/js/dist/vendor/react-jsx-runtime.min.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-inert.js
wordpress/wp-includes/js/dist/vendor/lodash.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-fetch.min.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-dom-rect.min.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-element-closest.min.js
wordpress/wp-includes/js/dist/vendor/moment.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-formdata.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-node-contains.min.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill.min.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-importmap.js
wordpress/wp-includes/js/dist/vendor/react.js
wordpress/wp-includes/js/dist/vendor/react-dom.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-url.min.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-element-closest.js
wordpress/wp-includes/js/dist/vendor/react.min.js
wordpress/wp-includes/js/dist/vendor/react-jsx-runtime.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-node-contains.js
wordpress/wp-includes/js/dist/vendor/react-dom.min.js.LICENSE.txt
wordpress/wp-includes/js/dist/vendor/wp-polyfill.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-url.js
wordpress/wp-includes/js/dist/vendor/regenerator-runtime.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-inert.min.js
wordpress/wp-includes/js/dist/vendor/react-jsx-runtime.min.js.LICENSE.txt
wordpress/wp-includes/js/dist/vendor/wp-polyfill-dom-rect.js
wordpress/wp-includes/js/dist/vendor/lodash.min.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-importmap.min.js
wordpress/wp-includes/js/dist/vendor/wp-polyfill-fetch.js
wordpress/wp-includes/js/dist/vendor/react.min.js.LICENSE.txt
wordpress/wp-includes/js/dist/vendor/wp-polyfill-formdata.min.js
wordpress/wp-includes/js/dist/vendor/react-dom.min.js
wordpress/wp-includes/js/dist/vendor/moment.min.js
wordpress/wp-includes/js/dist/blocks.js
wordpress/wp-includes/js/dist/private-apis.js
wordpress/wp-includes/js/dist/keyboard-shortcuts.min.js
wordpress/wp-includes/js/dist/router.js
wordpress/wp-includes/js/dist/block-library.min.js
wordpress/wp-includes/js/dist/token-list.js
wordpress/wp-includes/js/dist/widgets.min.js
wordpress/wp-includes/js/dist/reusable-blocks.js
wordpress/wp-includes/js/dist/style-engine.js
wordpress/wp-includes/js/dist/core-commands.min.js
wordpress/wp-includes/js/dist/commands.min.js
wordpress/wp-includes/js/dist/data.min.js
wordpress/wp-includes/js/dist/api-fetch.js
wordpress/wp-includes/js/dist/list-reusable-blocks.min.js
wordpress/wp-includes/js/dist/style-engine.min.js
wordpress/wp-includes/js/dist/interactivity.min.js
wordpress/wp-includes/js/dist/deprecated.min.js
wordpress/wp-includes/js/dist/edit-widgets.min.js
wordpress/wp-includes/js/dist/date.min.js
wordpress/wp-includes/js/dist/escape-html.min.js
wordpress/wp-includes/js/dist/edit-post.min.js
wordpress/wp-includes/js/dist/block-editor.min.js
wordpress/wp-includes/js/dist/dom-ready.js
wordpress/wp-includes/js/dist/blob.js
wordpress/wp-includes/js/dist/priority-queue.js
wordpress/wp-includes/js/dist/core-data.min.js
wordpress/wp-includes/js/dist/preferences.js
wordpress/wp-includes/js/dist/block-serialization-default-parser.js
wordpress/wp-includes/js/dist/compose.min.js
wordpress/wp-includes/js/dist/components.min.js
wordpress/wp-includes/js/dist/editor.min.js
wordpress/wp-includes/js/dist/is-shallow-equal.min.js
wordpress/wp-includes/js/dist/format-library.js
wordpress/wp-includes/js/dist/media-utils.min.js
wordpress/wp-includes/js/dist/date.js
wordpress/wp-includes/js/dist/i18n.js
wordpress/wp-includes/js/dist/edit-site.js
wordpress/wp-includes/js/dist/keycodes.min.js
wordpress/wp-includes/js/dist/preferences-persistence.min.js
wordpress/wp-includes/js/dist/block-serialization-default-parser.min.js
wordpress/wp-includes/js/dist/customize-widgets.js
wordpress/wp-includes/js/dist/notices.js
wordpress/wp-includes/js/dist/html-entities.min.js
wordpress/wp-includes/js/dist/preferences-persistence.js
wordpress/wp-includes/js/dist/hooks.js
wordpress/wp-includes/js/dist/media-utils.js
wordpress/wp-includes/js/dist/a11y.js
wordpress/wp-includes/js/dist/hooks.min.js
wordpress/wp-includes/js/dist/router.min.js
wordpress/wp-includes/js/dist/preferences.min.js
wordpress/wp-includes/js/dist/redux-routine.js
wordpress/wp-includes/js/dist/reusable-blocks.min.js
wordpress/wp-includes/js/dist/primitives.js
wordpress/wp-includes/js/dist/block-editor.js
wordpress/wp-includes/js/dist/warning.min.js
wordpress/wp-includes/js/dist/escape-html.js
wordpress/wp-includes/js/dist/i18n.min.js
wordpress/wp-includes/js/dist/rich-text.min.js
wordpress/wp-includes/js/dist/api-fetch.min.js
wordpress/wp-includes/js/dist/viewport.min.js
wordpress/wp-includes/js/dist/redux-routine.min.js
wordpress/wp-includes/js/dist/warning.js
wordpress/wp-includes/js/dist/notices.min.js
wordpress/wp-includes/js/dist/autop.min.js
wordpress/wp-includes/js/dist/undo-manager.js
wordpress/wp-includes/js/dist/data-controls.js
wordpress/wp-includes/js/dist/blob.min.js
wordpress/wp-includes/js/dist/block-library.js
wordpress/wp-includes/js/dist/token-list.min.js
wordpress/wp-includes/js/dist/plugins.js
wordpress/wp-includes/js/dist/editor.js
wordpress/wp-includes/js/dist/html-entities.js
wordpress/wp-includes/js/dist/deprecated.js
wordpress/wp-includes/js/dist/undo-manager.min.js
wordpress/wp-includes/js/dist/data.js
wordpress/wp-includes/js/dist/viewport.js
wordpress/wp-includes/js/dist/compose.js
wordpress/wp-includes/js/dist/nux.min.js
wordpress/wp-includes/js/dist/block-directory.min.js
wordpress/wp-includes/js/dist/commands.js
wordpress/wp-includes/js/dist/shortcode.min.js
wordpress/wp-includes/js/dist/widgets.js
wordpress/wp-includes/js/dist/interactivity-router.js
wordpress/wp-includes/js/dist/interactivity-router.min.js
wordpress/wp-includes/js/dist/blocks.min.js
wordpress/wp-includes/js/dist/customize-widgets.min.js
wordpress/wp-includes/js/dist/development/
wordpress/wp-includes/js/dist/development/react-refresh-runtime.js
wordpress/wp-includes/js/dist/development/react-refresh-entry.min.js
wordpress/wp-includes/js/dist/development/react-refresh-runtime.min.js
wordpress/wp-includes/js/dist/development/react-refresh-entry.js
wordpress/wp-includes/js/dist/patterns.min.js
wordpress/wp-includes/js/dist/nux.js
wordpress/wp-includes/js/dist/interactivity.js
wordpress/wp-includes/js/dist/priority-queue.min.js
wordpress/wp-includes/js/dist/format-library.min.js
wordpress/wp-includes/js/dist/plugins.min.js
wordpress/wp-includes/js/dist/shortcode.js
wordpress/wp-includes/js/dist/dom.js
wordpress/wp-includes/js/dist/data-controls.min.js
wordpress/wp-includes/js/dist/dom-ready.min.js
wordpress/wp-includes/js/dist/keycodes.js
wordpress/wp-includes/js/dist/element.js
wordpress/wp-includes/js/dist/private-apis.min.js
wordpress/wp-includes/js/dist/is-shallow-equal.js
wordpress/wp-includes/js/dist/rich-text.js
wordpress/wp-includes/js/dist/primitives.min.js
wordpress/wp-includes/js/dist/edit-post.js
wordpress/wp-includes/js/dist/autop.js
wordpress/wp-includes/js/dist/annotations.js
wordpress/wp-includes/js/dist/element.min.js
wordpress/wp-includes/js/dist/interactivity-router.min.asset.php
wordpress/wp-includes/js/dist/wordcount.min.js
wordpress/wp-includes/js/dist/a11y.min.js
wordpress/wp-includes/js/dist/server-side-render.min.js
wordpress/wp-includes/js/dist/interactivity-router.asset.php
wordpress/wp-includes/js/dist/url.js
wordpress/wp-includes/js/dist/server-side-render.js
wordpress/wp-includes/js/wp-embed-template.min.js
wordpress/wp-includes/js/customize-models.js
wordpress/wp-includes/js/wp-api.js
wordpress/wp-includes/js/tinymce/
wordpress/wp-includes/js/tinymce/tiny_mce_popup.js
wordpress/wp-includes/js/tinymce/langs/
wordpress/wp-includes/js/tinymce/langs/wp-langs-en.js
wordpress/wp-includes/js/tinymce/wp-tinymce.js
wordpress/wp-includes/js/tinymce/skins/
wordpress/wp-includes/js/tinymce/skins/wordpress/
wordpress/wp-includes/js/tinymce/skins/wordpress/images/
wordpress/wp-includes/js/tinymce/skins/wordpress/images/gallery.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/pagebreak.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/audio.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/more.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/pagebreak-2x.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/more-2x.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/dashicon-edit.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/playlist-audio.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/video.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/embedded.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/gallery-2x.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/dashicon-no.png
wordpress/wp-includes/js/tinymce/skins/wordpress/images/playlist-video.png
wordpress/wp-includes/js/tinymce/skins/wordpress/wp-content.css
wordpress/wp-includes/js/tinymce/skins/lightgray/
wordpress/wp-includes/js/tinymce/skins/lightgray/content.min.css
wordpress/wp-includes/js/tinymce/skins/lightgray/content.inline.min.css
wordpress/wp-includes/js/tinymce/skins/lightgray/img/
wordpress/wp-includes/js/tinymce/skins/lightgray/img/object.gif
wordpress/wp-includes/js/tinymce/skins/lightgray/img/loader.gif
wordpress/wp-includes/js/tinymce/skins/lightgray/img/trans.gif
wordpress/wp-includes/js/tinymce/skins/lightgray/img/anchor.gif
wordpress/wp-includes/js/tinymce/skins/lightgray/fonts/
wordpress/wp-includes/js/tinymce/skins/lightgray/fonts/tinymce.ttf
wordpress/wp-includes/js/tinymce/skins/lightgray/fonts/tinymce-small.ttf
wordpress/wp-includes/js/tinymce/skins/lightgray/fonts/tinymce.eot
wordpress/wp-includes/js/tinymce/skins/lightgray/fonts/tinymce-small.svg
wordpress/wp-includes/js/tinymce/skins/lightgray/fonts/tinymce.svg
wordpress/wp-includes/js/tinymce/skins/lightgray/fonts/tinymce-small.eot
wordpress/wp-includes/js/tinymce/skins/lightgray/fonts/tinymce-small.woff
wordpress/wp-includes/js/tinymce/skins/lightgray/fonts/tinymce.woff
wordpress/wp-includes/js/tinymce/skins/lightgray/skin.min.css
wordpress/wp-includes/js/tinymce/themes/
wordpress/wp-includes/js/tinymce/themes/inlite/
wordpress/wp-includes/js/tinymce/themes/inlite/theme.min.js
wordpress/wp-includes/js/tinymce/themes/inlite/theme.js
wordpress/wp-includes/js/tinymce/themes/modern/
wordpress/wp-includes/js/tinymce/themes/modern/theme.min.js
wordpress/wp-includes/js/tinymce/themes/modern/theme.js
wordpress/wp-includes/js/tinymce/plugins/
wordpress/wp-includes/js/tinymce/plugins/fullscreen/
wordpress/wp-includes/js/tinymce/plugins/fullscreen/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/fullscreen/plugin.js
wordpress/wp-includes/js/tinymce/plugins/wplink/
wordpress/wp-includes/js/tinymce/plugins/wplink/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/wplink/plugin.js
wordpress/wp-includes/js/tinymce/plugins/wpemoji/
wordpress/wp-includes/js/tinymce/plugins/wpemoji/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/wpemoji/plugin.js
wordpress/wp-includes/js/tinymce/plugins/media/
wordpress/wp-includes/js/tinymce/plugins/media/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/media/plugin.js
wordpress/wp-includes/js/tinymce/plugins/wptextpattern/
wordpress/wp-includes/js/tinymce/plugins/wptextpattern/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/wptextpattern/plugin.js
wordpress/wp-includes/js/tinymce/plugins/wpdialogs/
wordpress/wp-includes/js/tinymce/plugins/wpdialogs/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/wpdialogs/plugin.js
wordpress/wp-includes/js/tinymce/plugins/wpview/
wordpress/wp-includes/js/tinymce/plugins/wpview/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/wpview/plugin.js
wordpress/wp-includes/js/tinymce/plugins/wordpress/
wordpress/wp-includes/js/tinymce/plugins/wordpress/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/wordpress/plugin.js
wordpress/wp-includes/js/tinymce/plugins/wpautoresize/
wordpress/wp-includes/js/tinymce/plugins/wpautoresize/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/wpautoresize/plugin.js
wordpress/wp-includes/js/tinymce/plugins/paste/
wordpress/wp-includes/js/tinymce/plugins/paste/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/paste/plugin.js
wordpress/wp-includes/js/tinymce/plugins/colorpicker/
wordpress/wp-includes/js/tinymce/plugins/colorpicker/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/colorpicker/plugin.js
wordpress/wp-includes/js/tinymce/plugins/hr/
wordpress/wp-includes/js/tinymce/plugins/hr/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/hr/plugin.js
wordpress/wp-includes/js/tinymce/plugins/lists/
wordpress/wp-includes/js/tinymce/plugins/lists/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/lists/plugin.js
wordpress/wp-includes/js/tinymce/plugins/tabfocus/
wordpress/wp-includes/js/tinymce/plugins/tabfocus/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/tabfocus/plugin.js
wordpress/wp-includes/js/tinymce/plugins/compat3x/
wordpress/wp-includes/js/tinymce/plugins/compat3x/css/
wordpress/wp-includes/js/tinymce/plugins/compat3x/css/dialog.css
wordpress/wp-includes/js/tinymce/plugins/compat3x/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/compat3x/plugin.js
wordpress/wp-includes/js/tinymce/plugins/wpeditimage/
wordpress/wp-includes/js/tinymce/plugins/wpeditimage/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/wpeditimage/plugin.js
wordpress/wp-includes/js/tinymce/plugins/link/
wordpress/wp-includes/js/tinymce/plugins/link/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/link/plugin.js
wordpress/wp-includes/js/tinymce/plugins/directionality/
wordpress/wp-includes/js/tinymce/plugins/directionality/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/directionality/plugin.js
wordpress/wp-includes/js/tinymce/plugins/textcolor/
wordpress/wp-includes/js/tinymce/plugins/textcolor/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/textcolor/plugin.js
wordpress/wp-includes/js/tinymce/plugins/wpgallery/
wordpress/wp-includes/js/tinymce/plugins/wpgallery/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/wpgallery/plugin.js
wordpress/wp-includes/js/tinymce/plugins/image/
wordpress/wp-includes/js/tinymce/plugins/image/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/image/plugin.js
wordpress/wp-includes/js/tinymce/plugins/charmap/
wordpress/wp-includes/js/tinymce/plugins/charmap/plugin.min.js
wordpress/wp-includes/js/tinymce/plugins/charmap/plugin.js
wordpress/wp-includes/js/tinymce/tinymce.min.js
wordpress/wp-includes/js/tinymce/license.txt
wordpress/wp-includes/js/tinymce/utils/
wordpress/wp-includes/js/tinymce/utils/mctabs.js
wordpress/wp-includes/js/tinymce/utils/validate.js
wordpress/wp-includes/js/tinymce/utils/form_utils.js
wordpress/wp-includes/js/tinymce/utils/editable_selects.js
wordpress/wp-includes/js/tinymce/wp-tinymce.php
wordpress/wp-includes/js/wp-list-revisions.min.js
wordpress/wp-includes/js/imgareaselect/
wordpress/wp-includes/js/imgareaselect/border-anim-v.gif
wordpress/wp-includes/js/imgareaselect/imgareaselect.css
wordpress/wp-includes/js/imgareaselect/jquery.imgareaselect.js
wordpress/wp-includes/js/imgareaselect/jquery.imgareaselect.min.js
wordpress/wp-includes/js/imgareaselect/border-anim-h.gif
wordpress/wp-includes/js/autosave.min.js
wordpress/wp-includes/js/wp-lists.min.js
wordpress/wp-includes/js/wpdialog.js
wordpress/wp-includes/js/wpdialog.min.js
wordpress/wp-includes/js/admin-bar.js
wordpress/wp-includes/js/wp-embed.min.js
wordpress/wp-includes/js/media-models.min.js
wordpress/wp-includes/js/hoverIntent.js
wordpress/wp-includes/js/wp-auth-check.min.js
wordpress/wp-includes/js/colorpicker.js
wordpress/wp-includes/js/heartbeat.min.js
wordpress/wp-includes/js/underscore.js
wordpress/wp-includes/js/customize-selective-refresh.min.js
wordpress/wp-includes/js/api-request.js
wordpress/wp-includes/js/wp-emoji.min.js
wordpress/wp-includes/js/quicktags.min.js
wordpress/wp-includes/js/customize-preview.js
wordpress/wp-includes/js/customize-loader.min.js
wordpress/wp-includes/js/customize-views.js
wordpress/wp-includes/js/wp-util.js
wordpress/wp-includes/js/wp-backbone.min.js
wordpress/wp-includes/js/admin-bar.min.js
wordpress/wp-includes/js/tw-sack.js
wordpress/wp-includes/js/clipboard.min.js
wordpress/wp-includes/js/mce-view.min.js
wordpress/wp-includes/js/json2.min.js
wordpress/wp-includes/js/wp-ajax-response.min.js
wordpress/wp-includes/js/jquery/
wordpress/wp-includes/js/jquery/jquery.ui.touch-punch.js
wordpress/wp-includes/js/jquery/jquery.form.min.js
wordpress/wp-includes/js/jquery/jquery.color.min.js
wordpress/wp-includes/js/jquery/jquery-migrate.js
wordpress/wp-includes/js/jquery/jquery.hotkeys.js
wordpress/wp-includes/js/jquery/jquery-migrate.min.js
wordpress/wp-includes/js/jquery/jquery.masonry.min.js
wordpress/wp-includes/js/jquery/jquery.hotkeys.min.js
wordpress/wp-includes/js/jquery/jquery.table-hotkeys.min.js
wordpress/wp-includes/js/jquery/jquery.serialize-object.js
wordpress/wp-includes/js/jquery/suggest.min.js
wordpress/wp-includes/js/jquery/jquery.js
wordpress/wp-includes/js/jquery/suggest.js
wordpress/wp-includes/js/jquery/jquery.min.js
wordpress/wp-includes/js/jquery/ui/
wordpress/wp-includes/js/jquery/ui/effect-fade.js
wordpress/wp-includes/js/jquery/ui/controlgroup.min.js
wordpress/wp-includes/js/jquery/ui/effect-highlight.min.js
wordpress/wp-includes/js/jquery/ui/effect-clip.js
wordpress/wp-includes/js/jquery/ui/effect-highlight.js
wordpress/wp-includes/js/jquery/ui/button.js
wordpress/wp-includes/js/jquery/ui/tabs.min.js
wordpress/wp-includes/js/jquery/ui/selectable.min.js
wordpress/wp-includes/js/jquery/ui/draggable.js
wordpress/wp-includes/js/jquery/ui/droppable.min.js
wordpress/wp-includes/js/jquery/ui/effect.js
wordpress/wp-includes/js/jquery/ui/spinner.js
wordpress/wp-includes/js/jquery/ui/effect-explode.min.js
wordpress/wp-includes/js/jquery/ui/accordion.js
wordpress/wp-includes/js/jquery/ui/core.min.js
wordpress/wp-includes/js/jquery/ui/effect-pulsate.min.js
wordpress/wp-includes/js/jquery/ui/mouse.min.js
wordpress/wp-includes/js/jquery/ui/effect-puff.min.js
wordpress/wp-includes/js/jquery/ui/effect-shake.js
wordpress/wp-includes/js/jquery/ui/menu.js
wordpress/wp-includes/js/jquery/ui/draggable.min.js
wordpress/wp-includes/js/jquery/ui/selectmenu.js
wordpress/wp-includes/js/jquery/ui/sortable.js
wordpress/wp-includes/js/jquery/ui/core.js
wordpress/wp-includes/js/jquery/ui/effect-slide.min.js
wordpress/wp-includes/js/jquery/ui/effect-drop.js
wordpress/wp-includes/js/jquery/ui/effect-size.js
wordpress/wp-includes/js/jquery/ui/autocomplete.js
wordpress/wp-includes/js/jquery/ui/menu.min.js
wordpress/wp-includes/js/jquery/ui/tabs.js
wordpress/wp-includes/js/jquery/ui/effect-bounce.min.js
wordpress/wp-includes/js/jquery/ui/effect-drop.min.js
wordpress/wp-includes/js/jquery/ui/selectable.js
wordpress/wp-includes/js/jquery/ui/dialog.js
wordpress/wp-includes/js/jquery/ui/effect-fold.min.js
wordpress/wp-includes/js/jquery/ui/checkboxradio.min.js
wordpress/wp-includes/js/jquery/ui/effect-puff.js
wordpress/wp-includes/js/jquery/ui/autocomplete.min.js
wordpress/wp-includes/js/jquery/ui/slider.js
wordpress/wp-includes/js/jquery/ui/tooltip.min.js
wordpress/wp-includes/js/jquery/ui/sortable.min.js
wordpress/wp-includes/js/jquery/ui/droppable.js
wordpress/wp-includes/js/jquery/ui/effect-blind.min.js
wordpress/wp-includes/js/jquery/ui/effect-pulsate.js
wordpress/wp-includes/js/jquery/ui/resizable.min.js
wordpress/wp-includes/js/jquery/ui/datepicker.js
wordpress/wp-includes/js/jquery/ui/effect-scale.js
wordpress/wp-includes/js/jquery/ui/checkboxradio.js
wordpress/wp-includes/js/jquery/ui/spinner.min.js
wordpress/wp-includes/js/jquery/ui/button.min.js
wordpress/wp-includes/js/jquery/ui/progressbar.min.js
wordpress/wp-includes/js/jquery/ui/tooltip.js
wordpress/wp-includes/js/jquery/ui/effect.min.js
wordpress/wp-includes/js/jquery/ui/effect-transfer.js
wordpress/wp-includes/js/jquery/ui/accordion.min.js
wordpress/wp-includes/js/jquery/ui/effect-fade.min.js
wordpress/wp-includes/js/jquery/ui/effect-fold.js
wordpress/wp-includes/js/jquery/ui/effect-transfer.min.js
wordpress/wp-includes/js/jquery/ui/mouse.js
wordpress/wp-includes/js/jquery/ui/controlgroup.js
wordpress/wp-includes/js/jquery/ui/progressbar.js
wordpress/wp-includes/js/jquery/ui/effect-clip.min.js
wordpress/wp-includes/js/jquery/ui/effect-scale.min.js
wordpress/wp-includes/js/jquery/ui/selectmenu.min.js
wordpress/wp-includes/js/jquery/ui/effect-blind.js
wordpress/wp-includes/js/jquery/ui/effect-explode.js
wordpress/wp-includes/js/jquery/ui/resizable.js
wordpress/wp-includes/js/jquery/ui/dialog.min.js
wordpress/wp-includes/js/jquery/ui/effect-slide.js
wordpress/wp-includes/js/jquery/ui/slider.min.js
wordpress/wp-includes/js/jquery/ui/effect-bounce.js
wordpress/wp-includes/js/jquery/ui/effect-size.min.js
wordpress/wp-includes/js/jquery/ui/datepicker.min.js
wordpress/wp-includes/js/jquery/ui/effect-shake.min.js
wordpress/wp-includes/js/jquery/jquery.table-hotkeys.js
wordpress/wp-includes/js/jquery/jquery.form.js
wordpress/wp-includes/js/jquery/jquery.schedule.js
wordpress/wp-includes/js/jquery/jquery.query.js
wordpress/wp-includes/js/crop/
wordpress/wp-includes/js/crop/cropper.js
wordpress/wp-includes/js/crop/cropper.css
wordpress/wp-includes/js/crop/marqueeVert.gif
wordpress/wp-includes/js/crop/marqueeHoriz.gif
wordpress/wp-includes/js/twemoji.min.js
wordpress/wp-includes/js/twemoji.js
wordpress/wp-includes/js/thickbox/
wordpress/wp-includes/js/thickbox/thickbox.js
wordpress/wp-includes/js/thickbox/macFFBgHack.png
wordpress/wp-includes/js/thickbox/thickbox.css
wordpress/wp-includes/js/thickbox/loadingAnimation.gif
wordpress/wp-includes/js/zxcvbn.min.js
wordpress/wp-includes/js/shortcode.min.js
wordpress/wp-includes/js/zxcvbn-async.min.js
wordpress/wp-includes/js/imagesloaded.min.js
wordpress/wp-includes/js/customize-base.js
wordpress/wp-includes/js/clipboard.js
wordpress/wp-includes/js/mce-view.js
wordpress/wp-includes/js/customize-models.min.js
wordpress/wp-includes/js/mediaelement/
wordpress/wp-includes/js/mediaelement/mediaelementplayer-legacy.css
wordpress/wp-includes/js/mediaelement/mediaelement-migrate.min.js
wordpress/wp-includes/js/mediaelement/mediaelementplayer-legacy.min.css
wordpress/wp-includes/js/mediaelement/wp-mediaelement.css
wordpress/wp-includes/js/mediaelement/mediaelement-migrate.js
wordpress/wp-includes/js/mediaelement/mediaelement-and-player.js
wordpress/wp-includes/js/mediaelement/wp-playlist.min.js
wordpress/wp-includes/js/mediaelement/mediaelement.min.js
wordpress/wp-includes/js/mediaelement/wp-mediaelement.js
wordpress/wp-includes/js/mediaelement/wp-mediaelement.min.css
wordpress/wp-includes/js/mediaelement/mediaelementplayer.css
wordpress/wp-includes/js/mediaelement/wp-mediaelement.min.js
wordpress/wp-includes/js/mediaelement/mediaelement.js
wordpress/wp-includes/js/mediaelement/renderers/
wordpress/wp-includes/js/mediaelement/renderers/vimeo.min.js
wordpress/wp-includes/js/mediaelement/renderers/vimeo.js
wordpress/wp-includes/js/mediaelement/mejs-controls.png
wordpress/wp-includes/js/mediaelement/mediaelementplayer.min.css
wordpress/wp-includes/js/mediaelement/wp-playlist.js
wordpress/wp-includes/js/mediaelement/mediaelement-and-player.min.js
wordpress/wp-includes/js/mediaelement/mejs-controls.svg
wordpress/wp-includes/js/wp-list-revisions.js
wordpress/wp-includes/js/wp-pointer.min.js
wordpress/wp-includes/js/shortcode.js
wordpress/wp-includes/js/customize-base.min.js
wordpress/wp-includes/js/quicktags.js
wordpress/wp-includes/js/wp-custom-header.js
wordpress/wp-includes/js/media-audiovideo.min.js
wordpress/wp-includes/js/wp-lists.js
wordpress/wp-includes/js/wp-emoji-loader.min.js
wordpress/wp-includes/js/media-views.min.js
wordpress/wp-includes/js/wp-ajax-response.js
wordpress/wp-includes/js/wp-api.min.js
wordpress/wp-includes/js/wplink.min.js
wordpress/wp-includes/js/swfupload/
wordpress/wp-includes/js/swfupload/handlers.js
wordpress/wp-includes/js/swfupload/handlers.min.js
wordpress/wp-includes/js/swfupload/license.txt
wordpress/wp-includes/js/swfupload/swfupload.js
wordpress/wp-includes/js/wp-pointer.js
wordpress/wp-includes/js/backbone.min.js
wordpress/wp-includes/js/codemirror/
wordpress/wp-includes/js/codemirror/fakejshint.js
wordpress/wp-includes/js/codemirror/htmlhint-kses.js
wordpress/wp-includes/js/codemirror/csslint.js
wordpress/wp-includes/js/codemirror/esprima.js
wordpress/wp-includes/js/codemirror/htmlhint.js
wordpress/wp-includes/js/codemirror/jsonlint.js
wordpress/wp-includes/js/codemirror/codemirror.min.js
wordpress/wp-includes/js/codemirror/codemirror.min.css
wordpress/wp-includes/js/masonry.min.js
wordpress/wp-includes/js/wp-emoji-release.min.js
wordpress/wp-includes/js/media-editor.min.js
wordpress/wp-includes/js/wp-auth-check.js
wordpress/wp-includes/js/plupload/
wordpress/wp-includes/js/plupload/plupload.min.js
wordpress/wp-includes/js/plupload/handlers.js
wordpress/wp-includes/js/plupload/moxie.js
wordpress/wp-includes/js/plupload/plupload.js
wordpress/wp-includes/js/plupload/handlers.min.js
wordpress/wp-includes/js/plupload/wp-plupload.js
wordpress/wp-includes/js/plupload/license.txt
wordpress/wp-includes/js/plupload/wp-plupload.min.js
wordpress/wp-includes/js/plupload/moxie.min.js
wordpress/wp-includes/js/jcrop/
wordpress/wp-includes/js/jcrop/jquery.Jcrop.min.css
wordpress/wp-includes/js/jcrop/jquery.Jcrop.min.js
wordpress/wp-includes/js/jcrop/Jcrop.gif
wordpress/wp-includes/js/wp-custom-header.min.js
wordpress/wp-includes/js/api-request.min.js
wordpress/wp-includes/bookmark-template.php
wordpress/wp-includes/widgets.php
wordpress/wp-includes/class-wp-embed.php
wordpress/wp-includes/feed-atom.php
wordpress/wp-includes/class-wp-image-editor-imagick.php
wordpress/wp-includes/class-IXR.php
wordpress/wp-includes/style-engine/
wordpress/wp-includes/style-engine/class-wp-style-engine-processor.php
wordpress/wp-includes/style-engine/class-wp-style-engine.php
wordpress/wp-includes/style-engine/class-wp-style-engine-css-declarations.php
wordpress/wp-includes/style-engine/class-wp-style-engine-css-rules-store.php
wordpress/wp-includes/style-engine/class-wp-style-engine-css-rule.php
wordpress/wp-includes/wp-db.php
wordpress/wp-includes/nav-menu-template.php
wordpress/wp-includes/formatting.php
wordpress/wp-includes/class-wp-http-streams.php
wordpress/wp-includes/class-wp-metadata-lazyloader.php
wordpress/wp-includes/post-template.php
wordpress/wp-includes/feed-atom-comments.php
wordpress/wp-includes/pluggable-deprecated.php
wordpress/wp-includes/theme.php
wordpress/wp-includes/template.php
wordpress/wp-includes/class-wp-text-diff-renderer-table.php
wordpress/wp-includes/class-wp-session-tokens.php
wordpress/wp-includes/class-wp-block-type-registry.php
wordpress/wp-includes/wp-diff.php
wordpress/wp-includes/option.php
wordpress/wp-includes/class-wp-locale-switcher.php
wordpress/wp-includes/post-formats.php
wordpress/wp-includes/template-canvas.php
wordpress/wp-includes/functions.wp-scripts.php
wordpress/wp-includes/class-phpmailer.php
wordpress/wp-includes/class-wp-xmlrpc-server.php
wordpress/wp-includes/class-wp-http-encoding.php
wordpress/wp-includes/theme-previews.php
wordpress/wp-includes/ms-default-constants.php
wordpress/wp-activate.php
wordpress/wp-admin/
wordpress/wp-admin/edit-tag-form.php
wordpress/wp-admin/images/
wordpress/wp-admin/images/post-formats32-vs.png
wordpress/wp-admin/images/arrows-2x.png
wordpress/wp-admin/images/resize-rtl.gif
wordpress/wp-admin/images/contribute-no-code.svg
wordpress/wp-admin/images/date-button.gif
wordpress/wp-admin/images/browser-rtl.png
wordpress/wp-admin/images/wordpress-logo.png
wordpress/wp-admin/images/stars-2x.png
wordpress/wp-admin/images/browser.png
wordpress/wp-admin/images/post-formats32.png
wordpress/wp-admin/images/post-formats.png
wordpress/wp-admin/images/bubble_bg.gif
wordpress/wp-admin/images/icons32-vs-2x.png
wordpress/wp-admin/images/dashboard-background.svg
wordpress/wp-admin/images/spinner.gif
wordpress/wp-admin/images/comment-grey-bubble.png
wordpress/wp-admin/images/contribute-main.svg
wordpress/wp-admin/images/about-texture.png
wordpress/wp-admin/images/imgedit-icons-2x.png
wordpress/wp-admin/images/arrows.png
wordpress/wp-admin/images/align-center-2x.png
wordpress/wp-admin/images/list-2x.png
wordpress/wp-admin/images/wpspin_light-2x.gif
wordpress/wp-admin/images/xit-2x.gif
wordpress/wp-admin/images/generic.png
wordpress/wp-admin/images/menu-vs-2x.png
wordpress/wp-admin/images/icons32.png
wordpress/wp-admin/images/w-logo-blue.png
wordpress/wp-admin/images/media-button.png
wordpress/wp-admin/images/spinner-2x.gif
wordpress/wp-admin/images/about-release-badge.svg
wordpress/wp-admin/images/menu.png
wordpress/wp-admin/images/align-none.png
wordpress/wp-admin/images/icons32-2x.png
wordpress/wp-admin/images/marker.png
wordpress/wp-admin/images/resize.gif
wordpress/wp-admin/images/sort-2x.gif
wordpress/wp-admin/images/align-center.png
wordpress/wp-admin/images/freedom-3.svg
wordpress/wp-admin/images/loading.gif
wordpress/wp-admin/images/comment-grey-bubble-2x.png
wordpress/wp-admin/images/wordpress-logo.svg
wordpress/wp-admin/images/bubble_bg-2x.gif
wordpress/wp-admin/images/align-right.png
wordpress/wp-admin/images/freedom-4.svg
wordpress/wp-admin/images/wordpress-logo-white.svg
wordpress/wp-admin/images/media-button-image.gif
wordpress/wp-admin/images/imgedit-icons.png
wordpress/wp-admin/images/stars.png
wordpress/wp-admin/images/wpspin_light.gif
wordpress/wp-admin/images/align-none-2x.png
wordpress/wp-admin/images/xit.gif
wordpress/wp-admin/images/sort.gif
wordpress/wp-admin/images/list.png
wordpress/wp-admin/images/align-left.png
wordpress/wp-admin/images/w-logo-white.png
wordpress/wp-admin/images/contribute-code.svg
wordpress/wp-admin/images/freedom-2.svg
wordpress/wp-admin/images/align-right-2x.png
wordpress/wp-admin/images/media-button-other.gif
wordpress/wp-admin/images/se.png
wordpress/wp-admin/images/date-button-2x.gif
wordpress/wp-admin/images/resize-2x.gif
wordpress/wp-admin/images/icons32-vs.png
wordpress/wp-admin/images/align-left-2x.png
wordpress/wp-admin/images/media-button-2x.png
wordpress/wp-admin/images/yes.png
wordpress/wp-admin/images/freedom-1.svg
wordpress/wp-admin/images/resize-rtl-2x.gif
wordpress/wp-admin/images/media-button-video.gif
wordpress/wp-admin/images/privacy.svg
wordpress/wp-admin/images/mask.png
wordpress/wp-admin/images/post-formats-vs.png
wordpress/wp-admin/images/no.png
wordpress/wp-admin/images/wheel.png
wordpress/wp-admin/images/menu-vs.png
wordpress/wp-admin/images/menu-2x.png
wordpress/wp-admin/images/media-button-music.gif
wordpress/wp-admin/edit-form-comment.php
wordpress/wp-admin/ms-sites.php
wordpress/wp-admin/custom-header.php
wordpress/wp-admin/contribute.php
wordpress/wp-admin/custom-background.php
wordpress/wp-admin/customize.php
wordpress/wp-admin/admin-functions.php
wordpress/wp-admin/css/
wordpress/wp-admin/css/code-editor.css
wordpress/wp-admin/css/about.css
wordpress/wp-admin/css/customize-nav-menus-rtl.css
wordpress/wp-admin/css/wp-admin-rtl.min.css
wordpress/wp-admin/css/media-rtl.css
wordpress/wp-admin/css/list-tables-rtl.css
wordpress/wp-admin/css/site-health-rtl.css
wordpress/wp-admin/css/color-picker.css
wordpress/wp-admin/css/list-tables-rtl.min.css
wordpress/wp-admin/css/nav-menus.min.css
wordpress/wp-admin/css/themes.css
wordpress/wp-admin/css/login-rtl.min.css
wordpress/wp-admin/css/login-rtl.css
wordpress/wp-admin/css/revisions.css
wordpress/wp-admin/css/forms.css
wordpress/wp-admin/css/common-rtl.min.css
wordpress/wp-admin/css/deprecated-media.css
wordpress/wp-admin/css/site-health.css
wordpress/wp-admin/css/customize-widgets.css
wordpress/wp-admin/css/media-rtl.min.css
wordpress/wp-admin/css/list-tables.css
wordpress/wp-admin/css/edit.css
wordpress/wp-admin/css/nav-menus-rtl.min.css
wordpress/wp-admin/css/edit-rtl.min.css
wordpress/wp-admin/css/site-icon-rtl.min.css
wordpress/wp-admin/css/revisions-rtl.css
wordpress/wp-admin/css/wp-admin.min.css
wordpress/wp-admin/css/site-health-rtl.min.css
wordpress/wp-admin/css/media.min.css
wordpress/wp-admin/css/install.css
wordpress/wp-admin/css/widgets.min.css
wordpress/wp-admin/css/customize-controls.css
wordpress/wp-admin/css/customize-controls-rtl.css
wordpress/wp-admin/css/themes-rtl.css
wordpress/wp-admin/css/about-rtl.min.css
wordpress/wp-admin/css/common.css
wordpress/wp-admin/css/edit.min.css
wordpress/wp-admin/css/color-picker-rtl.min.css
wordpress/wp-admin/css/code-editor-rtl.min.css
wordpress/wp-admin/css/site-icon.css
wordpress/wp-admin/css/site-health.min.css
wordpress/wp-admin/css/nav-menus.css
wordpress/wp-admin/css/code-editor-rtl.css
wordpress/wp-admin/css/customize-nav-menus.min.css
wordpress/wp-admin/css/login.css
wordpress/wp-admin/css/deprecated-media-rtl.css
wordpress/wp-admin/css/admin-menu.css
wordpress/wp-admin/css/dashboard-rtl.css
wordpress/wp-admin/css/deprecated-media-rtl.min.css
wordpress/wp-admin/css/dashboard-rtl.min.css
wordpress/wp-admin/css/farbtastic-rtl.css
wordpress/wp-admin/css/revisions-rtl.min.css
wordpress/wp-admin/css/customize-nav-menus-rtl.min.css
wordpress/wp-admin/css/colors/
wordpress/wp-admin/css/colors/sunrise/
wordpress/wp-admin/css/colors/sunrise/colors.scss
wordpress/wp-admin/css/colors/sunrise/colors-rtl.min.css
wordpress/wp-admin/css/colors/sunrise/colors-rtl.css
wordpress/wp-admin/css/colors/sunrise/colors.min.css
wordpress/wp-admin/css/colors/sunrise/colors.css
wordpress/wp-admin/css/colors/ocean/
wordpress/wp-admin/css/colors/ocean/colors.scss
wordpress/wp-admin/css/colors/ocean/colors-rtl.min.css
wordpress/wp-admin/css/colors/ocean/colors-rtl.css
wordpress/wp-admin/css/colors/ocean/colors.min.css
wordpress/wp-admin/css/colors/ocean/colors.css
wordpress/wp-admin/css/colors/ectoplasm/
wordpress/wp-admin/css/colors/ectoplasm/colors.scss
wordpress/wp-admin/css/colors/ectoplasm/colors-rtl.min.css
wordpress/wp-admin/css/colors/ectoplasm/colors-rtl.css
wordpress/wp-admin/css/colors/ectoplasm/colors.min.css
wordpress/wp-admin/css/colors/ectoplasm/colors.css
wordpress/wp-admin/css/colors/_admin.scss
wordpress/wp-admin/css/colors/blue/
wordpress/wp-admin/css/colors/blue/colors.scss
wordpress/wp-admin/css/colors/blue/colors-rtl.min.css
wordpress/wp-admin/css/colors/blue/colors-rtl.css
wordpress/wp-admin/css/colors/blue/colors.min.css
wordpress/wp-admin/css/colors/blue/colors.css
wordpress/wp-admin/css/colors/light/
wordpress/wp-admin/css/colors/light/colors.scss
wordpress/wp-admin/css/colors/light/colors-rtl.min.css
wordpress/wp-admin/css/colors/light/colors-rtl.css
wordpress/wp-admin/css/colors/light/colors.min.css
wordpress/wp-admin/css/colors/light/colors.css
wordpress/wp-admin/css/colors/_mixins.scss
wordpress/wp-admin/css/colors/_variables.scss
wordpress/wp-admin/css/colors/midnight/
wordpress/wp-admin/css/colors/midnight/colors.scss
wordpress/wp-admin/css/colors/midnight/colors-rtl.min.css
wordpress/wp-admin/css/colors/midnight/colors-rtl.css
wordpress/wp-admin/css/colors/midnight/colors.min.css
wordpress/wp-admin/css/colors/midnight/colors.css
wordpress/wp-admin/css/colors/coffee/
wordpress/wp-admin/css/colors/coffee/colors.scss
wordpress/wp-admin/css/colors/coffee/colors-rtl.min.css
wordpress/wp-admin/css/colors/coffee/colors-rtl.css
wordpress/wp-admin/css/colors/coffee/colors.min.css
wordpress/wp-admin/css/colors/coffee/colors.css
wordpress/wp-admin/css/colors/modern/
wordpress/wp-admin/css/colors/modern/colors.scss
wordpress/wp-admin/css/colors/modern/colors-rtl.min.css
wordpress/wp-admin/css/colors/modern/colors-rtl.css
wordpress/wp-admin/css/colors/modern/colors.min.css
wordpress/wp-admin/css/colors/modern/colors.css
wordpress/wp-admin/css/install-rtl.css
wordpress/wp-admin/css/deprecated-media.min.css
wordpress/wp-admin/css/install.min.css
wordpress/wp-admin/css/themes.min.css
wordpress/wp-admin/css/site-icon.min.css
wordpress/wp-admin/css/edit-rtl.css
wordpress/wp-admin/css/color-picker-rtl.css
wordpress/wp-admin/css/customize-controls.min.css
wordpress/wp-admin/css/l10n.css
wordpress/wp-admin/css/farbtastic.min.css
wordpress/wp-admin/css/admin-menu-rtl.min.css
wordpress/wp-admin/css/dashboard.min.css
wordpress/wp-admin/css/media.css
wordpress/wp-admin/css/widgets-rtl.css
wordpress/wp-admin/css/customize-nav-menus.css
wordpress/wp-admin/css/install-rtl.min.css
wordpress/wp-admin/css/l10n.min.css
wordpress/wp-admin/css/nav-menus-rtl.css
wordpress/wp-admin/css/farbtastic-rtl.min.css
wordpress/wp-admin/css/admin-menu-rtl.css
wordpress/wp-admin/css/farbtastic.css
wordpress/wp-admin/css/code-editor.min.css
wordpress/wp-admin/css/customize-widgets.min.css
wordpress/wp-admin/css/wp-admin.css
wordpress/wp-admin/css/admin-menu.min.css
wordpress/wp-admin/css/common.min.css
wordpress/wp-admin/css/customize-widgets-rtl.css
wordpress/wp-admin/css/site-icon-rtl.css
wordpress/wp-admin/css/about-rtl.css
wordpress/wp-admin/css/about.min.css
wordpress/wp-admin/css/list-tables.min.css
wordpress/wp-admin/css/widgets.css
wordpress/wp-admin/css/revisions.min.css
wordpress/wp-admin/css/l10n-rtl.min.css
wordpress/wp-admin/css/dashboard.css
wordpress/wp-admin/css/widgets-rtl.min.css
wordpress/wp-admin/css/forms.min.css
wordpress/wp-admin/css/common-rtl.css
wordpress/wp-admin/css/forms-rtl.min.css
wordpress/wp-admin/css/login.min.css
wordpress/wp-admin/css/themes-rtl.min.css
wordpress/wp-admin/css/l10n-rtl.css
wordpress/wp-admin/css/customize-controls-rtl.min.css
wordpress/wp-admin/css/forms-rtl.css
wordpress/wp-admin/css/wp-admin-rtl.css
wordpress/wp-admin/css/customize-widgets-rtl.min.css
wordpress/wp-admin/css/color-picker.min.css
wordpress/wp-admin/term.php
wordpress/wp-admin/async-upload.php
wordpress/wp-admin/about.php
wordpress/wp-admin/upgrade-functions.php
wordpress/wp-admin/edit-tags.php
wordpress/wp-admin/my-sites.php
wordpress/wp-admin/export-personal-data.php
wordpress/wp-admin/profile.php
wordpress/wp-admin/site-health-info.php
wordpress/wp-admin/upload.php
wordpress/wp-admin/options-media.php
wordpress/wp-admin/upgrade.php
wordpress/wp-admin/media.php
wordpress/wp-admin/update-core.php
wordpress/wp-admin/edit.php
wordpress/wp-admin/widgets-form-blocks.php
wordpress/wp-admin/media-new.php
wordpress/wp-admin/menu.php
wordpress/wp-admin/ms-edit.php
wordpress/wp-admin/users.php
wordpress/wp-admin/edit-comments.php
wordpress/wp-admin/theme-editor.php
wordpress/wp-admin/options-general.php
wordpress/wp-admin/site-editor.php
wordpress/wp-admin/media-upload.php
wordpress/wp-admin/widgets-form.php
wordpress/wp-admin/link-parse-opml.php
wordpress/wp-admin/privacy-policy-guide.php
wordpress/wp-admin/revision.php
wordpress/wp-admin/options-privacy.php
wordpress/wp-admin/ms-options.php
wordpress/wp-admin/moderation.php
wordpress/wp-admin/admin-post.php
wordpress/wp-admin/nav-menus.php
wordpress/wp-admin/ms-users.php
wordpress/wp-admin/plugin-install.php
wordpress/wp-admin/tools.php
wordpress/wp-admin/network.php
wordpress/wp-admin/load-styles.php
wordpress/wp-admin/privacy.php
wordpress/wp-admin/erase-personal-data.php
wordpress/wp-admin/export.php
wordpress/wp-admin/link-manager.php
wordpress/wp-admin/ms-delete-site.php
wordpress/wp-admin/load-scripts.php
wordpress/wp-admin/comment.php
wordpress/wp-admin/user/
wordpress/wp-admin/user/contribute.php
wordpress/wp-admin/user/about.php
wordpress/wp-admin/user/profile.php
wordpress/wp-admin/user/menu.php
wordpress/wp-admin/user/privacy.php
wordpress/wp-admin/user/index.php
wordpress/wp-admin/user/credits.php
wordpress/wp-admin/user/user-edit.php
wordpress/wp-admin/user/admin.php
wordpress/wp-admin/user/freedoms.php
wordpress/wp-admin/plugin-editor.php
wordpress/wp-admin/options-writing.php
wordpress/wp-admin/site-health.php
wordpress/wp-admin/options.php
wordpress/wp-admin/index.php
wordpress/wp-admin/update.php
wordpress/wp-admin/includes/
wordpress/wp-admin/includes/admin-filters.php
wordpress/wp-admin/includes/class-wp-community-events.php
wordpress/wp-admin/includes/class-theme-installer-skin.php
wordpress/wp-admin/includes/class-pclzip.php
wordpress/wp-admin/includes/class-ftp-pure.php
wordpress/wp-admin/includes/edit-tag-messages.php
wordpress/wp-admin/includes/class-custom-image-header.php
wordpress/wp-admin/includes/class-plugin-upgrader.php
wordpress/wp-admin/includes/class-wp-themes-list-table.php
wordpress/wp-admin/includes/class-wp-posts-list-table.php
wordpress/wp-admin/includes/class-walker-nav-menu-edit.php
wordpress/wp-admin/includes/class-wp-upgrader-skins.php
wordpress/wp-admin/includes/class-wp-plugins-list-table.php
wordpress/wp-admin/includes/ms-admin-filters.php
wordpress/wp-admin/includes/class-wp-internal-pointers.php
wordpress/wp-admin/includes/upgrade.php
wordpress/wp-admin/includes/media.php
wordpress/wp-admin/includes/class-wp-screen.php
wordpress/wp-admin/includes/class-walker-nav-menu-checklist.php
wordpress/wp-admin/includes/class-wp-site-health-auto-updates.php
wordpress/wp-admin/includes/meta-boxes.php
wordpress/wp-admin/includes/image.php
wordpress/wp-admin/includes/noop.php
wordpress/wp-admin/includes/update-core.php
wordpress/wp-admin/includes/class-wp-ajax-upgrader-skin.php
wordpress/wp-admin/includes/menu.php
wordpress/wp-admin/includes/class-wp-plugin-install-list-table.php
wordpress/wp-admin/includes/image-edit.php
wordpress/wp-admin/includes/ms-deprecated.php
wordpress/wp-admin/includes/class-language-pack-upgrader-skin.php
wordpress/wp-admin/includes/class-custom-background.php
wordpress/wp-admin/includes/taxonomy.php
wordpress/wp-admin/includes/class-wp-privacy-requests-table.php
wordpress/wp-admin/includes/nav-menu.php
wordpress/wp-admin/includes/class-ftp.php
wordpress/wp-admin/includes/class-file-upload-upgrader.php
wordpress/wp-admin/includes/user.php
wordpress/wp-admin/includes/ajax-actions.php
wordpress/wp-admin/includes/class-wp-post-comments-list-table.php
wordpress/wp-admin/includes/class-plugin-installer-skin.php
wordpress/wp-admin/includes/class-wp-filesystem-direct.php
wordpress/wp-admin/includes/misc.php
wordpress/wp-admin/includes/class-wp-ms-sites-list-table.php
wordpress/wp-admin/includes/revision.php
wordpress/wp-admin/includes/class-wp-privacy-data-removal-requests-list-table.php
wordpress/wp-admin/includes/continents-cities.php
wordpress/wp-admin/includes/class-theme-upgrader.php
wordpress/wp-admin/includes/class-wp-site-health.php
wordpress/wp-admin/includes/class-wp-list-table.php
wordpress/wp-admin/includes/plugin-install.php
wordpress/wp-admin/includes/class-wp-site-icon.php
wordpress/wp-admin/includes/network.php
wordpress/wp-admin/includes/class-wp-importer.php
wordpress/wp-admin/includes/class-wp-application-passwords-list-table.php
wordpress/wp-admin/includes/deprecated.php
wordpress/wp-admin/includes/class-wp-terms-list-table.php
wordpress/wp-admin/includes/export.php
wordpress/wp-admin/includes/class-wp-filesystem-base.php
wordpress/wp-admin/includes/class-wp-ms-users-list-table.php
wordpress/wp-admin/includes/plugin.php
wordpress/wp-admin/includes/comment.php
wordpress/wp-admin/includes/class-wp-media-list-table.php
wordpress/wp-admin/includes/class-wp-debug-data.php
wordpress/wp-admin/includes/class-wp-comments-list-table.php
wordpress/wp-admin/includes/options.php
wordpress/wp-admin/includes/class-bulk-upgrader-skin.php
wordpress/wp-admin/includes/class-bulk-plugin-upgrader-skin.php
wordpress/wp-admin/includes/update.php
wordpress/wp-admin/includes/class-language-pack-upgrader.php
wordpress/wp-admin/includes/dashboard.php
wordpress/wp-admin/includes/class-theme-upgrader-skin.php
wordpress/wp-admin/includes/theme-install.php
wordpress/wp-admin/includes/schema.php
wordpress/wp-admin/includes/privacy-tools.php
wordpress/wp-admin/includes/class-wp-upgrader-skin.php
wordpress/wp-admin/includes/credits.php
wordpress/wp-admin/includes/class-wp-links-list-table.php
wordpress/wp-admin/includes/class-wp-filesystem-ftpext.php
wordpress/wp-admin/includes/class-bulk-theme-upgrader-skin.php
wordpress/wp-admin/includes/class-wp-list-table-compat.php
wordpress/wp-admin/includes/post.php
wordpress/wp-admin/includes/class-core-upgrader.php
wordpress/wp-admin/includes/import.php
wordpress/wp-admin/includes/class-ftp-sockets.php
wordpress/wp-admin/includes/class-wp-automatic-updater.php
wordpress/wp-admin/includes/list-table.php
wordpress/wp-admin/includes/class-wp-filesystem-ssh2.php
wordpress/wp-admin/includes/class-automatic-upgrader-skin.php
wordpress/wp-admin/includes/screen.php
wordpress/wp-admin/includes/class-wp-privacy-data-export-requests-list-table.php
wordpress/wp-admin/includes/translation-install.php
wordpress/wp-admin/includes/admin.php
wordpress/wp-admin/includes/class-wp-privacy-policy-content.php
wordpress/wp-admin/includes/file.php
wordpress/wp-admin/includes/bookmark.php
wordpress/wp-admin/includes/class-wp-upgrader.php
wordpress/wp-admin/includes/class-plugin-upgrader-skin.php
wordpress/wp-admin/includes/ms.php
wordpress/wp-admin/includes/widgets.php
wordpress/wp-admin/includes/class-wp-ms-themes-list-table.php
wordpress/wp-admin/includes/class-wp-filesystem-ftpsockets.php
wordpress/wp-admin/includes/class-wp-theme-install-list-table.php
wordpress/wp-admin/includes/theme.php
wordpress/wp-admin/includes/template.php
wordpress/wp-admin/includes/class-walker-category-checklist.php
wordpress/wp-admin/includes/class-wp-users-list-table.php
wordpress/wp-admin/menu-header.php
wordpress/wp-admin/options-head.php
wordpress/wp-admin/theme-install.php
wordpress/wp-admin/install-helper.php
wordpress/wp-admin/credits.php
wordpress/wp-admin/maint/
wordpress/wp-admin/maint/repair.php
wordpress/wp-admin/ms-upgrade-network.php
wordpress/wp-admin/ms-themes.php
wordpress/wp-admin/post.php
wordpress/wp-admin/edit-link-form.php
wordpress/wp-admin/edit-form-blocks.php
wordpress/wp-admin/user-edit.php
wordpress/wp-admin/press-this.php
wordpress/wp-admin/authorize-application.php
wordpress/wp-admin/admin-footer.php
wordpress/wp-admin/edit-form-advanced.php
wordpress/wp-admin/import.php
wordpress/wp-admin/ms-admin.php
wordpress/wp-admin/link.php
wordpress/wp-admin/network/
wordpress/wp-admin/network/contribute.php
wordpress/wp-admin/network/site-info.php
wordpress/wp-admin/network/about.php
wordpress/wp-admin/network/profile.php
wordpress/wp-admin/network/upgrade.php
wordpress/wp-admin/network/update-core.php
wordpress/wp-admin/network/edit.php
wordpress/wp-admin/network/sites.php
wordpress/wp-admin/network/menu.php
wordpress/wp-admin/network/users.php
wordpress/wp-admin/network/theme-editor.php
wordpress/wp-admin/network/site-users.php
wordpress/wp-admin/network/plugin-install.php
wordpress/wp-admin/network/privacy.php
wordpress/wp-admin/network/settings.php
wordpress/wp-admin/network/plugin-editor.php
wordpress/wp-admin/network/index.php
wordpress/wp-admin/network/update.php
wordpress/wp-admin/network/theme-install.php
wordpress/wp-admin/network/setup.php
wordpress/wp-admin/network/credits.php
wordpress/wp-admin/network/user-edit.php
wordpress/wp-admin/network/plugins.php
wordpress/wp-admin/network/admin.php
wordpress/wp-admin/network/freedoms.php
wordpress/wp-admin/network/user-new.php
wordpress/wp-admin/network/site-settings.php
wordpress/wp-admin/network/site-themes.php
wordpress/wp-admin/network/site-new.php
wordpress/wp-admin/network/themes.php
wordpress/wp-admin/plugins.php
wordpress/wp-admin/admin.php
wordpress/wp-admin/freedoms.php
wordpress/wp-admin/link-add.php
wordpress/wp-admin/user-new.php
wordpress/wp-admin/options-discussion.php
wordpress/wp-admin/admin-ajax.php
wordpress/wp-admin/js/
wordpress/wp-admin/js/auth-app.min.js
wordpress/wp-admin/js/revisions.min.js
wordpress/wp-admin/js/nav-menu.js
wordpress/wp-admin/js/plugin-install.min.js
wordpress/wp-admin/js/plugin-install.js
wordpress/wp-admin/js/inline-edit-tax.min.js
wordpress/wp-admin/js/inline-edit-tax.js
wordpress/wp-admin/js/widgets.min.js
wordpress/wp-admin/js/gallery.min.js
wordpress/wp-admin/js/tags-suggest.js
wordpress/wp-admin/js/accordion.js
wordpress/wp-admin/js/user-profile.js
wordpress/wp-admin/js/application-passwords.min.js
wordpress/wp-admin/js/media-gallery.js
wordpress/wp-admin/js/password-strength-meter.min.js
wordpress/wp-admin/js/dashboard.js
wordpress/wp-admin/js/iris.min.js
wordpress/wp-admin/js/revisions.js
wordpress/wp-admin/js/comment.min.js
wordpress/wp-admin/js/editor.min.js
wordpress/wp-admin/js/xfn.min.js
wordpress/wp-admin/js/farbtastic.js
wordpress/wp-admin/js/postbox.js
wordpress/wp-admin/js/tags-suggest.min.js
wordpress/wp-admin/js/word-count.min.js
wordpress/wp-admin/js/comment.js
wordpress/wp-admin/js/theme.min.js
wordpress/wp-admin/js/site-health.js
wordpress/wp-admin/js/edit-comments.min.js
wordpress/wp-admin/js/user-suggest.js
wordpress/wp-admin/js/user-suggest.min.js
wordpress/wp-admin/js/tags-box.js
wordpress/wp-admin/js/site-icon.js
wordpress/wp-admin/js/customize-widgets.js
wordpress/wp-admin/js/post.js
wordpress/wp-admin/js/image-edit.min.js
wordpress/wp-admin/js/xfn.js
wordpress/wp-admin/js/updates.min.js
wordpress/wp-admin/js/language-chooser.min.js
wordpress/wp-admin/js/widgets/
wordpress/wp-admin/js/widgets/media-image-widget.js
wordpress/wp-admin/js/widgets/media-video-widget.min.js
wordpress/wp-admin/js/widgets/media-widgets.min.js
wordpress/wp-admin/js/widgets/custom-html-widgets.min.js
wordpress/wp-admin/js/widgets/custom-html-widgets.js
wordpress/wp-admin/js/widgets/media-audio-widget.js
wordpress/wp-admin/js/widgets/media-image-widget.min.js
wordpress/wp-admin/js/widgets/media-gallery-widget.min.js
wordpress/wp-admin/js/widgets/media-audio-widget.min.js
wordpress/wp-admin/js/widgets/media-video-widget.js
wordpress/wp-admin/js/widgets/text-widgets.min.js
wordpress/wp-admin/js/widgets/media-gallery-widget.js
wordpress/wp-admin/js/widgets/media-widgets.js
wordpress/wp-admin/js/widgets/text-widgets.js
wordpress/wp-admin/js/language-chooser.js
wordpress/wp-admin/js/theme-plugin-editor.min.js
wordpress/wp-admin/js/post.min.js
wordpress/wp-admin/js/tags.js
wordpress/wp-admin/js/privacy-tools.min.js
wordpress/wp-admin/js/media-upload.min.js
wordpress/wp-admin/js/privacy-tools.js
wordpress/wp-admin/js/site-health.min.js
wordpress/wp-admin/js/media.min.js
wordpress/wp-admin/js/theme.js
wordpress/wp-admin/js/customize-controls.js
wordpress/wp-admin/js/edit-comments.js
wordpress/wp-admin/js/customize-nav-menus.min.js
wordpress/wp-admin/js/tags.min.js
wordpress/wp-admin/js/dashboard.min.js
wordpress/wp-admin/js/link.min.js
wordpress/wp-admin/js/editor.js
wordpress/wp-admin/js/customize-controls.min.js
wordpress/wp-admin/js/theme-plugin-editor.js
wordpress/wp-admin/js/nav-menu.min.js
wordpress/wp-admin/js/image-edit.js
wordpress/wp-admin/js/custom-background.min.js
wordpress/wp-admin/js/application-passwords.js
wordpress/wp-admin/js/password-toggle.js
wordpress/wp-admin/js/user-profile.min.js
wordpress/wp-admin/js/password-toggle.min.js
wordpress/wp-admin/js/svg-painter.js
wordpress/wp-admin/js/link.js
wordpress/wp-admin/js/custom-header.js
wordpress/wp-admin/js/widgets.js
wordpress/wp-admin/js/gallery.js
wordpress/wp-admin/js/word-count.js
wordpress/wp-admin/js/accordion.min.js
wordpress/wp-admin/js/inline-edit-post.min.js
wordpress/wp-admin/js/customize-widgets.min.js
wordpress/wp-admin/js/inline-edit-post.js
wordpress/wp-admin/js/updates.js
wordpress/wp-admin/js/media-upload.js
wordpress/wp-admin/js/media.js
wordpress/wp-admin/js/editor-expand.min.js
wordpress/wp-admin/js/media-gallery.min.js
wordpress/wp-admin/js/common.min.js
wordpress/wp-admin/js/tags-box.min.js
wordpress/wp-admin/js/svg-painter.min.js
wordpress/wp-admin/js/custom-background.js
wordpress/wp-admin/js/color-picker.min.js
wordpress/wp-admin/js/site-icon.min.js
wordpress/wp-admin/js/auth-app.js
wordpress/wp-admin/js/code-editor.js
wordpress/wp-admin/js/common.js
wordpress/wp-admin/js/set-post-thumbnail.min.js
wordpress/wp-admin/js/postbox.min.js
wordpress/wp-admin/js/color-picker.js
wordpress/wp-admin/js/password-strength-meter.js
wordpress/wp-admin/js/customize-nav-menus.js
wordpress/wp-admin/js/editor-expand.js
wordpress/wp-admin/js/code-editor.min.js
wordpress/wp-admin/js/set-post-thumbnail.js
wordpress/wp-admin/options-permalink.php
wordpress/wp-admin/widgets.php
wordpress/wp-admin/setup-config.php
wordpress/wp-admin/install.php
wordpress/wp-admin/admin-header.php
wordpress/wp-admin/post-new.php
wordpress/wp-admin/themes.php
wordpress/wp-admin/options-reading.php
wordpress/wp-trackback.php
wordpress/wp-comments-post.php
</details>

Crear sitio de Apache para WordPress:
```bash
nano /etc/apache2/sites-available/wordpress.conf
```
Y poner esto en el nano:
```bash
<VirtualHost *:80>
    DocumentRoot /srv/www/wordpress
    <Directory /srv/www/wordpress>
        Options FollowSymLinks
        AllowOverride Limit Options FileInfo
        DirectoryIndex index.php
        Require all granted
    </Directory>
    <Directory /srv/www/wordpress/wp-content>
        Options FollowSymLinks
        Require all granted
    </Directory>
</VirtualHost>
```
Habilitar el sitio con:
```bash
a2ensite wordpress
```
Actúe la reescritura de URL con:
```bash
a2enmod rewrite
```
Desactivar el sitio predeterminado de "It Works":
```bash
a2dissite 000-default
```
Finalmente, recarga apache2 para aplicar todos estos cambios:
```bash
sudo service apache2 reload
```



