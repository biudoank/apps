ChilliSpot : Aplikasi captive portal open source yang mengatur akses pengguna wireless. Ia akan mengarahkan pengguna ke halaman login sebelum mereka bisa mengakses internet. 
FreeRADIUS : Server RADIUS (Remote Authentication Dial-In User Service) open source yang bertugas memverifikasi kredensial pengguna (authentication), memberi izin akses (authorization), dan mencatat aktivitas (accounting).
Wireless LAN : Jaringan WiFi yang digunakan oleh pengguna untuk terhubung. Access Point diarahkan agar semua permintaan otentikasi lewat ChilliSpot dan FreeRADIUS.

1. Pengguna terhubung ke Access Point (WiFi).
2. Access Point mengarahkan semua trafik HTTP ke ChilliSpot (captive portal).
3. Pengguna memasukkan username/password di halaman login.
4. ChilliSpot mengirimkan data login ke FreeRADIUS untuk diverifikasi.
5. FreeRADIUS memeriksa data di database (MySQL, LDAP, dsb).
6. Jika benar → FreeRADIUS mengirimkan "Access-Accept" ke ChilliSpot.
7. ChilliSpot membuka akses internet untuk pengguna tersebut.
